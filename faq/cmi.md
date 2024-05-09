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

# ⁉️ CMI

### If you use CMI, you have to make the following changes in the CMI config:

### 1

config.yml:\
(change to the following values)

```yaml
Economy:
Enabled: false
```

### 2

settings/alias.yml\
(change to the following values)

```yaml
# /cmi pay $1-
/pay: 
   Enabled: false 
# /cmi money $1-
 /money: 
    Enabled: false
  # /cmi balance $1-
  /balance:
    Enabled: false
  /bal:
    Enabled: false
  # /cmi baltop $1-
  /baltop:
    Enabled: false
```
