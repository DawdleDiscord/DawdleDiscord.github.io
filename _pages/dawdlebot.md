---
permalink: /dawdlebot/
title: "Dawdlebot"
---

Dawdlebot was made to fill some niche bot roles, but has since expanded to become a general purpose bot for Dawdle. 

[Dawdlebot GitHub](https://github.com/DawdleDiscord/dawdlebot) <-- Currently private, DM amer for access.

Quick staff inks:

* [Moderation](https://dawdlediscord.github.io/dawdlebot/#moderation)
* [Warnings](https://dawdlediscord.github.io/dawdlebot/#warnings)
* [Members](https://dawdlediscord.github.io/dawdlebot/#members)
* [Roles](https://dawdlediscord.github.io/dawdlebot/#roles)
* [Bot Cleaning](https://dawdlediscord.github.io/dawdlebot/#bot-cleaning)
* [QOTD](https://dawdlediscord.github.io/dawdlebot/#qotd)
* [Autoreacts](https://dawdlediscord.github.io/dawdlebot/#autoreacts)
* [Info](https://dawdlediscord.github.io/dawdlebot/#info)
* [Birthdays](https://dawdlediscord.github.io/dawdlebot/#birthdays)
* [Trivia](https://dawdlediscord.github.io/dawdlebot/#trivia)
* [Welcome/Goodbye](https://dawdlediscord.github.io/dawdlebot/#welcomegoodbye)
* [Inventories](https://dawdlediscord.github.io/dawdlebot/#inventories)
* [Profiles](https://dawdlediscord.github.io/dawdlebot/#profiles)
* [Dailies](https://dawdlediscord.github.io/dawdlebot/#dailies)

## Commands: All Members
Required arguments are denoted by `<argument>`, optional arguments are denoted by `[argument]`.

`~info [topic] [subtopic]` displays information relevant to that (sub)topic. If a topic is not included all topics will be listed.

`~vent <text>` sends an anonymous vent for staff approval. If staff approves it will be posted in the vent channel.

`~report <text>` sends the text of the report to staff. Images can be included.

`~done` will check if you have your roles and intro, and if so it will remove your `.` role 

`~birthday <day> <month>` adds your birthday.

`~birthdaymonth <month>` displays all birthdays for that month.

`~trivia` lets you play a game of trivia!

`~trivia leaderboard` shows the current leaderboard of trivia streaks.

`~daily` Claims your dawdle daily if you have sent at least 10 messages in basement/parlor and have not claimed your daily since 00:00:00 UTC time.

`~inventory` to see your item inventory from lootboxes.

`~inventory info <item>` shows information about `item`.

`~profile [member]` see your (if no member put) or `member`'s Dawdle profile.

`~editprofile` brings up a menu to edit the **about** section of your profile.

`~editbanner` brings up a menu to enter a link to the image you would like to use for your profile's banner. You need to include the `https://` and it will only work for as long as that link is valid.

`~mywarnings` Shows all your warnings.

## Commands: Staff Only

Required arguments are denoted by `<argument>`, optional arguments are denoted by `[argument]`.

All `member` arguments work by ID, mention, username, or nickname. nick/usernames can be found by partial matches and are not case sensitive.

`~logout` forces the bot to shutdown in case it's doing something you don't want it to.

### Moderation

`~ban <member/userid> [rule #]` Bans the member/user. If a rule number is included an admonition is posted as

```<member/user> was banned by <you> (Rule [rule #])```

`~kick <member>` Kicks the member

`~unban <userID>` Unbans the user.

`~postadmonition <text>` Posts the text as an admonition.

`~prune <# of messages> [member/userID]` Prunes the given number of messages. Including a member or userID will prune only those messages sent by that user.

### Warnings

`~warn <member> <rule> [yes/no]` Will create a warning for `member`. It will ask for context, once you reply the warning will be saved. You can include attachments in the reply. `Yes/no` tells it whether or not to post an admonition/DM. The default option is `yes`, unless the `rule` is `verbal` in which case it never posts/DMs. 

`~warnings <member> [verbal/nonverbal]` Will pull up all warnings of `member`. Reference the warning number to edit/delete warnings. `verbal` will only show verbal warnings and `nonverbal` will only show nonverbal warnings.

`~editwarning <member> <warning number>` Edit the context of the `warning number` warning for `member`. Reference `~warning` to find the number. (Cannot edit attachments at this time.)

`~deletewarning <member> <warning number>` (alias: `~delwarning`) Delete the `warning number` warning for `member`. Reference `~warning` to find the number.

### Members

`~members clean [member]` cleans messages in identifying channels sent by users no longer in the server. If `member` is given it deletes messages only from that member.

`~members check` makes sure that every member has an intro and required roles.

### Roles

`~roles color <role> <newcolor>` changes the color of the role to `newcolor`.

`~roles mentionable <role>` toggles making the role mentionable

`~roles sidebar <role>` toggles displaying the role on the sidebar

`~roles position <role> <new position>` moves the role to the new integer position. Tip: use `~roles info` to see the position of other roles.

`~roles info <role>` gives information about the role

`~roles members <role>` lists all members who have the role.

`~roles give <member> <role> [true/false]` gives the member the role. True (default) shows the list as mentions, false shows as just a list of names. Yes/no also works.

`~roles take <member> <role>` removes the role from the member

`~roles kick <role> <hours>` This is the former `kick_role`. It will kick anyone with `role` who joined more than `hours` ago. Only works for @unverified  and @. roles.

`~roles watch add <role>` adds the role to the list of roles being watched. If a role is watched, the bot will send a message when someone gets or loses the role.

`~roles watch remove <role>` removes the role from the list of roles being watched.

`~roles watch list` lists the currently watched roles.

### Bot Cleaning

`~clean botadd <botname> <botprefix>` adds that prefix as a command prefix.

`~clean botremove <botname>` removes the bot and its prefix

`~clean botlist` displays all added bots and prefixes

`~clean channeladd` adds that channel to be cleaned

`~clean channelremove` removes that channel from being cleaned

`~clean channellist` lists channels that are cleaned

### QOTD

The bot will check once per hour if the current hour is 17 UTC time. If so, then it will post the next question in the queue.

`~qotd add <question>` adds a question to the queue

the bot will post next question in the queue every day, then delete it from the queue

`~qotd get <number>` gets the number of qotd questions specified in the queue. if you put a number greater than the number of questions it'll just give you all the questions it has

`~qotd remove <number>` removes the question at the number in the queue. You can reference the numbers next to the questions in `~qotd get`

`~qotd edit <number>` allows you to replace the question at the number in the queue. You can reference the numbers next to the questions in `~qotd get`

`~qotd post` force the bot to post a qotd. should be used if the normal time passes and no qotds were added

### Autoreacts

`~autoreact add <channel> <emoji 1> <emoji 2> ...` adds the channel and emojis for the bot to autoreact.

`~autoreact remove <channel>` removes the channel from the autoreact list.

`~autoreact list`shows all added channels and corresponding emojis.

### Info

`~sendinfo <member> <topic> [subtopic]` DMs the member the information in the (sub) topic.

`~editinfo addtopic <topic>` Adds the topic.

`~editinfo removetopic <topic>` Removes the topic.

`~editinfo addsubtopic <topic> <subtopic>` Adds the subtopic under the topic, and also will ask you to input the information. This can also be used to update information, as it will replace the old subtopic and give a warning before doing so. **To input general topic information, name the subtopic the same as the topic.**

`~editinfo removesubtopic <topic> <subtopic>` Removes the subtopic from the topic.

### Birthdays

`~addbirthday <member> <day> <month>` manually inputs the member's birthday.

`~birthdayclean` removes any birthdays of members no longer in the server if they are not deleted automatically.

### Trivia

`~trivia add <question>` Starts a menu for adding the correct and incorrect answers to the question, then saves it.

`~trivia list` Lists all current trivia questions. Use the arrows to go between pages.

`~trivia edit <question>` Starts an interface to edit or delete the question. Question can either be specified by the question text or the index next to it in `~trivia list`. Be careful of ambiguities between those two possibilities.

### Welcome/Goodbye

`~setwelcome` and `~setgoodbye` Brings up a menu to change the welcome/goodbye message. It requires putting a name in the new message, either as a mention, name#xxxx, or just name. 

Mention: `{ment}`

name#xxxx: `{user}`

name: `{name}`

Ex: Welcome {ment} to Dawdle!

### Inventories

`~editinv add <item_name>` add the item with the given item name to the list of givable items.

`~editinv remove <item_name>` remove the item with the given item name from the list of giveable items.

`~editinv list` list all givable items

`~inv give <member> <number> <item>` give the `member` the `number` amount of `item`.

`~inv take <member> <number> <item>` remove the `number` of `item` from `member`

`~inv show <member>` shows the inventory of another member.

### Profiles

`~givebadge <member_or_role> <emoji 1> <emoji 2> ...` gives either `member` or every member in `role` those emojis as badges.

`~takebadge <member_or_role> <emoji 1> <emoji 2> ...` removes from  either `member` or every member in `role` those emojis as badges.

`~cleanbadges <member_or_role>` will remove and badges whose emoji has been deleted or is otherwise not found.

`~cleanprofiles` will delete profile information of any members who left.

### Dailies
`~daily set <member> <streak>` Sets `member`'s streak to `streak`.

`~daily clean` Cleans out people not in the server anymore from the streak data.