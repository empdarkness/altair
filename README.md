
# Altair - Command List - [Invite](https://discord.com/oauth2/authorize?client_id=522879744786563075&permissions=0&scope=bot)
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

## Warframe
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
	- Usage: `a/price item`
		- Pricechecks an item from warframe.market top orders, sorted by price.
		- Scrolling embed for both buy and sell orders. Including the copy-paste message.
	- Alt: `a/p item`
		- Pricechecks an item and shows all orders in the first embed. (No copy/paste)
- **Status**
	- Usage: `a/status BaseStatusChance AddedStatusChance`
		- Literally just a status calculator.
- **Riven**
	- Usage: `a/riven <MR REQUIREMENT> <MODRANK> <ROLLS>`
		- Calculates Kuva spent and the Endo you would obtain from disolving riven mods.
		- Endo cost is estimated since we don't have an exact formula.
- **Riven Browser**
	- Usage: `a/r <weapon> <optional args>`
		- Gets list of rivens from provided args.
		- Sorted by price
		- Warframe.Market rivens have a filter. They will not appear if the owner has not been online in 7 days.
		- The posted embed includes riven stats and a copy-paste message
		- Argument usage can be found [**here**](https://github.com/empdarkness/altair/blob/master/rm.md)
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

