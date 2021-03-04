---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 54af80b230c3cb031e8927a82ec3536cc1a81ec0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943209"
---
# Disable-AzDataCollection

## SYNOPSIS
Az Azure PowerShell-parancsmagok fejlesztése érdekében leiratkozás az adatgyűjtésről. Az adatokat alapértelmezés szerint gyűjtjük, hacsak Ön kifejezetten le nem tiltja.

## SZINTAXIS

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS

A parancsmag az adatgyűjtés `Disable-AzDataCollection` letiltása. Az Azure PowerShell alapértelmezés szerint automatikusan telemetriai adatokat gyűjt. Az adatgyűjtés letiltásához explicit módon le kell tiltania az adatgyűjtést. A Microsoft összegyűjti az összegyűjtött adatokat a használati minták azonosítása, a gyakori problémák azonosítása és az Azure PowerShell használatának javítása érdekében. A Microsoft Azure PowerShell nem gyűjt személyes vagy személyes adatokat. Ha korábban már kikapcsolta, a parancsmag futtatásával engedélyezze újra az adatgyűjtést az aktuális gépen `Enable-AzDataCollection` lévő felhasználó számára.

## PÉLDÁK

### 1. példa: Az aktuális felhasználó adatgyűjtésének letiltása

Az alábbi példa bemutatja, hogyan tilthatja le az adatgyűjtést az aktuális felhasználó számára.

```powershell
Disable-AzDataCollection
```

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

### -Confirm

A parancsmag futtatása előtt a rendszer megerősítést kér.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Nincs

## KIMENETEK

### System.Void

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Enable-AzDataCollection](./Enable-AzDataCollection.md)
