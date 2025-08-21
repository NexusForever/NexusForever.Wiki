---
description: >-
  This page provides information on how to clone and build the NexusForever
  source code on Linux.
---

# Linux

## Prerequisites

* Install [.NET 9.0](https://learn.microsoft.com/en-us/dotnet/core/install/linux) SDK.

## Build

Run the following commands in your terminal to build the source code using the .NET SDK.

{% hint style="warning" %}
By default the `Debug` configuration will be selected, you can also choose `Release` by providing the parameter `--configuration Release` if you want to build NexusForever in release mode.
{% endhint %}

{% hint style="info" %}
Any warnings generated during the build process can be safely ignored.
{% endhint %}

{% code overflow="wrap" lineNumbers="true" %}
```
cd /opt/nexusforever/Source
sudo dotnet build
```
{% endcode %}

In your terminal you should see build succeeded.

<figure><img src="../../../.gitbook/assets/image (26).png" alt="" width="563"><figcaption></figcaption></figure>
