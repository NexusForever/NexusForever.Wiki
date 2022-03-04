---
description: A collection of commands to manage a guilds.
---

# Guild

{% hint style="warning" %}
This page is automatically generated from the NexusForever source code!
{% endhint %}

### Summary

A collection of commands to manage a guilds.

#### RBAC

Role-based access control required to access this command category.

```
Permission.Guild = 100
```

## GuildRegister

### Summary

Register a new guild.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in either the WildStar game chat, World server console or web console.

```
!guild register
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c guild register
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.GuildRegister = 101
```

### Parameters

<details>

<summary>Type</summary>

#### Summary

Guild type to create.

#### Optional

No

</details>

<details>

<summary>Name</summary>

#### Summary

Name of newly created guild.

#### Optional

No

</details>

<details>

<summary>LeaderRank</summary>

#### Summary



#### Optional

Yes

</details>

<details>

<summary>CouncilRank</summary>

#### Summary



#### Optional

Yes

</details>

<details>

<summary>MemberRank</summary>

#### Summary



#### Optional

Yes

</details>

## GuildJoin

### Summary

Join an existing guild.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in either the WildStar game chat, World server console or web console.

```
!guild join
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c guild join
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.GuildJoin = 102
```

### Parameters

<details>

<summary>Name</summary>

#### Summary

Name of guild to join.

#### Optional

No

</details>

