OpenFaaS Cloud
==============

Managed OpenFaaS for teams

![Conceptual diagram](/docs/ofc-github-conceptual.png)

The high-level workflow for the OpenFaaS Cloud CI/CD pipeline.

## Introduction

[![Build Status](https://travis-ci.com/openfaas/openfaas-cloud.svg?branch=master)](https://travis-ci.com/openfaas/openfaas-cloud)

OpenFaaS Cloud introduces an automated build and management system for your Serverless functions with native integrations into your source-control management system whether that is GitHub or GitLab.

With OpenFaaS Cloud functions are managed through typing `git push` which reduces the tooling and learning curve required to operate functions for your team. As soon as OpenFaaS Cloud receives a `push event` from `git` it will run through a build-workflow which clones your repo, builds a Docker image, pushes it to a registry and then deploys your functions to your cluster. Each user can access and monitor their functions through their personal dashboard.

Features:

* Portable - self-host or use the hosted Community Cluster (SaaS)
* Multi-user - use your GitHub/GitLab identity to log into your personal dashboard
* Automates CI/CD triggered by `git push` (also known as GitOps)
* Onboard new git repos with a single click by adding the *GitHub App* or a repository tag in *GitLab*
* Immediate feedback on your personal dashboard and through GitHub Checks or GitLab Statuses
* Sub-domain per user or organization with HTTPS
* Runtime-logs for your functions
* Fast, non-root image builds using [buildkit](https://github.com/moby/buildkit/) from Docker

The dashboard page for a user:

![Dashboard](/docs/dashboard.png)

The details page for a function:

![Details page](/docs/details.png)

## Overview

### KubeCon video

[![](http://img.youtube.com/vi/sD7hCwq3Gw0/maxresdefault.jpg)](https://www.youtube.com/watch?v=sD7hCwq3Gw0)

[KubeCon: OpenFaaS Cloud + Linkerd: A Secure, Multi-Tenant Serverless Platform - Charles Pretzer & Alex Ellis](https://www.youtube.com/watch?v=sD7hCwq3Gw0&feature=emb_title)

### Blog posts

* [Build your own OpenFaaS Cloud with AWS EKS](https://www.openfaas.com/blog/eks-openfaas-cloud-build-guide/)
* [Introducing OpenFaaS Cloud with GitLab](https://www.openfaas.com/blog/openfaas-cloud-gitlab/)
* [Introducing OpenFaaS Cloud](https://blog.alexellis.io/introducing-openfaas-cloud/)
* [Sailing through the Serverless Ocean with Spotinst & OpenFaaS Cloud](https://spotinst.com/blog/sailing-through-the-serverless-ocean-with-openfaas-cloud/)

### Documentation

* [Conceptual architecture](https://docs.openfaas.com/openfaas-cloud/architecture).
* [Authentication](https://docs.openfaas.com/openfaas-cloud/authentication/)
* [Multi-stage environments](https://docs.openfaas.com/openfaas-cloud/multi-stage/)
* [Manage secrets](https://docs.openfaas.com/openfaas-cloud/secrets/)
* [User guide](https://docs.openfaas.com/openfaas-cloud/user-guide/)

### Roadmap & Features

See the [Roadmap & Features](docs/ROADMAP.md)

## Get started

You can set up and host your own *OpenFaaS Cloud* or apply for access to the hosted Community Cluster.

### Option 1: Automated deployment (self-hosted)

You can set up your own OpenFaaS Cloud with authentication and wildcard certificates using ofc-bootstrap in around 100 seconds.

Get started: [ofc-bootstrap](https://github.com/openfaas-incubator/ofc-bootstrap)

This method assumes you are using Kubernetes and have a public IP available. Some basic knowledge of how to setup a GitHub App and GitHub OAuth App along with a DNS service account on Google Cloud DNS or AWS Route53.

### Option 2: Community Cluster (SaaS)

The OpenFaaS Community Cluster is a hosted version of OpenFaaS Cloud for community use and for evaluation.

* [Apply for the Community Cluster](https://github.com/openfaas/community-cluster/tree/master/docs)

### Option 3: Manual deployment (self-hosted)

The manual deployment takes longer, but covers all the requirements in detail and is the most flexible option. You may follow this guide if you are contributing to the project, or if you want to use Swarm.

Read the [developer's guide](docs/README.md) to find out more about the functions and to start hacking on OpenFaaS Cloud.

## Getting help

For help join #openfaas-cloud on the [OpenFaaS Slack workspace](https://docs.openfaas.com/community). If you need commercial support, contact [sales@openfaas.com](mailto:sales@openfaas.com)

