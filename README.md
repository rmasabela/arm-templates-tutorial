# arm-templates-tutorial
Azure Resource Manager template tutorial

## 01. Create first template

```bash
templateFile="01-first-template/azuredeploy.json"
az deployment group create \
  --name blanktemplate \
  --resource-group PilotoDevOps \
  --template-file $templateFile
```