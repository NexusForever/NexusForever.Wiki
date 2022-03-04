---
description: A collection of commands to manage realm shutdown.
---

# RealmShutdown

{% hint style="warning" %}
This page is automatically generated from the NexusForever source code!
{% endhint %}

### Summary

A collection of commands to manage realm shutdown.

#### RBAC

Role-based access control required to access this command category.

```
Permission.RealmShutdown = 107
```

## RealmShutdownStart

### Summary

Start a new realm shutdown.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in either the WildStar game chat, World server console or web console.

```
!realm shutdown start
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c realm shutdown start
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.RealmShutdownStart = 108
```

### Parameters

<details>

<summary>Span</summary>

#### Summary

Time till shutdown. (Format: dd:hh:mm:ss)

#### Optional

No

</details>

## RealmShutdownCancel

### Summary

Cancel pending realm shutdown.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in either the WildStar game chat, World server console or web console.

```
!realm shutdown cancel
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c realm shutdown cancel
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.RealmShutdownCancel = 109
```

### Parameters

This command has no parameters.

