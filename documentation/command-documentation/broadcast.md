---
description: A collection of commands to broadcast server wide messages.
---

# Broadcast

{% hint style="warning" %}
This page is automatically generated from the NexusForever source code!
{% endhint %}

### Summary

A collection of commands to broadcast server wide messages.

#### RBAC

Role-based access control required to access this command category.

```
Permission.Broadcast = 18
```

## BroadcastMessage

### Summary

Broadcast message to all players on the server.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!broadcast message [tier] [message]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c broadcast message [tier] [message]
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.BroadcastMessage = 19
```

### Parameters

<details>

<summary>Tier</summary>

#### Summary

Tier of the message being broadcast.

#### Values

The following numeric values can be used for this parameter.

```
High   = 0,
Medium = 1,
Low    = 2,
```

#### Optional

No

</details>

<details>

<summary>Message</summary>

#### Summary

Message to broadcast.

#### Optional

No

</details>

