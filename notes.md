# Notes

## Setup

[Create your first function in the Azure portal](https://docs.microsoft.com/en-us/azure/azure-functions/functions-create-function-app-portal)

subscription: `mamanuel-cse`
resource group: `serverless-cookbook`

Function App name: `hello-world-mamanuel`
Publish: Code
Runtime stack: `Node.js`
Version: `14 LTS`
Region: `Canada Central`

URL: `hello-world-mamanuel.azurewebsites.net`

Storage account: `storageaccountservead83`
Operating system: `Windows`

Plan type: `Consumption (Serverless)`

Application Insights: `hello-world-mamanuel (Central Canada)`

---

Summary
Function App
by Microsoft
Details
Subscription
a5259ef1-d736-482e-a447-308c22c09ed5
Resource Group
serverless-cookbook
Name
hello-world-mamanuel
Runtime stack
Node.js 14 LTS
Hosting
Storage (New)
Storage account
storageaccountservead83
Plan (New)
Plan type
Consumption (Serverless)
Name
ASP-serverlesscookbook-afd0
Operating System
Windows
Region
Canada Central
SKU
Dynamic
Monitoring (New)
Application Insights
Enabled
Name
hello-world-mamanuel
Region
Canada Central

---

At this point I've created a Function App.

Create function

Development Environment: `Develop in portal`

Template: `HTTP trigger`

New Function: `HttpTrigger1`
Authorization level: `Anonymous`

[HttpTrigger1](https://hello-world-mamanuel.azurewebsites.net/api/HttpTrigger1)

[HttpTrigger1 with Matt as name parameter](https://hello-world-mamanuel.azurewebsites.net/api/HttpTrigger1?name=Matt)

---

[Install the Azure Function Core Tools](https://docs.microsoft.com/en-us/azure/azure-functions/functions-run-local?tabs=v4%2Clinux%2Ccsharp%2Cportal%2Cbash%2Ckeda)

Installed Azure Functions extension in VS Code.

---

[Add messages to an Azure Storage queue using Functions](https://docs.microsoft.com/en-us/azure/azure-functions/functions-integrate-storage-queue-output-binding?tabs=nodejs)

Add output

Binding Type: `Azure Queue Storage`

Azure Queue Storage details

Storage account connection: `AzureWebJobsStorage`

Message parameter name: `outputQueueItem`

Queue name: `outqueue`

| Setting                    | Suggested value     | Description                                                                                              |
|----------------------------|---------------------|----------------------------------------------------------------------------------------------------------|
| Message parameter name     | outputQueueItem     | The name of the output binding parameter.                                                                |
| Queue name                 | outqueue            | The name of the queue to connect to in your Storage account.                                             |
| Storage account connection | AzureWebJobsStorage | You can use the storage account connection already being used by your function app, or create a new one. |

It worked. Not sure what to document here other than success. No other parameters.

I guess a question: Why would we write a message to a queue? Just for later processing maybe?

---

Now doing the same thing but with Python, and starting locally.

[Quickstart: Create a function in Azure with Python using Visual Studio Code](https://docs.microsoft.com/en-us/azure/azure-functions/create-first-function-vs-code-python)

Had to install the Python VS Code extension in Ubuntu. Had to install python3-venv package in Ubuntu.

`apt install python3.8-venv`
