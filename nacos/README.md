# Run nacos on Apple M1

## Quick start

```shell
# Install operator directly using helm
$ helm install nacos-operator ./nacos-operator
```

## Start single instance, standalone mode

```shell
$ cat config/samples/nacos.yaml
apiVersion: nacos.io/v1alpha1
kind: Nacos
metadata:
  name: nacos
spec:
  type: standalone
  image: nacos/nacos-server:v2.3.1-slim
  replicas: 1
```

```shell
# Install demo standalone mode
$ kubectl apply -f config/samples/nacos.yaml
```
