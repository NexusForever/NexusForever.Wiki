---
description: This page provides information on how to clone the NexusForever source code.
---

# Server Cloning

## Introduction

First we need to clone the NexusForever source code from the [GitHub](https://github.com/NexusForever/NexusForever) repo.

NexusForever clone guides are provided for both Windows and Linux.

## Clone

{% tabs %}
{% tab title="Windows" %}
### Prerequisites

* Install [Git](https://git-scm.com/downloads).

### Clone

Run the following commands in the Command Prompt to clone the latest version of the NexusForever source code into the folder.

{% hint style="info" %}
The `C:\nexusforever` folder can be substituted for another path although the guide will assume that this default directory is used.
{% endhint %}

{% code overflow="wrap" lineNumbers="true" %}
```
mkdir C:\nexusforever
cd C:\nexusforever
git clone https://github.com/NexusForever/NexusForever.git .
```
{% endcode %}

After cloning, the source directory will contain the most recent version of the NexusForever source code.

<figure><img src="../../.gitbook/assets/image (21).png" alt="" width="563"><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Linux" %}
### Prerequisites

* Install Git.\
  Git usually comes preinstalled with many Linux distributions. If not, consult your distribution's package manager for installation instructions.

### Clone

Run the following commands in your terminal to clone the latest version of the NexusForever source code into the folder.

{% hint style="info" %}
The `/opt/nexusforever` folder can be substituted for another path although the guide will assume that this default directory is used.
{% endhint %}

{% code overflow="wrap" lineNumbers="true" %}
```bash
sudo mkdir /opt/nexusforever
cd /opt/nexusforever
sudo git clone https://github.com/NexusForever/NexusForever.git .
```
{% endcode %}

After cloning, the source directory will contain the most recent version of the NexusForever source code.

<figure><img src="../../.gitbook/assets/image (25).png" alt="" width="485"><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}
