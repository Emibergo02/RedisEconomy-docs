---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# ▶️ Commands

## 1 **Player Commands**

### /balance or /money

Displays your balance (vault/default currency)\
Permission: `rediseconomy.balance`

### /balance (or /money) \<player> \[currencyName]

Displays \<player>'s balance\
CurrencyName is the name of the currency to be displayed\
Permission: `rediseconomy.balance.[currencyName]`

### /pay \<player> \<amount> \[currencyName]

Simple pay command but you can specify the currency\
Permission: `rediseconomy.pay`

### /pay \* \<amount> \[currencyName]

Pay all players in your server \<amount> money\
Permission: `rediseconomy.payall`

### /balancetop (or /baltop) \<page> \[currencyName]

Displays the top richest accounts (with vault/default currency)\
Permission: `rediseconomy.balancetop`

### /toggle-payments \<player or \* or all>

Blocks payments incoming from \<player>\
Permission: `rediseconomy.toggle-payments`

### /toggle-payments

Shows blocked accounts list\
Permission: `rediseconomy.toggle-payments`

## **2 OP Commands**

### /rediseconomy reload

reloads config.yml\
Permission: `rediseconomy.admin`

### /rediseconomy editmessage \<configField>

Edit a language field with a convenient web UI\
Permission: `rediseconomy.admin.editmessage`

### /balance \<player> \<currencyName> give \<amount> \[reason...]

With "reason" you can specify why the transaction has been made\
More on [transactions.md](../unique-features/transactions.md "mention")\
Permission: `rediseconomy.balance`

### /balance \<player> \<currency> take \<amount> \[/command... or reason...]&#x20;

Takes money from a player.\
It is possible to specify a command to execute if the player has sufficient funds.\
If the command does not have the "/" it will be registered as the reason\
Permission: `rediseconomy.balance`

### /balance \<player> \<currency> set \<amount>

Purely for moderation\
Permission: `rediseconomy.balance`

### /purge-balance \<player-regex>

Purges the balance of the players matching the regex \
ex. Steve(.\*) matches SteveCarell and Steve\_\
**USE WITH CAUTION**\
Permission: `rediseconomy.purge-balance`

### /switch-currency \<currency> \<newcurrency>

Switches all currency accounts with other currency accounts. You have to restart each instance of RedisEconomy to apply the changes\
Permission: `rediseconomy.pay.currencyname`

### /backup-economy \<filename>

Backups the economy system to a file\
Permission: `rediseconomy.admin.backup-restore`

### /restore-economy \<filename>

Restores the economy system from a file\
Permission: `rediseconomy.admin.backup-restore`



More commands are coming...\


## **3 Further permissions:**

### `rediseconomy.admin`

Allows the use of all OP commands&#x20;

## `rediseconomy.admin.giveall`

Allows a player to give money to all online players through balance command with \*
