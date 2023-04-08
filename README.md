# helm-charts

This is a personal repository for managing and building helm charts.  These charts are often experimental. YMMV

## Usage

Add charts to the helm cli

```sh
helm repo add codekow https://codekow.github.io/helm-charts
```

Add charts to openshift Developer Catalog

```sh
oc apply -f https://raw.githubusercontent.com/codekow/helm-charts/main/openshift/helm-codekow-repo.yaml
```

To include a chart from this repository in an umbrella chart, include it in your dependencies in your `Chart.yaml` file.

```yaml
apiVersion: v2
name: hello-openshift
description: A helm chart for the hello-openshift image
type: application

version: 0.0.1

appVersion: "1.2.0"

dependencies:
  - name: "hello-openshift"
    version: "0.0.1"
    repository: "https://codekow.github.io/helm-charts"
```

## Links

For additional charts, please also refer to the following:

- [OpenShift Helm Charts (Default Repo)](https://github.com/openshift-helm-charts/charts)
- [Red Hat Intelligent Application Practice Helm Charts](https://github.com/rh-intelligent-application-practice/helm-charts)
- [Red Hat Community of Practice Helm Charts](https://github.com/redhat-cop/helm-charts)
- [OpenShift Management Helm Charts](https://github.com/redhat-cop/openshift-management)

### Other Resources

- [template2helm](https://github.com/redhat-cop/template2helm) - Convert OpenShift Templates to Helm Charts
