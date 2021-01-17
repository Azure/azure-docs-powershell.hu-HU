---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
ms.openlocfilehash: 918ef18717cb09bad28ee10b91f635181dd5b3cb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380126"
---
# Get-AzExpressRoutePortsLocation

## SYNOPSIS
Beszerzheti az ExpressRoutePort-erőforrások rendelkezésre álló helyeit.

## SZINTAXIS

```
Get-AzExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzExpressRoutePortsLocation** parancsmaggal lekérheti az ExpressRoutePort-erőforrások rendelkezésre álló helyeit. A parancsmag adott helyet ad meg bemenetként, és megjeleníti az adott hely részleteit, azaz az adott helyen rendelkezésre álló sávszélességek listáját.

## PÉLDÁK

### 1. példa
```powershell
PS C:\> Get-AzExpressRoutePortsLocation
```

Felsorolja azokat a helyeket, ahol az ExpressRoutePort-erőforrások elérhetők.

### 2. példa
```powershell
PS C:\> Get-AzExpressRoutePortsLocation -LocationName $loc
```

Az ExpressRoutePort-sávszélességek listája a $loc.

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

### -LocationName
A hely neve.

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

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
