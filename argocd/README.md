- https://github.com/hoalongnatsu/argocd

- Install ArgoCD:
```
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

- Uninstall ArgoCD:
```
kubectl delete -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

- Get password:
```
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d ; echo
```

- Access
```
kubectl port-forward svc/argocd-server -n argocd 8000:443
```

```
kubectl get pod -n argocd
```

- Login
https://localhost:8000/
admin / ESqCNQKjOrqW5jFN
