# VPC




## Creating New VPC

Creating new VPC with `gcloud` command line

   ```sh 
   gcloud compute --project=traffic-trend-analysis networks create gcp-dev-vpc --description="Development VPC on GCP" --subnet-mode=custom
   ```
   
   Adding a  new Subnet to above VPC
   ```sh
   gcloud compute --project=traffic-trend-analysis networks subnets create dev-subnet-0 --network=gcp-dev-vpc --region=us-central1 --range=10.240.0.0/21
   ```
   
   
