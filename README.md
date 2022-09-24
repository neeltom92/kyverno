# kyverno
kyverno installation and config

1. ENSURE that Kyverno is installed before any other policies
2. Install via Kubectl

- kubectl create \
    --filename https://raw.githubusercontent.com/kyverno/kyverno/main/config/install.yaml

- kubectl --namespace kyverno \
    rollout status \
    deployment kyverno
3. Kyverno is not namespace scoped unlike Keda
4. Policy for CPU and resource limits
kubectl apply --filename container-must-have-limits.yaml 
