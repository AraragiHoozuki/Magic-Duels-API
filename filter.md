## functions

### filter:add conditions
`Add(filterType, operator , cardType)`

filterType:
```lua
FE_TYPE
FE_PLAYER_INSTANCE
FE_SUBTYPE
FE_CONTROLLER
FE_CHARACTERISTIC
FE_NUM_COLOURS
FE_IS_SPELL
FE_CARD_NAME
FE_CARD_INSTANCE
```
operator:
```lua
OP_IS
OP_NOT
OP_GREATER_THAN
```
cardType:
```lua
CARD_TYPE_XXXX,CREATURE_TYPE_XXXX
```
### set filter zone
`SetZone(zone,player)`

### set filter type
`SetFilterType( FILTER_TYPE_PLAYERS + FILTER_TYPE_CARDS )`

### other functions
```lua
Count()
CountStopAt(int) --returns integer
```
