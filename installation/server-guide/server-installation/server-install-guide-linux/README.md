---
description: >-
  This page provides information on setting up and running NexusForever on
  Linux.
---

# Linux

## Installation

{% hint style="warning" %}
This guide assumes the database, message broker and NexusForever are on the same machine. For more complex setups, you may need to adjust IP addresses and ports.
{% endhint %}

## Database Server

NexusForever requires a database and uses Entity Framework which is compatible with various databases, however official support is limited to MySQL and MariaDB.\
For other database providers not officially supported by NexusForever refer to the Entity Framework documentation.

### Prerequisites

* Install MariaDB via package manager.

{% hint style="warning" %}
This guide assumes you are using a Linux distribution that uses the APT package manager.\
If not, consult your distributions package manager for installation instructions.
{% endhint %}

{% code overflow="wrap" lineNumbers="true" %}
```bash
sudo apt install mariadb-server
```
{% endcode %}

* Ensure MariaDB service is running.

{% code overflow="wrap" lineNumbers="true" %}
```bash
sudo systemctl start mariadb
```
{% endcode %}

### Create Database User

NexusForever requires a database user which can be created using any database client that supports MySQL or MariaDB.

This guide will use the command line MySQL client to create the user.

Run the following commands in the Command Prompt to connect to the database using the database root user.

{% hint style="warning" %}
During the MariaDB installation, if you set a root password, use the `-p` parameter and enter your password when prompted.
{% endhint %}

{% code lineNumbers="true" %}
```
mysql -u root
```
{% endcode %}

Run the following commands in the MySQL prompt to create the database user `nexusforever` with the password `nexusforever` with all permissions to all databases.

{% code overflow="wrap" lineNumbers="true" %}
```sql
CREATE USER 'nexusforever' IDENTIFIED BY 'nexusforever';
GRANT ALL PRIVILEGES ON * . * TO 'nexusforever';
```
{% endcode %}

<figure><img src="../../../../.gitbook/assets/image (34).png" alt="" width="563"><figcaption></figcaption></figure>

## Message Broker

NexusForever requires a message broker and uses [Rebus](https://github.com/rebus-org/Rebus) which supports multiple message brokers, however offical support is limited to RabbitMQ and Azure Service Bus.\
For other message brokers not offically supported by NexusForever refer to the Rebus documentation.

### Prerequisites

* Install RabbitMQ via package manager.

{% hint style="warning" %}
This guide assumes you are using a Linux distribution that uses the APT package manager.\
If not, consult your distributions package manager for installation instructions.
{% endhint %}

{% code overflow="wrap" lineNumbers="true" %}
```bash
sudo apt install rabbitmq-server
```
{% endcode %}

* Ensure the RabbitMQ service is running.

{% code overflow="wrap" lineNumbers="true" %}
```bash
sudo systemctl start rabbitmq-server
```
{% endcode %}

### Create Broker User

Run the following commands in your terminal to create a new broker user `nexusforever` with the password `nexusforever` with administrator permissions to all virtual hosts.

{% code overflow="wrap" lineNumbers="true" %}
```bash
sudo rabbitmqctl add_user nexusforever nexusforever
sudo rabbitmqctl set_user_tags nexusforever administrator
sudo rabbitmqctl set_permissions -p / nexusforever ".*" ".*" ".*"
```
{% endcode %}

## NexusForever

### Copy Configuration Files

Run the following commands in your terminal to use the default server configuration files provided with NexusForever.

{% hint style="warning" %}
Substitute the `Debug` folder in the path with `Release` if you built NexusForever in release mode.
{% endhint %}

{% code overflow="wrap" lineNumbers="true" %}
```bash
cd /opt/nexusforever/Source/NexusForever.AuthServer/bin/Debug/net9.0/
sudo cp AuthServer.example.json AuthServer.json
cd /opt/nexusforever/Source/NexusForever.StsServer/bin/Debug/net9.0/
sudo cp StsServer.example.json StsServer.json
cd /opt/nexusforever/Source/NexusForever.WorldServer/bin/Debug/net9.0/
sudo cp WorldServer.example.json WorldServer.json
cd /opt/nexusforever/Source/NexusForever.Server.ChatServer/bin/Debug/net9.0/
sudo cp ChatServer.example.json ChatServer.json
cd /opt/nexusforever/Source/NexusForever.Server.GroupServer/bin/Debug/net9.0/
sudo cp GroupServer.example.json GroupServer.json
cd /opt/nexusforever/Source/NexusForever.API.Character/bin/Debug/net9.0/
sudo cp CharacterAPI.example.json CharacterAPI.json
```
{% endcode %}

## Database Migration

### Entity Core Migrations

Run the following commands in your terminal to install the required Entity Framework migration tool and run the migrations for each database.

{% hint style="danger" %}
It's advised to perform database migrations for auth, character, and world databases via the command line, rather than using the NexusForever world server as this feature will be deprecated in the future.
{% endhint %}

{% hint style="warning" %}
By default the `Debug` configuration will be selected, you can also choose `Release` by providing the parameter `--configuration Release` if you built NexusForever in release mode.
{% endhint %}

```bash
sudo dotnet tool install dotnet-ef --tool-path /usr/bin

cd /opt/nexusforever/Source/NexusForever.Server.WorldServer
sudo dotnet-ef database update --context AuthContext
sudo dotnet-ef database update --context CharacterContext
sudo dotnet-ef database update --context WorldContext

cd /opt/nexusforever/Source/NexusForever.Server.ChatServer
sudo dotnet-ef database update

cd /opt/nexusforever/Source/NexusForever.Server.GroupServer
sudo dotnet-ef database update
```

<figure><img src="../../../../.gitbook/assets/image (35).png" alt=""><figcaption></figcaption></figure>

### World Database

Run the following commands in your terminal to apply the NexusForever world database dumps to the world database.

{% hint style="warning" %}
During the MariaDB installation, if you set a root password, use the `-p` parameter and enter your password when prompted.
{% endhint %}

{% code overflow="wrap" lineNumbers="true" %}
```bash
find -type f -name '*.sql' -exec sh -c 'mysql -u root nexus_forever_world < "{}"' \;
```
{% endcode %}

## Linux Server

For setting up NexusForever on a dedicated Linux server check out the dedicated [Linux Server](linux-server.md) page.\
It includes details such as running NexusForever as a systemd service and configuring external access.
