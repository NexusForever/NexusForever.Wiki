---
description: A collection of commands to manage teleporting characters.
---

# Teleport

{% hint style="warning" %}
This page is automatically generated from the NexusForever source code!
{% endhint %}

### Summary

A collection of commands to manage teleporting characters.

#### RBAC

Role-based access control required to access this command category.

```
Permission.Teleport = 50
```

## TeleportCoordinates

### Summary

Teleport to the specified coordinates optionally specifying the world.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in either the WildStar game chat, World server console or web console.

```
!teleport coordinates
!port coordinates
!tele coordinates
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c teleport coordinates
/c port coordinates
/c tele coordinates
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.TeleportCoordinates = 51
```

### Parameters

<details>

<summary>X</summary>

#### Summary

X coordinate for target teleport position.

#### Optional

No

</details>

<details>

<summary>Y</summary>

#### Summary

Y coordinate for target teleport position.

#### Optional

No

</details>

<details>

<summary>Z</summary>

#### Summary

Z coordinate for target teleport position.

#### Optional

No

</details>

<details>

<summary>WorldId</summary>

#### Summary

Optional world id for target teleport position.

#### Optional

No

</details>

## TeleportLocation

### Summary

Teleport to the specified world location.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in either the WildStar game chat, World server console or web console.

```
!teleport location
!port location
!tele location
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c teleport location
/c port location
/c tele location
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.TeleportLocation = 52
```

### Parameters

<details>

<summary>WorldLocation2Id</summary>

#### Summary

World location id for target teleport position.

#### Optional

No

</details>

## TeleportName

### Summary

Teleport to the specified zone name.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in either the WildStar game chat, World server console or web console.

```
!teleport name
!port name
!tele name
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c teleport name
/c port name
/c tele name
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.TeleportName = 53
```

### Parameters

<details>

<summary>Name</summary>

#### Summary

Name of the zone for target teleport position.

#### Optional

No

</details>

