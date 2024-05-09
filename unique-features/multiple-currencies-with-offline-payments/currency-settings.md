---
description: Explanation on how to configure currencies
---

# Currency settings

{% code title="config.yml" %}
```yaml
# Default currency name (must be the same as the currency name in the currencies list)
defaultCurrencyName: vault
# Currencies
# payTax is the tax on payments, 0.1 = 10% tax
currencies:
- currencyName: vault
  currencySingle: euro
  currencyPlural: euros
  decimalFormat: '#.##'
  languageTag: en-US  #Some countries use "." instead of "," and vice-versa
  startingBalance: 0.0
  payTax: 0.0
  bankEnabled: true
  taxOnlyPay: false
```
{% endcode %}

**CurrencySingle and CurrencyPlural** are tags appended at the end of an amount\
For example, 1€ will be displayed `1euro` and 2€ will be displayed as `2euros`

**decimalFormat** is how the amount is formatted based on [DecimalFormat](https://www.baeldung.com/java-decimalformat) formatting

**payTax** is the relative percentage to charge on every transaction

`10%` tax rate will be `0.1` . So if you put `1.0` as payTax the player will be taxed `100%` of the amount transferred!!!

**bankEnabled** for Developers: enables the bank feature of [Vault's Economy class](https://github.com/MilkBowl/VaultAPI/blob/8bad2c479f531436b4b0694f5696b501d0afef3e/src/main/java/net/milkbowl/vault/economy/Economy.java#L45)

**taxOnlyPay** enable if you want `payTax` to be applied only to the pay command or on both pay and balance command
