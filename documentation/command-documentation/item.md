---
description: A collection of commands to manage items for a character.
---

# Item

{% hint style="warning" %}
This page is automatically generated from the NexusForever source code!
{% endhint %}

### Summary

A collection of commands to manage items for a character.

#### RBAC

Role-based access control required to access this command category.

```
Permission.Item = 59
```

## ItemAdd

### Summary

Add an item to inventory, optionally specifying quantity and charges.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!item add [itemId] [quantity] [charges]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c item add [itemId] [quantity] [charges]
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.ItemAdd = 6
```

### Parameters

<details>

<summary>ItemId</summary>

#### Summary

Item id to create.

#### Optional

No

</details>

<details>

<summary>Quantity</summary>

#### Summary

Quantity of item to create.

#### Optional

No

</details>

<details>

<summary>Charges</summary>

#### Summary

Amount of charges to add to the item.

#### Optional

No

</details>

## ItemLookup

### Summary

Lookup an item by partial name.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!item lookup [name] [maxResults]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c item lookup [name] [maxResults]
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.ItemLookup = 92
```

### Parameters

<details>

<summary>Name</summary>

#### Summary

Item name to lookup.

#### Optional

No

</details>

<details>

<summary>MaxResults</summary>

#### Summary

Maximum amount of results to return.

#### Optional

No

</details>

## ItemInfo

### Summary

Lookup item information by id.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!item info [itemId]
!item information [itemId]
!item i [itemId]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c item info [itemId]
/c item information [itemId]
/c item i [itemId]
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.ItemInfo = 116
```

### Parameters

<details>

<summary>ItemId</summary>

#### Summary

Id of item to get information on

#### Optional

No

</details>

