# MTG Magic Duels APIs
{δ}: Energy counter
## Filter

### functions

`Add(filterType, operator , cardType)`

- filterType: `FE_TYPE`, `FE_PLAYER_INSTANCE`, `FE_SUBTYPE` , `FE_CONTROLLER`, `FE_CHARACTERISTIC`, `FE_NUM_COLOURS`, `FE_IS_SPELL`, `FE_CARD_NAME`, `FE_CARD_INSTANCE`
- operator:`OP_IS, OP_NOT, OP_GREATER_THAN`
- cardType:`CARD_TYPE_XXXX`,`CREATURE_TYPE_XXXX`

`SetZone(zone,player)`

- zone:`ZONE_LIBRARY, ZONE_HAND` etc.
- player: player

`SetFilterType( FILTER_TYPE_PLAYERS + FILTER_TYPE_CARDS )`

`Count`: 很好理解……

`CountStopAt(int)`: returns integer

## Card

### functions

```lua
AddCounters()
AddScore()
AllowSFX()
AlterCost_PayableWithManaOfAnyColor()
AlterCost_SetMinConverted()
AlternateCostWasPaid()
Attach()
AttachToPlayer()
BecomeMonstrous()
BecomeRenown()
CalcScore()
CanAttachTo()
CanBePlayed()
CanPayCostWithManaOfAnyColor()
CanTransform()
ChangeTargetTo()
ClearDamage()
ClearFilter()
ConvergeColourCount()
CouldMeldWith()
CountAttachedAuras()
CountAttachedEquipment()
CountCounters()
CounterSpell()
DealDamageTo()
DealUnpreventableDamageTo()
DecreaseAbilityColouredCost()
DecreaseAbilityCost()
DecreaseColouredCost()
DecreaseCost()
Destroy()
DestroyWithoutRegenerate()
Discard()
Exile()
ExileFaceDown()
ExileWithMeldEffect()
ExileWithPlaneswalkerSpark()
GetBestOrWorstCounterType()
GetBlockVictim()
GetCardName()
GetCardTitle()
GetCardType()
GetColour()
GetController()
GetConvertedManaCost()
GetCurrentCharacteristics()
GetCurrentPower()
GetCurrentToughness()
GetDamage()
GetDataChest()
GetDefendingPlayer()
GetErstwhileErstwhileZone()
GetErstwhileErstwhileZoneController()
GetErstwhileZone()
GetErstwhileZoneController()
GetExpansionID()
GetFilter()
GetHitPoints()
GetKickedCount()
GetLastDamageAmountDealt()
GetManaX()
GetMonstrosity()
GetNumTargets()
GetNumXsInCost()
GetOwner()
GetPaidX()
GetParent()
GetParentPlayer()
GetPlaneswalkerAttacked()
GetPlayer()
GetPlayerAttacked()
GetRenown()
GetSetID()
GetSpec()
GetSubType()
GetSuperType()
GetZone()
GiveRegeneration()
GrantPseudoFlash()
GuidedReveal()
HasCategory()
HasSummoningSickness()
Hold()
IncreaseAbilityColouredCost()
IncreaseAbilityCost()
IncreaseColouredCost()
IncreaseCost()
IsAttacking()
IsBlocked()
IsBlocking()
IsEnchanted()
IsFaceDown()
IsMonstrous()
IsPermanent()
IsRenown()
IsTapped()
IsTargeting()
IsTargetingOnly()
IsToken()
IsTransformed()
IsVisibleTo()
LoadTargetDefinition()
LoadTargetDefinitionFromDC()
MarkForFilter()
MeldWith()
MidResolutionSetController()
NailOnto()
NumAttacksThisTurn()
PlayFreeFromAnywhere()
PreventDamage()
PreventNextDamage()
Protection()
PutInGraveyard()
PutInHand()
PutInLibrary()
PutInPlaneDeck()
PutOnBottomOfLibrary()
PutOntoBattlefield()
PutOntoBattlefieldAttachedTo()
PutOntoBattlefieldAttacking()
PutOntoBattlefieldBlocking()
PutOntoBattlefieldTapped()
PutOntoBattlefieldTappedAndAttacking()
PutOntoBattlefieldTransformed()
PutOntoBattlefieldUnTappedAndAttacking()
PutOntoBattlefieldWithCounters()
PutOnTopOfLibrary()
QueueZoneChange()
RemoveCounters()
RemoveFromCombat()
RemoveFromParent()
ResourceAbilityGetTimesActivated()
ReturnToOwnersHand()
SetBaseController()
SetController()
StoreCopiableValues()
Tap()
TapAndHold()
Transform()
TurnFaceDown()
TurnFaceUp()
Untap()
UseCopiableValues()()
WasBlocked()
WasCast()
WasCostPaid()
WasKicked()
WasPaidForWithColour()
Transform()
```



