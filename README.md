[![Mega-Linter](https://github.com/ronj/docker-infra/workflows/Mega-Linter/badge.svg?branch=master)](https://github.com/ronj/docker-infra/actions?query=workflow%3AMega-Linter+branch%3Amaster)

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

