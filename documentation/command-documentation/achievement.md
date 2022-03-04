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
Permission.Achievement= 15
```

## AchievementUpdate

### Summary

Update achievement criteria for player.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in either the WildStar game chat, World server console or web console.

```
!achievement update
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c achievement update
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
Invoke the command with the following syntax in either the WildStar game chat, World server console or web console.

```
!achievement update
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c achievement update
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.AchievementGrant= 16
```

### Parameters

<details>

<summary>AchievementId</summary>

#### Summary

Achievement id to grant.

#### Optional

No

</details>