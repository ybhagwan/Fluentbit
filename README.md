# Fluentbit
This repo contains fluentbit config files for cluster logging
Configuration Steps.

kubectl create namespace metrics
kubectl create -f fluent-bit-service-account.yaml
kubectl create -f fluent-bit-configmap.yaml
kubectl create -f fluent-bit-ds.yaml
kubectl create -f fluent-bit-collector.yaml
