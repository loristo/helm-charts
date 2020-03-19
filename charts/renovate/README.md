renovate
========
Universal dependency update tool that fits into your workflows.

Current chart version is `19.175.1`

Source code can be found [here](https://github.com/renovatebot/renovate)

## Installation

### Add Helm repository

```shell
helm repo add renovate https://renovatebot.github.io/helm-charts/
helm repo update
```

## Install Renovate chart

```bash
helm install --generate-name --set renovate.config='module.exports={...}' renovate/renovate
```

**NOTE**: `renovate.config` must be a valid Renovate [self-hosted configuration](https://docs.renovatebot.com/self-hosted-configuration/)

## Configuration

The following table lists the configurable parameters of the chart and the default values.

## Chart Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| cronjob.annotations | object | `{}` |  |
| cronjob.concurrencyPolicy | string | `""` |  |
| cronjob.failedJobsHistoryLimit | string | `""` |  |
| cronjob.jobRestartPolicy | string | `"Never"` |  |
| cronjob.labels | object | `{}` |  |
| cronjob.schedule | string | `"0 1 * * *"` |  |
| cronjob.successfulJobsHistoryLimit | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"renovate/renovate"` |  |
| image.tag | string | `"19.160.2"` |  |
| pod.annotations | object | `{}` |  |
| pod.labels | object | `{}` |  |
| renovate.config | string | `""` |  |
| resources | object | `{}` |  |