## characteristics

### function

```lua
CardType_GetWritable() --type:Add( CARD_TYPE_CREATURE) 
GetColour() -- colour:Add( COLOUR_BLACK )
GetConvertedManaCost()
Power_Add(int)
SubType_GetWritable() --see type
Toughness_Add(int)
Bool_Set(constant,1 or 0)
```

### constants

```lua
CHARACTERISTIC_ALL_CREATURES_MUST_BLOCK_THIS_IF_ABLE
CHARACTERISTIC_ANNIHILATOR
CHARACTERISTIC_BATTLE_CRY
CHARACTERISTIC_CANNOT_ATTACK_ALONE
CHARACTERISTIC_CANNOT_BLOCK_ALONE
CHARACTERISTIC_CANT_ATTACK
CHARACTERISTIC_CANT_BE_BLOCKED
CHARACTERISTIC_CANT_BE_BLOCKED_BY_CREATURES_WITH_LESS_POWER
CHARACTERISTIC_CANT_BE_BLOCKED_BY_MORE_THAN_ONE_CREATURE
CHARACTERISTIC_CANT_BE_BLOCKED_EXCEPT_BY_ALL_DEFENDING_CREATURES
CHARACTERISTIC_CANT_BE_BLOCKED_EXCEPT_BY_CREATURES_WITH_FLYING
CHARACTERISTIC_CANT_BE_BLOCKED_EXCEPT_BY_CREATURES_WITH_FLYING_OR_REACH
CHARACTERISTIC_CANT_BE_BLOCKED_EXCEPT_BY_THREE_OR_MORE_CREATURES
CHARACTERISTIC_CANT_BE_COUNTERED
CHARACTERISTIC_CANT_BE_PLAYED
CHARACTERISTIC_CANT_BE_REGENERATED
CHARACTERISTIC_CANT_BLOCK
CHARACTERISTIC_CANT_CREW_VEHICLES
CHARACTERISTIC_CANT_HAVE_COUNTERS
CHARACTERISTIC_CANT_USE_ACTIVATED_ABILITIES_EXCEPT_MANA_ABILITIES
CHARACTERISTIC_CANT_USE_ACTIVATED_ABILITIES_INCLUDING_MANA_ABILITIES
CHARACTERISTIC_CAN_ATTACK_AS_THOUGH_DIDNT_HAVE_DEFENDER
CHARACTERISTIC_CAN_ATTACK_AS_THOUGH_HAS_HASTE
CHARACTERISTIC_CAN_BLOCK_ANY_NUMBER_OF_CREATURES
CHARACTERISTIC_CAN_BLOCK_IF_TAPPED
CHARACTERISTIC_CAN_BLOCK_ONLY_CREATURES_WITH_FLYING
CHARACTERISTIC_CHANGELING
CHARACTERISTIC_COMES_INTO_PLAY_TAPPED
CHARACTERISTIC_DEATHTOUCH
CHARACTERISTIC_DEATHTOUCH_HINT
CHARACTERISTIC_DEFENDER
CHARACTERISTIC_DOESNT_DEAL_COMBAT_DAMAGE
CHARACTERISTIC_DOESNT_DEAL_DAMAGE
CHARACTERISTIC_DOESNT_RECEIVE_COMBAT_DAMAGE
CHARACTERISTIC_DOESNT_RECEIVE_DAMAGE
CHARACTERISTIC_DOESNT_UNTAP
CHARACTERISTIC_DOUBLE_STRIKE
CHARACTERISTIC_EXILE_IF_DIES
CHARACTERISTIC_EXILE_IF_GOES_TO_GRAVEYARD
CHARACTERISTIC_FADING
CHARACTERISTIC_FEAR
CHARACTERISTIC_FIRST_STRIKE
CHARACTERISTIC_FLANKING
CHARACTERISTIC_FLASH
CHARACTERISTIC_FLYING
CHARACTERISTIC_FORESTWALK
CHARACTERISTIC_HASTE
CHARACTERISTIC_HEXPROOF
CHARACTERISTIC_INDESTRUCTIBLE
CHARACTERISTIC_INFECT
CHARACTERISTIC_INTIMIDATE
CHARACTERISTIC_ISLANDWALK
CHARACTERISTIC_LIFELINK
CHARACTERISTIC_MENACE
CHARACTERISTIC_MOUNTAINWALK
CHARACTERISTIC_MUST_ATTACK
CHARACTERISTIC_MUST_ATTACK_EACH_TURN
CHARACTERISTIC_MUST_BE_BLOCKED_IF_ABLE
CHARACTERISTIC_MUST_BLOCK
CHARACTERISTIC_PHASING
CHARACTERISTIC_PLAINSWALK
CHARACTERISTIC_REACH
CHARACTERISTIC_SHADOW
CHARACTERISTIC_SHROUD
CHARACTERISTIC_SKULK
CHARACTERISTIC_SWAMPWALK
CHARACTERISTIC_TOTEM_ARMOUR
CHARACTERISTIC_TRAMPLE
CHARACTERISTIC_USE_TOUGHNESS_FOR_COMBAT_DAMAGE
CHARACTERISTIC_VIGILANCE
CHARACTERISTIC_WITHER
INT_CHARACTERISTIC_BUSHIDO
INT_CHARACTERISTIC_EXALTED
```

