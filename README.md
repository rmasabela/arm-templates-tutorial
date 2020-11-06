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