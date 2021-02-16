---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 0000a7a1dba5f175d70fb93631176a49a9da2d13
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149802"
---
# Set-AzTrafficManagerEndpoint

## SYNOPSIS
Frissíti a Traffic Manager-végpontot.

## SZINTAXIS

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Set-AzTrafficManagerEndpoint** parancsmag frissíti az Azure Traffic Manager egyik végpontját.
Ez a parancsmag frissíti a beállításokat egy helyi végpontobjektumból.
A végpontobjektumot a *TrafficManagerEndpoint* paraméterrel vagy a folyamat használatával adhatja meg.

A végpontot képviselő helyi objektumot a Get-AzTrafficManagerEndpoint használatával szerezheti be.
Módosítsa az objektumot helyben, majd a **Set-AzTrafficManagerEndpoint** segítségével véglegesítse a módosításokat.

## PÉLDÁK

### 1. példa: Végpont frissítése
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

Az első parancs a **Get-AzTrafficManagerEndpoint** parancsmag használatával kap egy Azure Traffic Manager-végpontot.
A parancs helyileg tárolja a végpontot a $TrafficManagerEndpoint változóban.

A második parancs helyileg módosítja a végpontot.
Ez a parancs 20-ra módosítja a végpont súlyát.

A harmadik parancs frissíti a végpontot a Traffic Managerben úgy, hogy megfeleljen a helyi $TrafficManagerEndpoint.

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

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

### -TrafficManagerEndpoint
Helyi **TrafficManagerEndpoint-objektumot ad** meg.
Ez a parancsmag frissíti a Traffic Managert, hogy megfeleljen ennek a helyi objektumnak.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## KIMENETEK

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
