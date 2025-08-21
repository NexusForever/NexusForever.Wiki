---
description: >-
  This page provides information on how to clone and build the NexusForever
  source code on Windows.
---

# Windows

## Build

After cloning the source code, build the solution using Visual Studio for local development, or the .NET SDK when building on a Windows server.

{% tabs %}
{% tab title="Command Line" %}
### Prerequisites

* Install [.NET 9.0 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/9.0).

### Build

Run the following commands in the Command Prompt to build the source code using the .NET SDK.

{% hint style="warning" %}
By default the `Debug` configuration will be selected, you can also choose `Release` by providing the parameter `--configuration Release` if you want to build NexusForever in release mode.
{% endhint %}

{% hint style="info" %}
Any warnings generated during the build process can be safely ignored.
{% endhint %}

{% code overflow="wrap" lineNumbers="true" %}
```
cd C:/nexusforever/Source
dotnet build
```
{% endcode %}

In the Command Prompt you should see build succeeded.

<figure><img src="../../../.gitbook/assets/image (12).png" alt="" width="563"><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Visual Studio" %}
### Prerequisites

* Install [Visual Studio 2022](https://visualstudio.microsoft.com/downloads/).\
  Ensure you install the "ASP.NET and web development" and ".NET desktop development" when installing Visual Studio.

<figure><img src="../../../.gitbook/assets/image.png" alt="" width="563"><figcaption></figcaption></figure>

### Build

* Open `C:\nexusforever\Source\NexusForever.sln` in Visual Studio.
* In the Solution Explorer, right click on the NexusForever solution and select Build Solution.

{% hint style="warning" %}
By default the `Debug` configuration will be selected, you can also choose `Release` from the configuration dropdown if you want to build NexusForever in release mode.
{% endhint %}

{% hint style="info" %}
Any warnings generated during the build process can be safely ignored.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (57).png" alt="" width="563"><figcaption></figcaption></figure>

In the Output tab, under Build output you should see Build Completed.

<figure><img src="../../../.gitbook/assets/image (59).png" alt="" width="563"><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}
