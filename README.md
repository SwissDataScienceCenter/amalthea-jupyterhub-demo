# Demo of Amalthea with Different Identity Providers

## Install Renku
```
helm repo add renku https://swissdatasciencecenter.github.io/helm-charts/
helm upgrade --install --namespace amaltheademo amaltheademo renku/amalthea -f values.yaml
```

## Using Gitlab OIDC
```
kubectl -n amaltheademo apply -f example-gitlab.yaml
```

## Using Github Oauth
```
kubectl -n amaltheademo apply -f example-github.yaml
```

