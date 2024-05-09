---
description: It is already documented on the config.yml
---

# 📄 Configuration

```yaml
# This is automatically generated on server startup (random UUID)
# YOU MUST HAVE A DIFFERENT serverId FOR EVERY RedisEconomy instance
serverId: 7e718dec-6b0f-4c01-8183-bceca638951b
# Language file
lang: en-US
# Webeditor URL
webEditorUrl: https://webui.advntr.dev/
# Leave password or user empty if you don't have a password or user
# Don't use the default credentials in production!! Generate new credentials on RedisLabs -> https://github.com/Emibergo02/RedisEconomy/wiki/Install-redis
# Default credentials lead to a non-persistent redis server, only for testing!!
redis:
  host: localhost
  port: 6379
  user: ''
  password: ''
  database: 0
  timeout: 2000
  clientName: RedisEconomy

# If true, the plugin registers who's calling it's methods inside transactions
registerCalls: false
# if true, migrates the bukkit offline uuids accounts to the default RedisEconomy currency
# During the migration, the plugin will be disabled. Restart all RedisEconomy instances after the migration.
migrationEnabled: false
# All RedisEconomy instances with the same cluster id will share the same data
clusterId: ''
# How many chars are needed for a command autocompletion
# Increase if you have a lot of players to list 
# so that your bandwidth wouldn't be saturated of usernames
tab_complete_chars: 0
# Default currency name (must be the same as the currency name in the currencies list)
defaultCurrencyName: vault
# Cooldown between payments in milliseconds
payCooldown: 500
# Minimum amount of money that can be paid
minPayAmount: 0.01
# Currencies
# payTax is the tax on payments, 0.1 = 10% tax
currencies:
- currencyName: vault
  currencySingle: euro
  currencyPlural: euros
  decimalFormat: '#.##'
  languageTag: en-US
  startingBalance: 0.0
  payTax: 0.0
  bankEnabled: true
  taxOnlyPay: false
- currencyName: dollar
  currencySingle: $
  currencyPlural: $
  decimalFormat: '#.##'
  languageTag: en-US
  startingBalance: 0.0
  payTax: 0.0
  bankEnabled: false
  taxOnlyPay: false

# Authors: Unnm3d

```

