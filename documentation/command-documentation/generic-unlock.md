---
description: A collection of commands to manage generic unlocks for an account.
---

# GenericUnlock

{% hint style="warning" %}
This page is automatically generated from the NexusForever source code!
{% endhint %}

### Summary

A collection of commands to manage generic unlocks for an account.

#### RBAC

Role-based access control required to access this command category.

```
Permission.Generic = 46
```

## GenericUnlockUnlock

### Summary

Unlock generic unlock entry for an account.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in either the WildStar game chat, World server console or web console.

```
!generic unlock
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c generic unlock
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.GenericUnlock = 47
```

### Parameters

<details>

<summary>GenericUnlockEntryId</summary>

#### Summary

Generic unlock entry to unlock.

#### Optional

No

</details>

## GenericUnlockUnlockAll

### Summary

Unlock all generic unlocks of type for an account.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in either the WildStar game chat, World server console or web console.

```
!generic unlockall
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c generic unlockall
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.GenericUnlockAll = 48
```

### Parameters

<details>

<summary>GenericUnlockType</summary>

#### Summary

Generic unlock type to unlock all entries from.

#### Optional

No

</details>

## GenericUnlockList

### Summary

ist all acquired generic unlock entries for an account.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in either the WildStar game chat, World server console or web console.

```
!generic list
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c generic list
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.GenericList = 49
```

### Parameters

This command has no parameters.

