---
description: >-
  This page provides information on how to generate base maps used by
  NexusForever from the WildStar client.
---

# Base Maps

## Information

Base maps are generated files used by NexusForever that contain various bits of information about the maps in Wildstar including grid, zone and terrain height information.

## Generate

We can use the map generator that is part of the main NexusForever repository to generate the base maps from the client.

{% hint style="warning" %}
Depending on your PC hardware base map generation may take an extended period of time to complete.
{% endhint %}

{% hint style="info" %}
The map generator accepts several parameters, with `--generate` and `--patchPath` being the primary ones.\
For details on additional optional parameters, run the map generator without any parameters.
{% endhint %}

{% tabs %}
{% tab title="Windows" %}
Run the following command in the Command Prompt to start the generation the base maps using the WildStar client.

{% hint style="warning" %}
Substitute the path `C:\Program Files (x86)\NCSOFT\WildStar\Patch` with the location of your WildStar client installation.
{% endhint %}

{% hint style="warning" %}
Substitute the `Debug` folder in the path with `Release` if you built NexusForever in release mode.
{% endhint %}

{% code overflow="wrap" lineNumbers="true" %}
```
cd C:\nexusforever\Source\NexusForever.MapGenerator\bin\Debug\net9.0
NexusForever.MapGenerator --generate --patchPath "C:\Program Files (x86)\NCSOFT\WildStar\Patch"
```
{% endcode %}

<figure><img src="../../../.gitbook/assets/image (22).png" alt="" width="563"><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (23).png" alt="" width="563"><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Linux" %}
Run the following command in your terminal to start the generation the base maps using the WildStar client.

{% hint style="warning" %}
Substitute the path `~/NCSOFT/WildStar/Patch` with the location of your WildStar client installation.
{% endhint %}

{% hint style="warning" %}
Substitute the `Debug` folder in the path with `Release` if you built NexusForever in release mode.
{% endhint %}

{% code overflow="wrap" lineNumbers="true" %}
```
cd /opt/nexusforever/Source/NexusForever.MapGenerator/bin/Debug/net9.0
sudo ./NexusForever.MapGenerator --generate --patchPath ~/NCSOFT/WildStar/Patch
```
{% endcode %}

<figure><img src="../../../.gitbook/assets/image (51).png" alt="" width="563"><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (52).png" alt="" width="563"><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}

Once the process completes you'll find a folder called map in the same folder as the map generator containing many `*.nfmap` files.

## Copy

The generated `*.nfmap` files are used by the world server and need to be copied into the build directoy.

{% tabs %}
{% tab title="WIndows" %}
Run the following command in the Command Prompt to copy the generated `*.nfmap` files from the map generator output directory to the world server build directory.

{% hint style="warning" %}
Substitute the `Debug` folder in the path with `Release` if you build NexusForever in release mode.
{% endhint %}

{% code overflow="wrap" lineNumbers="true" %}
```
cp map/*.nfmap /opt/nexusforever/Source/NexusForever.WorldServer/bin/Debug/net9.0/map/
```
{% endcode %}
{% endtab %}

{% tab title="Linux" %}
Run the following command in your terminal to copy the generated `*.nfmap` files from the map generator output directory to the world server build directory.

{% hint style="warning" %}
Substitute the `Debug` folder in the path with `Release` if you build NexusForever in release mode.
{% endhint %}

{% code overflow="wrap" lineNumbers="true" %}
```
sudo mkdir /opt/nexusforever/Source/NexusForever.WorldServer/bin/Debug/net9.0/map/
sudo cp map/*.nfmap /opt/nexusforever/Source/NexusForever.WorldServer/bin/Debug/net9.0/map/
```
{% endcode %}
{% endtab %}
{% endtabs %}
