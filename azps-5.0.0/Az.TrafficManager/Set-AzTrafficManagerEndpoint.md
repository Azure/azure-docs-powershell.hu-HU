---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 0000a7a1dba5f175d70fb93631176a49a9da2d13
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195646"
---
# Set-AzTrafficManagerEndpoint

## Áttekintés
A Traffic Manager végpontjának frissítése.

## SZINTAXISA

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **set-AzTrafficManagerEndpoint** parancsmag az Azure Traffic Manager végpontját frissíti.
Ez a parancsmag frissíti a helyi végpont-objektum beállításait.
A végpont-objektumot a *TrafficManagerEndpoint* paraméterrel vagy a csővezeték használatával is megadhatja.

A végpontokat az Get-AzTrafficManagerEndpoint parancsmag használatával is beolvashatja.
Módosítsa az objektumot helyileg, majd használja a **set-AzTrafficManagerEndpoint** a módosítások véglegesítéséhez.

## Példák

### Példa 1: végpont frissítése
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

Az első parancs az Azure Traffic Manager végpontját a **Get-AzTrafficManagerEndpoint** parancsmag segítségével kapja meg.
A parancs helyileg, a $TrafficManagerEndpoint változóban tárolja a végpontot.

A második parancs helyileg módosítja a végpontot.
Ez a parancs 20 értékre módosítja a végpont vastagságát.

A harmadik parancs a forgalmi vezető végpontját frissíti a $TrafficManagerEndpoint helyi értékének megfelelően.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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
Helyi **TrafficManagerEndpoint** -objektumot ad meg.
Ez a parancsmag frissíti a Traffic Manager alkalmazást a helyi objektum egyeztetéséhez.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. Azure. Command. TrafficManager. models. TrafficManagerEndpoint

## KIMENETEK

### Microsoft. Azure. Command. TrafficManager. models. TrafficManagerEndpoint

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
