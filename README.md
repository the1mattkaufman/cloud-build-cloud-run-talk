# Description

This is a repo for my talk on hosting and deploying your apps like a pro using Cloud Run and Cloud Build

# Getting Started with Cloud Run

1. Create a new Project in Google Cloud Console
   https://cloud.google.com/resource-manager/docs/creating-managing-projects

2. Enable Billing on the Project
   https://cloud.google.com/billing/docs/how-to/modify-project

3. Install ane Initialize the Cloud SDK Locally
   https://cloud.google.com/sdk/docs

4. Containerize your app by adding Dockerfile and .dockerignore files
   https://cloud.google.com/run/docs/quickstarts/build-and-deploy

5. Build an image of your container
   gcloud builds submit --tag gcr.io/PROJECT-ID/APP-NAME

6. Deploy the image to Cloud Run
   gcloud run deploy --image gcr.io/PROJECT-ID/APP-NAME --platform managed
