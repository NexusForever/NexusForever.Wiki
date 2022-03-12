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
Invoke the command with the following syntax in the WildStar game chat.

```
!generic unlock [genericUnlockEntryId]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c generic unlock [genericUnlockEntryId]
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
Invoke the command with the following syntax in the WildStar game chat.

```
!generic unlockall [genericUnlockType]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c generic unlockall [genericUnlockType]
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

#### Values

The following numeric values can be used for this parameter.

```
Unknown = 0,
Dye     = 1,
```

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
Invoke the command with the following syntax in the WildStar game chat.

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

