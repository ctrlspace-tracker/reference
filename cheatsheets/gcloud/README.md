gcloud auth list
gcloud config set account vasanthadeiveehan@gmail.com
gcloud config set project wise-dispatcher-238019

gcloud compute addresses create hello-web-static-ip --global
gcloud compute addresses delete hello-web-static-ip
gcloud container clusters get-credentials ctrl-space-cluster --zone=us-central1-a
