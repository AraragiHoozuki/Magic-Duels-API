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
AddCounters(counterType,int)
Attach(card) --结附
BecomeRenown(int) --铭勇
CountCounters(counterType)
CounterSpell()
DealDamageTo(amount, target)
DecreseCost(integer)
Destroy(sourceCard) --消灭 c，原因为 sourceCard
DestroyWithoutRegenerate() --消灭 c 且不能重生
Discard()
GetController()
GetCurrentCharacteristics() --获取当前属性
GetParent() --get attached card
IncreaseAbilityCost(int) --for activated abilities
Protection() --保护
PutInHand()
PutOntoBattlefieldTapped(player) --c 在 player 的控制下横置入场
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
--基本异能---------------------------------------
CHARACTERISTIC_VIGILANCE
CHARACTERISTIC_HEXPROOF
CHARACTERISTIC_DEFENDER
CHARACTERISTIC_FLYING
CHARACTERISTIC_HASTE
CHARACTERISTIC_FIRST_STRIKE
CHARACTERISTIC_DEATHTOUCH
CHARACTERISTIC_TRAMPLE
CHARACTERISTIC_DOUBLE_STRIKE
CHARACTERISTIC_REACH
CHARACTERISTIC_LIFELINK
--特殊异能----------------------------------------
CHARACTERISTIC_CAN_BLOCK_ANY_NUMBER_OF_CREATURES --多重阻挡
CHARACTERISTIC_DOESNT_RECEIVE_COMBAT_DAMAGE --不受战斗伤害
CHARACTERISTIC_CANT_BE_BLOCKED
CHARACTERISTIC_CANT_BE_BLOCKED_EXCEPT_BY_CREATURES_WITH_FLYING_OR_REACH
CHARACTERISTIC_CANT_BE_BLOCKED_BY_MORE_THAN_ONE_CREATURE
CHARACTERISTIC_CANT_BE_COUNTERED
CHARACTERISTIC_CANT_ATTACK
CHARACTERISTIC_CANT_BLOCK
CHARACTERISTIC_CANT_USE_ACTIVATED_ABILITIES_INCLUDING_MANA_ABILITIES
CHARACTERISTIC_EXILE_IF_DIES
CHARACTERISTIC_MUST_ATTACK_EACH_TURN
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

