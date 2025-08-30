---
description: >-
  This page provides additional information on setting up and running
  NexusForever on a dedicated Linux server.
---

# Linux Server

## Introduction

This page provides additional information and steps necessary for setting up a NexusForever server on a Linux server.\
Please first complete the [Linux](./) guide before proceeding with this page.

## Build

If you are running NexusForever on a dedicated Linux server it is _**highly**_ recommended that you build NexusForever in release mode and copy the built release binaries outside of the build directories.

This guide will continue to use debug and the default build directories for consistency, if you follow this suggestion you will need to substitute the paths.

## Systemd

NexusForever supports Systemd Services, it the preferred method for running NexusForever on a Linux server.

### Unit Files

{% hint style="warning" %}
It is suggested you create a new user to run the NexusForever server services.\
The example unit files do not define a user and as such the services will run as root.
{% endhint %}

<details>

<summary>Auth Server</summary>

Run the following commands in your terminal to create a new unit file for the auth server.

{% hint style="info" %}
Substitute Vim with your favorite text editor.
{% endhint %}

```bash
cd /etc/systemd/system
sudo vim nexusforever.authserver.service
```

Copy the contents of the example unit file and save.

{% hint style="warning" %}
Substitute the `Debug` folder in the path with `Release` if you built NexusForever in release mode.
{% endhint %}

```ini
[Unit]
Description=NexusForever.AuthServer

[Service]
Type=simple
ExecStart=/opt/nexusforever/Source/NexusForever.AuthServer/bin/Debug/net9.0/NexusForever.AuthServer
WorkingDirectory=/opt/nexusforever/Source/NexusForever.AuthServer/bin/Debug/net9.0

[Install]
WantedBy=multi-user.target
```

</details>

<details>

<summary>STS Server</summary>

Run the following commands in your terminal to create a new unit file for the sts server.

{% hint style="info" %}
Substitute Vim with your favorite text editor.
{% endhint %}

```bash
cd /etc/systemd/system
sudo vim nexusforever.stsserver.service
```

Copy the contents of the example unit file and save.

{% hint style="warning" %}
Substitute the `Debug` folder in the path with `Release` if you built NexusForever in release mode.
{% endhint %}

```ini
[Unit]
Description=NexusForever.StsServer

[Service]
Type=simple
ExecStart=/opt/nexusforever/Source/NexusForever.StsServer/bin/Debug/net9.0/NexusForever.StsServer
WorkingDirectory=/opt/nexusforever/Source/NexusForever.StsServer/bin/Debug/net9.0

[Install]
WantedBy=multi-user.target
```

</details>

<details>

<summary>World Server</summary>

Run the following commands in your terminal to create a new unit file for the world server.

{% hint style="info" %}
Substitute Vim with your favorite text editor.
{% endhint %}

```bash
cd /etc/systemd/system
sudo vim nexusforever.worldserver.service
```

Copy the contents of the example unit file and save.

{% hint style="warning" %}
Substitute the `Debug` folder in the path with `Release` if you built NexusForever in release mode.
{% endhint %}

```ini
[Unit]
Description=NexusForever.WorldServer

[Service]
Type=simple
ExecStart=/opt/nexusforever/Source/NexusForever.WorldServer/bin/Debug/net9.0/NexusForever.WorldServer
WorkingDirectory=/opt/nexusforever/Source/NexusForever.WorldServer/bin/Debug/net9.0

[Install]
WantedBy=multi-user.target
```

</details>

<details>

<summary>Chat Server</summary>

Run the following commands in your terminal to create a new unit file for the chat server.

{% hint style="info" %}
Substitute Vim with your favorite text editor.
{% endhint %}

```bash
cd /etc/systemd/system
sudo vim nexusforever.server.chat.service
```

Copy the contents of the example unit file and save.

{% hint style="warning" %}
Substitute the `Debug` folder in the path with `Release` if you built NexusForever in release mode.
{% endhint %}

