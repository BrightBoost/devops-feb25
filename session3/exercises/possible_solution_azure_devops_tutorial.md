Make sure to host (the demo app on your own Github account)[https://github.com/BrightBoost/deploy-azure]
You can fork the project.

Go to: https://portal.azure.com/
Login with your credentials.
Create a new password if prompted, make sure to write it down.
On Azure, go to App Service
Choose Web App.
Give it a name: e.g. demonodeapp20
Runtime stack: Node 20 LTS
Region: choose your region
Pricing plan: Free F1
Click on Review + Create
Click Create again and wait for the deployment to be done.

In the Azure portal search for Azure Devops Organisations and go there
Click on "my azure devops organizations"
Leave the name as is
Click on "create new organization"
Solve the impossible CAPTCHA
Wait for your Azure DevOps Organization to load
Click on create project, call it DemoNode

Go to pipelines on the left hand side and click on Create Pipeline
Choose GitHub and login
Choose the demo project
In the configure tab, choose Node js Express Web App to Linux on Azure
Review the pipeline and have a look at the steps, click on Run
For connection choose DataCouch
For Web App, choose the just created service "demonodeapp"
Click on Validate an Configure

Optional:
You might get the error: ##[error]No hosted parallelism has been purchased or granted. To request a free parallelism grant, please fill out the following form https://aka.ms/azpipelines-parallelism-request
Click on azure devops top left
left bottom: choose organization settings
Go to parallel jobs
Click on change next to monthly purchases for hosted 
Click on setup billing, subscription will load, click save
Set paid parallel jobs to 1 for MS hosted, click save
It may take a few minutes before it's working, 
this is the part where you go and get some coffee
Go back to the pipeline and click Run

In the deploy phase it will "pipeline needs permission to access a resource", click on view and click permit
After the pipeline completed successfully, go to the URL (you can find this in the azure portal if you click on the App Service or find it in the log of the deploy)