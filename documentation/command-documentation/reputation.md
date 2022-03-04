---
description: A collection of commands for managing character reputations.
---

# Reputation

{% hint style="warning" %}
This page is automatically generated from the NexusForever source code!
{% endhint %}

### Summary

A collection of commands for managing character reputations.

#### RBAC

Role-based access control required to access this command category.

```
Permission.Reputation = 98
```

## ReputationUpdate

### Summary

Update the reputation for a character.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in either the WildStar game chat, World server console or web console.

```
!rep update
!reputation update
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c rep update
/c reputation update
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.ReputationUpdate = 99
```

### Parameters

<details>

<summary>FactionId</summary>

#### Summary

Faction id to update reputation.

#### Optional

No

</details>

<details>

<summary>Value</summary>

#### Summary

Amount to modify the reputation.

#### Optional

No

</details>

