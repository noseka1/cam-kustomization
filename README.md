# Kustomization for Deploying Cluster Application Migration on OpenShift 4

This kustomization makes use of [ocs-operator](https://github.com/openshift/ocs-operator) to deploy OpenShift Container Storage.

Red Hat OpenShift Container Storage product documentation can be found [here](https://access.redhat.com/documentation/en-us/red_hat_openshift_container_storage).

## Installing Cluster Application Migration

The commands in this section must be issued by an OpenShift user with a *cluster-admin* role.

### Installing cam-operator

```
$ oc apply --kustomize cam-operator/base
```

### Creating CAM instance

To deploy a CAM instance, issue the command:

```
$ oc apply --kustomize cam-instance/base
```
