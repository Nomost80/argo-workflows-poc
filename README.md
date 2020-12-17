# Goal
The goal of this POC is to test the most popular kubernetes native pipelines solution called [Argo Workflows](https://argoproj.github.io/argo/).

# Requirements
* A running Kubernetes Cluster

# Steps
1. Install Argo Workflows: https://argoproj.github.io/argo/quick-start/
2. Install Argo Events: https://argoproj.github.io/argo-events/installation/
3. Replaces Roles by ClusterRoles otherwise install both in same namespace
4. Replace `ci/github-access.yml` values with yours
5. Setup Github [Event Source](https://argoproj.github.io/argo-events/setup/github/), Sensor and Trigger: `kubectl apply -f -r ./ci` 
6. Expose publicly the webhook 
7. Add the webhook in the GitHub repository settings

# My Opinion
* Great flexibility with Kubernetes
* Very verbose compared to other CI solutions
* Powerful DAGs