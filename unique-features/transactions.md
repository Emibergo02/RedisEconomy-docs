---
description: Register your currency movements and browse the transaction chain
---

# 📜 Transactions

You can search or reverse transactions.\
Example:\


<figure><img src="../.gitbook/assets/image (28).png" alt=""><figcaption><p>Transaction visualization</p></figcaption></figure>

* <img src="../.gitbook/assets/image (3).png" alt="" data-size="original"> is the **transaction ID**&#x20;
* <img src="../.gitbook/assets/image (4).png" alt="" data-size="original"> You can hover over this component to see **the exact time the transaction was executed**
* ![](<../.gitbook/assets/image (6).png>) This is the button to **revert the transaction** (the amount will be transferred from the receiver to the sender

### Commands:

* **transaction \<player> \<transaction-id> \[revert]** - Rollback a transaction with another transaction\
  Permission: `rediseconomy.admin.transaction`
* **browse-transactions \<player> \[beforedate] \[afterdate]** - View transactions of a player (you can navigate inside it: **all the playernames are clickable)**\
  Permission: `rediseconomy.admin.browse-transactions`
* **archive-transactions \<filename>** - Dump all transaction data to a file. Use it when your transaction db is too heavy\
  Permission: `rediseconomy.admin.archive-transactions`

