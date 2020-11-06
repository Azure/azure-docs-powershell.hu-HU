---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 4d9442ba87ba46704aaa93b31f41f111519c980b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504367"
---
# Get-AzureRmExpressRouteCircuitConnectionConfig

## Áttekintés
ExpressRoute-áramköri kapcsolati konfigurációt kap, amely a ExpressRouteCircuit privát kinézetéhez van társítva.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmExpressRouteCircuitConnectionConfig** parancsmag kikeresi a magánjellegű kapcsolattal rendelkező ExpressRoute-áramkörhöz társított áramköri kapcsolat konfigurációját.

## Példák

### Példa 1: ExpressRoute-áramkör áramkör-kapcsolati konfigurációjának megjelenítése
```
$circuit_init = Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### 2. példa: ExpressRoute-áramkörrel társított áramköri kapcsolati erőforrás csővezetékekkel való használata
```
Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

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

### -ExpressRouteCircuit
Az áramköri kapcsolat konfigurációját tartalmazó ExpressRoute Circuit objektum.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (név)
A lekérdezni kívánt áramkör-kapcsolat konfigurációjának neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit
Paraméterek: ExpressRouteCircuit (ByValue)

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSExpressRouteCircuitConnection

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmExpressRouteCircuit](Get-AzureRmExpressRouteCircuit.md)

[Add-AzureRmExpressRouteCircuitConnectionConfig](Add-AzureRmExpressRouteCircuitConnectionConfig.md)

[Remove-AzureRmExpressRouteCircuitConnectionConfig](Remove-AzureRmExpressRouteCircuitConnectionConfig.md)

[Set-AzureRmExpressRouteCircuitConnectionConfig](Set-AzureRmExpressRouteCircuitConnectionConfig.md)

[Új – AzureRmExpressRouteCircuitConnectionConfig](New-AzureRmExpressRouteCircuitConnectionConfig.md)
