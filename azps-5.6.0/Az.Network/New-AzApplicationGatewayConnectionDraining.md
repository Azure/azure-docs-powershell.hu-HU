---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: b5bfedea118aa3770bac3141d05db379a4655906
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006214"
---
# New-AzApplicationGatewayConnectionDraining

## SYNOPSIS
Új kapcsolatelvezetési konfigurációt hoz létre a háttér HTTP-beállításokhoz.

## SZINTAXIS

```
New-AzApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **New-AzApplicationGatewayConnectionDraining** parancsmag új kapcsolatelvezetési konfigurációt hoz létre a háttér HTTP-beállításokhoz.

## PÉLDÁK

### 1. példa
```
PS C:\> $connectionDraining = New-AzApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

A parancs létrehoz egy új kapcsolatelvezetési konfigurációt, amelynél az Engedélyezett beállítás Igaz, az DrainTimeoutInSec pedig 42 másodpercre van állítva, és a beállítást $connectionDraining.

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

### -DrainTimeoutInSec
Aktív a kapcsolatelvezetés másodpercek alatt lefolyatva.
Az elfogadható értékek 1 másodperctől 3600 másodpercig esnek.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Engedélyezve
Hogy engedélyezve van-e a kapcsolat lemerülése.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Nincs

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzApplicationGatewayConnectionDraining](./Get-AzApplicationGatewayConnectionDraining.md)

[Remove-AzApplicationGatewayConnectionDraining](./Remove-AzApplicationGatewayConnectionDraining.md)

[Set-AzApplicationGatewayConnectionDraining](./Set-AzApplicationGatewayConnectionDraining.md)

