---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D345
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerIpAddressRange.md
ms.openlocfilehash: 5bb661dbc5a65b9a245fcfa35cdc194bbcded1eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492677"
---
# Remove-AzureRmTrafficManagerIpAddressRange

## Áttekintés
Címtartomány vagy alhálózat eltávolítása egy helyi forgalomirányítási végpont-objektumból.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Remove-AzureRmTrafficManagerIpAddressRange -First <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **Remove-AzureRmTrafficManagerIpAddressRange** parancsmag a helyi Azure Traffic Manager végpont-objektumból távolítja el az IP-cím tartományát.
Végpontot a New-AzureRmTrafficManagerEndpoint vagy Get-AzureRmTrafficManagerEndpoint parancsmagok használatával kaphat.

Ez a parancsmag a helyi végpont-objektumon működik.
Végezze el a módosításokat a forgalomirányító végpontján a Set-AzureRmTrafficManagerEndpoint parancsmag használatával.

## Példák

### 1. példa: az IP-címtartományok eltávolítása végpontról
```
PS C:\> $TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

Az első parancs megkapja a contoso nevű Azure-végpontot a ContosoProfile nevű ResourceGroup11 nevű erőforráscsoport profiljában, majd az adott objektumot a $TrafficManagerEndpoint változóban tárolja.
A második parancs eltávolítja az IP-címtartományt a $TrafficManagerEndpointban tárolt végpontból.
A végleges parancs a Traffic Manager végpontját frissíti a $TrafficManagerEndpoint helyi értékének megfelelően.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -TrafficManagerEndpoint
Helyi **TrafficManagerEndpoint** -objektumot ad meg.
Ez a parancsmag módosította ezt a helyi objektumot.
**TrafficManagerEndpoint** -objektum beolvasásához használja a Get-AzureRmTrafficManagerEndpoint vagy New-AzureRmTrafficManagerEndpoint parancsmagot.

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

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut. A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Első
Az első IP-címet adja meg az eltávolítandó adattartománnyal.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. Azure. commands. Network. TrafficManagerEndpoint
Ez a parancsmag egy **TrafficManagerEndpoint** -objektumot fogad erre a parancsmagra.

## KIMENETEK

### Microsoft. Azure. commands. Network. TrafficManagerEndpoint
Ez a parancsmag egy módosított TrafficManagerEndpoint objektumot ad eredményül.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureRmTrafficManagerIpAddressRange](./Add-AzureRmTrafficManagerIpAddressRange.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerEndpoint.md)

[Új – AzureRmTrafficManagerEndpoint](./New-AzureRmTrafficManagerEndpoint.md)

[Set-AzureRmTrafficManagerEndpoint](./Set-AzureRmTrafficManagerEndpoint.md)
