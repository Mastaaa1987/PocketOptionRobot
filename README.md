# PocketOptionRobot
MyBot is a full in Python written Standalone Windows executable Robot. It is designed to catch Signals via Telegram and trade directly on PocketOption platform. 

![MyBot](https://raw.githubusercontent.com/Mastaaa1987/pocketoptionrobot/refs/heads/main/docs/MyBot.png)

### If you have some questions or suggestions or some thing like this, you can contact me via Telegram: @mastaaa667

## What you Need?

<details>
<summary>Click HERE for Content.</summary>

### 1. A Telegram Account with a Signal Group/Channel like this:

![Telegram](https://raw.githubusercontent.com/Mastaaa1987/pocketoptionrobot/refs/heads/main/docs/Telegram.png)

### 2. A PocketOption Account to trade with.

### 3. My Robot.

</details>

## Installation

<details>
<summary>Click HERE for Content.</summary>

### Download MyBot from Here and Start the Robot to get this Screen:

![FirstScreen](https://raw.githubusercontent.com/Mastaaa1987/pocketoptionrobot/refs/heads/main/docs/FirstScreen.png)

</details>

## Setup

<details>
<summary>Click HERE for Content.</summary>

### To get the bot running properly, two prerequisites must be met. 

### 1. It need a Telegram ID and Hash.

## HowTo get ID & Hash from Telegram?

<details>
<summary>Click HERE for Content.</summary>

### For the Telegram ID & Hash it need to get a Developer Account. 

- Visit https://my.telegram.org/auth & start Rgistration with your Phone number.
- In follow the Registration you need to set a Name for your App. You can take what ever you want, Nobody will check that.
- The Same with the Info. After the Registration you got your App ID & Hash.

</details>

### 2. It need the SSID from the PocketOption platform.

## HowTo get SSID from PocketOption?

<details>
<summary>Click HERE for Content.</summary>

- With Chrome/Firefox Browser goto https://pocketoption.com/ & Login with your Account.
- Next bind F12 to Open the Developer Tools, goto Network & Filter "Socket" only. 
- Now it is important to check on which platform you are, on Real Account or on Demo. 
- Refresh the Site with F5 to see all WebSocket connections to PocketOption.
- Go into the Socket Messages & look after the Message it beginning with: 

```shell
42["auth",{"session"...
```

![PocketOption](https://raw.githubusercontent.com/Mastaaa1987/pocketoptionrobot/refs/heads/main/docs/PocketOption.png)

Example Demo SSID:

```shell
42["auth",{"session":"1abcdef2ghijk3lmnop4qrest7","isDemo":1,"uid":12345678,"platform":2,"isFastHistory":true,"isOptimized":true}]
```

Example Real SSID:

```shell
42["auth",{"session":"a:4:{s:10:\"session_id\";s:32:\"1abcdef2ghijk3lmnop4qrest7uvwxyz\";s:10:\"ip_address\";s:14:\"11.222.333.444\";s:10:\"user_agent\";s:111:\"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/144.0.0.0 Safari/537.36\";s:13:\"last_activity\";i:1770790020;}a78001006094d91025e66f8b335d83d2","isDemo":0,"uid":12345678,"platform":2,"isFastHistory":true,"isOptimized":true}]
```

- Copy the right Message and past them inside Settings of Bot.

![Setup](https://raw.githubusercontent.com/Mastaaa1987/pocketoptionrobot/refs/heads/main/docs/Setup.png)

</details>

### 3. Last but not least it need the ID of the Channel you want to catch this Signal.

(at start you can create quick & simple a Group or Channel to Send your own test Signals into it ...)

## HowTo get Telegram Channel ID?

<details>
<summary>Click HERE for Content.</summary>

### Search Telegram User @ScanIDBot and send /start to get the Channel/Group ID.

![Telegram1](https://raw.githubusercontent.com/Mastaaa1987/pocketoptionrobot/refs/heads/main/docs/Telegram1.png)

![Telegram2](https://raw.githubusercontent.com/Mastaaa1987/pocketoptionrobot/refs/heads/main/docs/Telegram2.png)

![Telegram3](https://raw.githubusercontent.com/Mastaaa1987/pocketoptionrobot/refs/heads/main/docs/Telegram3.png)

![Telegram4](https://raw.githubusercontent.com/Mastaaa1987/pocketoptionrobot/refs/heads/main/docs/Telegram4.png)

</details>

## What is the UTC Setting & HowTo set it?

<details>
<summary>Click HERE for Content.</summary>

### UTC means the Time different between the Signal and your Host System. 

Here are 2 Examples how to calculate the UTC Setting:

![UTC](https://raw.githubusercontent.com/Mastaaa1987/pocketoptionrobot/refs/heads/main/docs/UTC.png)

</details>

</details>

## Run Settings

<details>
<summary>Click HERE for Content.</summary>

### On the left Side (Automatic Mode) are many Settings for the Trades itself.



| Setting              | Input Value  | Info                                                                           |
| :------------------: | :----------: | :----------------------------------------------------------------------------: |
| min_payout           | 0-92         | Is the minimal Payout what the Pair need to Trade in %.
| pair_multi_trades    | ON/OFF       | ON: Trade only one Time each Pair. OFF: Trade multi times each Pair.
| min_win_ratio        | 0-100        | Minimal Win ratio from Signal Server.
| mtg_coefficient      | 1.0-..       | Faktor to increase the amount on MTG's.
| trade_amount         | 0,1.0-..     | Value of Trade Amount. (0 = Disable)
| trade_amount_type    | $/%          | Value Type of Trade Amount. Percent or Doller.
| trade_mode           | DEMO/REAL    | Mode to Trade on PocketOption (Demo or Real Account).
| loglevel             | INFO-ERROR   | The Loglevel.
| period               | M1-M5        | The Period which the Bot look for as Signal (e.g. Only 1 min Signals).
| pairs_type           | ALL/REAL/OTC | Wich Art of Pairs is to Trade (Stock/OTC)
| mtg_level            | 0-9          | The Count of Rebuy if the trade is loss.
| max_trades           | 0-9          | Maximal Trade count at same Time. (0 = No Trading!)
| anti_mtg             | FALSE/TRUE   | Invert Trade. (e.g. First Call, Second Put, Third Call ..)
| mtg_typ              | 0/1/2        | 0: next_candle_same_pair, 1: next_signal_same_pair, 2: next_signal_any_pair.
| mtg_dynamic          | FALSE/TRUE   | TRUE: Calculate MTG on Payout each Pair. 
| amount_dynamic       | FALSE/TRUE   | TRUE: Use the Amount as take Out, FALSE: Use the Amount as put In.
| trade_only_top_pairs | ALL/1-10     | Trade only Top Pairs from Telegram Ranking.
| signal_server        | ANY/..       | Which Channel you want to Use (<del>from Settings Tab</del>).
| take_profit          | EMPTY/1-..   | How many Profit is to take before the bot going to sleep.
| stoploss             | EMPTY/1-..   | How many Loss is to take before the bot going to sleep.
| trade_time           | FROM/TO      | The Time where the Bot can take Trades.
| trade_expiration     | AUTO/M1-H1   | Trade a specify time period. (e.g. 1 min, 2 min ...)

</details>

# Optional addition: Setup own Signal Server.

<details>
<summary>Click HERE for Content.</summary>

### If you don't have (or don't want) a external Telegram Signal Server

### is here a Quick & Dirty howto to setup your own one. 

## Prerequire Steps:

<details>
<summary>Click HERE for Content.</summary>

## Get Metatrader 4

At first you need to download Meta Trader 4 Version from here:

[www.fxcm.com](https://www.fxcm.com/de/plattformen/metatrader-4/herunterladen/)

After the installation you need only to register a demo Account until this Screen:

![MetaTrader1](https://raw.githubusercontent.com/Mastaaa1987/pocketoptionrobot/refs/heads/main/docs/MetaTrader1.png)

Next open the Settings with Ctrl+O and switch to the Expert Tab. There hit the checkbox Allow to import DLL's & Allow trusted WebRequest for following URL's.

As URL you need to add: https://api.telegram.org

![MetaTrader2](https://raw.githubusercontent.com/Mastaaa1987/pocketoptionrobot/refs/heads/main/docs/MetaTrader2.png)

As next step click on File (on Top left) and then on open Filefolder (i don't know how exactly in English, sorry), to open the MetaTrader File Folder:

![MetaTrader3](https://raw.githubusercontent.com/Mastaaa1987/pocketoptionrobot/refs/heads/main/docs/MetaTrader3.png)

Now copy the Content inside the MetaTrader folder from my Repo (e.g. the MQL4 Folder) into this Folder.

![MetaTrader4](https://raw.githubusercontent.com/Mastaaa1987/pocketoptionrobot/refs/heads/main/docs/MetaTrader4.png)

The last step for now is to restart MetaTrader. Now the first prerequire steps are done.

## Create own Telegram Channel and Bot

At First we create a Telegram Bot. Here for start Conversation with @BotFather and send a Message with: /start

Next send /newbot & follow the industructions to recieve the Bot token.

![Telegram5](https://raw.githubusercontent.com/Mastaaa1987/pocketoptionrobot/refs/heads/main/docs/Telegram5.png)

Now click on the Bot Name (4) and send him a /start Message. 

Next create a new Group or Channel with Name you want.

![Telegram6](https://raw.githubusercontent.com/Mastaaa1987/pocketoptionrobot/refs/heads/main/docs/Telegram6.png)

As last step add your Bot to your Channel and give them Admin rights.

![Telegram7](https://raw.githubusercontent.com/Mastaaa1987/pocketoptionrobot/refs/heads/main/docs/Telegram7.png)

### Now the prerequire Step's are done ...

</details>

## Expert: MCharts-OTC (Mastaaa's OTC Charts)

<details>
<summary>Click HERE for Content.</summary>

### With the MCharts-OTC Expert you can get Live OTC Charts from PocketOption (and other Platforms) for free.

Here for you need only to open One other Chart from the List (Top left), with a right click on any Symbol and then in the Submenu click on New Chartwindow.

Then in the Navigator menu under Experts search after MCharts-OTC-v1.9 double click on it to add them on the Chart.

![MetaTrader5](https://raw.githubusercontent.com/Mastaaa1987/pocketoptionrobot/refs/heads/main/docs/MetaTrader5.png)

When everything working right it gives 2 Ways to open OTC Charts. You can click on File -> Open offline Charts, or simple click on Open All OTC Charts button inside the Chart.

![MetaTrader6](https://raw.githubusercontent.com/Mastaaa1987/pocketoptionrobot/refs/heads/main/docs/MetaTrader6.png)

</details>

## Indicator: MUT-Connector (Mastaaa's Ultimate Telegram - Connector)

<details>
<summary>Click HERE for Content.</summary>

### In Metatrader it gives 3 different Ways to catch the Signal from a Indicator on a Chart.

### 1. Get the buffer of an Indicator on Chart.

This method is working allways, but be warned: You can work with every Indicator but you can't make any setup for the Indicator! It working only with default settings of a Indicator ...

### 2. Get a Object of an Indicator on Chart.

This working only with Indicators which draw Objects on a Chart like Arrows. And this will not really do in the most of it. With this method you can change the Settings of the Indicator!

### 3. Get the Alert of an Indicator on Chart.

Here the same if condition as the Object method. It working only if the Indicator will send a Alert Message in Metatrader.

### Important is you need to add the MUT-Connector one time on any Chart you work with

### Here are the Settings which in all 3 Modes available:

![MUT1](https://raw.githubusercontent.com/Mastaaa1987/pocketoptionrobot/refs/heads/main/docs/MUT1.png)

## Buffer Mode

<details>
<summary>Click HERE for Content.</summary>

### For the Buffer Mode you NOT need to add the Indicator on the Chart! 

### The MUT-Connector needs to be add one Time on every Chart.

You only need the Name of Indicator, i added a Test Indicator with Name: Donchain_Hill-v1.0

And you need the number of (Buy & Sell) Buffer. Next i will explane how to get the right number of Indicator Buffer.

To see all Buffers of an Indicator you need first to add it on a Chart. Then press Ctrl + D to get the Datawindow.

When you go with the Mouse over a Candle in the Datawindow you see the Value of any Buffer of the Indicator ...

![MUT2](https://raw.githubusercontent.com/Mastaaa1987/pocketoptionrobot/refs/heads/main/docs/MUT2.png)

The Buffer Numbers are from Top to Bottom 0,1,2,3 ... The Call/Buy Buffer have the Number: 0

![MUT3](https://raw.githubusercontent.com/Mastaaa1987/pocketoptionrobot/refs/heads/main/docs/MUT3.png)

Here the Same Indicator but this Time a Put/Sell Candle to see. With Buffer Number: 1

The next Picture Show's the right Buffer Mode Settings:

![MUT4](https://raw.githubusercontent.com/Mastaaa1987/pocketoptionrobot/refs/heads/main/docs/MUT4.png)

With the Buffer Shift setting you can shift the Candle which is used for the Signal from 0 to a later one.

(Info: Candle 0 is this Candle what is currently Open but not Closed! Candle 1 is behind and the first Closed one.)

![MUT5](https://raw.githubusercontent.com/Mastaaa1987/pocketoptionrobot/refs/heads/main/docs/MUT5.png)

In the End you can check if is all right when you add simple the Indicator & the MUT-Connector on the Chart and 

look after the Call/Put Buffer form the Connector & the Indicator. 

If have both a Value in the right Buffer everything working fine ...

</details>

## Object Mode

<details>
<summary>Click HERE for Content.</summary>

### For the Object Mode you need to add the Indicator & MUT-Connector on the Chart!

### (Not any Indicator draw Arrows as Objects! You need to check this first ...)

First add the Indicator on a Chart and make a right click on it and choise Objectives or Type Simple: Ctrl + B

Now in the next Window you can see how many Objects are really on the Chart.

(if the list is empty the Indicator doesn't draw Objects!)

You have 2 Options to catch a Object with the MUT-Connector. 1. By Object Name. 2. By Object Color.

Both Infos are to see in the Object setting Window (when you double click on a Object in a Row ...)

![MUT6](https://raw.githubusercontent.com/Mastaaa1987/pocketoptionrobot/refs/heads/main/docs/MUT6.png)

In this Example have all Object the same Name, so we need to work with the different Colors of the Arrows. 

E.g. Red (for Put/Sell) & Lime Green (for Call/Buy). 

![MUT7](https://raw.githubusercontent.com/Mastaaa1987/pocketoptionrobot/refs/heads/main/docs/MUT7.png)

If you are set the right Colors to catch you can easy open the Datawindow (with Ctrl+D) and then go with the Mouse over a Candle with a Object.

If anything is working correctly the Call or Put Buffer (Buffer 0 and 1) of the MUT-Connector should be shows "1.0". Then all is Working fine.

![MUT8](https://raw.githubusercontent.com/Mastaaa1987/pocketoptionrobot/refs/heads/main/docs/MUT8.png)

</details>

## Alarm Mode

<details>
<summary>Click HERE for Content.</summary>

### You need to add the MUT-Connector on every Chart you want to catch a Signal!



</details>

</details>

</details>

