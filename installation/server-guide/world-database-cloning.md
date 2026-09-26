---
description: >-
  This page provides information on how to clone the NexusForever database
  source code.
---

# World Database Cloning

## Introduction

After cloning the NexusForever source code we can clone the NexusForever database source code from the [GitHub](https://github.com/NexusForever/NexusForever.WorldDatabase) repo.

NexusForever database clone guides are provided for both Windows and Linux.

The NexusForever database schema is provided through Entity Framework migrations within the main NexusForever repository.\
The actual world data is stored in a separate repository, this additional data is optional but highly recommended as Nexus will be empty without it.

{% hint style="warning" %}
The world database must match the schema of the server branch you built. At the time of writing, the world database is built against the `expedition-evil-from-the-ether` branch, not the default `game_rework` branch. On `game_rework` the import fails with errors about missing tables and columns (`entity_script`, `entity_property`, `creature_info_property`, `entity.Mode`), because the `EntityProperty`, `CreatureInfo` and `EntityMode` migrations only exist on `expedition-evil-from-the-ether`.

To use the world database, check out that branch before building and running the migrations:

```bash
git checkout expedition-evil-from-the-ether
```
{% endhint %}

## Clone

{% tabs %}
{% tab title="Windows" %}
### Prerequisites

* Install [Git](https://git-scm.com/downloads).

### Clone

Run the following commands in the Command Prompt to clone the latest version of the NexusForever database into the folder.

{% hint style="info" %}
The `C:\nexusforever-database` folder can be substituted for another path although the guide will assume that this default directory is used.
{% endhint %}

{% code overflow="wrap" lineNumbers="true" %}
```
mkdir C:\nexusforever-database
cd C:\nexusforever-database
git clone https://github.com/NexusForever/NexusForever.WorldDatabase.git .
```
{% endcode %}

After cloning, the database source directory will contain the most recent version of the NexusForever source code.

<figure><img src="../../.gitbook/assets/image (15).png" alt="" width="563"><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Linux" %}
### Prerequisites

* Install Git.\
  Git usually comes preinstalled with many Linux distributions. If not, consult your distribution's package manager for installation instructions.

### Clone

Run the following commands in your terminal to clone the latest version of the NexusForever database into the folder.

{% hint style="info" %}
The `/opt/nexusforever-database` folder can be substituted for another path although the guide will assume that this default directory is used.
{% endhint %}

{% code overflow="wrap" lineNumbers="true" %}
```bash
sudo mkdir /opt/nexusforever-database
cd /opt/nexusforever-database
sudo git clone https://github.com/NexusForever/NexusForever.WorldDatabase.git .
```
{% endcode %}

After cloning, the database source directory will contain the most recent version of the NexusForever source code.

<figure><img src="../../.gitbook/assets/image (24).png" alt="" width="480"><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}
