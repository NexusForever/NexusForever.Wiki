---
description: A collection of commands to manage the realm.
---

# Realm

{% hint style="warning" %}
This page is automatically generated from the NexusForever source code!
{% endhint %}

### Summary

A collection of commands to manage the realm.

#### RBAC

Role-based access control required to access this command category.

```
Permission.Realm = 82
```

## RealmMotd

### Summary

Set the realm's message of the day and announce to the realm.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in either the WildStar game chat, World server console or web console.

```
!realm motd
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c realm motd
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.RealmMOTD = 94
```

### Parameters

<details>

<summary>Message</summary>

#### Summary

New message of the day for the realm.

#### Optional

No

</details>

## RealmMax

### Summary

Set the maximum players allowed to connect.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in either the WildStar game chat, World server console or web console.

```
!realm max
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c realm max
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.RealmMaxPlayers = 111
```

### Parameters

<details>

<summary>MaxPlayers</summary>

#### Summary

Max players allowed.

#### Optional

No

</details>

