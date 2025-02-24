

# Iniciar

Para iniciar o cluster flux

```shell
flux bootstrap github \
 --token-auth \
 --owner=Matheus-de-Souza \
 --repository=fluxcd-test \
 --branch=master \
 --path=clusters/flux-test \
 --personal
```

Para adicionar os secrets do ecr-registry

```
kubectl create secret generic ecr-registry-helper-secrets \
  --from-literal=AWS_ACCESS_KEY_ID=$AWS_ACCESS_KEY_ID \
  --from-literal=AWS_SECRET_ACCESS_KEY=$AWS_SECRET_ACCESS_KEY \
  --from-literal=AWS_REGION=$AWS_REGION \
  --from-literal=AWS_ACCOUNT=$AWS_ACCOUNT
```

Para setar variáveis de ambiente

`export $(cat .env | xargs)`



