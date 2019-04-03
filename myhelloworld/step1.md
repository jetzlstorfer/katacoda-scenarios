# Install the Dyntrace OneAgent

1. Create Dynatrace namespace `kubectl create ns dynatrace`{{execute}}

1. Get latest release `LATEST_RELEASE=$(curl -s https://api.github.com/repos/dynatrace/dynatrace-oneagent-operator/releases/latest | grep tag_name | cut -d '"' -f 4)` {{execute}}

1. create resources `kubectl create -f https://raw.githubusercontent.com/Dynatrace/dynatrace-oneagent-operator/$LATEST_RELEASE/deploy/kubernetes.yaml`{{execute}}

1. show logs `kubectl -n dynatrace logs -f deployment/dynatrace-oneagent-operator`{{execute}}

