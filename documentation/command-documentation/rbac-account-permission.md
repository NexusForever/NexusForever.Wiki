---
description: A collection of commands to manage RBAC permissions for an account.
---

# RBACAccountPermission

{% hint style="warning" %}
This page is automatically generated from the NexusForever source code!
{% endhint %}

### Summary

A collection of commands to manage RBAC permissions for an account.

#### RBAC

Role-based access control required to access this command category.

```
Permission.RBACAccountPermission = 9
```

## RBACAccountPermissionGrant

### Summary

Grant permission to account

#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!rbac account permission grant [permission]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c rbac account permission grant [permission]
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.RBACAccountPermissionGrant = 10
```

### Parameters

<details>

<summary>Permission</summary>

#### Summary

Permission to grant

#### Values

The following numeric values can be used for this parameter.

```
None                        = 0,
Account                     = 1,
AccountCreate               = 2,
AccountDelete               = 3,
Help                        = 4,
CharacterSave               = 5,
ItemAdd                     = 6,
RBAC                        = 7,
RBACAccount                 = 8,
RBACAccountPermission       = 9,
RBACAccountPermissionGrant  = 10,
RBACAccountPermissionRevoke = 11,
RBACAccountRole             = 12,
RBACAccountRoleGrant        = 13,
RBACAccountRoleRevoke       = 14,
Achievement                 = 15,
AchievementGrant            = 16,
AchievementUpdate           = 17,
Broadcast                   = 18,
BroadcastMessage            = 19,
Character                   = 20,
CharacterXP                 = 21,
CharacterLevel              = 22,
Currency                    = 23,
CurrencyAccount             = 24,
CurrencyAccountAdd          = 25,
CurrencyAccountList         = 26,
CurrencyCharacter           = 27,
CurrencyCharacterAdd        = 28,
CurrencyCharacterList       = 29,
Disable                     = 30,
DisableInfo                 = 31,
DisableReload               = 32,
Door                        = 33,
DoorOpen                    = 34,
DoorClose                   = 35,
Entitlement                 = 36,
EntitlementCharacter        = 37,
EntitlementCharacterList    = 39,
EntitlementAccount          = 40,
EntitlementAdd              = 41,
EntitlementAccountList      = 42,
Entity                      = 43,
EntityInfo                  = 44,
EntityProperties            = 45,
Generic                     = 46,
GenericUnlock               = 47,
GenericUnlockAll            = 48,
GenericList                 = 49,
Teleport                    = 50,
TeleportCoordinates         = 51,
TeleportLocation            = 52,
TeleportName                = 53,
House                       = 54,
HouseDecor                  = 55,
HouseDecorAdd               = 56,
HouseDecorLookup            = 57,
HouseTeleport               = 58,
Item                        = 59,
EntityModify                = 60,
EntityModifyDisplayInfo     = 61,
Movement                    = 62,
MovementSpline              = 63,
MovementSplineAdd           = 64,
MovementSplineClear         = 65,
MovementSplineLaunch        = 66,
MovementGenerator           = 67,
MovementGeneratorDirect     = 68,
MovementGeneratorRandom     = 69,
Path                        = 70,
PathUnlock                  = 71,
PathActivate                = 72,
PathXP                      = 73,
Pet                         = 74,
PetUnlockFlair              = 75,
Quest                       = 76,
QuestAdd                    = 77,
QuestAchieve                = 78,
QuestAchieveObjective       = 79,
QuestObjective              = 80,
QuestKill                   = 81,
Realm                       = 82,
Spell                       = 83,
SpellAdd                    = 84,
SpellCast                   = 85,
SpellResetCooldown          = 86,
Title                       = 87,
TitleAdd                    = 88,
TitleRevoke                 = 89,
TitleAll                    = 90,
TitleNone                   = 91,
ItemLookup                  = 92,
RealmMOTD                   = 94,
Story                       = 95,
StoryPanel                  = 96,
StoryCommunicator           = 97,
Reputation                  = 98,
ReputationUpdate            = 99,
Guild                       = 100,
GuildRegister               = 101,
GuildJoin                   = 102,
Map                         = 103,
MapUnload                   = 104,
MapPlayerRemove             = 105,
MapPlayerRemoveCancel       = 106,
RealmShutdown               = 107,
RealmShutdownStart          = 108,
RealmShutdownCancel         = 109,
QuestList                   = 110,
RealmMaxPlayers             = 111,
InstantLogout               = 10000,
Signature                   = 10001,
BypassInstanceLimits        = 10002,
GMFlag                      = 10003,
EntitlementGrantOther       = 10004,
```

#### Optional

No

</details>

## RBACAccountPermissionRevoke

### Summary



#### Invoke

Invoke this command with one of the two following methods:

{% tabs %}
{% tab title="Method 1" %}
Invoke the command with the following syntax in the WildStar game chat.

```
!rbac account permission revoke [permission]
```
{% endtab %}

{% tab title="Method 2" %}
Invoke the command with the following syntax in the WildStar game chat.

```
/c rbac account permission revoke [permission]
```
{% endtab %}
{% endtabs %}

#### RBAC

Role-based access control required to access this command.

```
Permission.RBACAccountPermissionRevoke = 11
```

### Parameters

<details>

<summary>Permission</summary>

#### Summary

Permission to revoke

#### Values

The following numeric values can be used for this parameter.

```
None                        = 0,
Account                     = 1,
AccountCreate               = 2,
AccountDelete               = 3,
Help                        = 4,
CharacterSave               = 5,
ItemAdd                     = 6,
RBAC                        = 7,
RBACAccount                 = 8,
RBACAccountPermission       = 9,
RBACAccountPermissionGrant  = 10,
RBACAccountPermissionRevoke = 11,
RBACAccountRole             = 12,
RBACAccountRoleGrant        = 13,
RBACAccountRoleRevoke       = 14,
Achievement                 = 15,
AchievementGrant            = 16,
AchievementUpdate           = 17,
Broadcast                   = 18,
BroadcastMessage            = 19,
Character                   = 20,
CharacterXP                 = 21,
CharacterLevel              = 22,
Currency                    = 23,
CurrencyAccount             = 24,
CurrencyAccountAdd          = 25,
CurrencyAccountList         = 26,
CurrencyCharacter           = 27,
CurrencyCharacterAdd        = 28,
CurrencyCharacterList       = 29,
Disable                     = 30,
DisableInfo                 = 31,
DisableReload               = 32,
Door                        = 33,
DoorOpen                    = 34,
DoorClose                   = 35,
Entitlement                 = 36,
EntitlementCharacter        = 37,
EntitlementCharacterList    = 39,
EntitlementAccount          = 40,
EntitlementAdd              = 41,
EntitlementAccountList      = 42,
Entity                      = 43,
EntityInfo                  = 44,
EntityProperties            = 45,
Generic                     = 46,
GenericUnlock               = 47,
GenericUnlockAll            = 48,
GenericList                 = 49,
Teleport                    = 50,
TeleportCoordinates         = 51,
TeleportLocation            = 52,
TeleportName                = 53,
House                       = 54,
HouseDecor                  = 55,
HouseDecorAdd               = 56,
HouseDecorLookup            = 57,
HouseTeleport               = 58,
Item                        = 59,
EntityModify                = 60,
EntityModifyDisplayInfo     = 61,
Movement                    = 62,
MovementSpline              = 63,
MovementSplineAdd           = 64,
MovementSplineClear         = 65,
MovementSplineLaunch        = 66,
MovementGenerator           = 67,
MovementGeneratorDirect     = 68,
MovementGeneratorRandom     = 69,
Path                        = 70,
PathUnlock                  = 71,
PathActivate                = 72,
PathXP                      = 73,
Pet                         = 74,
PetUnlockFlair              = 75,
Quest                       = 76,
QuestAdd                    = 77,
QuestAchieve                = 78,
QuestAchieveObjective       = 79,
QuestObjective              = 80,
QuestKill                   = 81,
Realm                       = 82,
Spell                       = 83,
SpellAdd                    = 84,
SpellCast                   = 85,
SpellResetCooldown          = 86,
Title                       = 87,
TitleAdd                    = 88,
TitleRevoke                 = 89,
TitleAll                    = 90,
TitleNone                   = 91,
ItemLookup                  = 92,
RealmMOTD                   = 94,
Story                       = 95,
StoryPanel                  = 96,
StoryCommunicator           = 97,
Reputation                  = 98,
ReputationUpdate            = 99,
Guild                       = 100,
GuildRegister               = 101,
GuildJoin                   = 102,
Map                         = 103,
MapUnload                   = 104,
MapPlayerRemove             = 105,
MapPlayerRemoveCancel       = 106,
RealmShutdown               = 107,
RealmShutdownStart          = 108,
RealmShutdownCancel         = 109,
QuestList                   = 110,
RealmMaxPlayers             = 111,
InstantLogout               = 10000,
Signature                   = 10001,
BypassInstanceLimits        = 10002,
GMFlag                      = 10003,
EntitlementGrantOther       = 10004,
```

#### Optional

No

</details>

