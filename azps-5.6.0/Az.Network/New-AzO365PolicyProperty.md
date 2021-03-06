---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azo365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
ms.openlocfilehash: a2b3a4878db022018bd0fae1d8e43e3700dd5e35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921794"
---
# New-AzO365PolicyProperty

## SYNOPSIS
Hozzon létre egy Office 365-ös forgalomtörési házirendobjektumot.

## SZINTAXIS

```
New-AzO365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
Hozzon létre egy office 365-ös szabálytörési házirendet, amely a New-AzVpnSite és Update-AzVpnSite használható.
## PÉLDÁK

### 1. példa
```powershell
PS C:\> $policy = New-AzO365PolicyProperty -Allow -Optimize
```

Hozzon létre egy office 365-ös forgalom-törési házirendet, amely lehetővé teszi az adatforgalom engedélyezett és optimalizálható kategóriáját.

## PARAMETERS

### -Allow
Törd meg az engedélyezőkategória-forgalmat.

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

### -Alapértelmezett
Törje meg az alapértelmezett kategóriaforgalmat.

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

### - Optimalizálás
A kategória optimális forgalmának lebontása.

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

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Nincs

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
