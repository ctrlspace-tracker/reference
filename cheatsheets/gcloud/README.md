gcloud auth list
gcloud config set account <email-id>
gcloud config set project <projectname>

gcloud compute addresses create hello-web-static-ip --global
gcloud compute addresses delete hello-web-static-ip
gcloud container clusters get-credentials ctrl-space-cluster --zone=us-central1-a


EC2:
gcloud compute instances create instance-2 --zone us-central1-a --labels env=prod,owner=sam,component=backend
gcloud compute instances describe instance-2 --zone us-central1-a --format 'default(labels)'
gcloud compute instances update instance-2 --zone us-central1-a --update-labels owner=sue,state=readyfordeletion
gcloud compute instances update instance-2 --zone us-central1-a --remove-labels state


IAM:
gcloud projects get-iam-policy <project id> > iam.yaml
gcloud projects set-iam-policy <project id> iam.yaml
gcloud projects add-iam-policy-binding <project id> --member user:(email)--role roles/editor
