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
Invoke the command with the following syntax in either the WildStar game chat, World server console or web console.

```
!disable info
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c disable info
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
Invoke the command with the following syntax in either the WildStar game chat, World server console or web console.

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

