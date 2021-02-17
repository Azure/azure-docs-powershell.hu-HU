---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
ms.openlocfilehash: 2eeaf4d4c1f0a2cf97359610d34963e32b50d1c9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147571"
---
# Get-AzMlCommitmentPlan

## SYNOPSIS
Egy vagy több kötelezettségvállalási csomag összegző adatait olvassa be.

## SZINTAXIS

```
Get-AzMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
Beolvassa a kötelezettségvállalási terv adatait.
A átadott paraméterektől függően a parancsmag adott kötelezettségvállalási tervet, az aktuális előfizetés egy adott erőforráscsoportra vonatkozó kötelezettségvállalási tervek gyűjteményét vagy a kötelezettségvállalási csomagok gyűjteményét adja vissza az aktuális előfizetésen belül.

## PÉLDÁK

### 1. példa: Konkrét kötelezettségvállalási csomag lekérte
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### 2. példa: A kötelezettségvállalási terv összes erőforrásának lekérte az aktuális előfizetést
```
Get-AzMlCommitmentPlan
```

### 3. példa: Az aktuális előfizetés és adott erőforráscsoport összes kötelezettségvállalási csomagja
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
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
Az Azure ML kötelezettségvállalási terv erőforráscsoportja neve.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Nincs

## KIMENETEK

### Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan

## MEGJEGYZÉSEK
Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, gépi, gépi tanulás, azureml

## KAPCSOLÓDÓ HIVATKOZÁSOK
