# Helm Chart Access Guide

This guide explains how to download and access the Helm chart hosted on GitHub Pages.

## Prerequisites

Before proceeding, make sure you have the following:

- [Helm](https://helm.sh/docs/intro/install/) installed on your system.
- A Kubernetes cluster (can be local or cloud-based).
- GitHub repository where the Helm chart is hosted on GitHub Pages.

## Step 1: Add the GitHub Pages repository to Helm

1. Open your terminal.

2. Add the GitHub Pages repository to Helm by running the following command:

   ```bash
   helm repo add my-helm-repo https://chandrasai1702.github.io/my-helm-charts/

3. Update your Helm repositories to get the latest charts:
   ```bash
   helm repo update
   
## Step 2: Install the Helm Chart
Once the repository is added, you can now install the Helm chart. For example, to install the todo-helmchart:

    helm install todo-app my-helm-repo/todo-helmchart 

## Step 3: Verify Installation
  To verify the installation, you can check the status of the release:
  
      helm list

## Step 4: Access through port-forwarding
    
    kubectl port-forward $POD_NAME 8080:8080 --namespace default
