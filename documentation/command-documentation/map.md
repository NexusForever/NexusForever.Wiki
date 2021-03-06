---
description: A collection of commands to manage maps.
---

# Map

{% hint style="warning" %}
This page is automatically generated from the NexusForever source code!
{% endhint %}

### Summary

A collection of commands to manage maps.

#### RBAC

Role-based access control required to access this command category.

```
Permission.Map = 103
```

## MapUnload

### Summary

Unload current map instance.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!map unload
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c map unload 
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.MapUnload = 104
```

### Parameters

This command has no parameters.

## MapPlayerRemove

### Summary

Remove player from current map instance.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!map remove [removalReason]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c map remove [removalReason]
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.MapPlayerRemove = 105
```

### Parameters

<details>

<summary>RemovalReason</summary>

#### Summary

Removal reason.

#### Values

The following numeric values can be used for this parameter.

```
GroupMembership     = 0,
KickedFromCommunity = 1,
CommunityDisband    = 2,
LeftCommunity       = 3,
```

#### Optional

No

</details>

## MapPlayerRemoveCancel

### Summary

Cancel removal of player from current map instance.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!map cancel
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c map cancel 
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.MapPlayerRemoveCancel = 106
```

### Parameters

This command has no parameters.

