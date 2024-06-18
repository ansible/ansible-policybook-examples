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

```bash
$ ansible-policy -p examples/check_project/k8s.yml --policy-dir ansible-policybook-examples/policy/infra/k8s/
TASK [Create a k8s namespace] examples/check_project/k8s.yml L2-8 ****************************************************************
... check_module_arguments_to_only_use_kubeconfig Not Validated
    use kubeconfig
```
