---
description: A collection of commands to interact with door entities.
---

# Door

{% hint style="warning" %}
This page is automatically generated from the NexusForever source code!
{% endhint %}

### Summary

A collection of commands to interact with door entities.

#### RBAC

Role-based access control required to access this command category.

```
Permission.Door = 33
```

## DoorOpen

### Summary

Open all doors within a specified range.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in either the WildStar game chat, World server console or web console.

```
!door open
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c door open
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.DoorOpen = 34
```

### Parameters

<details>

<summary>SearchRange</summary>

#### Summary

Distance to search for doors to open.

#### Optional

No

</details>

## DoorClose

### Summary

Close all doors within a specified range.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in either the WildStar game chat, World server console or web console.

```
!door close
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c door close
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.DoorClose = 35
```

### Parameters

<details>

<summary>SearchRange</summary>

#### Summary

Distance to search for doors to close.

#### Optional

No

</details>

