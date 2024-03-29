# NIMS
A non-invasive membership screening Discord bot

## Why use NIMS
There are a lot of great Discord bots out there for verifying new members/preventing raids. However, most of these Discord bots make every single new user complete some type of verification. While this method can be effective, it is usually annoying for new users joining your server. 

NIMS solves this issue a little differently than other Discord bots. Instead of requiring verification for all new members, NIMS allows you to select what type of new users will have to complete additional verification. You can decide if only new Discord users will be flagged or if more details about a Discord account should be considered. 
## Installation
1. Invite the bot with this [LINK](https://discord.com/oauth2/authorize?client_id=809157071270051850&scope=bot&permissions=8)
2. Once the bot has successfully joined your Discord server, run the command `?setup` (the server owner can only run this command!)
3. The bot will begin to configure your server
4. Once the bot has completed the setup, you are good to go!


## Settings
Setting up the bot is simple, but NIMS comes with many customizable settings for you to play with. These settings control how strict the bot is when classifying suspected bots and the captcha the bot sends to members during verification. 

You can view your current settings by running the command `?settings`

### Server Settings
#### Tiers
The tier used by the bot determines if a user is legitimate or not. There are two tiers the bot uses, 1 and 2. 
Tier 1 will only flag members who have created their account in the past 24 hours. Tier 2 is a little more complicated
and takes into account a series of factors. These factors include but are not limited to account creation date, profile picture, and badges. 
By default, the bot will use tier 1. If you would like to make the bot use tier 2 instead, you can run the command `?settings tier 2`

#### Min Score
If you have set the bot to tier 2, you can also set the minimum score a user needs to not be flagged by the bot. 
The score is 1 - 100. By default, the minimum score is set to 50. This means that new users who have a score below 50 will be required to complete additional verification before they can access the rest of your server.
You can change the minimum score by running the command `?settings score SCORE`. For example, let's say you wanted to change the minimum score to 60. You would have to run the command `?settings score 60`

### Captcha Settings
#### Captcha Font
There are three fonts you can use for the captchas sent by the bot. The two options are `default`, `roboto`, and `color`. By default, the bot uses the captcha font `default`. If you would like to change the captcha font to Roboto, you would run the command `?settings captcha font roboto`

The font `color` is a little easier for users to solve.

##### Examples of the captcha fonts
###### color
![color font](https://cdn.discordapp.com/attachments/809181845379612722/829059200696320101/captcha.png)

##### default
![default font](https://cdn.discordapp.com/attachments/809181845379612722/829026174688559134/captcha.png)

#### roboto
![coming soon]()



#### Captcha Case
You can also change the character case of the text in the captchas sent by NIMS. By default, NIMS will send captchas will both upper and lowercase letters. However, sometimes this can be too difficult for users to solve. You can make the captcha easier by changing the font to only upper or lower case. For example, you can change the captcha font to only use lower case by running the command `?settings captcha case lower`. Or if you want the captchas to be all uppercase, you can use the command `?settings captcha case upper`

### Advanced Settings
#### Lockdown Mode
If you are experiencing a large amount of fake Discord accounts joining your server, congrats... you are being raided. Now what to do about it? Well, NIMS is pretty good at catching bots before they can do much damage, but what do you do once NIMS catches an account? Well, you can have NIMS automatically kick new users who haven't run the `?verify` command more than 60 seconds after they join the server. The way you do this is by enabling Lockdown Mode. You can enable Lockdown Mode by running the command `?lockdown`.
NIMS will then ask if you are sure you want to enable Lockdown Mode. Just reply to NIMS with `yes` if you are sure you want to enable Lockdown Mode. Once you do that, you are good to go!


A couple of things to note about Lockdown Mode. I recommend you **DO NOT** keep it enabled 24/7. Since Lockdown Mode might lead to some real users being kicked because they are multi-tasking or not paying attention. I recommend you only use Lockdown Mode if your server is actively being raided. 

#### Kick Unverified Members
If you want to kick all unverified members, you can use the command `?kick uv`. The bot will then ask if you are sure that you want to proceed. If you answer the bot with `yes` then all unverified members will be kicked from your server. 
#### Score Testing
If you want to check what score NIMS would give you, you can check that by running the command `?test score`. If you want to see what someone else's score is, you can check by running the command `?test score THEIR_USER_ID`. For example `?test score 539581928387510273`

#### Removing NIMS

If you no longer want to use NIMS, don't just kick it from your server. You can run the command `?remove` instead! The `?remove` command will delete all roles, channels, and permissions created by NIMS on your server. 
