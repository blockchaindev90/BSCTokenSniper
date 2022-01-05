# 🚀 Pancakeswap BSC Sniper Bot 🚀

## TELEGRAM GROUP: https://t.me/+KXvQjzlHv8c2NGU1 - please join to assist in development, ask questions, share any successes etc.
## BSCTokenSniper v2.2 in development and will be released in next few days.

## BSCTokenSniper v2.1 Beta available

### Getting Started
A bot written in Python to automatically buy tokens on the Binance Smart Chain as soon as liquidity is provided.
•	BSCMultiScan - automatically detects new tokens as soon as liquidity is added. It will check if it is not a scam and honeypot and if not bot will buy it. It will then monitor the price of the token and auto sell at the specified profit margin (eg. 1.5x, 2x, 10x etc).
•	BSCSpecificScan - allows you to snipe new token launches paired with any token (eg. BNB, BUSD). It has the ability to mempool snipe and will instantly buy when liquidity is added. It constantly updates the price and shows you the profit you've made, has the ability to autosell at a specified profit margin (eg, 2x, 10x etc).
By avoiding web interfaces & Metamask and directly with nodes you can snipe tokens faster than any of the web-based platforms. This allows tokens to be sniped almost instantly. During our testing we found the bot would typically be within the first 3 buy transactions of all tokens it finds. The bot buys the tokens using the user's wallet address and private key. This information is kept secure, is only stored locally on your computer, and is only ever used to buy tokens.
The bot does not incur any additional fees except from the dev fees on profit made, only fees are BSC network transaction fees and PancakeSwap fees.
The bot's source code is heavily obfuscated and compiled to prevent people stealing code and scammers trying to bypass this system as this has happened before. If you have concerns about the security of this bot then you should create a new wallet with a small amount of BNB and use that wallet's details in the config file. If you make a profit then that can be transferred to your main wallet.

### Prerequisites
•	A reasonably fast internet connection
•	Python 3 or later installed (ideally 3.9.9 or later)
•	BscScan API key
•	BSC wallet address and private key (not seed phrase)
•	A BSC node
•	Enough BNB in your wallet to snipe tokens
•	Python3.9.9 & Web3 & BscScan API
1.	Download Git
2.	Download python Python3.9.9
3.	Clone the repo: git clone https://github.com/blockchaindev90/BSCTokenSniper
4.	Go to repo directory : cd BSCTokenSniper 
5.	Install web3 : pip install web3

** If you are not familiar with Python please have a look at https://github.com/blockchaindev90/BSCTokenSniper/releases/, there you can download Windows executable. **
### Setup file config.json
Setup by flow https://github.com/blockchaindev90/BSCTokenSniper/blob/main/BSC%20Sniper%20Bot%20with%20QUICK%20NODE%20Guide%20v2.1%20(%20Websocket%20supported).pdf
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
### If you’ve found this bot useful and have profited from it please consider donating any token to my BSC wallet address: 0x6Cf2dE5aF8951Bc5ab4B80360fa9F821B767Ce04
Thanks 
Blockchain Guru and dev team
