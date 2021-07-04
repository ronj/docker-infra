# docker-infra

## Deploy

`
docker stack deploy -c infra-network.yml infra-network
ACME_EMAIL=admin@domain.tld DOMAIN=domain.tld docker stack deploy --with-registry-auth -c infra-applications.yml infra-applications
`

