---
description: A collection of commands to manage account entitlements
---

# EntitlementAccount

{% hint style="warning" %}
This page is automatically generated from the NexusForever source code!
{% endhint %}

### Summary

A collection of commands to manage account entitlements

#### RBAC

Role-based access control required to access this command category.

```
Permission.EntitlementAccount = 40
```

## EntitlementCommandAccountAdd

### Summary

Create or update an account entitlement.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in either the WildStar game chat, World server console or web console.

```
!entitlement account add
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c entitlement account add
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.EntitlementAccountAdd = 41
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

## EntitlementCommandAccountList

### Summary

List all entitlements for character.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in either the WildStar game chat, World server console or web console.

```
!entitlement account list
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c entitlement account list
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.EntitlementAccountList = 42
```

### Parameters

This command has no parameters.

