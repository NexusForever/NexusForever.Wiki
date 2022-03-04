---
description: A collection of commands to manage quests for a character.
---

# Quest

{% hint style="warning" %}
This page is automatically generated from the NexusForever source code!
{% endhint %}

### Summary

A collection of commands to manage quests for a character.

#### RBAC

Role-based access control required to access this command category.

```
Permission.Quest = 76
```

## QuestList

### Summary

List all active quests.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!quest list
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c quest list 
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.QuestList = 110
```

### Parameters

This command has no parameters.

## QuestAdd

### Summary

Add a new quest to character.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!quest add [questId]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c quest add [questId]
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.QuestAdd = 77
```

### Parameters

<details>

<summary>QuestId</summary>

#### Summary

Quest entry id to add to character.

#### Optional

No

</details>

## QuestAchieve

### Summary

Achieve an existing quest by completing all objectives for character.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!quest achieve [questId]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c quest achieve [questId]
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.QuestAchieve = 78
```

### Parameters

<details>

<summary>QuestId</summary>

#### Summary

Quest entry id to achieve for character.

#### Optional

No

</details>

## QuestAchieveObjective

### Summary

Achieve a single objective for an existing quest for character.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!quest achieveobjective [questId] [index]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c quest achieveobjective [questId] [index]
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.QuestAchieveObjective = 79
```

### Parameters

<details>

<summary>QuestId</summary>

#### Summary

Quest entry id to achieve for character.

#### Optional

No

</details>

<details>

<summary>Index</summary>

#### Summary

Quest objective index to achieve for character.

#### Optional

No

</details>

## QuestObjective

### Summary

Update all quest objectives with type for character.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!quest objective [type] [data] [progress]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c quest objective [type] [data] [progress]
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.QuestObjective = 80
```

### Parameters

<details>

<summary>Type</summary>

#### Summary

Quest objective type for objectives to update.

#### Optional

No

</details>

<details>

<summary>Data</summary>

#### Summary

Data value to match quest objectives against.

#### Optional

No

</details>

<details>

<summary>Progress</summary>

#### Summary

Progress to increment matching quest objectives.

#### Optional

No

</details>

## QuestKill

### Summary

Update all quest objectives that require a kill with the given creature id.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!quest kill [creatureId] [quantity]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c quest kill [creatureId] [quantity]
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.QuestKill = 81
```

### Parameters

<details>

<summary>CreatureId</summary>

#### Summary

Creature id to match quest objectives against.

#### Optional

No

</details>

<details>

<summary>Quantity</summary>

#### Summary

Quantity to update quest objectives by.

#### Optional

No

</details>

