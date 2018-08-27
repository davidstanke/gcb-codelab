# gcb-codelab
Learn the basics of CICD with Google Cloud Build

##STEPS

[basic init]
[initialize gke / kubectl]

Save project ID to a var
export PROJECT_ID=$(gcloud config list --format 'value(core.project)')

Build from dockerfile
gcloud builds submit . --tag=gcr.io/$PROJECT_ID/gceme

Build from YAML [simple config with identical result to dockerfile]
gcloud builds submit . --config=gcb/cloudbuild.yaml
