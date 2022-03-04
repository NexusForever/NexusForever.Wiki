---
description: A collection of commands to modify game accounts.
---

# Account

{% hint style="warning" %}
This page is automatically generated from the NexusForever source code!
{% endhint %}

### Summary

A collection of commands to modify game accounts.

#### RBAC

Role-based access control required to access this command category.

```
Permission.Account = 1
```

## AccountCreate

### Summary

Create a new account.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in either the WildStar game chat, World server console or web console.

```
!acc create
!account create
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c acc create
/c account create
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.AccountCreate = 2
```

### Parameters

<details>

<summary>Email</summary>

#### Summary

Email address for the new account

#### Optional

No

</details>

<details>

<summary>Password</summary>

#### Summary

Password for the new account

#### Optional

No

</details>

## AccountDelete

### Summary

Delete an account.

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in either the WildStar game chat, World server console or web console.

```
!acc delete
!account delete
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c acc delete
/c account delete
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.AccountDelete = 3
```

### Parameters

<details>

<summary>Email</summary>

#### Summary

Email address of the account to delete

#### Optional

No

</details>

