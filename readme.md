### Tech Friday Commands

## Init
1. ``gcloud container clusters get-credentials tech-friday-k8s --zone europe-central2-a --project fgp-devzoo``
2. ``kubectl describe nodes`` - test whether it works

## Commands
- `kubectl config set-context --current --namespace=<name_space>` - change namespace
- `kubectl describe pods` - debug all pods for actual namespace
- `kubectl logs <pod_id>` - get logs for pod
- `kubectl apply -f . --validate=false` - update/init instance for actual folder
- `kubectl set image deployment/foodadvisor-backend foodadvisor-api=foodadvisor-api:latest` - update istance
- `kubectl top pod <pod_id>  --containers ` - show uses recorces by pods
- `	kubectl exec -it <pod_id> /bin/bash` - exec bash for concret pods
## Optional to prepare env (GCP)
Install tf to prepare cluster for gcp
https://learn.hashicorp.com/tutorials/terraform/install-cli
1. ``cd tf``
2. ``terraform init``
3. ``terraform plan``
4. ``terraform apply``
5. ``kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.1.0/deploy/static/provider/cloud/deploy.yaml``