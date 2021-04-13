# Kustomization for Deploying Migration Toolkit for Containers on OpenShift 4

This kustomization makes use of the [Crane Operator](https://github.com/konveyor/mig-operator) to deploy Migration Toolkit for Containers on OpenShift 4.

The documentation for the Migration Toolkit for Containers (MTC) can be found [here](https://docs.openshift.com/container-platform/4.7/migration/migrating_4_1_4/migrating-application-workloads-4-1-4.html).

Migration toolkit leverages [OpenShift Velero Plugin](https://github.com/konveyor/openshift-velero-plugin).

Related docs:

* https://github.com/konveyor/mig-operator/tree/master/docs/usage
* https://github.com/konveyor/mig-controller/tree/master/docs/scenarios
* https://github.com/konveyor/velero/tree/konveyor-dev/design

## Installing

The commands in this section must be issued by an OpenShift user with a *cluster-admin* role.

### Installing MTC operator

```
$ oc apply --kustomize mtc-operator/base
```

### Creating MTC instance

To deploy a MTC instance, issue the command:

```
$ oc apply --kustomize mtc-instance/base
```
