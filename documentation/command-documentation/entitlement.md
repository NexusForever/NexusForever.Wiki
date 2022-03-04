---
description: A collection of commands to manage account and character entitlements.
---

# Entitlement

{% hint style="warning" %}
This page is automatically generated from the NexusForever source code!
{% endhint %}

### Summary

A collection of commands to manage account and character entitlements.

#### RBAC

Role-based access control required to access this command category.

```
Permission.Entitlement = 36
```

## EntitlementCommandAdd

### Summary

Create or update an entitlement.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!entitlement add [entitlementType] [value]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c entitlement add [entitlementType] [value]
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.EntitlementAdd = 41
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