## Player

### functions

```lua
CanPayManaCost("{}")
CastSpellForFree(card)
DiscardNRandomCards(int) --随机弃牌 int 张
DrawCards(int)
GainEnergyCounters(int)
GainLife(int)
GetLifeTotal()
GetTeam()
Hand_Count()
Library_GetNth(int)
MyTurn() --return boolean
Sacrifice(card)
SetItemPrompt(i,"QUERY_TAG")
ShuffleLibrary()
```

```lua
--multiple choice
player:SetCustomQueryInstructionManaCost( mana_string )
player:BeginNewMultipleChoice()
player:AddMultipleChoiceAnswer( "CARD_QUERY_ANSWER_PSYCHIC_FEEDBACK_1" )   
player:AddMultipleChoiceAnswer( "CARD_QUERY_ANSWER_PSYCHIC_FEEDBACK_2" )   
player:AskMultipleChoiceQuestion( "CARD_QUERY_QUESTION_PSYCHIC_FEEDBACK" )
--------------------------------------------------------------------------
player:GetMultipleChoiceResult() --returns integer
```



## Team

### functions

```
TakeExtraTurn()
```

## EffectDC

### functions

```lua
Get_Targets(int) --:Get_CardPtr(int)
```



## other

```lua
GetEffectX() --for cards whose mana cost contain {X}
--must be used with:
    <DERIVED_INFO tag="DERIVED_INFO_X_IS">
    if EffectSource():GetZone() ~= ZONE_STACK then
    	return ""
    end
    local effectX = GetEffectX()
    if effectX ~= 0 then
    	return effectX
    end
    return EffectSource():GetPaidX()
    </DERIVED_INFO>
```

