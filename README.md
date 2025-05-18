# Helm charts

## Usage

[Helm](https://helm.sh) must be installed to use the charts.  Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

```bash
helm repo add merge-bot https://gasoid.github.io/helm-charts
```

If you had already added this repo earlier, run `helm repo update` to retrieve
the latest versions of the packages.  You can then run `helm search repo merge-bot` to see the charts.

To install the merge-bot chart:

```bash
helm install my-merge-bot merge-bot/merge-bot
```

To uninstall the chart:

```bash
helm uninstall my-merge-bot
```
