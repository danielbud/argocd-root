


kind create cluster




helm repo add argo https://argoproj.github.io/argo-helm
helm repo update

helm upgrade --install \
    argocd argo/argo-cd \
    --namespace argocd-system \
    --create-namespace \
    --wait


kubectl apply -f rootapplication.yaml



