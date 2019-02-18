SourceBans Discord Forward
===

### Install / Settings / compile
- put in your webhooks url's in the following places (sbpp_discord.sp) - marked `XXX`
````
Convars[Ban] = CreateConVar("sbpp_discord_banhook", "XXX", "Discord web hook endpoint for ban forward", FCVAR_PROTECTED);
	
	Convars[Report] = CreateConVar("sbpp_discord_reporthook", "XXX", "Discord web hook endpoint for report forward. If left empty, the ban endpoint will be used instead", FCVAR_PROTECTED);
	
	Convars[Comms] = CreateConVar("sbpp_discord_commshook", "XXX", "Discord web hook endpoint for comms forward. If left empty, the ban endpoint will be used instead", FCVAR_PROTECTED);

`````
- get these 4 files if you don't have them already in your includes/ folder

`wget https://raw.githubusercontent.com/sbpp/sourcebans-pp/v1.x/game/addons/sourcemod/scripting/include/sourcebanspp.inc -O include/sourcebanspp.inc`

`wget https://raw.githubusercontent.com/sbpp/sourcebans-pp/v1.x/game/addons/sourcemod/scripting/include/sourcecomms.inc -O include/sourcecomms.inc`

`wget https://raw.githubusercontent.com/KyleSanderson/SteamWorks/master/Pawn/includes/SteamWorks.inc -O include/SteamWorks.inc`

`wget https://raw.githubusercontent.com/thraaawn/SMJansson/master/pawn/scripting/include/smjansson.inc -O include/smjansson.inc`

- compile your plugin with `./compile.sh sbpp_discord.sp` and move it to your plugins folder

Original by [SourceBans](https://github.com/sbpp/discord-forward)