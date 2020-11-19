OpenJDK from PPA
================

[![Travis](https://img.shields.io/travis/honatas/ansible-role-openjdk-ppa?style=plastic)](https://travis-ci.org/Honatas/ansible-role-openjdk-ppa "View the build status on Travis")
[![coffee](https://img.shields.io/badge/buy%20me%20a-coffee-orange?style=plastic)](https://ko-fi.com/honatas "Buy me a coffee")  

Installs any version of OpenJDK from Matthias Klose's openjdk-r PPA repository

Role Variables
--------------

**openjdk_version** - The version of the jdk (default: 14)  
**openjdk_types** - A list of different installs (default: - jdk-headless)

Examples
--------

The default installs openjdk-14-jdk-headless:
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
