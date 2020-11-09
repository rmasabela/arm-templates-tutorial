# arm-templates-tutorial
Azure Resource Manager template tutorial

## 01. Create first template

```bash
templateFile="01-first-template/azuredeploy.json"
az deployment group create \
  --name blanktemplate \
  --resource-group PilotoDevOps \
  --template-file $templateFile \
  --verbose
```

## 02. Add resource

```bash
templateFile="02-add-resource/azuredeploy.json"
az deployment group create \
  --name addstorage \
  --resource-group PilotoDevOps \
  --template-file $templateFile \
  --verbose
```

## 03. Add parameters

```bash
templateFile="03-add-parameters/azuredeploy.json"
az deployment group create \
  --name addstoragewithparams \
  --resource-group PilotoDevOps \
  --template-file $templateFile \
  --parameters storageName=storagedemordma \
  --verbose
```

```bash
templateFile="03-add-parameters/azuredeploy.json"
az deployment group create \
  --name usenondefaultsku \
  --resource-group PilotoDevOps \
  --template-file $templateFile \
  --parameters storageName=storagedemordma storageSKU=Standard_GRS \
  --verbose
```

```bash
templateFile="03-add-parameters/azuredeploy.json"
az deployment group create \
  --name useinvalidsku \
  --resource-group PilotoDevOps \
  --template-file $templateFile \
  --parameters storageName=storagedemordma storageSKU=Basic \
  --verbose
```