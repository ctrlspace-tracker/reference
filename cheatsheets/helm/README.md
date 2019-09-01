## HELM commands



#### Installation

brew install kubernetes-helm
kubectl create -f rbac-config.yml
helm init --service-account tiller --history-max 200 --upgrade
