---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
ms.openlocfilehash: 14c0ec31f10a6405fb2a3f412f004d53dbdeb9a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156978"
---
# Get-AzLocalNetworkGateway

## SYNOPSIS
Helyi hálózati átjárót kap

## SZINTAXIS

```
Get-AzLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A helyi hálózati átjáró a virtuális magánhálózati eszköz helyszíni objektuma.
A **Get-AzLocalNetworkGateway** parancsmag a név és az erőforráscsoport neve alapján visszaadja a helyi átjárónak megfelelő objektumot.

## PÉLDÁK

### 1. példa: Helyi hálózati átjáró létrehozása
```powershell
Get-AzLocalNetworkGateway -Name myLocalGW1 -ResourceGroupName myRG

Name                     : myLocalGW1
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

A helyi hálózati átjáró "myLocalGW1" nevű objektumát adja eredményül a "myRG" erőforráscsoporton belül.

### 2. példa: Helyi hálózati átjárók be szerezni szűrés használatával
```powershell
Get-AzLocalNetworkGateway -Name myLocalGW* -ResourceGroupName myRG

Name                     : myLocalGW1
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null

Name                     : myLocalGW2
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW2
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

A helyi hálózati átjárónak a "myRG" erőforráscsoporton belüli "myLocalGW" névvel kezdődő nevű objektumát adja eredményül.

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

### Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[New-AzLocalNetworkGateway](./New-AzLocalNetworkGateway.md)

[Remove-AzLocalNetworkGateway](./Remove-AzLocalNetworkGateway.md)

[Set-AzLocalNetworkGateway](./Set-AzLocalNetworkGateway.md)
