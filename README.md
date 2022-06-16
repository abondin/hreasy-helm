# hreasy-helm

Helm 3 charts to deploy HR Easy in Kubernetes Cluster

## Preconditions

1) Add repo for postgresql
```
helm repo add bitnami https://charts.bitnami.com/bitnami
```

## Install HR Easy for new organization or update version of existing installation
```
export DOMAIN=stm
export HREASY_VERSION=latest
export NAMESPACE=${DOMAIN}
export RELEASE_NAME=hreasy-${NAMESPACE}

helm upgrade -i --namespace ${NAMESPACE} \
	--create-namespace \
	--atomic \
	--timeout "500s" \
	--wait \
	--values values.yaml \
	$RELEASE_NAME \
	./
```

## PostgreSQL

HR Easy uses charts provided by bitnami https://artifacthub.io/packages/helm/bitnami/postgresql


## HR Easy Platform

//TODO

## HR Easy Web