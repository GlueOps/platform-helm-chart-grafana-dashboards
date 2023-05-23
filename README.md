# glueops-grafana-dashboards

![Version: 0.7.1-alpha-2](https://img.shields.io/badge/Version-0.7.1--alpha--2-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 0.1.0](https://img.shields.io/badge/AppVersion-0.1.0-informational?style=flat-square)

A Helm chart for Grafana Dashboards for the GlueOps Platform. Given how Helm template works whenever you have a `{{var}}` in your grafana json you need to change it so that its excplitity escaped with a backtick. ORIGINAL- {{kubernetes_pod_name}} WORKING- ```{{`{{kubernetes_pod_name}}`}}```

