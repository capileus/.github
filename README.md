# Capileus Github Repository

# Introduction

Capileus is a comprehensive tool for managing your cloud environments including, deploy, backup and restore capabilities. It uses an infrastructure as configuration solution to provide a simplified approach to ensuring your cloud environment is managed, monitored and maintained. This configuration management approach enables robust guardrails to be delivered as part of the solution that monitor and enforce the configuration, ensuring that the environment is always compliant with any policies. 

The heart of the capileus eco system is the configuration files that define the cloud environment. These files contain all of the information required to build the cloud environment from scratch and any modification to the cloud environment is performed by changing the configuration files. 

However, as capileus also contains a robust backup facility, the problem of drift becomes much more manageable. The configuration of environments that are not being tightly managed, for example Sandpits, Development and PoC environments, can be quickly extracted. This configuration can then be used to build new solutions in more controlled environments or to bring these unmanaged environments under control. This facility can also be used to audit existing cloud environments and bring them under the control of the Capileus eco system. 

## Getting started

Clone repository
Create New Cloud Environment (if required)
Autheticate with the Cloud

## Backup Existing Environment

The first step is to backup the cloud environment. This creates the initial set of configuration files that are used to manage the environment going forwards.  

capileus backup 

## Identify Changes

The environment can now be managed directly from the configuration files and any changes can be identifies by runnning a comparison between the configuration files and the cloud environment. This will highlight the differences, including any drift in the cloud environment, and show the changes that will be made if the current configuration is deployed. 

capileus compare

A combination of the backup process and deployment process can be used to accept change from both the cloud environment and configuration files. 

## Deploy Configuration

Any changes to the configuration can be deployed using the deployment process. This will ensure that the cloud environment matches the configuration files. Any changes made in the cloud environment that are not reflected in the configuration files will be reverted. 

capileus deploy

## Install Management

Capileus can also be used to manage the cloud environment dynamically, ensuring that the environment is only managed through the configuration files and remediating any changes made through the console. This is achieved using a storage bucket and serverless compute to provide a lightweight, secure and cost effective management solution.  

capileus manage

## Continuous Deployment

Capileus can easily integrate with your existing pipeline approach or be easily deployed using github actions. 
