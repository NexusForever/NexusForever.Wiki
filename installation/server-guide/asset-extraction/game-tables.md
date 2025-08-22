---
description: >-
  This page provides information on how to extract game tables used by
  NexusForever from the WildStar client.
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

# Game Tables

## Information

WildStar uses client side game tables (similar to dbc or db2 files from World of Warcraft) to supply the client with various bits of information about items, quest, spells, etc..., NexusForever utilises this information as well.

## Extract

We can use the map generator that is part of the main NexusForever repository to extract the game tables and localisations from the client.

{% hint style="info" %}
The map generator accepts several parameters, with `--generate` and `--patchPath` being the primary ones.\
For details on additional optional parameters, run the map generator without any parameters.
{% endhint %}

{% tabs %}
{% tab title="Windows" %}
Run the following commands in the Command Prompt to start the extraction of the game table and localisation files using the WildStar client.

{% hint style="warning" %}
Substitute the path `C:\Program Files (x86)\NCSOFT\WildStar\Patch` with the location of your WildStar client installation.
{% endhint %}

{% hint style="warning" %}
Substitute the `Debug` folder in the path with `Release` if you built NexusForever in release mode.
{% endhint %}

{% code overflow="wrap" lineNumbers="true" %}
```
cd C:\nexusforever\Source\NexusForever.MapGenerator\bin\Debug\net9.0
NexusForever.MapGenerator --extract --patchPath "C:\Program Files (x86)\NCSOFT\WildStar\Patch"
```
{% endcode %}

<figure><img src="../../../.gitbook/assets/image (13).png" alt="" width="563"><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (14).png" alt="" width="563"><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Linux" %}
Run the following commands in your terminal to start the extraction of the game table and localisation files using the WildStar client.

{% hint style="warning" %}
Substitute the path `~/NCSOFT/WildStar/Patch` with the location of your WildStar client installation.
{% endhint %}

{% hint style="warning" %}
Substitute the `Debug` folder in the path with `Release` if you built NexusForever in release mode.
{% endhint %}

{% code overflow="wrap" lineNumbers="true" %}
```bash
cd /opt/nexusforever/Source/NexusForever.MapGenerator/bin/Debug/net9.0
sudo ./NexusForever.MapGenerator --extract --patchPath ~/NCSOFT/WildStar/Patch
```
{% endcode %}

<figure><img src="../../../.gitbook/assets/image (49).png" alt="" width="563"><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (50).png" alt="" width="563"><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}

Once the process completes you'll find a folder called tbl in the same folder as the map generator containing many `*.tbl` files and one or more `*.bin` localisation files depending on the amount of client languages you have installed.

## Copy

The generated `*.tbl` and `*.bin` files are used by both the chat and world servers.

This guide copies the files into the build directories of both servers. Alternatively, you can place the files in a shared directory and update each server’s configuration to reference that location, avoiding duplicate copies.\
See the configuration section in the [Server Installation](../server-installation/) guides for more information on how to do this.

{% tabs %}
{% tab title="WIndows" %}
Run the following command in the Command Prompt to copy the generated `*.tbl` and `*.bin` files from the map generator output directory to the chat and world server build directories.

{% hint style="warning" %}
Substitute the `Debug` folder in the path with `Release` if you built NexusForever in release mode.
{% endhint %}

{% code overflow="wrap" lineNumbers="true" %}
```
cd C:\nexusforever\Source\NexusForever.MapGenerator\bin\Debug\net9.0\tbl\
xcopy tbl\*.* C:\nexusforever\Source\NexusForever.WorldServer\bin\Debug\net9.0\tbl\
xcopy tbl\*.* C:\nexusforever\Source\NexusForever.Server.ChatServer\bin\Debug\net9.0\tbl\
```
{% endcode %}
{% endtab %}

{% tab title="Linux" %}
Run the following command in your terminal to copy the generated `*.tbl` and `*.bin` files from the map generator output directory to the chat and world server build directories.

{% hint style="warning" %}
Substitute the `Debug` folder in the path with `Release` if you built NexusForever in release mode.
{% endhint %}

{% code overflow="wrap" lineNumbers="true" %}
```bash
cd /opt/nexusforever/Source/NexusForever.MapGenerator/bin/Debug/net9.0/tbl/
sudo mkdir /opt/nexusforever/Source/NexusForever.WorldServer/bin/Debug/net9.0/tbl/
sudo cp tbl/*.* /opt/nexusforever/Source/NexusForever.WorldServer/bin/Debug/net9.0/tbl/
sudo mkdir /opt/nexusforever/Source/NexusForever.Server.ChatServer/bin/Debug/net9.0/tbl/
sudo cp tbl/*.* /opt/nexusforever/Source/NexusForever.Server.ChatServer/bin/Debug/net9.0/tbl/
```
{% endcode %}
{% endtab %}
{% endtabs %}

