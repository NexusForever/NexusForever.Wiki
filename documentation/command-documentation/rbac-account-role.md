---
description: A collection of commands to manage RBAC roles for an account.
---

# RBACAccountRole

{% hint style="warning" %}
This page is automatically generated from the NexusForever source code!
{% endhint %}

### Summary

A collection of commands to manage RBAC roles for an account.

#### RBAC

Role-based access control required to access this command category.

```
Permission.RBACAccountRole = 12
```

## RBACAccountRoleGrant

### Summary

Grant role to account

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!rbac account role grant [role]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c rbac account role grant [role]
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.RBACAccountRoleGrant = 13
```

### Parameters

<details>

<summary>Role</summary>

#### Summary

Role to grant

#### Values

The following numeric values can be used for this parameter.

```
Player        = 1,
GameMaster    = 2,
Administrator = 3,
Console       = 4,
WebSocket     = 5,
```

#### Optional

No

</details>

## RBACAccountRoleRevoke

### Summary

Remove role from account

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!rbac account role revoke [role]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c rbac account role revoke [role]
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.RBACAccountRoleRevoke = 14
```

### Parameters

<details>

<summary>Role</summary>

#### Summary

Role to revoke

#### Values

The following numeric values can be used for this parameter.

```
Player        = 1,
GameMaster    = 2,
Administrator = 3,
Console       = 4,
WebSocket     = 5,
```

#### Optional

No

</details>

