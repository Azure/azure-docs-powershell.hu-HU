---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 33712b9813d6c23ed72097597d94a22bf7644992
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938561"
---
# Set-AzPublicIpAddress

## SYNOPSIS
Nyilvános IP-cím frissítése.

## SZINTAXIS

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
A **Set-AzPublicIpAddress** parancsmag frissíti a nyilvános IP-címet.

## PÉLDÁK

### 1: Nyilvános IP-cím kiosztási módszerének módosítása
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 Az első parancs a nyilvános IP-cím erőforrást kapja meg, $publicIPName az erőforráscsoportban $rgName.
A második parancs a nyilvános IP-címobjektum kiosztási módját "Statikusra" állítja.
Set-AzPublicIPAddress parancs frissíti a nyilvános IP-címforrást a frissített objektummal, és "Statikus" módra módosítja a terhelési módot. A nyilvános IP-címeket a rendszer azonnal kiosztja.

### 2: NYILVÁNOS IP-cím DNS-tartománycímkéinek hozzáadása
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings = @{"DomainNameLabel" = "newdnsprefix"}
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

Az első parancs a nyilvános IP-cím erőforrást kapja meg, $publicIPName az erőforráscsoportban $rgName.
A második parancs a DomainNameLabel tulajdonságot a szükséges DNS-előtagra állítja.
Set-AzPublicIPAddress parancs frissíti a nyilvános IP-cím erőforrást a frissített objektummal. A DomainNameLabel & Fqdn a várt módon módosul.
    
### 3: Nyilvános IP-cím DNS-tartománycímkéinek módosítása
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

Az első parancs a nyilvános IP-cím erőforrást kapja meg, $publicIPName az erőforráscsoportban $rgName.
A második parancs a DomainNameLabel tulajdonságot a szükséges DNS-előtagra állítja.
Set-AzPublicIPAddress parancs frissíti a nyilvános IP-cím erőforrást a frissített objektummal. A DomainNameLabel & Fqdn a várt módon módosul.

## PARAMETERS

### -AsJob
Parancsmag futtatása a háttérben

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

### -PublicIpAddress
Egy olyan nyilvános IP-címobjektumot ad meg, amely azt az állapotot képviseli, amelyben a nyilvános IP-címet be kell állítani.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzPublicIpAddress](./Get-AzPublicIpAddress.md)

[New-AzPublicIpAddress](./New-AzPublicIpAddress.md)

[Remove-AzPublicIpAddress](./Remove-AzPublicIpAddress.md)


