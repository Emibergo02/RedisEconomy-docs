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

## Register calling plugin

Append the **stacktrace** of the method that called the RedisEconomy API method inside the\
transaction `reason` field

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

To enable this feature, use `registerCallsVerbosity` field

{% code title="config.yml" overflow="wrap" %}
```yaml
# Set to 0 if you want the feature disabled
# Set to 1 if you want only the calling class to be saved
# Set to 2 to have both class and method, or 3 to have line number too
registerCallsVerbosity: 0 #By default is 0
```
{% endcode %}

### Commands:

* <mark style="color:orange;">**`transaction <player> <transaction-id> [revert]`**</mark> - Rollback a transaction with another transaction\
  Permission: <mark style="color:orange;">`rediseconomy.admin.transaction`</mark>
* <mark style="color:orange;">**`browse-transactions <player> [beforedate] [afterdate]`**</mark> - View transactions of a player (you can navigate inside it: **all the playernames are clickable)**\
  Permission: <mark style="color:orange;">`rediseconomy.admin.browse-transactions`</mark>\
  Dates format: <mark style="color:blue;">`yyyy-MM-dd_HH.mm.ss`</mark>
* <mark style="color:orange;">**`archive-transactions <filename>`**</mark> - Dump all transaction data to a file. Use it when your transaction db is too heavy\
  Permission: <mark style="color:orange;">`rediseconomy.admin.archive-transactions`</mark>

(Check transactionTTL inside [currency-settings.md](multiple-currencies-with-offline-payments/currency-settings.md "mention") to unlock the full potential of transactions)
