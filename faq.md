## Warframe.market is delayed.
A: Unfortunately this is out of my control, the public api they provide updates very slowly, like once every 2 or so minutes.

## Why does it say no configs are found or that I cant remove a config I just added?
You more than likely created a config without the route argument, which creates a DM config by default. You have to use the list/removal commands in DMs with the bot to see these configurations.

## Is there an easier way to view all configurations?
Yes, there is. https://altair.empx.cc/ 

## Sniper Refresh timer?
5s

## General refresh timer?
1m

## I have patreon, but I'm still getting delays.
Make sure you run /patreon setguild within the server the config is set to.

## Sniper embed image is emtpy.
This is a rare occurrence and can usually be fixed by copying the link to the auction and using it with a/g to see the image. Sometimes this can also be chalked up to discord loading the image slowly, the bot currently uses discord's own cdn to host the image.

## Why does the sniper grade rivens as if they're maxed?
Some people list stuff as unranked but with maxed stats, I've seen it occur more often than not, so I decided to do this. You can copy the auction link and use it in a/g to grade it as listed rank.

## Data removal/collection?
Only data that is needed to be held onto is held indefinitely until specific things occur:
- If data is only used once, it is not kept.
- Guild specific data is wiped on bot removal or upon calling /dataremoval within a guild with admin perms.
- User data is removed upon request or through the /dataremoval command within DMs.
