# 🚀 Pancakeswap BSC Sniper Bot 🚀

## TELEGRAM GROUP: https://t.me/+KXvQjzlHv8c2NGU1 - please join to assist in development, ask questions, share any successes etc.
## BSCTokenSniper v2.2 in development and will be released in next few days.

## BSCTokenSniper v2.1.1 Beta available
Improvements:
- Added code blacklist (rug_function.txt): the program will ignore any program with code that is in this file
- Added min liquidity checker (won't buy token unless it has certain amount of liquidity) - edit threshold in config.json
- Fixed issue with buy - saying transaction failed when it was fine
- Websocketprovider - alot more reliable and also faster, should be less crashing as well
- Some bits of code tidied up

### Getting Started
A bot written in Python to automatically buy tokens on the Binance Smart Chain as soon as liquidity is provided.
•	BSCMultiScan - automatically detects new tokens as soon as liquidity is added. It will check if it is not a scam and honeypot and if not bot will buy it. It will then monitor the price of the token and auto sell at the specified profit margin (eg. 1.5x, 2x, 10x etc).
•	BSCSpecificScan - allows you to snipe new token launches paired with any token (eg. BNB, BUSD). It has the ability to mempool snipe and will instantly buy when liquidity is added. It constantly updates the price and shows you the profit you've made, has the ability to autosell at a specified profit margin (eg, 2x, 10x etc).
By avoiding web interfaces & Metamask and directly with nodes you can snipe tokens faster than any of the web-based platforms. This allows tokens to be sniped almost instantly. During our testing we found the bot would typically be within the first 3 buy transactions of all tokens it finds. The bot buys the tokens using the user's wallet address and private key. This information is kept secure, is only stored locally on your computer, and is only ever used to buy tokens.
The bot does not incur any additional fees except from the dev fees on profit made, only fees are BSC network transaction fees and PancakeSwap fees.
The bot's source code is heavily obfuscated and compiled to prevent people stealing code and scammers trying to bypass this system as this has happened before. If you have concerns about the security of this bot then you should create a new wallet with a small amount of BNB and use that wallet's details in the config file. If you make a profit then that can be transferred to your main wallet.

### Prerequisites
- Python 3 or later installed
- Node.js installed (easiest way) – Install windows version from https://nodejs.org/en/download/
- Web3 installed (in windows command line type: pip install web3)
- BscScan API key (completely free of charge, create an account on BscScan and generate a free API key)
- BSC wallet address and private key
- enough BNB in your wallet to snipe tokens.

### Description
The aim of BSC Token Sniper is to buy new tokens with a specified amount of BNB, with the aim of the price rising Once the bot detects a PairCreated event, it is able to check the token (mini audit).
 It can check if:
-	Source code is verified.
-	If valid PancakeSwap v2 router is being used 
-	If a mint function exists
-	If it is a potential honeypot
-	PancakeSwap v1 router address is not being used.
The user can decide whether to enable the mini audit or turn it off (bear in mind you will likely be investing in a lot of scams if you don’t).
Once the token has/hasn't been through a mini audit the bot will then attempt to buy X amount of tokens with the specified amount of BNB.
The bot will buy the tokens directly through the Binance Smart Chain using the PancakeSwap v2 router and factory address, so it is much quicker than the PancakeSwap web interface.
By avoiding web interfaces & Metamask and directly with Ethereum & EVM Nodes you can snipe tokens faster than any of the web-based platforms. This allows tokens to be sniped almost instantly. During our testing we found the bot would typically be within the first 3 buy transactions of all tokens it finds.
The bot buys the tokens using the user's wallet address and private key. This information is kept secure, is only stored locally on your computer, and is only ever used to buy tokens (look through the code to see for yourself).
The bot does not incur any additional fees, only fees are BSC network transaction fees and PancakeSwap fees.

## Setup
 ### Supported OS's
  1. Windows
  2. Linux 
  3. Mac 
  4. Android 
## **INSTALLATION**
  ### Windows
   1. Download git [Git](https://git-scm.com/)
   2. . Clone the repo or download repo: 
    - `https://github.com/blockchaindev90/BSCTokenSniper.git`
   3. Download python  [Python](https://www.python.org/) ( should see Python 3.9.8 or later showing)
   4. Run CMD : pip install web3
   5. Check python version : python --version
   6. Select BSCTokenSniper bot with your python version
   7. run bat file ( ex : launch_3.10.1.bat)
   #### Note if you get error when running pip install web3 , check this 				 https://github.com/blockchaindev90/BSCTokenSniper/blob/main/guide%20to%20fix%20errors%20when%20installing%20web3.pdf ***
  ### Linux User
  Install package With `sudo`
  Debian / Ubuntu : 
    1. install all dependency using command below : ` apt install git && apt install python3-pip && pip install web3 ` 
      
    2. Clone repository and install web3 : `https://github.com/blockchaindev90/BSCTokenSniper.git && cd BSCTokenSniper && pip install web3`
        
  Fedora Linux / Centos
    1. install all dependency using command below : ` dnf git && dnf install python3-pip && pip install web3 ` 
       
    2. Clone repository and install web3 : `https://github.com/blockchaindev90/BSCTokenSniper && cd BSCTokenSniper && pip install web3`
       
  Arch Linux
    1. install all dependency using command below : ` pacman -S git && pacman -S install python3-pip && pip install web3 ` 
       
    2. Clone repository and install web3 : `https://github.com/blockchaindev90/BSCTokenSniper.git && cd BSCTokenSniper && pip install web3`
        
  ### Mac (Intel / Universal)
    NOTE: BSCLaunchSniper is currently not working for M1 Macs (Apple silicon chips) due to the keyboard module being incompatible. This will hopefully be fixed in the future.
    Make sure python 3 is installed
    open terminal window
    type : python3 --version
    if you get an error message and python3 isn't installed, you need to add it.
    go to https://www.python.org/ and install latest version of python for mac
    in terminal window one last check to see you have Python 3 installed
    type : python3 --version
   should see Python 3.9.8 or later showing
      
  ### Android
   1. Install Termux [Link](https://play.google.com/store/apps/details?id=com.termux&hl=en&gl=US)
   2. Update
      `pkg update && pkg upgrade`
   3. Install dependency
     `pkg install git python3 python3-pip`
    4. Clone the repo using git
	    `https://github.com/blockchaindev90/BSCTokenSniper.git && cd BSCTokenSniper`
     Note:
     You may find an error when installing web3 in android. You should install dependency needed by web3 manually using pip.
     The web3 version that work for this bot is web3 5.x.x if your web3 is 3.x.x the bot will not work.
## Run python script
Assuming you are in BSCTokenSniper Directory.
run `python BSCTokenSniper.pyc`
To use other version you need to go to the directory needed and run the python script.
** If you are not familiar with Python please have a look at https://github.com/blockchaindev90/BSCTokenSniper/releases/, there you can download Windows executable. **
## Configuration File
Setup file config.json
https://github.com/blockchaindev90/BSCTokenSniper/blob/main/BSC%20Sniper%20Bot%20with%20QUICK%20NODE%20Guide%20v2.1.1%20(%20Websocket%20supported).pdf
### Mini audit
The bot has an optional mini audit feature which aims to filter some of the scam coins (eg. wrongly configured, honeypots). Obviously, this is not going to be as good as a proper audit (eg. CertiK) but at least the coins the bot will buy will be higher quality and if you enable the options, you should be able to sell the tokens later on (provided it hasn’t been rugged).
The following json entries are for mini audit. Set all to false to disable mini audits, although beware you will probably be buying a lot of scam coins.
checkSourceCode: checks if source code is verified. This function is needed for all the other functions so if you disable this be sure to disable all the other audit options. Recommended. v1.3 onwards will use RugDoc tool to check for honeypots and high fee tokens.
checkValidPancakeV2: checks if the correct PancakeSwap v2 router address is used in the code. Be aware some contracts may externally set their router address so this function may reject a potentially good token. Not recommended.
checkMintFunction: checks if a mint function is present in the code. Recommended.
checkHoneypot: checks the code to see if it might be a honeypot (where you can buy tokens but cannot sell). Recommended.
checkPancakeV1Router: checks to see if the PancakeSwap v1 router address is used in the code. You will not be able to sell the tokens later on if PCS v1 router address is used. Highly recommended.
checkForTest: checks for tokens that are named 'test'. Often these tokens don't work or are not an investment opportunity.

Note: be very careful when editing config.json and make sure to not alter the syntax. For mini audit options, either use “True” or “False” making sure to capitalise the 1st letter. Any other spelling will not work.

### Things to note
-	Do not worry if you are not seeing any new tokens being detected. There are often around 10-20 new tokens being created per minute but that can vary quite a lot. Sometimes no new tokens may be detected for a few minutes.
-	The bot only buys tokens whose liquidity is paired with Wrapped BNB (WBNB). You could alter the code to buy tokens paired with another currency if you wanted.
-	Please check that you have enough BNB in your wallet to afford sniping new tokens. If you don’t the bot will not work.
-	Please be careful when editing the config.json file. If you delete a comma or quotation mark etc. the bot will not work and throw an error.
-	To launch the bot, run the ‘launch.bat’. The bot should then open in a cmd window and load.
-	Don’t left click in the cmd window as it will enable select mode and stop the output (you will see ‘Select’ in the title). If this happens right click your mouse to deselect it. 

### Risks:
Investing in BSC tokens / shitcoins is risky and be aware you could lose all your money. For this reason, do not invest more money than you are prepared to lose.
It is pretty much impossible to snipe bots very early and be sure it isn’t a rug pull. When people create tokens in most situations, they will manually create liquidity in PancakeSwap. This is when the bot will detect the token. If they burn / lock liquidity, they will then usually send their LP tokens manually to a deadcoin address or put them in a liquidity locker. Therefore, you can’t immediately snipe the tokens with 100% certainty they aren’t rugpulls.
The mini audit feature can’t be 100% accurate but aims to filter out the majority of scams / hacks and reduce the chance of losing your money.
If a programmer creates token code in a unique way, they may be able to bypass detection although this is generally quite rare, as the majority of tokens are forks of big projects with very little of the code having been changed e.g., Safemoon.

### Things to do / improve / fix:
- Look into rugpull detection (in development)
- Auto sell after certain profit reached? (in development)
- Make ETHTokenSniper that does the exact same but runs on the ethereum blockchain
- Are all tokens that haven't verified their source code bad? Probably not. But the bot currently just assumes that developers will verify their source code before adding liquidity. The bot can't tell if it's a scam or not if the source code isn't verified.
 - Also maybe an option to sell it at a certain price point. Look what happened to Refinable, a bot bought a huge chunk of the tokens and made an insane amount of money in a few minutes.
- Improve reliability: the program can sometimes unexpectedly freeze. This is being investigated.
- Allow user to set slippage percentage
### If you’ve found this bot useful and have profited from it please consider donating any token to my BSC wallet address: 0x581424c4ED701F261f0A963386cc437Ed986ea34
Thanks 

Blockchain Guru and dev team
