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

Access logs through pods/container
------
1. kubectl get pod log-collector-0 -n metrics -o jsonpath=‘{.spec.containers[*].name}'
 (To list down all the container in a log-collector-0 pod)
2. kubectl exec -i -t log-collector-0 -n metrics --container nginx -- /bin/bash   (log-collector-0 --> log-collector pod)
3. cd /usr/share/nginx/html    (Logs location)
