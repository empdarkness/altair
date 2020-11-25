
# Altair - Command List - [Invite](https://discord.com/oauth2/authorize?client_id=522879744786563075&permissions=0&scope=bot)
## Warframe
- **Enemy**  
	 - Usage: `a/enemy "Enemy" CurrentLevel MissionLevel new/old/current`
		 - Calculates DPH, Armor, Health, Shields, EHP, and Damage Reduction
		 - Can use old/new/current scaling formulas. Default usage is current scaling, If mission level is above 100, it will change to calculate for Steel Path Scaling. You can override this.
		 - Some enemies do not have known base damage values. As such, the only damage related thing shown is their multiplier.
		 - When calculating things such as EHP, there is no consideration in damage types. 
- **Specter**
	- Usage: `a/specter Warframe "Weapon" CurrentLevel MissionLevel new/old/current`
		- Similar usage to enemy calculator.
- **Arby**
	- Usage: `a/arby`
		- Posts current arbitration.
- **Price**
	- Usage: `a/price item`
		- Pricechecks an item from warframe.market.
			- Unpopular items may fail to be price checked. (payload error)
- **Status**
	- Usage: `a/status BaseStatusChance AddedStatusChance`
		- Literally just a status calculator.
- **Riven**
	- Usage: `a/riven <MR REQUIREMENT> <MODRANK> <ROLLS>`
		- Calculates Kuva spent and the Endo you would obtain from disolving riven mods.
		- Endo cost is estimated since we don't have an exact formula.
- **RM**
	- Usage: `a/rm <weapon> <optional args>`
		- Gets cheapest online riven for specified weapon from riven.market
		- The posted embed includes riven stats and a copy-paste message
		- Argument usage can be found [**here**](https://github.com/empdarkness/altair/blob/master/rm.md)
- **Baro**
	- Usage: `a/baro`
		- Posts Baro Ki'Teers current inventory.
			- If he is not available, it will post an embed telling when he will arrive and where.
- **Nightwave**
	- Usage: `a/nw`
		- Posts current nightwave with standing rewards.
- **Amp**
	- Usage: `a/amp <number combo>`
		- Ex. `!amp 227
		- Posts an embed with stats for both primary and alternative fire for the amp.

