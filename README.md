
# Altair - Command List - [Invite](https://discord.com/oauth2/authorize?client_id=522879744786563075&permissions=0&scope=bot) - [Support Server](https://discord.gg/pByz6CVEKQ)

### Note: Some commands have slash equals with guided assistance.
## Warframe
- **Riven Sniper - RM & WFM**
	- Usage: `a/sa dm/#channel weapon *args`
	- Ex: `a/sa dm kronen -p critdmg range -n finisher -2p1n -c "<@&123456789>`
	 	- To set it up to a guild channel, you will need administrator perms.
	 	- Behavior is extremely similar to the riven browser, it needs to be using the same [arguments](https://github.com/empdarkness/altair/blob/master/rm.md).
	 	- You can use the keywords `Any`, `all`, or `None` as the stat and `Any` in a weapon position, however you cannot use `Any` on both weapon and a stat, this is by design.
	 	- Additionally: The keywords will override the section it is placed in. Only `Any` works in a positive position, all 3 work in the negative position.
		- The amount of positive and negative stats you can have is uncapped, however if you go above 3 on positive, you must have at least 3 of the positive stats for it to be considered a match. If you go above 1 negative, it will only need to match one of them.
	- Additional args: 
	 	- `-t 1337` - plat threshold, it will only post rivens equal to or below this price
	 	- `-2p1n` - Adding this will make the configuration only look for rivens with 2 positives and 1 negative.
	 	- `-g` - Grades it for every variant of the weapon.
	 	- `-c "<@123456789"` - You can add text to be sent with the posting, you can use up to 255 characters. In order to use a role, type it out like you're gonna ping it.
	- Alt Usage:
	 	- `a/sr id` - Snipe config removal, if linked to server channel, you can force remove it with admin perms
	 	- `a/sl` - View the total amount of listings setup. If you use it in DMs, it will look for ones tied to you, and if used in a guild, it will look up ones tied to the guild.
	 	- `a/sb dm/guild -a/-r/-c user` - RM User Blacklist (Guild/Direct Message)
	 		- Ex: `a/sb dm -a user1,user2,user3`
			- View: `a/bl` in dms or guild to view respective list
			- You will need admin perms to add a user to the guild blacklist. It will default to DM mode if you try and do not have admin perms.
			- Modes:
				- `-a` - Adds to blacklist
				- `-r` - Removes from blacklist
				- `-c` - Clears blacklist, user arg wont do anything

- **Manual Grading**
	- Usage: `a/grade tenet_envoy 64cc 52.4cd 45.8ms -41.3impact` `a/grade vectis 69.5ele 88.8cd 76.8heat 58.5recoil`
	- Use `-r` and a number between 0 and 8 to grade it based on the riven rank. This argument is optional as it grades it maxed as default.
		- You only need to designate a non-recoil negative. Recoil is automatically handled as a negative if it has positive stats.
		
- **Riven Ranges**
	- Usage: `a/range Archgun/Rifle/Shotgun/Pistol/Melee -p 3 -n 1 -d 1.5`
		- `-p` `-n` Designates how many positives/negatives the riven has.
		- `-d` Disposition to scale ranges.

- **Riven Browser**
	- Usage: `a/r <weapon> <optional args>`
		- Gets list of rivens from provided args.
		- Sorted by price
		- Warframe.Market rivens have a filter. They will not appear if the owner has not been online in 7 days.
		- The posted embed includes riven stats and a copy-paste message
		- Argument usage can be found [**here**](https://github.com/empdarkness/altair/blob/master/rm.md)
		
- **Scaling Calculator**  
	 - Usage: `a/s "Enemy or Specter" CurrentLevel MissionLevel new/old/current`
		 - Calculates DPH, Armor, Health, Shields, EHP, and Damage Reduction
		 - Can use old/new/current scaling formulas. Default usage is current scaling, If mission level is above 100, it will change to calculate for Steel Path Scaling. You can override this.
		 - Enemies do not have public base damage values. As such, the only damage related thing shown is their multiplier.
		 - When calculating things such as EHP, there is no consideration in damage types. 
		 - You can append `-w Exergis` to the command to have it calculate the scaled damage of any weapon.
- **Arby**
	- Usage: `a/arby`
		- Posts current arbitration.
- **Price**
	- Usage: `a/p item`
		- Pricechecks an item from warframe.market top orders, sorted by price.
		- Scrolling embed for both buy and sell orders. Including the copy-paste message.
- **Status**
	- Usage: `a/status BaseStatusChance AddedStatusChance`
		- Literally just a status calculator.
- **Riven**
	- Usage: `a/riven <MR REQUIREMENT> <MODRANK> <ROLLS>`
		- Calculates Kuva spent and the Endo you would obtain from disolving riven mods.
		- Endo cost is estimated since we don't have an exact formula.
- **Baro**
	- Usage: `a/baro`
		- Posts Baro Ki'Teer's current inventory as an image.
			- If he is not available, it will post an embed telling when he will arrive and where.
	- Alt: `a/b`
		- Posts Baro'Ki'Teer's current inventory in text form.
- **Nightwave**
	- Usage: `a/nw`
		- Posts current nightwave with standing rewards.
- **Amp**
	- Usage: `a/amp <number combo>`
		- Ex. `!amp 227`
		- Posts an embed with stats for both primary and alternative fire for the amp.
- **WFConfig**
	- Usage: `a/wfconfig channel_type channel_mention`
	- Ex: `a/wfconfig arbitration #general`
	- Types: baro, gftl, invasions, arbitration
		- Automatic posting when one of the four things occurs:
			- Baro Ki'Teer
			- Gift From the Lotus
			- Invasions (Orokin Reactor/Catalyst only)
			- Arbitrations (with optional role mentions, see below)
				- Factions: `Grineer`, `Infested`, `Corpus`, `Orokin`
				- Types: `Defense`, `Survival`, `Salvage`..
				- Faction+Types: `Grineer Defense`, `Corpus Survival`..
				- Nodes: `Sechura`, `Helene`, `Hydron`..
## Misc
- **Coinflip**
	- Usage: `a/flip`
		- This also involves the coin being able to land on its side. 1/6000
- **Quoter**
	- Usage: `a/quote id` - Must be called in the channel to search for the message
	- Alias: `a/q id`
	- Usage: `a/quotechat #channel id`
	- Alias: `a/qc #channel id`

- **Remindme**
	- Usage: `a/remindme timestamp reminder`
	- Removal Usage: `a/remindme remove ref_id`
		- Use [this website](https://www.epochconverter.com/) to generate an appropriate Epoch timestamp.
		- You must share a server with the bot in order to receive the reminder, otherwise it would fail to DM you and would be removed from the database.
		- Make sure your DMs are open, as the bot will attempt you message you. It will still be removed if it fails to send.
