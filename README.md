# Fluentbit
This repo contains fluentbit config files for cluster logging
--------
Configuration Steps.
--------
1. kubectl create namespace metrics
2. kubectl create -f fluent-bit-service-account.yaml
3. kubectl create -f fluent-bit-configmap.yaml
4. kubectl create -f fluent-bit-ds.yaml
5. kubectl create -f fluent-bit-collector.yaml
