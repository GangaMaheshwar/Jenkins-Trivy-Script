# Jenkins-Trivy-Script
Automating container security with Trivy using Jenkins pipeline script

Using this script you can automate the scanning container images from jenkins.
Prerequisites
  1. AWS CLI - https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html
  2. Docker - https://docs.docker.com/engine/install/
  3. Trivy - https://github.com/aquasecurity/trivy

From Jenkins go the pipeline scripts and copy the script. Modify the data with your data like AWS Account ID, AWS ECR URL, AWS Repository name and Image Tag.

In the first stage of scripts you are logging into AWS ECR where the containers are stored.
In the second stage you are pulling the docker container image from the ECR.
In the third stage you are running the Trivy scan. In the script I mentioned only for severity HIGH and Critical you can modify according to your need. we can create report into gitlab,junit and html format for that you need to load the Template location. when trivy is cloned you can see the contrib folder there you can find the .tpl files. Then mention the output file location where you want to generate the report.

configure your email settings in the jenkins to receive the report directly to you email ID.

