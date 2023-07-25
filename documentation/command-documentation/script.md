---
description: A collection of commands to manage the script system.
---

# Script

{% hint style="warning" %}
This page is automatically generated from the NexusForever source code!
{% endhint %}

### Summary

A collection of commands to manage the script system.

#### RBAC

Role-based access control required to access this command category.

```
Permission.Script = 112
```

## ScriptReload

### Summary

Reload a script assembly.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!script reload [assemblyName] [reloadType]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c script reload [assemblyName] [reloadType]
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.ScriptReload = 113
```

### Parameters

<details>

<summary>AssemblyName</summary>

#### Summary

Assembly name to reload.

#### Optional

No

</details>

<details>

<summary>ReloadType</summary>

#### Summary

Type of assembly reload to perform.

#### Values

The following numeric values can be used for this parameter.

```
Assembly = 0,
Source   = 1,
```

#### Optional

No

</details>

## ScriptInfo

### Summary



#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!script info
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c script info 
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.ScriptInfo = 114
```

### Parameters

This command has no parameters.

