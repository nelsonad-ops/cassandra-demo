# cassandra-demo

curl http://169.254.169.254/latest/meta-data/public-ipv4
yum install python3 -y

helm repo add k8ssandra https://helm.k8ssandra.io/stable
helm repo add traefik https://helm.traefik.io/traefik
helm repo update

helm install traefik traefik/traefik -f traefik.yaml
kubectl get svc
helm install -f k8ssandra.yaml k8ssandra k8ssandra/k8ssandra
kubectl get pods

kubectl get secret k8ssandra-superuser -o jsonpath="{.data.username}" | base64 --decode ; echo
kubectl get secret k8ssandra-superuser -o jsonpath="{.data.password}" | base64 --decode ; echo

