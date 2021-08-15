# Istio demo
- My blog: [Service Mesh](https://viblo.asia/p/tim-hieu-ve-service-mesh-phan-tiep-theo-ORNZqnJrl0n)
## How to setup
- Install [Istio](https://istio.io/latest/docs/setup/install/)
```yaml
$ istioctl install
```
- Inject proxy

```shell
$ kubectl label namespace default istio-injection=enabled
```

- Install app
```shell
$ kubectl apply -f kubernetes-manifests.yaml
```

- Install Istio addons

```shell
$ kubectl apply -f ./addons
```

- Use Kiali
```shell
$ kubectl port-forward svc/kiali -n istio-system 20001
```

- Use Jaeger
```shell
$ istioctl dashboard jaeger
```
