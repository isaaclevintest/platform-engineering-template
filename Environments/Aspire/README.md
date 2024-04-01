# .NET Aspire Azure Deployment Environment Definition

This environment definition enables the ability to both provision the Azure resources needed, as well as deploys the application code for a .NET Aspire project.

## What does this Definition Do?

This environment definition takes advantage of a Azure Deployment Environments Custom Runner that provisions and deploys a .NET Aspire application to Azure using the Azure Developer CLI. 

The source code for the runner is [here](https://github.com/isaacrlevin/azd-ade-custom-runner).

## How to use

The simplest way to use this definition is to do the following.
- Fork this repo
- Add forked repo as [catalog to your Dev Center](https://learn.microsoft.com/en-us/azure/deployment-environments/how-to-configure-catalog). 

## Definition Parameters

The environment definition has the following parameters in order for it to execute

- **Name**: Name of Environment. This will be used to create the resource group for the Azure resources that are provisioned.
- **Repo Url**: Url of Git Repo that contains the .NET Aspire application. **NOTE THIS MUST BE A PUBLIC REPO AT THIS TIME**
- **Branch**: Branch that will be deployed. If none is provided, it will use the default branch. 