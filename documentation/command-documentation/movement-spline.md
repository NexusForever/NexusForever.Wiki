---
description: A collection of commands to control entity spline movement.
---

# MovementSpline

{% hint style="warning" %}
This page is automatically generated from the NexusForever source code!
{% endhint %}

### Summary

A collection of commands to control entity spline movement.

#### RBAC

Role-based access control required to access this command category.

```
Permission.MovementSpline = 63
```

## MovementSplineAddHandler

### Summary

A position to target entity spine nodes.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in either the WildStar game chat, World server console or web console.

```
!movement spline add
!move spline add
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c movement spline add
/c move spline add
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.MovementSplineAdd = 64
```

### Parameters

This command has no parameters.

## MovementSplineClearHandler

### Summary

Clear all positions from target entity spline nodes.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in either the WildStar game chat, World server console or web console.

```
!movement spline clear
!move spline clear
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c movement spline clear
/c move spline clear
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.MovementSplineClear = 65
```

### Parameters

This command has no parameters.

## MovementSplineLaunchHandler

### Summary

Launch spline for target entity with previously defined nodes and optional mode and speed.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in either the WildStar game chat, World server console or web console.

```
!movement spline launch
!move spline launch
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c movement spline launch
/c move spline launch
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.MovementSplineLaunch = 66
```

### Parameters

<details>

<summary>Mode</summary>

#### Summary

Mode to launch the spline.

#### Optional

No

</details>

<details>

<summary>Speed</summary>

#### Summary

Speed to launch the spline.

#### Optional

No

</details>

