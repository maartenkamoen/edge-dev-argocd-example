# Create cilium manifest

kustomize build > output.yaml


kustomize build  | yq -i 'with(.cluster.inlineManifests.[] | select(.name=="argocd"); .contents=load_str("/dev/stdin"))' argocd.yaml
