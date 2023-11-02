## openjdk

[![CI](https://github.com/Oefenweb/ansible-openjdk/workflows/CI/badge.svg)](https://github.com/Oefenweb/ansible-openjdk/actions?query=workflow%3ACI)
[![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-oracle--java-blue.svg)](https://galaxy.ansible.com/Oefenweb/openjdk)

Set up (the default or a specific update version of) openjdk Debian-like systems.

#### Requirements

None

#### Variables

* `openjdk_versions`: [default: `[{version: 'default', set_as_default: true}]`]: Oracle java version(s) to install
* `openjdk_versions.{n}.version`: [required]: Version to install (`8`, `9`, `default`)
* `openjdk_versions.{n}.set_as_default`: [default: `false`]: Whether or not to set as default (does not work for `version` `default`)

#### Dependencies

None

#### Example(s)

##### Simple

```yaml
---
- hosts: all
  roles:
    - oefenweb.openjdk
```

##### Advanced

```yaml
---
- hosts: all
  roles:
    - oefenweb.openjdk
  vars:
    openjdk_versions:
      - version: 8
      - version: 9
        set_as_default: true
```

#### License

MIT

#### Author Information

Mischa ter Smitten

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-openjdk/issues)!
