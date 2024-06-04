# Cmds to run this

## to login
`azd auth login`

## to provision and deploy the server
`azd up`

## if already provisoned then just deploy
`azd deploy`

## files path
in the data folder (pdfs, excels and docs)

## to ingest data
`./scripts/prepdocs.ps`

## to remove ingested data 
`./scripts/prepdocs.ps1` uncomment line `--removeall`

## to run locally
`cd app && ./start.ps1`

## frontend url 
should be printed in the logs upon completing `az up`

## If you've only changed the `backend/frontend code` in the app folder, then you don't need to re-provision the Azure resources. You can just run:
`azd deploy`

## If you've changed the infrastructure files (`infra folder` or `azure.yaml`), then you'll need to re-provision the Azure resources. You can do that by running:
`azd up`

azd env set AZURE_RESOURCE_GROUP resources-1
azd env set AZURE_LOCATION francecentral

azd env set AZURE_OPENAI_CHATGPT_DEPLOYMENT chat
azd env set AZURE_OPENAI_CHATGPT_DEPLOYMENT chatV4
azd env set AZURE_OPENAI_CHATGPT_DEPLOYMENT chat4o

azd env set AZURE_OPENAI_CHATGPT_MODEL gpt-35-turbo
azd env set AZURE_OPENAI_CHATGPT_MODEL gpt-4-32k
azd env set AZURE_OPENAI_CHATGPT_MODEL gpt-4o

azd env set AZURE_OPENAI_CHATGPT_DEPLOYMENT_CAPACITY 10

# only available in eastus2
azd env set AZURE_OPENAI_CHATGPT_DEPLOYMENT_VERSION 0301 
azd env set AZURE_OPENAI_CHATGPT_DEPLOYMENT_VERSION 0613
azd env set AZURE_OPENAI_CHATGPT_DEPLOYMENT_VERSION 2024-05-13

azd env set AZURE_OPENAI_EMB_MODEL_NAME text-embedding-3-large
azd env set AZURE_OPENAI_EMB_DIMENSIONS 3072
azd env set AZURE_OPENAI_EMB_DEPLOYMENT_VERSION 1

azd up

