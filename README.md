use helm to install traefik ingress controller in your k8s cluster

instll helm useing below commands
```
  curl https://baltocdn.com/helm/signing.asc | sudo apt-key add -
  sudo apt-get install apt-transport-https --yes
  echo "deb https://baltocdn.com/helm/stable/debian/ all main" | sudo tee /etc/apt/sources.list.d/helm-stable-debian.list
  sudo apt-get update
  sudo apt-get install helm
```
after that add traefik repo to helm using below commands
```
  helm repo add traefik https://helm.traefik.io/traefik
  helm repo update
```
then install traefik in your cluster using below command
```
  helm install traefik traefik/traefik --namespace=kube-system --values=values.yml
```
done
