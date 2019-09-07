##gCloud reference commands

Install gCloud using the following url:
https://cloud.google.com/sdk/docs/quickstart-macos

> 1. Download the gcloud sdk in a local directory (say ~/SOFTWARES/<sdk>)
> 2. Run /~/SOFTWARES/sdk/install.sh

This should install the gcloud. 


### GCloud setup configurations
```shell script
gcloud init
```
This will open a new window and login to google console with a userid and password, once verified, 
gcloud will setup in local and point to the project which you have logged in using the console.

This will also install bash completion for gcloud, which means you can use <tab> if you want to know the next attribute in a gcloud command.

```
gcloud --help                           // help reference for gcloud
gcloud auth list                        // Shows list of all gcloud accounts
gcloud config set account <email-id>    // Set a different account.
gcloud config set project <projectname> // Set a different project. 
```

### Compute

#### Static addresses
```
gcloud compute addresses list
gcloud compute addresses create <static ip address name> --global
gcloud compute addresses describe <static ip address anme>
gcloud compute addresses delete <static ip address name>
```

#### container (Kubernetes)

Connecting to a new cluster. 
``` 
gcloud container clusters get-credentials ctrl-space-cluster --zone=us-central1-a --project <project-id>
gcloud components install kubectl       // Install kubectl in local using gcloud
```

### EC2:
```
gcloud compute instances create instance-2 --zone us-central1-a --labels env=prod,owner=sam,component=backend
gcloud compute instances describe instance-2 --zone us-central1-a --format 'default(labels)'
gcloud compute instances update instance-2 --zone us-central1-a --update-labels owner=sue,state=readyfordeletion
gcloud compute instances update instance-2 --zone us-central1-a --remove-labels state
```

### IAM:

```
gcloud projects get-iam-policy <project id> > iam.yaml
gcloud projects set-iam-policy <project id> iam.yaml
gcloud projects add-iam-policy-binding <project id> --member user:(email)--role roles/editor
```
