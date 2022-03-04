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
Invoke the command with the following syntax in the WildStar game chat.

```
!teleport coordinates [x] [y] [z] [worldId]
!port coordinates [x] [y] [z] [worldId]
!tele coordinates [x] [y] [z] [worldId]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c teleport coordinates [x] [y] [z] [worldId]
/c port coordinates [x] [y] [z] [worldId]
/c tele coordinates [x] [y] [z] [worldId]
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
Invoke the command with the following syntax in the WildStar game chat.

```
!teleport location [worldLocation2Id]
!port location [worldLocation2Id]
!tele location [worldLocation2Id]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c teleport location [worldLocation2Id]
/c port location [worldLocation2Id]
/c tele location [worldLocation2Id]
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
Invoke the command with the following syntax in the WildStar game chat.

```
!teleport name [name]
!port name [name]
!tele name [name]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c teleport name [name]
/c port name [name]
/c tele name [name]
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

