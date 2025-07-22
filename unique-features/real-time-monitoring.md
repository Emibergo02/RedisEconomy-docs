---
description: Keep track of your actual economy
---

# ⏱️ Real-time monitoring

### Balance is updated almost real-time

when you execute `/baltop <page> [currency]` RedisChat will download the first 200 accounts instantly with no cache update time (thanks to [SortedSet](https://redis.io/glossary/redis-sorted-sets/) data structure)

### Placeholders are updated once every 5 seconds

You can check with `%rediseco_totsupply_<currency>%` the current total supply of the specified currency, A.K.A. how much money is in the system every 5 seconds,\
So you can see if someone is using any money duplication glitch with any plugin using VaultAPI, for example.

There are many placeholders relative to baltop. Check them inside [#advanced-placeholders](../features/placeholders.md#advanced-placeholders "mention")
