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

#### Values

The following numeric values can be used for this parameter.

```
CostumeSlots                           = 3,
Warplots                               = 4,
CoreTester                             = 5,
TwoStepVerification                    = 9,
BaseCharacterProgressionCaps           = 10,
BaseCharacterSlots                     = 12,
BaseCurrencyCaps                       = 14,
EconomyParticipation                   = 15,
GuildsAccess                           = 16,
FullSocialParticipation                = 17,
CREDDUsage                             = 18,
InGameCSAccess                         = 19,
Signature                              = 22,
ExtraAuctions                          = 23,
ExtraCommodityOrders                   = 25,
ExtraDecorSlots                        = 26,
ExtraBankSlots                         = 27,
Free                                   = 31,
LoyaltyBonusCoordinateCraftingRadius   = 32,
CosmicRewardsOmnibitDropRate           = 35,
AdditionalCostumeUnlocks               = 36,
CosmicRewardsReputationGain            = 37,
FullGuildsAccess                       = 38,
CosmicRewardsCircuitBoardCraftingBonus = 39,
WakeHereCooldownReduction              = 41,
LoyaltyExtraCommodityOrders            = 42,
LoyaltyExtraAuctions                   = 43,
LoyaltyChallengeBonus                  = 44,
LoyaltyRestXpBonus                     = 45,
CosmicRewardsHarvestingBoost           = 46,
VIPTier                                = 48,
FraudCheck                             = 49,
TitleImmortal                          = 55,
TitleOriginalFury                      = 56,
TitleMasterofSteel                     = 57,
TitleBladewind                         = 58,
TitleRedmoonRobber                     = 59,
TitleRotostarConqueror                 = 60,
ChuaWarriorUnlock                      = 61,
AurinEngineerUnlock                    = 62,
CanPurchasePromotionToken              = 63,
TitleTheArctester                      = 64,
ExtraSupplySatchelSlots                = 71,
SharedRealmBankUnlock                  = 74,
SharedRealmBankSlots                   = 75,
```

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

