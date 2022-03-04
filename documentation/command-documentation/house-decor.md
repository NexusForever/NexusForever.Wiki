---
description: A collection of commands to modify decor in housing residences.
---

# HouseDecor

{% hint style="warning" %}
This page is automatically generated from the NexusForever source code!
{% endhint %}

### Summary

A collection of commands to modify decor in housing residences.

#### RBAC

Role-based access control required to access this command category.

```
Permission.HouseDecor = 55
```

## HouseDecorAdd

### Summary

Add decor to housing residence crate optionally specifying quantity.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in either the WildStar game chat, World server console or web console.

```
!house decor add
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c house decor add
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.HouseDecorAdd = 56
```

### Parameters

<details>

<summary>DecorInfoId</summary>

#### Summary

Decor info id entry to add to the crate.

#### Optional

No

</details>

<details>

<summary>Quantity</summary>

#### Summary

Quantity of decor to add to the crate.

#### Optional

No

</details>

## HouseDecorLookup

### Summary

Returns a list of decor ids that match the supplied name.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in either the WildStar game chat, World server console or web console.

```
!house decor lookup
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c house decor lookup
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.HouseDecorLookup = 57
```

### Parameters

<details>

<summary>Name</summary>

#### Summary

Name or partial name of the housing decor item to search for.

#### Optional

No

</details>

