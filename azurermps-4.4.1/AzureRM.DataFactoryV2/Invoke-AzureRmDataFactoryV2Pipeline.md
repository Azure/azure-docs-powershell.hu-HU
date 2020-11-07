---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 45095fefa0d4866a40b59c61ca02a98c118cf37a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679784"
---
# Invoke-AzureRmDataFactoryV2Pipeline

## Áttekintés
  Arra hívja fel a futószalagot, hogy indítsa el a futtatását.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ByFactoryNameByParameterFile (alapértelmezett)
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [-WhatIf] [-Confirm]
```

### ByPipelineObjectByParameterFile
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>] [-WhatIf] [-Confirm]
```

### ByPipelineObjectByParameterObject
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>] [-WhatIf] [-Confirm]
```

### ByFactoryNameByParameterObject
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [-WhatIf] [-Confirm]
```

## Leírás
Az **AzureRmDataFactoryV2Pipeline** parancs a megadott csővezetéken futtatja a futást, és a futtatott érték azonosítóját adja eredményül. Ezt a GUID-ot átadhatja a **Get-AzureRmDataFactoryV2PipelineRun** vagy a **Get-AzureRmDataFactoryV2ActivityRun** , ha további részleteket szeretne kapni erről a futtatásról.

## Példák

### 1. példa: a futószalag indítását kezdeményezi a futtatáshoz
```
PS C:\> Invoke-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

Ez a parancs elindítja a Run for "DPWikisample" ("WikiADF") csővezetéket az "" gyárban.

## PARAMÉTEREK

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataFactoryName
Az adatgyári név.

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ParameterFile
Annak a fájlnak a neve, amelyen a csővezeték-Futtatás paraméterei láthatók.

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByPipelineObjectByParameterFile
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Paraméter
A csővezeték-Futtatás paraméterei.

```yaml
Type: Hashtable
Parameter Sets: ByPipelineObjectByParameterObject, ByFactoryNameByParameterObject
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InputObject
Az Data Factory objektum.

```yaml
Type: PSPipeline
Parameter Sets: ByPipelineObjectByParameterFile, ByPipelineObjectByParameterObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PipelineName
A csővezeték neve.

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforrás csoport neve.

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WhatIf
Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## BEMENETEK

### Microsoft. Azure. Command. DataFactoryV2. models. PSPipeline
System. String System. Collections. Hashtable


## KIMENETEK

### Microsoft. Azure. Command. DataFactoryV2. models. PSPipeline


## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
[Get-AzureRmDataFactoryV2PipelineRun]()

[Get-AzureRmDataFactoryV2ActivityRun]()

