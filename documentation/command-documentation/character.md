---
description: A collection of commands to manage a character.
---

# Character

{% hint style="warning" %}
This page is automatically generated from the NexusForever source code!
{% endhint %}

### Summary

A collection of commands to manage a character.

#### RBAC

Role-based access control required to access this command category.

```
Permission.Character = 20
```

## CharacterXP

### Summary

Add XP to character.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!character xp [amount]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c character xp [amount]
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.CharacterXP = 21
```

### Parameters

<details>

<summary>Amount</summary>

#### Summary

Amount of XP to grant character.

#### Optional

No

</details>

## CharacterLevel

### Summary

Add level to character

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!character level [level]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c character level [level]
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.CharacterLevel = 22
```

### Parameters

<details>

<summary>Level</summary>

#### Summary

Level to set character.

#### Optional

No

</details>

## CharacterSave

### Summary

Save any pending changes to the character to the database.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!character save
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c character save 
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.CharacterSave = 5
```

### Parameters

This command has no parameters.

