# Overview


[![Python application test with Github Actions](https://github.com/alka077/udacity_project2_CICD/actions/workflows/pythonapp.yml/badge.svg)](https://github.com/alka077/udacity_project2_CICD/actions/workflows/pythonapp.yml)


In this project, I build a Github repository from scratch and create a scaffolding that will assist me in performing both Continuous Integration and Continuous Delivery. I will use Github Actions along with a Makefile, requirements.txt and application code to perform an initial lint, test, and install cycle. Next, I will integrate this project with Azure Pipelines to enable Continuous Delivery to Azure App Service.

This repositry demonstrate:

* Deploying the app in Azure CloudShell
* Deploying the app as a web server using Azure App Service.

## Project Plan

* A link to a Trello board for the project https://trello.com/b/agz2gagW/udacity
* A link to a spreadsheet that includes [project-management-template (1).xlsx](https://github.com/alka077/udacity_project2_CICD/files/9309410/project-management-template.1.xlsx)
the original and final project plan>

## Instructions

* Architectural Diagram (Shows how key parts of the system work)>
* ![image](https://user-images.githubusercontent.com/106584802/184150199-dee1bfce-bd45-49b7-b98b-d8ddf7b6f337.png)


In Azure Cloud Shell, clone the repo:

* ![image](https://user-images.githubusercontent.com/106584802/184150456-7f84ec08-3afb-498a-8043-f8807668737e.png)

ADD The SSH key to github account:

![image](https://user-images.githubusercontent.com/106584802/184152975-100efc92-2e14-49e1-b7b3-6d284302d60b.png)


* Passing tests that are displayed after running the `make all` command from the `Makefile`


 ![image](https://user-images.githubusercontent.com/106584802/184150584-37033ff8-0c15-49ce-ac80-eb71966d6c1c.png)


* Enable Git hub actions and update the pythonapp.YML file


* ![image](https://user-images.githubusercontent.com/106584802/184150783-0294d7b2-748f-4fdd-bc70-f85fbed8a8f4.png)


Create an web app service using below cmd
az webapp up --name <appname> --resource-group <rgname> --location <location> --runtime "PYTHON:3.7"

![image](https://user-images.githubusercontent.com/106584802/184151020-f4b642cc-9f73-43bf-8e8f-80554077feb0.png)


create the pipeline and deploy
![image](https://user-images.githubusercontent.com/106584802/184151316-c33ce537-e259-47e4-982e-e62f9d39dd05.png)


Webapp deployment center
 
 
![image](https://user-images.githubusercontent.com/106584802/184151391-ffa1bdcc-1a24-460d-b642-3934452af079.png)


* Output of streamed log files from deployed application by running below cmd
 
 az webapp log tail

> ![image](https://user-images.githubusercontent.com/106584802/184151497-cfc22750-31aa-4270-a030-db43ee1e8d6a.png)


## Enhancements

these pipelines will help in delivering continously and will integrate with our incremental release

## Demo 

https://www.youtube.com/watch?v=wOxy6o2dDhM


