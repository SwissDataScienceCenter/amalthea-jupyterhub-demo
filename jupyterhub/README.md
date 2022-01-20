# Deploy commands

```
helm repo add jupyterhub https://jupyterhub.github.io/helm-chart/
helm repo update
```

```
helm upgrade --install amaltheademo-jupyterhub jupyterhub/jupyterhub --namespace amaltheademo --version=1.2.0 --values values.yaml
```

# Useful Links

https://jupyterhub.readthedocs.io/en/stable/reference/services.html#implementing-your-own-authentication-with-jupyterhub
https://github.com/jupyterhub/jupyterhub/tree/HEAD/examples/service-fastapi
https://github.com/jupyterhub/zero-to-jupyterhub-k8s