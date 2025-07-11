---
description: Register your currency movements and browse the transaction chain
---

# 📜 Transactions

You can search or reverse transactions. \
Example:

<figure><img src="../.gitbook/assets/image (28).png" alt=""><figcaption><p>Transaction visualization</p></figcaption></figure>

* <img src="../.gitbook/assets/image (3).png" alt="" data-size="original"> is the **transaction ID**
* <img src="../.gitbook/assets/image (4).png" alt="" data-size="original"> You can hover over this component to see **the exact time the transaction was executed**
* ![](<../.gitbook/assets/image (6).png>) This is the button to **revert the transaction** (the amount will be transferred from the receiver to the sender

### Commands:

* <mark style="color:orange;">**`transaction <player> <transaction-id> [revert]`**</mark> - Rollback a transaction with another transaction\
  Permission: <mark style="color:orange;">`rediseconomy.admin.transaction`</mark>
* <mark style="color:orange;">**`browse-transactions <player> [beforedate] [afterdate]`**</mark> - View transactions of a player (you can navigate inside it: **all the playernames are clickable)**\
  Permission: <mark style="color:orange;">`rediseconomy.admin.browse-transactions`</mark>\
  Dates format: <mark style="color:blue;">`yyyy-MM-dd_HH.mm.ss`</mark>
* <mark style="color:orange;">**`archive-transactions <filename>`**</mark> - Dump all transaction data to a file. Use it when your transaction db is too heavy\
  Permission: <mark style="color:orange;">`rediseconomy.admin.archive-transactions`</mark>



(Check transactionTTL inside [currency-settings.md](multiple-currencies-with-offline-payments/currency-settings.md "mention") to unlock the full potential of transactions)
