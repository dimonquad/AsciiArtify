# Create cluster
```
k3d cluster create argo
```
# Create namespace
```
kubectl create namespace argocd
```

# Install argoCD
```
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

# Check that everything is ok
```
kubectl get all -n argocd
```
<img width="953" height="306" alt="image" src="https://github.com/user-attachments/assets/b9aff254-33e3-4a68-ab54-adef071c21bd" />

# making port forwarding
```
kubectl port-forward svc/argocd-server -n argocd 8080:443
```

# How to get creds for first login in ArgoCD
```
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | ForEach-Object { [System.Text.Encoding]::UTF8.GetString([System.Convert]::FromBase64String($_)) }
```

# Use login as "admin" and retrived pass from previous step

# Adding new users
Refer to documentation for adding users: https://argo-cd.readthedocs.io/en/stable/operator-manual/user-management/

#Final screenshot after successful deployment
<img width="1905" height="663" alt="image" src="https://github.com/user-attachments/assets/1291815c-9c7f-41aa-afd4-0665aebaf6cb" />

