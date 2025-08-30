---
description: >-
  This page provides additional information on setting up and running
  NexusForever on Windows Server.
---

# Windows Server

## Introduction

This page provides additional information and steps necessary for setting up a NexusForever server on Windows Server.\
Please first complete the [Windows](./) guide before proceeding with this page.

## Build

If you are running NexusForever on Windows Server it is _**highly**_ recommended that you build NexusForever in release mode and copy the built release binaries outside of the build directories.

This guide will continue to use debug and the default build directories for consistency, if you follow this suggestion you will need to substitute the paths.

## Windows Services

NexusForever supports Windows Services, it the preferred method for running NexusForever on a Windows server.

Run the following commands in the Command Prompt to create Windows services for each NexusForever server.

{% hint style="warning" %}
Substitute the `Debug` folder in the path with `Release` if you built NexusForever in release mode.
{% endhint %}

{% code overflow="wrap" lineNumbers="true" %}
```
sc create NexusForever.AuthServer binPath="C:\nexusforever\Source\NexusForever.AuthServer\bin\Debug\net9.0\NexusForever.AuthServer.exe"
sc create NexusForever.StsServer binPath="C:\nexusforever\Source\NexusForever.StsServer\bin\Debug\net9.0\NexusForever.StsServer.exe"
sc create NexusForever.WorldServer binPath="C:\nexusforever\Source\NexusForever.WorldServer\bin\Debug\net9.0\NexusForever.WorldServer.exe"
sc create NexusForever.ChatServer binPath="C:\nexusforever\Source\NexusForever.Server.ChatServer\bin\Debug\net9.0\NexusForever.Server.ChatServer.exe"
sc create NexusForever.GroupServer binPath="C:\nexusforever\Source\NexusForever.Server.GroupServer\bin\Debug\net9.0\NexusForever.Server.GroupServer.exe"
sc create NexusForever.API.Character binPath="C:\nexusforever\Source\NexusForever.API.Character\bin\Debug\net9.0\NexusForever.API.Character.exe"
```
{% endcode %}

<figure><img src="../../../../.gitbook/assets/image (16).png" alt="" width="563"><figcaption></figcaption></figure>

Run the following commands in the Command Prompt to start the newly created Windows services.

{% code overflow="wrap" lineNumbers="true" %}
```
sc start NexusForever.AuthServer
sc start NexusForever.StsServer
sc start NexusForever.WorldServer
sc start NexusForever.ChatServer
sc start NexusForever.GroupServer
sc start NexusForever.API.Character
```
{% endcode %}

<figure><img src="../../../../.gitbook/assets/image (20).png" alt="" width="563"><figcaption></figcaption></figure>

## External Access

If your NexusForever server is running on a different machine than the one with the WildStar client you need to configure some additional settings.

### Port Forwarding

In order to connect to an external NexusForever server you need to portforward TCP ports 6600, 23115 and 24000.

{% hint style="warning" %}
You may also be required to setup firewall rules on additional physical or virtual hardware.
{% endhint %}

Run the following commands in the Command Prompt to open the Windows firewall settings.

{% code overflow="wrap" lineNumbers="true" %}
```
wf.msc
```
{% endcode %}

Select "Inbound Rules" then click "New Rule...".

<figure><img src="../../../../.gitbook/assets/image (19).png" alt="" width="563"><figcaption></figcaption></figure>

Select "Port".

<figure><img src="../../../../.gitbook/assets/image (17).png" alt="" width="563"><figcaption></figcaption></figure>

Select "TCP" then enter "6600, 23115, 24000" into the "Specific Local Ports" box.

<figure><img src="../../../../.gitbook/assets/image (18).png" alt="" width="563"><figcaption></figcaption></figure>

### World External IP

When connecting to a NexusForever server, the server's IP address is sent to the client.\
By default this IP is `127.0.0.1`, which is suitable when the WildStar client and NexusForever server run on the same machine. However if the server is hosted on a different computer you need to update this IP.

Run the following commands in the Command Prompt to connect to the database using the database root user.

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
mysql -u root
```
{% endcode %}

Run the following commands in the MySQL prompt to update the World Server external IP.

{% hint style="warning" %}
Replace `127.0.0.1` with the machine's internal or external IP address hosting the NexusForever server.\
Ensure this IP is publicly accessible and open as it will be sent to the WildStar client.
{% endhint %}

{% code overflow="wrap" lineNumbers="true" %}
```sql
USE nexus_forever_auth;
UPDATE server SET host = '127.0.0.1' WHERE id = 1;
```
{% endcode %}
