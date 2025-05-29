# glueops-grafana-dashboards

![Version: 0.13.2-rc59](https://img.shields.io/badge/Version-0.13.2--rc59-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 0.1.0](https://img.shields.io/badge/AppVersion-0.1.0-informational?style=flat-square)

This is a Helm chart for deploying Grafana dashboards for the GlueOps Platform.

## Handling Variables in Helm Templates

When using Helm templates with Grafana JSON configurations, you need to explicitly escape variables like `{{var}}` to work correctly with Helm's templating system.

### Example

**Original (not working):**

```
{{kubernetes_pod_name}}
```

**Correct (working):**

```
{{`{{kubernetes_pod_name}}`}}
```

The backticks around the variable ensure that Helm interprets the template correctly without prematurely evaluating the variable.

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| captain_domain | string | `"nonprod.gliese667cc.onglueops.rocks"` |  |
