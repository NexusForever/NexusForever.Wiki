---
description: A collection of commands to manage player achievements.
---

# Achievement

{% hint style="warning" %}
This page is automatically generated from the NexusForever source code!
{% endhint %}

## AchievementUpdate

### Summary

Update achievement criteria for player.

#### Invoke

```
!achievement update
/c achievement update
```

#### RBAC

Permission.AchievementUpdate = 17

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

```
!achievement grant
/c achievement grant
```

#### RBAC

Permission.AchievementUpdate = 17

### Parameters

<details>

<summary>AchievementId</summary>

#### Summary

Achievement id to grant.

#### Optional

No

</details>
