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

# Introduction

RedisEconomy is an affordable cross-server plugin for real-time management and synchronization of your in-game money across multiple servers

The plugin is also proxy-less, meaning it **doesn't require any additional proxy plugins!!**\


&#x20;Unlike some data bridges, the data storage is Redis instead of a slow MySQL\
&#x20;More information [here (Benchmarks)](https://docs.google.com/spreadsheets/d/1f4gG-muUXa\_wYlLxlLMRUk4cRT8UQCfLxoGgza-Mv-k)

RedisEconomy takes advantage of a particular data structure of Redis called [SortedSet](https://redis.io/glossary/redis-sorted-sets/)\
Since MySQL doesn't have this kind of data structure, a SQL database would be many times slower than a Redis NoSQL database
