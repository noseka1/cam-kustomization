# Kustomization for Deploying Cluster Application Migration on OpenShift 4

This kustomization makes use of the [OpenShift Migration Operator](https://github.com/konveyor/mig-operator) to deploy CAM tool on OpenShift 4.

The documentation for the Cluster Application Migration tool can be found [here](https://docs.openshift.com/container-platform/latest/migration/migrating_3_4/about-migration.html).

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
