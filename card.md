# Card API
## functions
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
