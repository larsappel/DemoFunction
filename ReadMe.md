
Install the Azure Functions Core Tools
https://learn.microsoft.com/en-us/azure/azure-functions/create-first-function-cli-csharp?tabs=linux%2Cazure-cli#install-the-azure-functions-core-tools

```bash
# Create a local function project
func init --worker-runtime dotnet-isolated --target-framework net8.0

# Add a function to your project by using the following command
func new --name HttpDemo --template "HTTP trigger" --authlevel "anonymous"
func new --name TableDemo --template "HTTP trigger" --authlevel "anonymous"

# Run the function locally
func start
```

Create supporting Azure resources for your function


Deploy the function project to Azure
func azure functionapp publish DemoFunc241013

```bash
#Add packages
dotnet add package Newtonsoft.Json
dotnet add package Azure.Data.Tables
```


> local.settings.json
```json
{
    "IsEncrypted": false,
    "Values": {
        "AzureWebJobsStorage": "UseDevelopmentStorage=true",
        "FUNCTIONS_WORKER_RUNTIME": "dotnet-isolated"
    }
}
```
