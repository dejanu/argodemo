# argodemo

* Install argo:

```bash
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml

# port forward
kubectl port-forward svc/argocd-server -n argocd 8080:443

# get secret
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d
```

* CLI:

```bash
brew install argocd
argocd login 127.0.0.1:8080
```
