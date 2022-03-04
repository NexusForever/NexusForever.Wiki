---
description: A collection of commands to modify character currency.
---

# CurrencyCharacter

{% hint style="warning" %}
This page is automatically generated from the NexusForever source code!
{% endhint %}

### Summary

A collection of commands to modify character currency.

#### RBAC

Role-based access control required to access this command category.

```
Permission.CurrencyCharacter = 27
```

## CurrencyCharacterAdd

### Summary

Add currency to character.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in either the WildStar game chat, World server console or web console.

```
!currency character add
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c currency character add
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.CurrencyCharacterAdd = 28
```

### Parameters

<details>

<summary>CurrencyId</summary>

#### Summary

Currency id to grant.

#### Optional

No

</details>

<details>

<summary>Amount</summary>

#### Summary

Amount of currency to grant.

#### Optional

No

</details>

## CurrencyCharacterList

### Summary

List all currency types.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in either the WildStar game chat, World server console or web console.

```
!currency character list
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c currency character list
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.CurrencyCharacterList = 29
```

### Parameters

This command has no parameters.
