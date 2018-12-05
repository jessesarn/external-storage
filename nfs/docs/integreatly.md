The process for installing the nfs-provisioner on an Integreatly cluster follows the same basic steps described in the Quickstart.  However, the files under deploy/integreatly should be used instead of the files under deploy/kuberentes.  The files there can be used as-is without any modifications.  Therefore installation on an Integreatly cluster is simply:
```
oc project openshift-infra
oc create -f deploy/integreatly/scc.yaml
oc create -f deploy/integreatly/rbac.yaml
oc create -f deploy/integreatly/statefulset.yaml
oc create -f deploy/integreatly/class.yaml
oc create -f deploy/integreatly/exportpvc.yaml
```

