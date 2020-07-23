
# Altair - Command List
### Warframe
- **Enemy**  
	 - Usage: `!enemy "Enemy" primary/melee CurrentLevel MissionLevel new/old/current`
		 - Calculates DPH, DPS, Armor, Health, Shields, EHP, and Damage Reduction
		 - Can use old/new/current scaling formulas. Default usage is current scaling, If mission level is above 100, it will change to calculate for Steel Path Scaling. You can override this.
		 - Some enemies do not have known base damage values, such as Infested units, and they will show up as always having 0 DPH/DPS.
		 - When calculating things such as EHP, there is no consideration in damage types. 
- **Specter**
	- Usage: `!specter Warframe "Weapon" CurrentLevel MissionLevel new/old/current`
		- Similar usage to enemy calculator.
- **Arby**
	- Usage: `!arby`
		- Posts current arbitration.
- **Price**
	- Usage: `!price item`
		- Pricechecks an item from warframe.market.
			- Unpopular items may fail to be price checked. (payload error)
- **Status**
	- Usage: `!status BaseStatusChance AddedStatusChance`
		- Literally just a status calculator.
- **Baro**
	- Usage: `!baro`
		- Posts Baro Ki'Teers current inventory.
			- If he is not available, it will post an embed telling when he will arrive and where.
- **Nightwave**
	- Usage: `!nw`
		- Posts current nightwave with standing rewards.
