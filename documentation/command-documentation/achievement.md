---
description: A collection of commands to manage player achievements.
---

# Achievement

{% hint style="warning" %}
This page is automatically generated from the NexusForever source code!
{% endhint %}

### Summary

A collection of commands to manage player achievements.

#### RBAC

Role-based access control required to access this command category.

```
Permission.Achievement = 15
```

## AchievementUpdate

### Summary

Update achievement criteria for player.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!achievement update [type] [objectId] [objectIdAlt] [count]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c achievement update [type] [objectId] [objectIdAlt] [count]
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.AchievementUpdate = 17
```

### Parameters

<details>

<summary>Type</summary>

#### Summary

Achievement criteria type to update.

#### Values

The following numeric values can be used for this parameter.

```
KillCreatureEntry = 1,
KillCreatureGroup = 2,
QuestComplete     = 3,
MapComplete       = 53,
ItemConsume       = 80,
```

#### Optional

No

</details>

<details>

<summary>ObjectId</summary>

#### Summary

Object id to match against.

#### Optional

No

</details>

<details>

<summary>ObjectIdAlt</summary>

#### Summary

Alternative object id to match against.

#### Optional

No

</details>

<details>

<summary>Count</summary>

#### Summary

Update count for matched criteria.

#### Optional

No

</details>

## AchievementGrant

### Summary

Grant achievement to player.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!achievement grant [achievementId]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c achievement grant [achievementId]
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.AchievementGrant = 16
```

### Parameters

<details>

<summary>AchievementId</summary>

#### Summary

Achievement id to grant.

#### Optional

No

</details>

