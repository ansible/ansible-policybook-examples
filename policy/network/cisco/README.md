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

```bash
$ ansible-policy -p examples/check_project/cisco_ios.yml --policy-dir ansible-policybook-examples/policy/network/cisco/
TASK [Configure Cisco IOS] examples/check_project/cisco_ios.yml L2-10 ************************************************************
... Check_on_IOS_configuration Not Validated
    WARNING: Cisco IOS settings violation

--------------------------------------------------------------------------------------------------------------------------------------------
SUMMARY
... Total files: 1, Validated: 0, Not Validated: 1

Violations are detected! in 1 task
```
