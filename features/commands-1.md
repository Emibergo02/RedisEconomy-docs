# ▶️ OP commands

### <mark style="color:orange;">`/rediseconomy reload`</mark>

reloads config.yml\
Permission: <mark style="color:yellow;">`rediseconomy.admin`</mark>

### <mark style="color:orange;">`/rediseconomy editmessage <configField>`</mark>

Edit a language field with a convenient web UI\
Permission: <mark style="color:yellow;">`rediseconomy.admin.editmessage`</mark>

### <mark style="color:orange;">**`/browse-transactions <player> [beforedate] [afterdate]`**</mark>&#x20;

View transactions of a player (you can navigate inside the browser: _all the playernames are clickable_**)**\
Permission: <mark style="color:yellow;">`rediseconomy.admin.browse-transactions`</mark>\
Dates format: <mark style="color:blue;">`yyyy-MM-dd_HH.mm.ss`</mark>

### <mark style="color:orange;">`/balance <player> <currencyName> give <amount> [reason...]`</mark>

With "reason" you can specify why the transaction has been made\
More on [transactions.md](../unique-features/transactions.md "mention")\
Permission: <mark style="color:yellow;">`rediseconomy.admin`</mark>

### <mark style="color:orange;">`/balance <player> <currency> take <amount> [/command... or reason...]`</mark>

Takes money from a player.\
It is possible to specify a command to execute if the player has sufficient funds.\
If the command does not have the "/" it will be registered as the reason\
Permission: <mark style="color:yellow;">`rediseconomy.admin`</mark>

### <mark style="color:orange;">`/balance <player> <currency> set <amount>`</mark>

Purely for moderation\
Permission: <mark style="color:yellow;">`rediseconomy.admin`</mark>

### <mark style="color:orange;">`/balance <player> <currency> set-max <amount>`</mark>

Set the maximum balance for a player (useful for mana systems or similar)\
The player deposits would be limited by max balance.\
By default a currency has 1.7x10³⁰⁸ as limit\
Permission: <mark style="color:yellow;">`rediseconomy.admin`</mark>

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

### <mark style="color:orange;">**`/transaction <player> <transaction-id> [revert]`**</mark>&#x20;

Rollback a transaction with another transaction or just displays it without "revert" parameter\
Permission: <mark style="color:yellow;">`rediseconomy.admin.transaction`</mark>

### <mark style="color:orange;">**`/archive-transactions <filename>`**</mark>&#x20;

Dump all transaction data to a file. Use it when your transaction db is too heavy\
This is deprecated. It will be removed in the future after the `Transaction TTL Update`\
Permission: <mark style="color:yellow;">`rediseconomy.admin.archive-transactions`</mark>

### <mark style="color:orange;">`/rediseconomy test`</mark>

Performs 10k transactions on 10 different bank accounts and tells the timings.\
This serves as a benchmark to see if Redis can handle many transactions and if some performance tuning is needed on RedisEconomy configs\
Permission: <mark style="color:yellow;">`rediseconomy.admin.editmessage`</mark>

## **Further permissions:**

### <mark style="color:yellow;">`rediseconomy.admin`</mark>

Allows the use of all OP commands

### <mark style="color:yellow;">`rediseconomy.admin.giveall`</mark>

Allows a player to give money to all online players through balance command with \*
