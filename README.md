# Ansible Automation Platform - OpenShift Virtualization Inventory Source

You can use OCP-V as an inventory source for AAP.

You need:

- a custom execution environment with the openshift_virtualization collection
- a custom credential
- at the minium, the API and TOKEN to connect to OCP

AAP Custom credential:

Injector:

```
fields:
  - id: K8S_AUTH_HOST
    type: string
    label: API endpoint
    secret: true
  - id: K8S_AUTH_API_KEY
    type: string
    label: token
    secret: true
required:
  - K8S_AUTH_HOST
  - K8S_AUTH_API_KEY
```

Input:

```
env:
  K8S_AUTH_HOST: '{{ K8S_AUTH_HOST }}'
  K8S_AUTH_API_KEY: '{{ K8S_AUTH_API_KEY }}'
```

Create a project in AAP.

Point to this repository.

Create your custom credential.

Create an inventory.

Add a source.

Point to your new project, choose your custom execution environment that contains the openshift_virtualization collection.

Sync.
