# k8s-helm-charts-manifest-template

## Brief Intro

This template uses the Prometheus Operator chart to install Prometheus and Alertmanager, and configures an alert rule that triggers when a node is down for more than 15 seconds, it checks the state of the node by checking the value of the up metric, if the value is 0, that means the node is down, it then sends an alert to the webhook receiver, which can be configured to send a notification to an incoming webhook.

## What do you need in advance?

    1. A Kubernetes Cluster (you are free to choose any provider you want)
    2. Helm Chart Package installed
    3. Prometheus Operator installed
    4. Having access to the kubeconfig file for the cluster, which you can use to authenticate with the K8S API.
