# DotNetMigrationDemo
The purpose of this demo environment is to provide experience with migrating a .Net application from virtual machines to Azure App service and SQL Managed Instance. This is a common migration pattern as moving an application from VM to Azure PaaS allows customers to focus more on their application and not on managing server environments. The image below gives a preview of the Azure resources that are deployed. 

![Architecture Diagram](./images/architecture.png)

The demo .Net application is installed on the App VM virtual machine. It is a basic banking application that allows money transfers between several bank accounts. The application is deployed to IIS. The application uses SQL as its backend database. SQL server 2022 Developer Edition is installed on the App VM virtual machine. This document will provide guidance on how to migrate the application from IIS to the deployed App Service resource. In addition, the SQL database will be moved to the SQL Managed Instance.

  1.	[The link here](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FMr-MSFT%2FDotNetMigrationDemo%2Fmain%2FDemoAppMigrationARM.json) can be used to deploy the ARM template via the Azure portal. The ARM template deploys all the necessary resources   for the demo. The resources can take    up to two hours to deploy.
  2.	Log into the App VM via bastion. There will be a link on the desktop named **BankPortal** that launches the demo web application. Take some time to play do some account        transfers and become familiar with the app.
    ![AppScreen](./images/appscreenshot.png)
