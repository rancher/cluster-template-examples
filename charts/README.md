# rke2 cluster template

Helm chart that can be used as rke2 cluster template

### how to use

```bash
# generate random id to build multiple clusters for testing
export INSTANCE_PREFIX=rke2-vsphere-helm-demo-${RANDOM}

helm upgrade --install ${INSTANCE_PREFIX} ./charts \
  --namespace fleet-default \
  --values ./charts/values-vsphere.yaml \
  --set cluster.name=${INSTANCE_PREFIX} \
  --set nodepools[0].name=${INSTANCE_PREFIX}-nodepool \
  --set nodepools[0].quantity=1 
  # --debug --dry-run
```

General cluster options are available through [values.yaml](./values.yaml)

For different cloud provider drivers:

[Amazonec2](./values-aws.yaml)

[Vsphere](./values-vsphere.yaml)

[Digitalocean](./values-do.yaml)

[Azure](./values-azure.yaml)