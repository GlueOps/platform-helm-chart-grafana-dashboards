# platform-helm-chart-grafana-dashboards

## Notes

Given how Helm template works whenever you have a `{{var}}` in your grafana json you need to change it so that it's excplitity escaped with a backtick `. Below is an example:

```yaml
ORIGINAL:
{{kubernetes_pod_name}}

WORKING:
{{`{{kubernetes_pod_name}}`}}
```
