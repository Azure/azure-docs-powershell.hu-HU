---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: f0b081911d1bcd2a2b195d3185eb3b36505060c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672716"
---
# Get-AzureRmMlCommitmentPlan

## Áttekintés
Lekérdezi egy vagy több kötelezettségvállalási terv összefoglaló adatát.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
Kikeresi a kötelezettségvállalási terv adatait.
Az átadott paramenters függően a parancsmag egy konkrét kötelezettségvállalási tervet ad eredményül, amely egy adott erőforráscsoport számára az aktuális előfizetésben, illetve az aktuális előfizetéshez tartozó kötelezettségvállalási tervek gyűjteménye.

## Példák

### Példa 1: konkrét kötelezettségvállalási terv beszerzése
```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### 2. példa: az összes kötelezettségvállalási terv erőforrásainak beolvasása a jelenlegi előfizetésben
```
Get-AzureRmMlCommitmentPlan
```

### 3. példa: az összes kötelezettségvállalási terv beszerzése az aktuális előfizetésben és az adott erőforráscsoportben
```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A kötelezettségvállalási terv neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Az Azure ML kötelezettségvállalási csomag erőforráscsoport neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan

## MEGJEGYZI
Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml

## KAPCSOLÓDÓ HIVATKOZÁSOK
