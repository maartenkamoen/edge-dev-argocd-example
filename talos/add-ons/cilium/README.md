# Create cilium manifest

helm template cilium/cilium --version 1.17.2 --kube-version 1.32 -f ./values.yaml --namespace kube-system > cilium.yaml