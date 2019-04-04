# Create Secret

1. Create k8s secret: `kubectl -n dynatrace create secret generic oneagent --from-literal="apiToken=API_TOKEN" --from-literal="paasToken=PAAS_TOKEN"`{{copy}}

1. Download: `curl -o cr.yaml https://raw.githubusercontent.com/Dynatrace/dynatrace-oneagent-operator/$LATEST_RELEASE/deploy/cr.yaml`{{execute}}

1. Edit: `nano cr.yaml`{{execute}}

1. Apply `kubectl create -f cr.yaml`{{execute}}

1. Check if pods are running `kubectl get pods -n dynatrace -w`{{execute}}
