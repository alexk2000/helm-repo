helm create app3

edit chart ./app3

helm package app3

helm repo index . 

git add app3-1.19.3.tgz index.yaml
git commit -m "Add chart to chart repo"
git push

helm repo add my-repo https://alexk2000.github.io/helm-repo
helm repo update
helm search repo  app3
NAME            CHART VERSION   APP VERSION     DESCRIPTION
my-repo/app3    1.19.3          1.19.3          A Helm chart for Kubernetes