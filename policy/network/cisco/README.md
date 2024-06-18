Here is a sample playbook, let's call it "cisco_ios.yml", which can be used to demonstrate policy checks:

```bash
---
- name: Configure Cisco IOS
  cisco.ios.ios_config:
    lines:
      - hostname foobar
      - line vty 0
      - password password123
      - no login
      - set ntp server 127.0.0.1
```
