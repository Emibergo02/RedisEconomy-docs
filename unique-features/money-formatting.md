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

# 🗳️ Money formatting

## 1 Amount formatting

### 1.1 Order of magnitude symbols

You can use suffixes after the amount to specify if you want the amount to be parsed as thousands, millions, trillions or quadrillions. \
By default it is:\
&#x20;   \- `k` for thousands\
&#x20;   \- `m` for millions\
&#x20;   \- `b` for billions\
&#x20;   \- `t` for trillions\
&#x20;   \- `q` for quadrillions

So 10k will be 10000 and 0.1m will be 100000

### 1.2 Percentage formatting

You can also use `%` symbol to send money based on your total balance or based on the balance of the recipient

Examples:\
`/pay <target> 10%` will send 10% of your total balance to \<target> player\
`/balance <target> vault give 10%` will give \<target> 10% of his current balance

## 2 DecimalFormatting

This is for displaying decimal numbers on balances or payments

As you can see inside [currency-settings.md](multiple-currencies-with-offline-payments/currency-settings.md "mention") section there is a default [DecimalFormat ](https://www.baeldung.com/java-decimalformat)for every currency

Inside [placeholders.md](../features/placeholders.md "mention") section is explained how to use [DecimalFormat ](https://www.baeldung.com/java-decimalformat)to have a custom output with placeholders
