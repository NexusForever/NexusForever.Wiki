---
description: A collection of commands to modify account currency.
---

# CurrencyAccount

{% hint style="warning" %}
This page is automatically generated from the NexusForever source code!
{% endhint %}

### Summary

A collection of commands to modify account currency.

#### RBAC

Role-based access control required to access this command category.

```
Permission.CurrencyAccount = 24
```

## CurrencyAccountAdd

### Summary

Add currency to account.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!currency account add [currencyId] [amount]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c currency account add [currencyId] [amount]
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.CurrencyAccountAdd = 25
```

### Parameters

<details>

<summary>CurrencyId</summary>

#### Summary

Account currency id to grant.

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

## CurrencyAccountList

### Summary

List all account currency types

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!currency account list
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c currency account list 
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.CurrencyAccountList = 26
```

### Parameters

This command has no parameters.

