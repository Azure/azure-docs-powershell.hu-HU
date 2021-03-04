---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: e4b972944f757c9b0072f091dc820de5fa5d5b1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924745"
---
# Get-AzVirtualNetworkGatewayConnection

## SYNOPSIS
Virtuális hálózati átjárókapcsolatot létesít

## SZINTAXIS

```
Get-AzVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A virtuális hálózati átjáró kapcsolata az Az Azure virtuális hálózati átjáróhoz csatlakoztatott IPsec-csatornát (Site-to-Site vagy Vnet-to-Vnet) képviselő objektum.
A **Get-AzVirtualNetworkGatewayConnection** parancsmag a kapcsolat objektumát adja vissza a Név és az Erőforráscsoport neve alapján.
Ha a **Get-AzVirtualNetworkGatewayConnection** parancsmagot a -Name paraméter megadása nélkül bocsátotta ki, a kimenet nem fogja tartalmazni a ConnectionStatus és a SharedKey adatait.

## PÉLDÁK

### 1: Virtuális hálózati átjárókapcsolat létrehozása
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

A virtuális hálózati átjáró kapcsolatának "myTunnel" nevű objektumát adja eredményül a "myRG" erőforráscsoporton belül.

### 2: Az összes virtuális hálózati átjárókapcsolat behozása szűrés használatával
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel* -ResourceGroupName myRG
```

Visszaadja a "myTunnel" kezdetű virtuális hálózati átjárókapcsolatokat a "myRG" erőforráscsoporton belül.

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

### -Name
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### -ResourceGroupName
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[New-AzVirtualNetworkGatewayConnection](./New-AzVirtualNetworkGatewayConnection.md)

[Remove-AzVirtualNetworkGatewayConnection](./Remove-AzVirtualNetworkGatewayConnection.md)

[Set-AzVirtualNetworkGatewayConnection](./Set-AzVirtualNetworkGatewayConnection.md)
