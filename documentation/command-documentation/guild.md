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
Invoke the command with the following syntax in the WildStar game chat.

```
!guild register [type] [name] [leaderRank] [councilRank] [memberRank]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c guild register [type] [name] [leaderRank] [councilRank] [memberRank]
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

#### Values

The following numeric values can be used for this parameter.

```
None         = 0,
Guild        = 1,
Circle       = 2,
WarParty     = 3,
ArenaTeam2v2 = 4,
ArenaTeam3v3 = 5,
ArenaTeam5v5 = 6,
Community    = 7,
```

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

The parameter has no summary.

#### Optional

Yes

</details>

<details>

<summary>CouncilRank</summary>

#### Summary

The parameter has no summary.

#### Optional

Yes

</details>

<details>

<summary>MemberRank</summary>

#### Summary

The parameter has no summary.

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
Invoke the command with the following syntax in the WildStar game chat.

```
!guild join [type] [name]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c guild join [type] [name]
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

<summary>Type</summary>

#### Summary

Type of guild to join.

#### Values

The following numeric values can be used for this parameter.

```
None         = 0,
Guild        = 1,
Circle       = 2,
WarParty     = 3,
ArenaTeam2v2 = 4,
ArenaTeam3v3 = 5,
ArenaTeam5v5 = 6,
Community    = 7,
```

#### Optional

No

</details>

<details>

<summary>Name</summary>

#### Summary

Name of guild to join.

#### Optional

No

</details>

