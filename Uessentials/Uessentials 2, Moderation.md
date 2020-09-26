# Section 2. Moderation

## /freeze
There are many moderation commands for Uessentials but first we will focus on the /freeze command.
/freeze is the command to stop players from moving. They are stuck in 1 place until unfrozen. In the Config.json file of Uessentials exist the following lines:
  "UnfreezeOnDeath": false,
  "UnfreezeOnQuit": true,
 
The first one (UnfreezeOnDeath) is refering to, if the player dies, is killed, or commits suicide they are unfrozen. The false means that this will not happen. So what this config 
tells us, is that when someone is frozen and dies, they will still be frozen. The second config (UnfreezeOnQuit) is refering to, if the player leaves the server for whatever reason
the player will be unfrozen and free to go. The true shows that this will happen. In all, what this config tells us, is that when the player leaves and rejoins they will be unfrozen.
Without any Permissions, only admins can do it. (Players who have /admin aka blue hammer). To give players permission to do /freeze put in the following permission:
```essentials.command.freeze``` this permission will give the group who has it the permission to only freeze, to give people permission to do /unfreeze, the following permission should
be given to them >essentials.command.unfreeze<. 

## Inventory managment
First I will discuss /ci or /clear inventroy which you can use to clear all inventories, to clear your own or to clear someone elses. These all are given a separate permission.
For example you can allow your players to clear their own inventories but not others. You can allow mods to clear their own and others (lets say with a cooldown). The first permission
for clearing your own inventory. essentials.command.clearinventory This permission gives players who have it the permission to clear their own inventories only. This means unless they
have admin, they will only be able to clear their own inventory. The permission essentials.command.clearinventory.all will allow the person/people to clear the inventories of all 
players in the server. They will have to have the permission to clear their own inventory for the permission to clear inventories of all players in the server. These players
will be able to clear their own inventory, or all people in the server at the same time. The following Permissions will give players permission to clear the inventories of 
individual people: essentials.command.clearinventory.other This Permission will give the player the permission to clear the inventory of 1 person at a time. This will require
the permission to clear their own inventory. 

## Kicking players
The command /kick is a base game command so its permission is just kick. The permission for /kickall which is the command to kick all players from this server. This does not ban them.
The permission for /kickall is >essentials.command.kickall<. This permission does not require any prior permissions and will allow anyone with it to do /kickall which will kick all
players in the server.

## Checking Private messages
Uessentials has a great system where you can do /msg and /r to message and respond to people in game. These messages are private and can only be seen by players who can do the 
/spypm command which will show all private messages in their chat. the permission for this command is >essentials.command.spypm<. This does not require any other permissions to 
operate. 

## Force killing players
This is for killing people without shooting, starving so on. This command can be done with the permission >essentials.command.kill< and will instantly kill anyone who this is
done to unless they are in godmode, in which case their health will be set to 0 but they will still be alive. When killed, the reason for death will be "Killed by server admin"

## Antispam
The antispam fuction is there to stop users from spaming chat. In the configuration files of uessentials on the first block of text at the bottom will be this:
  "AntiSpam": {
    "Enabled": false,
    "Interval": 3
The enabled true/false part is the part that tells uessentials to enforce or not enforce the setting. In this configuration users can spam without the plugin doing anything.
However if  the setting is changed to true users will be able to type 1 message evert 3 secconds. The interval portion is how many secconds between each message.


An example below is of a normal player, Moderator and admin.
```xml
  <Groups>
    <Group>
      <Id>default</Id>
      <DisplayName>Guest</DisplayName>
      <Prefix />
      <Suffix />
      <Color>white</Color>
      <Members />
      <Priority>1000</Priority>
      <Permissions>
        <Permission Cooldown="0">essentials.command.clearinventory</Permission>
      </Permissions>
    </Group>
    <Group>
      <Id>Moderator</Id>
      <DisplayName>Moderator</DisplayName>
      <Prefix />
      <Suffix>[Admin]</Suffix>
      <Color>FF9900</Color>
      <Members>
        <Member>76561198134265241</Member>
      </Members>
      <ParentGroup>default</ParentGroup>
      <Priority>30</Priority>
      <Permissions>
		<Permission Cooldown="0">essentials.command.freeze</Permission>
		<Permission Cooldown="0">essentials.command.unfreeze</Permission>
		<Permission Cooldown="0">essentials.command.clearinventory.other</Permission>
      </Permissions>
    </Group>
    <Group>
      <Id>Admin</Id>
      <DisplayName>Admin</DisplayName>
      <Prefix />
      <Suffix>[Admin]</Suffix>
      <Color>FF9900</Color>
      <Members>
        <Member>76561198134265241</Member>
      </Members>
      <ParentGroup>default</ParentGroup>
      <Priority>30</Priority>
      <Permissions>
		<Permission Cooldown="0">essentials.command.spypm</Permission>
		<Permission Cooldown="0">essentials.command.clearinventory.other</Permission>
		<Permission Cooldown="0">essentials.command.clearinventory.all</Permission>
		<Permission Cooldown="0">essentials.command.freeze</Permission>
		<Permission Cooldown="0">essentials.command.unfreeze</Permission>	
      </Permissions>
    </Group>
```