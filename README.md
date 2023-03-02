# Container Image scannen with Github Actions

This repository can be used as example on how to implement container image scanning during the developemnt lifecycle.

## Repository structure

The project is structured as follows:

- **.github/workflows**: 
  - This directory contains Github Workflows. More information about the specific workflows can be found in the Workflows section.
- **.github/containerscan
  - **allowedlist.yaml**: This file contains CVE's and CSI's that you allow
- **Dockerfil**: A Dockerfile to build a simple image based on the nginx image
- **index.html**: A simple page use for the Docker image we build

## Workflows

The project has one workflows:

1. **.github/vulnerability-scan.yaml**: This workflow first builds an image and then scans the container image. The pipeline runs when there is a push to the repository. In the [Actions Tab](https://github.com/bryteblue/container-image-scanning/actions) you can click on one of the runs and in the Job Summary you will find the results of the image scan. The result will give a summary with the amount of found vulnerabilities and best CSI benchmark best practices, but it will also give you a link to each CVE and CSI to get more information about and a potential fix.

