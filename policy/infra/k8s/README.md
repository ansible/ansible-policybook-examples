Here is a sample playbook, let's call it "k8s.yml" which can be used to demonstrate policy rules:

```bash
---
- name: Create a k8s namespace
  kubernetes.core.k8s:
    name: testing
    api_version: v1
    kind: Namespace
    state: present
```

