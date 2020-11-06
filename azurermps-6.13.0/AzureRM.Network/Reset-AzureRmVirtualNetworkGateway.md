---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: c5d77619fa5f89c60ce20a097e096709e9a48bae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503487"
---
# Reset-AzureRmVirtualNetworkGateway

## Áttekintés
A virtuális hálózat átjárójának alaphelyzetbe állítása

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A virtuális hálózat átjárójának alaphelyzetbe állítása

## Példák

### Példa 1:
```
$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway
```

## PARAMÉTEREK

### -AsJob
A parancsmag futtatása a háttérben

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -GatewayVip
Az átjáró VIP az adott átjáró alaphelyzetbe állításához (például Active-Active funkció engedélyezett átjárók esetén) Alapértelmezés szerint az átjáró elsődleges példánya alapértelmezés szerint vissza fog állítani, ha nem ad át értéket.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
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

### Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway
Paraméterek: VirtualNetworkGateway (ByValue)

### System. String
Paraméterek: GatewayVip (ByValue)

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmVirtualNetworkGateway](./Get-AzureRmVirtualNetworkGateway.md)

[Új – AzureRmVirtualNetworkGateway](./New-AzureRmVirtualNetworkGateway.md)

[Remove-AzureRmVirtualNetworkGateway](./Remove-AzureRmVirtualNetworkGateway.md)

[Átméretezés-AzureRmVirtualNetworkGateway](./Resize-AzureRmVirtualNetworkGateway.md)

[Set-AzureRmVirtualNetworkGateway](./Set-AzureRmVirtualNetworkGateway.md)


