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
Invoke the command with the following syntax in the WildStar game chat.

```
!currency character add [currencyId] [amount]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c currency character add [currencyId] [amount]
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

#### Values

The following numeric values can be used for this parameter.

```
None               = 0,
Credits            = 1,
Renown             = 2,
ElderGems          = 3,
CraftingVoucher    = 4,
Prestige           = 5,
ShadesEveSilver    = 6,
Glory              = 7,
WinterfestColdCast = 9,
Triploons          = 10,
RedEssence         = 11,
BlueEssence        = 12,
GreenEssence       = 13,
PurpleEssence      = 14,
```

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
Invoke the command with the following syntax in the WildStar game chat.

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

