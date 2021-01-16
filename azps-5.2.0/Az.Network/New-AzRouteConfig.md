---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteConfig.md
ms.openlocfilehash: 54a12f4485e56b592b2e42d7b9515af595d4b6c4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367539"
---
# New-AzRouteConfig

## SYNOPSIS
Útvonalat hoz létre egy útvonaltáblához.

## SZINTAXIS

```
New-AzRouteConfig [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## LEÍRÁS
A **New-AzRouteConfig** parancsmag létrehoz egy útvonalat egy Azure útválasztási táblához.

## PÉLDÁK

### 1. példa: Útvonal létrehozása
```powershell
PS C:\>$Route = New-AzRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> $Route
Name              : Route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

Az első parancs létrehoz egy Route07 nevű útvonalat, majd tárolja azt a $Route változóban.
Ez az útvonal csomagokat továbbít a helyi virtuális hálózatra.
A második parancs megjeleníti az útvonal tulajdonságait.

### 2. példa

Útvonalat hoz létre egy útvonaltáblához. (automatikusan generált)

<!-- Aladdin Generated Example -->
```powershell
New-AzRouteConfig -AddressPrefix 10.1.0.0/16 -Name 'Route07' -NextHopIpAddress '12.0.0.5' -NextHopType 'VnetLocal'
```

## PARAMETERS

### -AddressPrefix
Az útvonal célhelyét adja meg Classless Interdomain Routing (CIDR) formátumban.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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
Az útvonal nevét adja meg.

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

### -NextHopIpAddress
Az Azurevirtual-hálózathoz adott virtuális készülék IP-címét adja meg.
Ez az útvonal csomagokat továbbít erre a címre.
Ezt a paramétert csak akkor adja meg, ha a VirtualAppliance értéket adja meg a *NextHopType paraméterhez.*

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NextHopType
Meghatározza, hogy ez az útvonal hogyan továbbítja a csomagokat.
A paraméter elfogadható értékei a következőek:
- Internet.
Az Azure által biztosított alapértelmezett internetes átjáró. 
- Nincs.
Ha ezt az értéket adja meg, az útvonal nem továbbítja a csomagokat. 
- VirtualAppliance.
Egy virtuális eszköz, amely hozzáadva az Azure virtuális hálózatához. 
- VirtualNetworkGateway.
Azure server-to-server virtual private network gateway. 
- VnetLocal.
A helyi virtuális hálózat.
Ha két alhálózata van: 10.1.0.0/16 és 10.2.0.0/16 ugyanabban a virtuális hálózatban, válassza ki az egyes alhálózatok VnetLocal-értékét a másik alhálózatra való továbbításhoz.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

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
A parancsmag futtatásakor a program megjeleníti, hogy mi történik. A parancsmag nem fut.

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

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSRoute

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzRouteConfig](./Add-AzRouteConfig.md)

[Get-AzRouteConfig](./Get-AzRouteConfig.md)

[Remove-AzRouteConfig](./Remove-AzRouteConfig.md)

[Set-AzRouteConfig](./Set-AzRouteConfig.md)


