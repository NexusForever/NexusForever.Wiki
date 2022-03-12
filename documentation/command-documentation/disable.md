---
description: A collection of commands to manage entity disables.
---

# Disable

{% hint style="warning" %}
This page is automatically generated from the NexusForever source code!
{% endhint %}

### Summary

A collection of commands to manage entity disables.

#### RBAC

Role-based access control required to access this command category.

```
Permission.Disable = 30
```

## DisableInfo

### Summary

Return information on the supplied disable and object id.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!disable info [disableType] [objectId]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c disable info [disableType] [objectId]
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.DisableInfo = 31
```

### Parameters

<details>

<summary>DisableType</summary>

#### Summary

Disabled entity type.

#### Values

The following numeric values can be used for this parameter.

```
Quest           = 0,
Spell           = 1,
BaseSpell       = 2,
Item            = 3,
World           = 4,
Currency        = 5,
AccountCurrency = 6,
Achievement     = 7,
```

#### Optional

No

</details>

<details>

<summary>ObjectId</summary>

#### Summary

Object id for the disabled entity type.

#### Optional

No

</details>

## DisableReload

### Summary

Reload all entity disables from the database.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!disable reload
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c disable reload 
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.DisableReload = 32
```

### Parameters

This command has no parameters.

