
```yaml
kind: GitRepo
apiVersion: fleet.cattle.io/v1alpha1
metadata:
  name: test-istio
  namespace: fleet-default
spec:
  repo: https://github.com/jiaqiluo/fleet-examples
  branch: istio-app
  bundleDirs:
  - test-istio
  targets:
  - name: dev
    clusterSelector:
      matchLabels:
        env: dev

  - name: test
    clusterSelector:
      matchLabels:
        env: test

  - name: prod
    clusterSelector:
      matchLabels:
        env: prod
```
