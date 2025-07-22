---
description: Provider for PlaceholderAPI's placeholders
---

# #️⃣ Placeholders

### Simple placeholders

* <mark style="color:orange;">`%rediseco_bal_<currency>%`</mark> - returns the balance with 2 decimals
* <mark style="color:orange;">`%rediseco_bal_formatted_<currency>%`</mark> - returns the balance with 2 decimals with currency symbol
* <mark style="color:orange;">`%rediseco_bal_short_<currency>%`</mark> - returns the balance with the unit symbol specified in the config (millions,billions,thousands...)

You can use both of them toghether (ex. %rediseco\_bal\_formatted\_short\_vault%)

### Message placeholders

Inside `lang.yml` you may set <mark style="color:orange;">`%balance_short%`</mark> instead of <mark style="color:orange;">`%balance%`</mark> to have the amount formatted and shortened. This is `balance`, `balanceOther and` `balanceTopFormat`

### Advanced placeholders

* <mark style="color:orange;">`%rediseco_bal_decformat<decimal-format>_<currency>%`</mark>\
  Shows your balance based on a [DecimalFormat](https://www.baeldung.com/java-decimalformat) (ex. %rediseco\_bal\_decformat\_#.#0\_vault% will show 6.5323555 as 6.50)
* <mark style="color:orange;">`%rediseco_totsupply_<currency>%`</mark>\
  All the circulating money of this currency (you can use `_formatted` and `_short` parameters)
* <mark style="color:orange;">`%rediseco_top_1_bal_<short/formatted>_<currency>%`</mark>\
  Displays the player balance at position 1 ("1" is the rank. you can put whatever you want)
* <mark style="color:orange;">`%rediseco_top_1_name_<short/formatted>_<currency>%`</mark>\
  Displays the player name at position 1 ("1" is the rank. you can put whatever you want)
* <mark style="color:orange;">`%rediseco_top_1_playerprefix_<currency>%`</mark>\
  Displays the vault prefix of the player at position 1 ("1" is the rank. you can put whatever you want)
* <mark style="color:orange;">`%rediseco_top_1_playersuffix_<currency>%`</mark>\
  Displays the vault suffix of the player at position 1 ("1" is the rank. you can put whatever you want)
* <mark style="color:orange;">`%rediseco_top_position_<currency>%`</mark>\
  Shows in which position the player is in the baltop
* <mark style="color:orange;">`%rediseco_maxbal_<currency>%`</mark>\
  Shows the current max balance for the currency specified

### Format tags

* `formatted` - Adds the currency symbol at the end of the amount
* `short` - Appends amount suffixes at the end of the amount\
  (ex: 10k, 40M are 10 thousands and 40 Millions)
* `decformat` - Use this if you want a custom format based on [DecimalFormat](https://www.baeldung.com/java-decimalformat)\
  Example: if you want `197.311` to appear as `197.30` you must use `#.#0` as this: `%rediseco_bal_decformat#.#0_vault%`

**You can use multiple tags inside a placeholder!!**\
<mark style="color:orange;">`%rediseco_bal_formatted_short_<currency>%`</mark> will return 1.52k€ for example
