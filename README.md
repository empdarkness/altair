
# Altair - Command List - [Invite](https://discord.com/api/oauth2/authorize?client_id=522879744786563075&permissions=0&scope=bot%20applications.commands) - [Discord Server](https://discord.gg/7EgHQ8Zm8m)

### Note: Most commands are now slash based, however some are still not. <br> If you need help setting up anything, feel free to join the Discord and ask.
## Warframe
- **Riven/Lich Sniper - RM & WFM**
	- Usage: `/sniper`
	- To set it up to a guild channel, you will need administrator perms. Use route argument.
	- Rivens
		- Behavior is extremely similar to the riven browser, it needs to be using the same [arguments](https://github.com/empdarkness/altair/blob/master/rm.md).
		- Notices are posted with the most recent relist by same seller/list by another seller/similar seen.
			- The criteria for being seen with another seller is a 1 to 1 copy of the stats.<br>Relisted requires the seller to be the same and have the same stats, doesnt show if a slight variation.<br>Similar requires the seller to be different, matching stat names, and a variation in stat values.
			<br>🔸 Riven was seen with another seller. Emperor - 1/99999
			<br>🔸 WFM 15 days ago
			<br>🔹 Riven was relisted by same seller. Last seen price: 99999
			<br>🔹 RM 15 days ago
			<br>👀 Similar riven spotted from: Emperor - pmo
			<br>👀 TC 15 days ago
		- 2p1n - Toggling this will make the configuration only look for rivens with 2 positives and 1 negative. Use this with None as a negative to only look for 2p0n.
		- Automatic Grading - Grades it for every variant of the weapon.
		- Endo/plat checking - Endo per plat value for endo roll sniping. There is a catch to wfm rivens with infinite buyout, this will only work on those with a starting price equal to or above 100, this is to reduce the spam of 1 plat infinite buyouts.
	- Lich/Sisters
		- Weapon - Only lets you select Kuva/Tenet weapons and has a wildcard for all weapons `Any`/`All`.
		- Element - Only lets you select the current available elements for liches and has an option for every element.
		- Percentage - Integer between 25 and 60.
		- Percentage Method - Greater than or equal to, less than or equal to, or equal to.
	- Price - It will only post rivens equal to or below this price
	- Optional Text - You can add text to be sent with the posting, you can use up to 255 characters. In order to use a role, type it out like you're gonna ping it.
	- `a/sb dm/guild -a/-r/-c user` - User Blacklist (Guild/Direct Message)
		- Ex: `a/sb dm -a user1,user2,user3`
		- View: `a/bl` in dms or guild to view respective list
		- You will need admin perms to add a user to the guild blacklist. It will default to DM mode if you try and do not have admin perms.
		- Modes:
			- `-a` - Adds to blacklist
			- `-r` - Removes from blacklist
			- `-c` - Clears blacklist, user arg wont do anything

- **Manual Grading**
	- Usage: `a/grade tenet_envoy 64cc 52.4cd 45.8ms -41.3impact` `a/g vectis 69.5ele 88.8cd 76.8heat 58.5recoil`
	- Use `-r` and a number between 0 and 8 to grade it based on the riven rank. This argument is optional as it grades it maxed as default.
		- You only need to designate a non-recoil negative. Recoil is automatically handled as a negative if it has positive stats.
	- Use `-d #` to override the disposition.
	- Alt Usage: `a/grade https://warframe.market/auction/613eb4eebf237003f3ffb7a1` (Only wfm links work)

- **Unrolled Riven Prices**
	- Usage: `/unroll`
	- Has weapon autocomplete
		
- **WFM Riven Auction Alerts**
	- Usage: `/auction`
	- Auction updated (price change, desc change, etc.)
	- New/Removed Bids
	- Auction close/winner/deletion
	- Can use wfm auction ids or link

- **WFM Price Alerts**
	- Usage: `/market`
	- The item query has autocomplete and will find 10 matches to it.
	- The matches it finds will DM you an embed with the id, seller, rank, quantity, and a copy/paste message.
	
|Item Behavior|Relic Behavior|
|--|--|
|Mods/Arcanes: == config rank<br>WTS: ≥ config price<br>WTB: ≤ config price|Equal to rank<br>0 - All<br>1 - Intact<br>2 - Exceptional<br>3 - Flawless<br>4 - Radiant|

- **Riven Ranges**
	- Usage: `a/range Archgun/Rifle/Shotgun/Pistol/Melee -p 3 -n 1 -d 1.5`
		- `-p` `-n` - Designates how many positives/negatives the riven has.
		- `-d` - Disposition to scale ranges.
		- `-r` - Riven rank

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
	- Usage: `/arby`
		- Posts current arbitration.
- **Price**
	- Usage: `/price`
		- Has item autocomplete
	 	- Only shows online orders
		- Pricechecks an item from warframe.market top orders, sorted by price.
		- Scrolling embed for both buy and sell orders. Including the copy-paste message.
- **Endo**
	- Usage: `/endo`
		- Calculates Kuva spent and the Endo you would obtain from disolving a riven mod.
- **Baro**
	- Usage: `/baro`
		- Posts Baro Ki'Teer's current inventory as an image.
			- If he is not available, it will post an embed telling when he will arrive and where.
- **Nightwave**
	- Usage: `/nightwave`
		- Posts current nightwave with standing rewards.
- **WFConfig**
	- Usage: `/wfconfig`
	- Needs administrator permissions to use.
	- Types: baro, gftl, invasions, arbitration
		- Automatic posting when one of the four things occurs:
			- Baro Ki'Teer
			- Gift From the Lotus
			- Invasions (Orokin Reactor/Catalyst only)
			- Arbitrations (with optional role mentions, see below for formatting)
				- Factions: `Grineer`, `Infested`, `Corpus`, `Orokin`
				- Types: `Defense`, `Survival`, `Salvage`..
				- Faction+Types: `Grineer Defense`, `Corpus Survival`..
				- Nodes: `Sechura`, `Helene`, `Hydron`..
## Patron Exclusive
- T1+ **Stalk**
	- Usage: `/stalk`
	- Will send you a DM notification if somebody interacts with the WFM site at all, including while invisible.
- T2+ **Name History**
	- Usage: `/namehistory`
	- Will allow you to see the name history of every user seen by the bot. This only works if said users are changing their names on the sites and not making alts.
- T2+ **Riven History**
	- Usage: `a/rh acceltra cc cd ms rec` `a/rh acceltra cc cd ms -z`
	- Lets you see the 5 most recent listings of a specific stat roll, up to a total of 15.

## Misc
- **Coinflip**
	- Usage: `/flip`
		- This also involves the coin being able to land on its side. 1/6000

- **Remindme**
	- Usage: `a/remindme timestamp reminder`
	- Removal Usage: `a/remindme remove ref_id`
		- Use [this website](https://www.epochconverter.com/) to generate an appropriate Epoch timestamp.
		- You must share a server with the bot in order to receive the reminder, otherwise it would fail to DM you and would be removed from the database.
		- Make sure your DMs are open, as the bot will attempt you message you. It will still be removed if it fails to send.
