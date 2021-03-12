# Reading messages from Azure log analytics workspaxe and sending message to MS Teams

Monitoring failed Azure data factory pipelines. There is a query that runs every hour once and see if there are any failed pipline, this can be configured by changing the reccuring information.


## Requierments

+ Azure account 
+ ADF
+ Possibility to create resources 
+ Resource group
+ Logic app
+ Log analytics workspace
+ Diagnostics enabled on Data factory

+ Inside the azuredeloy script there is a possibility to add a error documentation link



## How to deploy 




Azure Cli installed for this or you can deploy the ARM template from Azure portal as well.


Chaneg the parameters file based on your needs

```


az group create --name rg-logic-app-d --location westeurope

az deployment group create \
  --name monitoring_adf_d \
  --resource-group rg-logic-app-d  \
  --template-file azuredeloy.json\
  --parameters azuredeploy.parameters.json


```

```
-> go azure portal and see if the logic app is there 

```



## Contributing

+ Feedback and everything else is always welcome. 

+ Some Design work would be nice 

+ Initial work:

Kaarel Kõrvemaa 
