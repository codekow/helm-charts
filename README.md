# helm-charts

This is a personal repository for managing and building helm charts.  These charts are often experimental.  For additional charts, please also refer to the [Red Hat Intelligent Application Practice Helm Charts](https://github.com/rh-intelligent-application-practice/helm-charts) repo.

## Usage

To access charts from this from the cli repository add it:

```sh
helm repo add codekow https://codekow.github.io/helm-charts
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
