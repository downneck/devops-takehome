# DevOps Docker/TF/K8S Take Home
Thank you for taking the time to interview here! In this repo, we want you to do the following:

1. Fix a broken docker-compose file
2. Create a Terraform module
3. Create some Kubernetes manifests

Please commit like usual on your local and reply to this email with a zip file containing your changes when you're done!

### Part 1
We have an Elasticsearch/Kibana stack for collecting our local development logs. A developer made some changes to the `docker-compose.yml` file and now things are not working. Try to get this `docker-compose` file back up and working and commit your changes.

### Part 2
We just received a request to run our EK set up for a development environment via Terraform. Let's a create reusable terraform module under the `/terraform` directory which spins up the resources required:

- A server with docker installed
- An ALB w/ a target group
- DNS record (if AWS Route53)
- A README explaining the module and how it works

Feel free to mock any values that are required for the terraform module (e.g. a Route 53 zone ID). Commit your `terraform plan` to your fork, there's no need to actually create the resource. If you do not have an AWS account, you can use other cloud platforms.

### Part 3
Now that we have our local EK stack going, let's convert our compose file into `kubernetes` manifests and run it in a local kubernetes cluster. Make any changes to environment variables as necessary. Commit your manifests to the `/k8s` directory.
