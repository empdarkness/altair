
# Altair - Command List - [Invite](https://discord.com/api/oauth2/authorize?client_id=522879744786563075&permissions=0&scope=bot%20applications.commands) - [Discord Server](https://discord.gg/7EgHQ8Zm8m)

### Note: Most commands are now slash based, however some are still not. <br> If you need help setting up anything, feel free to join the Discord and ask.
### [FAQ/Common Issues](https://github.com/empdarkness/altair/blob/master/faq.md)
## Warframe
- **Riven/Lich Sniper - RM & WFM**
	- Usage: `/sniper`
	- To set it up to a guild channel, you will need administrator perms. Use route argument.
	- Rivens
		- When specifying stats, use the [arguments](https://github.com/empdarkness/altair/blob/master/rm.md) listed here.
		- Notices are posted with the most recent relist by same seller/list by another seller/similar seen.
			- The criteria for being seen with another seller is a 1 to 1 copy of the stats.<br>Relisted requires the seller to be the same and have the same stats, doesnt show if a slight variation.<br>Similar requires the seller to be different, matching stat names, and a variation in stat values.
			<br>🔸 Riven was seen with another seller. Emperor - 1/99999
			<br>🔸 WFM 15 days ago
			<br>🔹 Riven was relisted by same seller. Last seen price: 99999
			<br>🔹 RM 15 days ago
			<br>👀 Similar riven spotted from: Emperor - pmo
			<br>👀 TC 15 days ago
		- Weapon wildcards
			- Riven type - `Archgun` `Shotgun` `Rifle` `Pistol` `Melee`
			- Everything - `All` `Any`
		- Positive stat lists - Allows a single spot to be held by multiple stats
			- Only one stat between the group of `~` needs to match.
			- Ex: `ele~tox~cold~heat ms cd`
		- 2p1n - Toggling this will make the configuration only look for rivens with 2 positives and 1 negative. Use this with None as a negative to only look for 2p0n.
		- Automatic Grading - Grades it for every variant of the weapon.
		- Endo/plat checking - Endo per plat value for endo roll sniping. There is a catch to wfm rivens with infinite buyout, this will only work on those with a starting price equal to or above 100, this is to reduce the spam of 1 plat infinite buyouts.
		- Minimum endo - Self explanatory
		- Roll count range - Only post rivens between this range. Ex: `0-0` for unrolled, `0-10` for any between 0 and 10
		- Minimum disposition - One variant has to have a disposition above or equal to this
		- Positive stat range/grade filtering
			- Usage: `ms101-105` `ms101-105~106-110`
			- Use a `~` to add an additional range to the stat
			- Space apart different stats
	- Lich/Sisters
		- Weapon - Only lets you select Kuva/Tenet weapons and has a wildcard for all weapons `Any`/`All`.
		- Element - Only lets you select the current available elements for liches and has an option for every element.
		- Percentage - Integer between 25 and 60.
		- Percentage Method - Greater than or equal to, less than or equal to, or equal to.
	- Price - It will only post rivens equal to or below this price
	- Optional Text - You can add text to be sent with the posting, you can use up to 255 characters. In order to use a role, type it out like you're gonna ping it.
	- `/sniper blacklist`
		- Call view in dms or guild to view respective list
		- You will need admin perms to add a user to the guild blacklist. It will default to DM mode if you try and do not have admin perms.
		- Channel allows you to redirect every blacklisted seller to a specific channel.

- **Manual Grading**
	- Usage: `a/grade tenet_envoy 64cc 52.4cd 45.8ms -41.3impact` `a/g vectis 69.5ele 88.8cd 76.8heat 58.5recoil`
	- Slash: `/grade`
	- Use `-r` and a number between 0 and 8 to grade it based on the riven rank. This argument is optional as it grades it maxed as default.
		- You only need to designate a non-recoil negative. Recoil is automatically handled as a negative if it has positive stats.
	- Use `-d #` to override the disposition.
	- Alt Usage: `a/grade https://warframe.market/auction/613eb4eebf237003f3ffb7a1` (Only wfm links work)

- **Manual Grading - Image**
	- Usage: `a/gi catchmoon 61.6ms 49cd 40.9fr -45.9imp -mr 16 -ro 9999 -p nar -r 8`
		- `-mr` - Mastery rank 8-16
		- `-ro` - Rerolls 0-9999
		- `-p` - Polarity (mad, vaz, nar)
		- `-r` - Rank
		- `-d` - Disposition override

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



- **GDPR Parser**
	- Usage: `a/profile` `a/trades` with attached file relative to the command.
		- Profile only accepts the non trade-data file.
		- Trades only accepts the trade-data file, if you have multiple, append them to a single text file.
		- The data is not stored, it is deleted once it is loaded in for parsing.

- **Riven Ranges**
	- Usage: `/range`
		- Shows riven ranges for a specific weapon.
		- Has autocomplete and allows selection as the weapon type as a weapon. Use this in conjunction with the disposition override for seeing specific dispos.

- **Loadout Parser**
	- Usage: `/loadout`
		- Attempts to find the riven on your selected slot, grades it, and gives you the riven.market import string.
		- This will also show the actual values of all variants, so if you have it equipped on prime, it will also show the real values of non prime.
		- Requires the share loadouts permission from [here](https://www.warframe.com/user) under User Information - Data Permissions.
		- If you have the permissions turned on and its still not working after a couple of minutes, toggle it off, save, and then turn it back on and save. Wait a couple min after and it should work again.

- **Riven Browser**
	- Usage: `/browse`
		- Gets list of rivens from provided args.
		- Sorted by price
		- The posted embed includes riven stats and a copy-paste message
		- Argument usage can be found [**here**](https://github.com/empdarkness/altair/blob/master/rm.md)
		
- **Scaling Calculator**  
	 - Usage: `/scaling`
		 - Calculates DPS/DPH or Damage Multiplier, Armor, Health, Shields, EHP, and Damage Reduction
		 - Can use old/new/current scaling formulas. Default usage is current scaling, If mission level is above 100, it will change to calculate for Steel Path Scaling. You can override this.
		 - Enemies do not have public base damage values. As such, the only damage related thing shown is their multiplier.
		 - When calculating things such as EHP, there is no consideration in damage types. 
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
- **Darvo**
	- Usage: `/darvo`
		- Will DM you every time Darvo brings the item you designated.
		- The current selection of items is pre-configured but will expand over time as he brings items the bot has not seen before.

- **WFConfig**
	- Usage: `/wfconfig`
	- Needs administrator permissions to use.
	- Every type except arbitration has optional text.
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
- T1+ **User Alert**
	- Usage: `/useralert`
	- Will send you a DM notification if somebody interacts with the WFM site at all, including while invisible.
- T2+ **Name History**
	- Usage: `/namehistory`
	- Will allow you to see the name history of every user seen by the bot. This only works if said users are changing their names on the sites and not making alts.
- T2+ **Riven History**
	- Usage: `a/rh acceltra cc cd ms rec` `a/rh acceltra cc cd ms -z`
	- Lets you see the 5 most recent listings of a specific stat roll, up to a total of 15.

## Black Desert Online
- **Pearl Item History**
	- Usage: `a/pearl` `a/pearl 30`
	- Will show the total amount of listed outfits and buff items (Moon, Kama, VP) seen within the last 7 days or specified amount of days.<br>The bot started scraping on 1/31/2022.
	- Currently this is only available for NA PC.
- **Most of X Drop**
	- Usage `a/most caphras`

## Misc
- **Starboard**
	- Usage: `/starboard`
	- Requires administrator permissions to setup.
	- Will repost the message to the designated channel when the ⭐ reacts reach the designated amount.
	
- **Coinflip**
	- Usage: `/flip`
	- This also involves the coin being able to land on its side. 1/60,000

- **Remindme**
	- Usage: `a/remindme timestamp reminder`
	- Removal Usage: `a/remindme remove ref_id`
		- Use [this website](https://www.epochconverter.com/) to generate an appropriate Epoch timestamp.
		- You must share a server with the bot in order to receive the reminder, otherwise it would fail to DM you and would be removed from the database.
		- Make sure your DMs are open, as the bot will attempt you message you. It will still be removed if it fails to send.
