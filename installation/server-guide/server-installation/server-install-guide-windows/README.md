---
description: >-
  This page provides information on setting up and running NexusForever on
  Windows.
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
---

# Windows

{% hint style="warning" %}
This guide assumes the database, message broker and NexusForever are on the same machine. For more complex setups, you may need to adjust IP addresses and ports.
{% endhint %}

## Database Server

NexusForever requires a database and uses Entity Framework which is compatible with various databases, however official support is limited to MySQL and MariaDB.\
For other database providers not officially supported by NexusForever refer to the Entity Framework documentation.

### Prerequisites

* Install [MariaDB](https://mariadb.org/download/).
* Ensure MariaDB service is running.

<figure><img src="../../../../.gitbook/assets/image (53).png" alt="" width="563"><figcaption></figcaption></figure>

### Create Database User

NexusForever requires a database user which can be created using any database client that supports MySQL or MariaDB, like HeidiSQL which is included with both by default.

This guide will use HeidiSQL or the command line MySQL client to create the user.

{% tabs %}
{% tab title="Command Line" %}
Run the following commands in the Command Prompt to connect to the database using the database root user.

{% hint style="warning" %}
At the time of writing this guide, MariaDB version 12.0 was the latest version.\
You may need to replace the version number in the path with the latest version.
{% endhint %}

{% hint style="warning" %}
During the MariaDB installation, if you set a root password, use the `-p` parameter and enter your password when prompted.
{% endhint %}

{% code lineNumbers="true" %}
```
cd C:\Program Files\MariaDB 12.0\bin
mysql -u root
```
{% endcode %}

<figure><img src="../../../../.gitbook/assets/image (11).png" alt="" width="563"><figcaption></figcaption></figure>

Run the following commands in the MySQL prompt to create the database user `nexusforever` with the password `nexusforever` with all permissions to all databases.

{% code overflow="wrap" lineNumbers="true" %}
```sql
CREATE USER 'nexusforever' IDENTIFIED BY 'nexusforever';
GRANT ALL PRIVILEGES ON * . * TO 'nexusforever';
```
{% endcode %}
{% endtab %}

{% tab title="HeidiSQL" %}
Open HeidiSQL, if this is your first time you will need to setup the connection to the database.

1. Click the "New" button and enter a name for the connection, then press Enter.
2. On the right side, set the "Network Type" dropdown to "MariaDB or MySQL (TCP/IP)".
3. For "Hostname / IP", enter `127.0.0.1`, for the "Port" enter 3306.
4. Ensure the "User" field is set to `root`. If you set a root password during the MariaDB installation, enter it in the "Password" field.
5. Click "Save".

<figure><img src="../../../../.gitbook/assets/image (27).png" alt="" width="563"><figcaption></figcaption></figure>

Open the "User Manager" which can be found under the "Tools" menu.

<figure><img src="../../../../.gitbook/assets/image (28).png" alt="" width="436"><figcaption></figcaption></figure>

1. Click the "Add" button, enter `nexusforever` for both the username and password.
2. Check the "Global Privileges" box
3. Click "Save".

<figure><img src="../../../../.gitbook/assets/image (29).png" alt="" width="548"><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}

## Message Broker

NexusForever requires a message broker and uses [Rebus](https://github.com/rebus-org/Rebus) which supports multiple message brokers, however offical support is limited to RabbitMQ and Azure Service Bus.\
For other message brokers not offically supported by NexusForever refer to the Rebus documentation.

### Prerequisites

* Install [RabbitMQ](https://github.com/rabbitmq/rabbitmq-server/releases).
* Ensure the RabbitMQ service is running.

<figure><img src="../../../../.gitbook/assets/image (55).png" alt="" width="563"><figcaption></figcaption></figure>

### Create Broker User

Run the following commands in the Command Prompt to create a new broker user `nexusforever` with the password `nexusforever` with administrator permissions to all virtual hosts.

{% hint style="warning" %}
At the time of writing this guide, RabbitMQ version 4.1.3 was the latest available. You may need to replace the version number in the path with the latest version.
{% endhint %}

{% code overflow="wrap" lineNumbers="true" %}
```
cd C:\Program Files\RabbitMQ Server\rabbitmq_server-4.1.3\sbin
rabbitmqctl add_user nexusforever nexusforever
rabbitmqctl set_user_tags nexusforever administrator
rabbitmqctl set_permissions -p / nexusforever ".*" ".*" ".*"
```
{% endcode %}

## NexusForever

### Copy Configuration Files

Run the following commands in the Command Prompt to use the default server configuration files provided with NexusForever.

{% hint style="warning" %}
Substitute the `Debug` folder in the path with `Release` if you built NexusForever in release mode.
{% endhint %}

{% code overflow="wrap" lineNumbers="true" %}
```
cd C:\nexusforever\Source\NexusForever.AuthServer\bin\Debug\net10.0\
copy AuthServer.example.json AuthServer.json
cd C:\nexusforever\Source\NexusForever.StsServer\bin\Debug\net10.0\
copy StsServer.example.json StsServer.json
cd C:\nexusforever\Source\NexusForever.WorldServer\bin\Debug\net10.0\
copy WorldServer.example.json WorldServer.json
cd C:\nexusforever\Source\NexusForever.Server.ChatServer\bin\Debug\net10.0\
copy ChatServer.example.json ChatServer.json
cd C:\nexusforever\Source\NexusForever.Server.GroupServer\bin\Debug\net10.0\
copy GroupServer.example.json GroupServer.json
cd C:\nexusforever\Source\NexusForever.API.Character\bin\Debug\net10.0\
copy CharacterAPI.example.json CharacterAPI.json
```
{% endcode %}

## Database Population

### Entity Core Migrations

Run the following commands in the Command Prompt to install the required Entity Framework migration tool and run the migrations for each database.

{% hint style="danger" %}
It's advised to perform database migrations for auth, character, and world databases via the command line, rather than using the NexusForever world server as this feature will be deprecated in the future.
{% endhint %}

{% hint style="warning" %}
By default the `Debug` configuration will be selected, you can also choose `Release` by providing the parameter `--configuration Release` if you built NexusForever in release mode.
{% endhint %}

{% code overflow="wrap" lineNumbers="true" %}
```
dotnet tool install dotnet-ef --global

cd C:\nexusforever\Source\NexusForever.WorldServer
dotnet-ef database update --context AuthContext
dotnet-ef database update --context CharacterContext
dotnet-ef database update --context WorldContext

cd C:\nexusforever\Source\NexusForever.Server.ChatServer
dotnet-ef database update

cd C:\nexusforever\Source\NexusForever.Server.GroupServer
dotnet-ef database update
```
{% endcode %}

### World Database

Run the following commands in the Command Prompt to apply the NexusForever world database dumps to the world database.

{% hint style="warning" %}
At the time of writing this guide, MariaDB version 12.0 was the latest version.\
You may need to replace the version number in the path with the latest version.
{% endhint %}

{% hint style="warning" %}
During the MariaDB installation, if you set a root password, use the `-p` parameter and enter your password when prompted.
{% endhint %}

{% code overflow="wrap" lineNumbers="true" %}
```
cd C:\Program Files\MariaDB 12.0\bin
for /R "C:\nexusforever-database" %f in (*.sql) do mysql -u root nexus_forever_world < "%f"
```
{% endcode %}

## Windows Server

For setting up NexusForever on Windows Server check out the dedicated [Windows Server](windows-server.md) page.\
It includes details such as running NexusForever as a Windows service and configuring external access.
