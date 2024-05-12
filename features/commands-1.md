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

# ▶️ OP commands

### <mark style="color:orange;">`/rediseconomy reload`</mark>

reloads config.yml\
Permission: <mark style="color:yellow;">`rediseconomy.admin`</mark>

### <mark style="color:orange;">`/rediseconomy editmessage <configField>`</mark>

Edit a language field with a convenient web UI\
Permission: <mark style="color:yellow;">`rediseconomy.admin.editmessage`</mark>

### <mark style="color:orange;">`/balance <player> <currencyName> give <amount> [reason...]`</mark>

With "reason" you can specify why the transaction has been made\
More on [transactions.md](../unique-features/transactions.md "mention")\
Permission: <mark style="color:yellow;">`rediseconomy.balance`</mark>

### <mark style="color:orange;">`/balance <player> <currency> take <amount> [/command... or reason...]`</mark>

Takes money from a player.\
It is possible to specify a command to execute if the player has sufficient funds.\
If the command does not have the "/" it will be registered as the reason\
Permission: <mark style="color:yellow;">`rediseconomy.balance`</mark>

### <mark style="color:orange;">`/balance <player> <currency> set <amount>`</mark>

Purely for moderation\
Permission: <mark style="color:yellow;">`rediseconomy.balance`</mark>

### <mark style="color:orange;">`/purge-balance <player-regex>`</mark>

Purges the balance of the players matching the regex\
ex. Steve(.\*) matches SteveCarell and Steve\_\
**USE WITH CAUTION**\
Permission: <mark style="color:yellow;">`rediseconomy.purge-balance`</mark>

### <mark style="color:orange;">`/switch-currency <currency> <newcurrency>`</mark>

Switches all currency accounts with other currency accounts. You have to restart each instance of RedisEconomy to apply the changes\
Permission: <mark style="color:yellow;">`rediseconomy.pay.currencyname`</mark>

### <mark style="color:orange;">`/backup-economy <filename>`</mark>

Backups the economy system to a file\
Permission: <mark style="color:yellow;">`rediseconomy.admin.backup-restore`</mark>

### <mark style="color:orange;">`/restore-economy <filename>`</mark>

Restores the economy system from a file\
Permission: <mark style="color:yellow;">`rediseconomy.admin.backup-restore`</mark>

More commands are coming...\\

## **Further permissions:**

### <mark style="color:yellow;">`rediseconomy.admin`</mark>

Allows the use of all OP commands

### <mark style="color:yellow;">`rediseconomy.admin.giveall`</mark>

Allows a player to give money to all online players through balance command with \*
