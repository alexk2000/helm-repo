helm create app3

edit chart ./app3

helm package app3

helm repo index . 

git add app3-1.19.3.tgz index.yaml
git commit -m "Add chart to chart repo"
git push

