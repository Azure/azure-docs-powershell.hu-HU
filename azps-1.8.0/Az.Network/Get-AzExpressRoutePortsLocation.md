---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
ms.openlocfilehash: 196cc354ddac7f317400b7baa665b8975dcc9df9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670570"
---
# Get-AzExpressRoutePortsLocation

## Áttekintés
Itt érheti el azokat a helyeket, amelyeken elérhetők a ExpressRoutePort-források.

## SZINTAXISA

```
Get-AzExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzExpressRoutePortsLocation** parancsmag segítségével megkeresheti azokat a helyeket, amelyeken elérhetők a ExpressRoutePort-források. A parancsmag az adott helyen adja meg a kívánt helyet, a parancsmag a hely részleteit (például a rendelkezésre álló sávszélességek listáját) jeleníti meg.

## Példák

### Példa 1
```powershell
PS C:\> Get-AzExpressRoutePortsLocation
```

Felsorolja azokat a helyeket, amelyeken elérhetők a ExpressRoutePort-források.

### 2. példa
```powershell
PS C:\> Get-AzExpressRoutePortsLocation -LocationName $loc
```

A hely $loc elérhető ExpressRoutePort-sávszélességek listája.

## PARAMÉTEREK

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSExpressRoutePortsLocation

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
