# what is this?

## Etherpad collab space


* Slack at https://cloud-operators-ch.slack.com
* Etherpad https://etherpad.openstack.org/p/kubenordics

We are trying to create code to deploy kubernetes clusters across various
infrastructure-providers.

## Step #1 Terraform-work goals

We use Terraform to provision images on the infrastructure which we
later will use to provision kubernetes. The first step will produce an Ansible
inventory.

* Use the research-lab (latest?) code as a basis because it has a refactor of
  the TF code into modules per infrastructure provider.
* Set up automated testing of TF code on Travis CI
* AWS account provided by Safespring
* Azure account provided by x
* Openstack projects provided by UH IaaS, Safespring
* Standardized naming of TF resources across providers
* Do we need S3 shared state? Probably not.

### After testing is up ... 

* no force pushes to master!!!
* all changes as PRs

## Step #2 Do https://github.com/kelseyhightower/kubernetes-the-hard-way

* use the free credits from a new Google account if possible =) or ask for money

## Step #3 Look at the current Ansible roles/code design flow


## Step #4 Add Prometheus with Grafana based monitoring


## Step #5 Document maintenance workflows


## Step #6 Look at and discuss potential next steps

* What potential solutions for persistent storage should we look at?
* Pre-build images for the Terraform step using Packer tooling
* Use Jerakia as a data provider for both TF and Ansible

### Kubernetes design choices TBD

* Support external lb in front of cluster
* Do not support persistent storage for now
* Traefik as the ingress controller
* Calico CNI plugin for networking/policy

