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
  languageTag: en-US
  startingBalance: 0.0
  maxBalance: 1.0E14
  payTax: 0.0
  saveTransactions: true
  transactionsTTL: 0
  bankEnabled: true
  taxOnlyPay: false
  executorThreads: 3
```
{% endcode %}

* **CurrencySingle and CurrencyPlural**: Tags used to display currency amounts. For example, `1€` is shown as `1euro`, and `2€` as `2euros`.
* **decimalFormat**: Specifies the format of the amount based on DecimalFormat patterns.
* **payTax**: The tax rate applied to transactions. A `10%` tax rate is represented as `0.1`. Setting `1.0` results in a `100%` tax.
* **bankEnabled**: Enables the bank feature in Vault's Economy class for developers.
* **taxOnlyPay**: If enabled, `payTax` applies only to the pay command; otherwise, it applies to both pay and balance commands.
* **saveTransaction**: When enabled, transactions are recorded for every money movement.
* **transactionTTL**: The time, in seconds, after which a transaction is removed from the system to keep the transaction database manageable.
* **executorThreads**: The number of threads allocated to make balance modification (every account has a dedicated thread based on it's ID to keep thread-safety over balances)
