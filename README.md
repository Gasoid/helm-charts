# Merge-bot helm charts

![Version: 1.6.0](https://img.shields.io/badge/Version-1.6.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 3.5.0](https://img.shields.io/badge/AppVersion-3.5.0-informational?style=flat-square)

## Usage

[Helm](https://helm.sh) must be installed to use the charts.  Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

To install the merge-bot chart:

```bash
helm install --repo https://gasoid.github.io/helm-charts my-merge-bot merge-bot
```

To uninstall the chart:

```bash
helm uninstall my-merge-bot
```

## Variables

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| mergebot.tlsEnabled | bool | `false` | whether tls is enabled, certificate will be issued by letsencrypt you have to provide tlsDomain  |
| mergebot.tlsDomain | string | `""` | if tlsEnabled is true, you have to set tlsDomain |
| mergebot.gitlabToken | string | `""` | gitlab token |
| mergebot.gitlabURL | string | `""` | gitlab url in case it is not gitlab cloud |
| mergebot.gitlabMaxRepoSize | string | `"500Mb"` | max repo size for !update, !merge command |
| mergebot.gitlabSecret.enabled | bool | `false` | whether to use secret, it must contain gitlab-token secret. |
| mergebot.gitlabSecret.name | string | `"merge-bot"` | secret name k8s secret where gitlab token is stored, gitlabToken will be ignored, secret example: data:   gitlab-token: "secret" |
| mergebot.sentryEnabled | bool | `true` | sentry |
| mergebot.debug | bool | `false` | debug mode |
| metrics | object | `{"enabled":true}` | whether prometheus metrics are exposed port is 8081, port name is metrics |
