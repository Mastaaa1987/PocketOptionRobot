# PocketOptionRobot
MyBot is a full in Python written Standalone Windows executable Robot. It is designed to catch Signals via Telegram and trade directly on PocketOption platform. 

![MyBot](https://raw.githubusercontent.com/Mastaaa1987/pocketoptionrobot/refs/heads/main/docs/MyBot.png)

## What you Need?

<details>
<summary>Click HERE for Content.</summary>

### A Telegram Account with a Signal Group/Channel like this:

![Telegram](https://raw.githubusercontent.com/Mastaaa1987/pocketoptionrobot/refs/heads/main/docs/Telegram.png)

### A PocketOption Account to trade with.

### My Robot.

</details>

## Installation

<details>
<summary>Click HERE for Content.</summary>

### Download MyBot here and start the Robot to get this Screen:

![FirstScreen](https://raw.githubusercontent.com/Mastaaa1987/pocketoptionrobot/refs/heads/main/docs/FirstScreen.png)

</details>

## Setup

<details>
<summary>Click HERE for Content.</summary>

### To get the bot running properly, two prerequisites must be met. First, we need a Telegram ID and hash.

## HowTo get ID & Hash from Telegram?

<details>
<summary>Click HERE for Content.</summary>

### For the Telegram ID & Hash we need to get a Developer Account. 

- Visit https://my.telegram.org/auth & start Rgistration with your Phone number.
- In follow the Registration you need to set a Name for your App. You can take what ever you want, Nobody will check that.
- The Same with the Info. After the Registration you got your App ID & Hash.

</details>

### And Second we need the SSID from the PocketOption platform.

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

### Last but not least we need the ID of the Channel We want to catch the Signal with the Bot.

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

### Here are 2 Examples how to calculate the UTC Setting:

![UTC](https://raw.githubusercontent.com/Mastaaa1987/pocketoptionrobot/refs/heads/main/docs/UTC.png)

</details>

</details>

