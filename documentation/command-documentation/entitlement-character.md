---
description: A collection of commands to manage character entitlements
---

# EntitlementCharacter

{% hint style="warning" %}
This page is automatically generated from the NexusForever source code!
{% endhint %}

### Summary

A collection of commands to manage character entitlements

#### RBAC

Role-based access control required to access this command category.

```
Permission.EntitlementCharacter = 37
```

## EntitlementCommandCharacterAdd

### Summary

Create or update a character entitlement.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!entitlement character add [entitlementType] [value]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c entitlement character add [entitlementType] [value]
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.EntitlementCharacterAdd = 38
```

### Parameters

<details>

<summary>EntitlementType</summary>

#### Summary

Entitlement type to modify.

#### Optional

No

</details>

<details>

<summary>Value</summary>

#### Summary

Value to modify the entitlement.

#### Optional

No

</details>

## EntitlementCommandCharacterList

### Summary

List all entitlements for account.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!entitlement character list
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c entitlement character list 
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.EntitlementCharacterList = 39
```

### Parameters

This command has no parameters.

