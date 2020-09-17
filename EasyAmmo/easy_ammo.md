# EasyAmmo
## index
* [General Info](#general-info)
* [Commands](#commands)
* [Source Code Github Repo](#source-code-github-repo)

# General Info
EasyAmmo provides easy commands to use to spawn ammo mags for your currently held weapon and supports uconomy as well

# Commands
## /ammo 
#### usage: 
* /ammo (amount; default 1) (c; for give current mag)
#### permission: 
* ammo
#### summary:
directly puts ammo for your currently held weapon into your inventory

adding `c` to the end of the arguments makes the command give you the weapons current magazine

without the `c` it gives the gun's default magazine the gun spawns with

user's require the `ammo.amount` permission to be able to specify the amount of magazines to spawn

example usages: 
* /ammo c  
* /ammo 
* /ammo 10 
* /ammo 10 c

## /dropammo 
#### usage: 
* /dropammo (amount; default 1) (c; for give current mag)
#### permission: 
* dropammo
#### aliases:
* dammo
* da
* dropa
#### summary:
drops ammo for your currently held weapon onto the ground

adding `c` to the end of the arguments makes the command give you the weapons current magazine

without the `c` it gives the gun's default magazine the gun spawns with

user's require the `dropammo.amount` permission to be able to specify the amount of magazines to drop

example usages: 
* /dropammo c  
* /dropammo 
* /dropammo 10 
* /dropammo 10 c

## /clonei 
#### usage: 
* /clonei (amount; default 1)
#### permission: 
* clonei
#### summary:
gives the user a clone if their currently held item

user's require the `clonei.amount` permission to be able to specify the amount of magazines to drop

example usages: 
* /clonei   
* /clonei 4

# /clearmag
#### usage: 
* /clearmag
#### permission: 
* clearmag
#### aliases:
* clearm
* cm
#### summary:
clears all magazines from the user's inventory

example usages: 
* /clearmag
* /cm   


# Source Code Github Repo
Project source code / home

https://github.com/sharkbound/EasyAmmoRocketMod