```ini
[Unit]
Description=NexusForever.Server.GroupServer

[Service]
Type=simple
ExecStart=/opt/nexusforever/Source/NexusForever.Server.ChatServer/bin/Debug/net9.0/NexusForever.Server.ChatServer
WorkingDirectory=/opt/nexusforever/Source/NexusForever.Server.ChatServer/bin/Debug/net9.0

[Install]
WantedBy=multi-user.target
```

</details>

<details>

<summary>Group Server</summary>

Run the following commands in your terminal to create a new unit file for the group server.

{% hint style="info" %}
Substitute Vim with your favorite text editor.
{% endhint %}

```bash
cd /etc/systemd/system
sudo vim nexusforever.server.group.service
```

Copy the contents of the example unit file and save.

{% hint style="warning" %}
Substitute the `Debug` folder in the path with `Release` if you built NexusForever in release mode.
{% endhint %}

```ini
[Unit]
Description=NexusForever.Server.GroupServer

[Service]
Type=simple
ExecStart=/opt/nexusforever/Source/NexusForever.Server.GroupServer/bin/Debug/net9.0/NexusForever.Server.GroupServer
WorkingDirectory=/opt/nexusforever/Source/NexusForever.Server.GroupServer/bin/Debug/net9.0

[Install]
WantedBy=multi-user.target
```

</details>

<details>

<summary>Character API</summary>

Run the following commands in your terminal to create a new unit file for the character api.

{% hint style="info" %}
Substitute Vim with your favorite text editor.
{% endhint %}

```bash
cd /etc/systemd/system
sudo vim nexusforever.api.character.service
```

Copy the contents of the example unit file and save.

{% hint style="warning" %}
Substitute the `Debug` folder in the path with `Release` if you built NexusForever in release mode.
{% endhint %}

```ini
[Unit]
Description=NexusForever.API.Character

[Service]
Type=simple
ExecStart=/opt/nexusforever/Source/NexusForever.API.Character/bin/Debug/net9.0/NexusForever.API.Character
WorkingDirectory=/opt/nexusforever/Source/NexusForever.API.Character/bin/Debug/net9.0

[Install]
WantedBy=multi-user.target
```

</details>

Run the following commands to reload the services daemon to load the newly created systemd services.

{% code overflow="wrap" lineNumbers="true" %}
```bash
cd /etc/systemd/system
sudo systemctl daemon-reload
```
{% endcode %}

Run the following commands in your terminal to start the newly created systemd services.

{% code overflow="wrap" lineNumbers="true" %}
```bash
sudo systemctl start nexusforever.authserver
sudo systemctl start nexusforever.stsserver
sudo systemctl start nexusforever.worldserver
sudo systemctl start nexusforever.server.chat
sudo systemctl start nexusforever.server.group
sudo systemctl start nexusforever.api.character
```
{% endcode %}

## External Access

If your NexusForever server is running on a different machine than the one with the WildStar client you need to configure some additional settings.

## Port Forwarding

In order to connect to an external NexusForever server you need to portforward TCP ports 6600, 23115 and 24000.

{% hint style="warning" %}
This guide assumes you are a Linux distribution that uses Uncomplicated Firewall.\
If not, either install Uncomplicated Firewall with your distributions package manager, configure the firewall directly usiing IP tables or consult your distributions documentation on firewall configuration.
{% endhint %}

{% hint style="warning" %}
You may also be required to setup firewall rules on additional physical or virtual hardware.
{% endhint %}

Run the following commands in your terminal to allow connections on the required ports.

{% code overflow="wrap" lineNumbers="true" %}
```bash
sudo ufw allow 23115
sudo ufw allow 6600
sudo ufw allow 24000
```
{% endcode %}

### World External IP

When connecting to a NexusForever server, the server's IP address is sent to the client.\
By default this IP is `127.0.0.1`, which is suitable when the WildStar client and NexusForever server run on the same machine. However if the server is hosted on a different computer you need to update this IP.

Run the following commands in your terminal to connect to the database using the database root user.

{% hint style="warning" %}
During the MariaDB installation, if you set a root password, use the `-p` parameter and enter your password when prompted.
{% endhint %}

{% code overflow="wrap" lineNumbers="true" %}
```bash
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
