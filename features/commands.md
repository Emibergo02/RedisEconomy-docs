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

# ▶️ Player commands

### <mark style="color:orange;">`/balance`</mark>

Permission: `rediseconomy.balance`\
Displays your balance (vault/default currency)\
Aliases: <mark style="color:orange;">`/money`</mark>

### <mark style="color:orange;">`/balance <player> [currencyName]`</mark>

Permission: <mark style="color:yellow;">`rediseconomy.balance.[currencyName]`</mark>\
Displays \<player>'s balance\
CurrencyName is the name of the currency to be displayed

### <mark style="color:orange;">`/pay <player> <amount> [currencyName]`</mark>

Permission: <mark style="color:yellow;">`rediseconomy.pay`</mark>\
Simple pay command but you can specify the currency

### <mark style="color:orange;">`/pay * <amount> [currencyName]`</mark>

Permission: <mark style="color:yellow;">`rediseconomy.payall`</mark>\
Pay all players in your server \<amount> money

### <mark style="color:orange;">`/balancetop <page> [currencyName]`</mark>

Permission: <mark style="color:yellow;">`rediseconomy.balancetop`</mark>\
Displays the top richest accounts (with vault/default currency)\
Aliases: <mark style="color:orange;">`/baltop`</mark>

### <mark style="color:orange;">`/toggle-payments <player or * or all>`</mark>

Permission: <mark style="color:yellow;">`rediseconomy.toggle-payments`</mark>\
Blocks payments incoming from \<player>

### <mark style="color:orange;">`/toggle-payments`</mark>

Shows blocked accounts list\
Permission: <mark style="color:orange;">`rediseconomy.toggle-payments`</mark>
