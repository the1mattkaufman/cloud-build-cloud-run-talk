# Description

This is a repo for my talk on hosting and deploying your apps like a pro using Cloud Run and Cloud Build

# Getting Started with Cloud Run

1. Create a new Project in Google Cloud Console
   https://cloud.google.com/resource-manager/docs/creating-managing-projects

2. Enable Billing on the Project
   https://cloud.google.com/billing/docs/how-to/modify-project

3. In the Google Cloud Console, enable the Cloud Build, Cloud Run, Container Registry, and Resource Manager APIs:
   https://console.cloud.google.com/flows/enableapi?apiid=cloudbuild.googleapis.com,run.googleapis.com,containerregistry.googleapis.com,cloudresourcemanager.googleapis.com&redirect=https://cloud.google.com/cloud-build/docs/deploying-builds/deploy-cloud-run

4. In the Google Cloud Console, enable the Cloud Run Admin and Service Account User roles to the Cloud Build service account in IAM permissions
   https://console.cloud.google.com/cloud-build/settings/service-account?project=PROJECT-ID&folder=&organizationId=

5. Install and Initialize the Cloud SDK Locally
   https://cloud.google.com/sdk/docs

6. Containerize your app by adding Dockerfile and .dockerignore files
   https://cloud.google.com/run/docs/quickstarts/build-and-deploy

7. Build an image of your container using gcloud
   gcloud builds submit --tag gcr.io/PROJECT-ID/APP-NAME

8. Deploy the image to Cloud Run
   gcloud run deploy --image gcr.io/PROJECT-ID/APP-NAME --platform managed

Notes:
a. PROJECT-ID should be all lowercase
b. Be sure to re-login and set your project in gcloud if you already had it installed
b. You can view your container in the Container Registry at: https://console.cloud.google.com/gcr/images/PROJECT-ID?project=PROJECT-ID
c. You can build your image locally using docker build and upload later using docker push

# Getting Started with Cloud Build

1. View your service in Cloud Run

2. Click Set Up Continuous Deployment

3. Click Manage connected repositories to auth into Github and link your repo

4. Choose your Branch

5. Choose your Dockerfile

6. Click Save

Notes:
a. You can view your Cloud Build Dashboard at: https://console.cloud.google.com/cloud-build/dashboard?project=PROJECT-ID
