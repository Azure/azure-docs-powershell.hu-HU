---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/set-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 99f621824d10b574c7f64fb7653bc4154ba6766e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672506"
---
# Set-AzureRmTrafficManagerEndpoint

## Áttekintés
A Traffic Manager végpontjának frissítése.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **set-AzureRmTrafficManagerEndpoint** parancsmag az Azure Traffic Manager végpontját frissíti.
Ez a parancsmag frissíti a helyi végpont-objektum beállításait.
A végpont-objektumot a *TrafficManagerEndpoint* paraméterrel vagy a csővezeték használatával is megadhatja.

A végpontokat az Get-AzureRmTrafficManagerEndpoint parancsmag használatával is beolvashatja.
Módosítsa az objektumot helyileg, majd használja a **set-AzureRmTrafficManagerEndpoint** a módosítások véglegesítéséhez.

## Példák

### Példa 1: végpont frissítése
```
PS C:\>$TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

Az első parancs az Azure Traffic Manager végpontját a **Get-AzureRmTrafficManagerEndpoint** parancsmag segítségével kapja meg.
A parancs helyileg, a $TrafficManagerEndpoint változóban tárolja a végpontot.

A második parancs helyileg módosítja a végpontot.
Ez a parancs 20 értékre módosítja a végpont vastagságát.

A harmadik parancs a forgalmi vezető végpontját frissíti a $TrafficManagerEndpoint helyi értékének megfelelően.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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
Type: TrafficManagerEndpoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. Azure. commands. Network. TrafficManagerEndpoint
Ez a parancsmag a **TrafficManagerEndpoint** -objektumot fogadja el.

## KIMENETEK

### Microsoft. Azure. commands. Network. TrafficManagerEndpoint
Ez a parancsmag egy **TrafficManagerEndpoint** objektumot ad eredményül.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

