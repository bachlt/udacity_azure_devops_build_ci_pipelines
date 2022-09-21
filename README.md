[![Python application test with Github Actions](https://github.com/bachlt/udacity_azure_devops_build_ci_pipelines/actions/workflows/pythonapp.yml/badge.svg)](https://github.com/bachlt/udacity_azure_devops_build_ci_pipelines/actions/workflows/pythonapp.yml)

# Building a CI/CD Pipeline

## Introduction
This project contains a python application to predict housing prices. This repo included:
- Deploy the app in Azure CloudShell
- Deploy the app as an Azure App Service

## Architecture Diagram
- Developer commit source code to github in feature branch.
- Reviewer will merge commit to main branch.
- Github action will be triggered to verify commit
- Azure pipeline also be triggered to build source code to zip file and deploy to Azure App service.
![Architecture Diagram](https://video.udacity-data.com/topher/2020/August/5f3447ab_cd-diagram/cd-diagram.png)
- A [Trello](https://trello.com/b/BHbvpAav/udacity-bachlt) board to manage task for member.
- A [spreadsheet](project_schedule.xlsx) to manage project schedule.
- A [Demo Youtube](https://youtu.be/k6yUoqCteqM) to demo our project.


## Set Up Azure Cloud Shell
- Create udacity account by clicking access lab OR use your own account
- Create storage account ==> for create azure cloudshell
- Gen ssh key and integrate to github
- Clone project by cmd: git clone git@github.com:bachlt/udacity_azure_devops_build_ci_pipelines.git
![Clone Git From Cloud Shell](screenshot/1_cloudshell_clone_git.PNG) 
- Run test make all
![Run test make all](screenshot/1_cloudshell_test_make_all.PNG) 

## Deploy Webapp by Azure pipeline
- Create App service plan and app service in Azure portal
![ App service](screenshot/3.1_azure_app_services.PNG) 
- Create Project in Azure devops
- Create Service connection to Azure portal
- Create github connection
- Create Pipeline by existing yaml file in project.
- Run pipeline to deploy Web app to App Services.
![Pipeline Run](screenshot/3.2_azure_pipeline.PNG)
![Pipeline Run](screenshot/3.4_azure_pipeline_2.PNG)
- Check log web app
![log web app](screenshot/3.3_deploy_webapp_logs.PNG)
- Test deploy webapp successfully by run file make_predict_azure_app
![Run Test in cloud shell](screenshot/3.1_azure_app_make_predict.PNG)

## Load test by Locust
- Install Locust by cmd: pip install locust
- Run Locust and test our web app by cmd: locust
- Check report on localhost:8089
![Locust report](screenshot/4_locust_screenshot.PNG)

## Improvement
- This project is only have single branch for 1 developer. In reality, the project have many branch for all develop team to contribute source code. We have to improve source code management, branch of pipeline trigger, how to merge code to staging and production environment etc..

