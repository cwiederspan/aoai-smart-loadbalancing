# Personal Notes

## To Do List

* Change the main.bicep file to include the service tag


```bash

# Wire-up the variables needed
TENANT_ID=<<YOUR_TENANT_ID>>
SUBSCRIPTION_ID=<<YOUR_SUBSCRIPTION_ID>>
ENVIRONMENT_NAME=<<YOUR_ENVIRONMENT_NAME>>
LOCATION=<<YOUR_AZURE_REGION>>

# Or...

source .env


# Login and execute the commands from the AZD CLI
azd auth login --tenant-id $TENANT_ID

azd env new $ENVIRONMENT_NAME --subscription $SUBSCRIPTION_ID --location $LOCATION

azd provision

azd deploy

azd pipeline config -e $ENVIRONMENT_NAME --provider github

```