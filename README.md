
# Building a CI/CD Pipeline


## Set Up Azure Cloud Shell
- Create udacity account by clicking access lab OR use your own account
- Create storage account ==> for create azure cloudshell
- Gen ssh key and integrate to github
- Clone project by cmd: git clone git@github.com:bachlt/udacity_azure_devops_build_ci_pipelines.git
- Run test make all

## Deploy Webapp by Azure pipeline
- Create App service plan and app service in Azure portal
- Create Project in Azure devops
- Create Service connection to Azure portal
- Create github connection
- Create Pipeline by existing yaml file in project.
- Run pipeline to deploy Web app to App Services.
- Check log web app
- Test deploy webapp successfully by run file make_predict_azure_app
