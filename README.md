# helm-chart
Registfy's helm chart template

A Templated Helm chart that can be consumed within any other Microservice Deployment with applying Kubernetes best practices

The purpose of this repository is to provide a place for maintaining and contributing Registfy Charts, with CI processes in place for managing the releasing of Charts into the repository.

## How Do I Enable the Repository for Helm ?
- To add the Helm Charts for your client, you will need a <access_token> :
```
helm repo add --username <username> --password <access_token> project-1 https://gitlab.com/api/v4/projects/35915648/packages/helm/stable

helm dependency update .
```

- Syntax testing and Dry run:

```
helm template . | kubectl apply --dry-run -f -
```
- Packaging and Pushing the helm release tgz file:

```
helm package .
helm cm-push ./service-${RELEASE_VERSION}.tgz helm-chart
```

new readme file

# helm-chart
Registfy's Helm chart template

A templated Helm chart that can be consumed within any other microservice deployment while applying Kubernetes best practices.

The purpose of this repository is to provide a place for maintaining and contributing Registfy Charts, with CI processes in place for managing the release of charts into the repository.

## How Do I Enable the Repository for Helm?
- To add the Helm charts for your client, use the following command:
```bash

helm repo add helm-chart https://raw.githubusercontent.com/registfyrepos/helm-chart/main/charts/
helm dependency update .
