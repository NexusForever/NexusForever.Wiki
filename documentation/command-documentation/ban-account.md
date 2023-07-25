---
description: A collection of commands to manage account bans.
---

# BanAccount

{% hint style="warning" %}
This page is automatically generated from the NexusForever source code!
{% endhint %}

### Summary

A collection of commands to manage account bans.

#### RBAC

Role-based access control required to access this command category.

```
Permission.BanAccount = 118
```

## BanAccountPlayer

### Summary

Ban an account of a player.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!ban account player [reason] [bannedTill]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c ban account player [reason] [bannedTill]
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.BanAccountPlayer = 119
```

### Parameters

<details>

<summary>Reason</summary>

#### Summary

Reason for ban.

#### Optional

No

</details>

<details>

<summary>BannedTill</summary>

#### Summary

Ban expiry time.

#### Optional

No

</details>

## BanAccountCharacter

### Summary

Ban an account of a character.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!ban account character [name] [reason] [bannedTill]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c ban account character [name] [reason] [bannedTill]
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.BanAccountCharacter = 120
```

### Parameters

<details>

<summary>Name</summary>

#### Summary

Name of character that belongs to account to be banned.

#### Optional

No

</details>

<details>

<summary>Reason</summary>

#### Summary

Reason for ban.

#### Optional

No

</details>

<details>

<summary>BannedTill</summary>

#### Summary

Ban expiry time.

#### Optional

No

</details>

