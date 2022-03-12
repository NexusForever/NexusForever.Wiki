---
description: A collection of commands to manage paths for a character.
---

# Path

{% hint style="warning" %}
This page is automatically generated from the NexusForever source code!
{% endhint %}

### Summary

A collection of commands to manage paths for a character.

#### RBAC

Role-based access control required to access this command category.

```
Permission.Path = 70
```

## PathUnlock

### Summary

Unlock a path for character.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!path unlock [path]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c path unlock [path]
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.PathUnlock = 71
```

### Parameters

<details>

<summary>Path</summary>

#### Summary

Path id to unlock.

#### Values

The following numeric values can be used for this parameter.

```
Soldier   = 0,
Settler   = 1,
Scientist = 2,
Explorer  = 3,
```

#### Optional

No

</details>

## PathActivate

### Summary

Activate a path for character.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!path activate [path]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c path activate [path]
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.PathActivate = 72
```

### Parameters

<details>

<summary>Path</summary>

#### Summary

Path id to activate.

#### Values

The following numeric values can be used for this parameter.

```
Soldier   = 0,
Settler   = 1,
Scientist = 2,
Explorer  = 3,
```

#### Optional

No

</details>

## PathXP

### Summary

Add XP to current path for character.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!path xp [xp]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c path xp [xp]
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.PathXP = 73
```

### Parameters

<details>

<summary>Xp</summary>

#### Summary

XP amount to add to currency path.

#### Optional

No

</details>

