# Demo of Amalthea with Different Identity Providers

## Install Renku
```
helm repo add renku https://swissdatasciencecenter.github.io/helm-charts/
helm upgrade --install --namespace amaltheademo amaltheademo renku/amalthea -f values.yaml
```

## Create the Secrets Used in the Examples

There are two secrets, one each for the Github and Gitlab exaples.
Once you register an application to be used with Oauth in Gitlab and/or
Github then save the credentials in a secret like below. The secrets
are then referecened in the manifests for the examples.

```yaml
apiVersion: v1
stringData:
  clientId: XXXXXX
  clientSecret: XXXXXX
kind: Secret
metadata:
  name: github-oauth-secret
  namespace: amaltheademo
type: Opaque
```

```yaml
apiVersion: v1
stringData:
  clientId: XXXXXX
  clientSecret: XXXXXX
kind: Secret
metadata:
  name: gitlab-oauth-secret
  namespace: amaltheademo
type: Opaque
```

## Using Gitlab OIDC
```
kubectl -n amaltheademo apply -f example-gitlab.yaml
```

## Using Github Oauth
```
kubectl -n amaltheademo apply -f example-github.yaml
```

