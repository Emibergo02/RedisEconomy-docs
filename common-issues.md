# Common issues

During migration duplicated uuids will result as `<uuid>-Unknown` inside the baltop

If you have hanging uuid-Unknown on Redis, use \
<mark style="color:orange;">`/purge-balance (.{36}-Unknown) onlyNameUUID`</mark>\
to clear the redis data

## Updating to 4.5.0 from a version below

Step 1: <mark style="color:orange;">**`/archive-transactions economybackup.txt`**</mark> to save all current transactions to file and delete all transaction from Redis

Step 2: Make sure that NO TRANSACTION IS BEING CREATED BETWEEN Step 1 and Step 3!

Step 3: Update RedisEconomy jar inside plugins folder to 4.5.0

Step 4 (Optional): <mark style="color:red;">Upgrade your Redis Server to version 7.4</mark> or above to <mark style="color:red;">unlock the full potential</mark> of `Transaction Time-To-Live` which allows to automatically forget transactions after a certain amount of time defined inside config.yml
