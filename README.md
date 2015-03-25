ansible-newrelic for Debian/Ubuntu
============

Ansible role for installing New Relic on your Debian/Ubuntu system.

## Overwrite Default Variables

The `vars/main.yml` file should contain your list of packages you want to install in order to override defaults found in `defaults/main.yml`.

```yml
---
newrelic_install: true
newrelic_config:
  key: "REPLACE_WITH_REAL_KEY"
  app_name: "REPLACE_WITH_REAL_NAME"
  sysmond_key: "REPLACE_WITH_REAL_KEY"

newrelic_packages:
  - newrelic-sysmond
  - newrelic-php5
```

Additionally, you can overwrite the variables as part of your playbook.

```yml
---
...
  vars:
    newrelic_install: true
    newrelic_config:
      key: "REPLACE_WITH_REAL_KEY"
      app_name: "REPLACE_WITH_REAL_NAME"
      sysmond_key: "REPLACE_WITH_REAL_KEY"

    newrelic_packages:
      - newrelic-sysmond
      - newrelic-php5
...
```
