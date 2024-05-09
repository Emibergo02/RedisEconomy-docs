# 📩 Installation

### Steps to install

1. Download the jar from SpigotMC and put it into your server's plugins folder
2. Start the server
3. Set up your Redis credentials inside config.yml [(How to install Redis)](https://github.com/Emibergo02/RedisEconomy/wiki/Install-redis)

{% code title="config.yml" %}
```yaml
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
```
{% endcode %}

### Migration (Optional)

{% code title="config.yml" %}
```yaml
migration-enabled: true #Set this to true
```
{% endcode %}

After you set it to true, restart the server

Keep in mind that **Vault economy is disabled during migration**. You'll need to restart

Migrate to one server only. **Shut down any other instance of RedisEconomy during migration**
