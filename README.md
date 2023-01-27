# k8s-helm-charts

## Brief Intro
This template uses the Prometheus Operator chart to install Prometheus and Alertmanager, and configures an alert rule that triggers when a node is down for more than 15 seconds, it checks the state of the node by checking the value of the up metric, if the value is 0, that means the node is down, it then sends an alert to the webhook receiver, which can be configured to send a notification to an incoming webhook.