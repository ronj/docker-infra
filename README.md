# docker-infra

## Preparation

```
mkdir infra/data
touch infra/data/acme.json
chmod 600 infra/data/acme.json
```

## Deploy

```
docker stack deploy -c infa/infra-network.yml infra-network
ACME_EMAIL=admin@domain.tld DOMAIN=domain.tld docker stack deploy --with-registry-auth -c infra/infra-applications.yml infra-applications
```

