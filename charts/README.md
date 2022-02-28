# rke2 cluster template

Helm chart that can be used as rke2 cluster template

### how to use

```bash
helm install --namespace fleet-default --value ./your-values.yaml my-cluster ./charts
```

General cluster options are available through [values.yaml](./values.yaml)

For different cloud provider drivers:

[Amazonec2](./values-aws.yaml)

[Vsphere](./values-vsphere.yaml)

[Digitalocean](./values-do.yaml)

[Harvester](./values-harvester.yaml)

[Azure](./values-azure.yaml)
