---
description: A collection of commands to manage spells.
---

# Spell

{% hint style="warning" %}
This page is automatically generated from the NexusForever source code!
{% endhint %}

### Summary

A collection of commands to manage spells.

#### RBAC

Role-based access control required to access this command category.

```
Permission.Spell = 83
```

## SpellAdd

### Summary

Add a base spell to character, optionally supplying the tier.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in either the WildStar game chat, World server console or web console.

```
!spell add
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c spell add
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.SpellAdd = 84
```

### Parameters

<details>

<summary>Spell4BaseId</summary>

#### Summary

Spell base id to add to character.

#### Optional

No

</details>

<details>

<summary>Tier</summary>

#### Summary

Tier of the base spell to add to character.

#### Optional

No

</details>

## SpellCast

### Summary

Cast a base spell for target, optionally supplying the tier.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in either the WildStar game chat, World server console or web console.

```
!spell cast
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c spell cast
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.SpellCast = 85
```

### Parameters

<details>

<summary>Spell4BaseId</summary>

#### Summary

Spell base id to cast from target.

#### Optional

No

</details>

<details>

<summary>Tier</summary>

#### Summary

Tier of the base spell to cast from target.

#### Optional

No

</details>

## SpellResetCooldown

### Summary

Reset a single spell cooldown for character, if no spell if supplied all cooldowns will be reset

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in either the WildStar game chat, World server console or web console.

```
!spell resetcooldown
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c spell resetcooldown
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.SpellResetCooldown = 86
```

### Parameters

<details>

<summary>Spell4Id</summary>

#### Summary

Spell id to reset cooldown for character.

#### Optional

No

</details>

