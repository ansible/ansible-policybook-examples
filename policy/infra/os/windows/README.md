Policybooks related to Windows OS tasks. 

You can use something like this windows.yml playbook to test:
```bash
---
- name: Run some Windows automation
  hosts: localhost
  gather_facts: false
  vars:
    win: dows

  tasks:
  - name: Add local user account
    ansible.windows.win_user:
      name: bob
      password: B0bP4ssw0rd
      state: present
      groups:
        - Users
```
