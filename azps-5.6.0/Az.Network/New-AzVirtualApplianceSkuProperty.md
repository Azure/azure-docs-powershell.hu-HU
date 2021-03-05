---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualapplianceskuproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
ms.openlocfilehash: 0179a033d9cc99ff2f373dbaceb1bcb97ab3468f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006181"
---
# New-AzVirtualApplianceSkuProperty

## SYNOPSIS
Definiáljon egy hálózati virtuális eszköz termékváltozatot az erőforráshoz.

## SZINTAXIS

```
New-AzVirtualApplianceSkuProperty -VendorName <String> -BundledScaleUnit <String> -MarketPlaceVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A New-AzVirtualApplianceSkuProperties parancs meghatároz egy termékváltozatot a hálózati virtuális eszköz erőforráshoz.

## PÉLDÁK

### 1. példa
```powershell
PS C:\> $var=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
```

Hozzon létre egy virtuális berendezés-termékváltozat tulajdonságai objektumot, amely a New-AzNetworkVirtualAppliance használható. 

## PARAMETERS

### -BundledScaleUnit
A kötegelt méretarány.

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

### -MarketPlaceVersion
A piachely verziója.

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

### -VendorName
A szállító neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Nincs

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
