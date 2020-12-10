OpenJDK from PPA
================

[![GitHub](https://img.shields.io/github/license/honatas/ansible-role-openjdk-ppa?style=plastic)](https://github.com/Honatas/ansible-role-openjdk-ppa/blob/master/LICENSE)
[![Travis](https://img.shields.io/travis/honatas/ansible-role-openjdk-ppa?style=plastic)](https://travis-ci.org/Honatas/ansible-role-openjdk-ppa "View the build status on Travis")
[![Ansible Quality Score](https://img.shields.io/ansible/quality/48203?style=plastic)](https://galaxy.ansible.com/honatas/openjdk_ppa)
[![coffee](https://img.shields.io/badge/buy%20me%20a-coffee-brown?style=plastic)](https://ko-fi.com/honatas "Buy me a coffee")  

Installs any version of OpenJDK from Matthias Klose's [openjdk-r PPA repository](https://launchpad.net/~openjdk-r/+archive/ubuntu/ppa)  

Role Variables
--------------

**openjdk_version** - The version of the jdk (default: 15)  
**openjdk_types** - A list of different installs (default: - jdk-headless)

Examples
--------

The default installs openjdk-15-jdk-headless:
```yaml
roles:
  - honatas.openjdk_ppa
```

If you want to install Java 8 (openjdk-8-jdk-headless):
```yaml
roles:
  - { role: honatas.openjdk_ppa, openjdk_version: 8 }
```

If you want a full Java 11 development environment (this will install openjdk-11-jdk, openjdk-11-doc, openjdk-11-source, openjdk-11-demo)
```yaml
roles:
  - role: honatas.openjdk_ppa
    openjdk_version: 11
    openjdk_types:
      - jdk
      - doc
      - source
      - demo
```


Requirements
------------

None

Dependencies
------------

None

License
-------

MIT


Contributions
-------------

Feel free to open an issue or add a pull request. Anytime. Really, I mean it.  

Also, if you like my work, I'll let you know that I love [coffee](https://ko-fi.com/honatas).  
