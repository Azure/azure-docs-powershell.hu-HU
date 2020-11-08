---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 27b3565191d7de110a5ba3a1e37d204fe3301cbf
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/30/2020
ms.locfileid: "94015080"
---
# Disable-AzDataCollection

## Áttekintés
Az Azure PowerShell-parancsmagok fejlesztésére az adatok gyűjtésének kijavítása. Az adatokat alapértelmezés szerint gyűjtjük, hacsak nem kifejezetten kikapcsolja.

## SZINTAXISA

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás

A `Disable-AzDataCollection` parancsmag az adatgyűjtési szolgáltatás kikapcsolásához használható. Az Azure PowerShell alapértelmezés szerint automatikusan gyűjti a telemetriai adatokat. Az adatgyűjtés letiltásához explicit módon le kell jelentkeznie. A Microsoft összesíti az összegyűjtött adatokat a használati minták meghatározására, a gyakori problémák felismerésére, valamint az Azure PowerShell használatának javítására. A Microsoft Azure PowerShell nem gyűjt semmilyen személyes vagy személyes adatot. Ha korábban kikapcsolta a rendszert, futtassa a `Enable-AzDataCollection` parancsmagot, és engedélyezze újra a jelenlegi felhasználó adatgyűjtését az aktuális gépen.

## Példák

### 1. példa: az aktuális felhasználó adatgyűjtésének letiltása

Az alábbi példa azt szemlélteti, hogy miként tilthatja le az aktuális felhasználó adatgyűjtését.

```powershell
Disable-AzDataCollection
```

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

### – Megerősítés

A parancsmag futtatása előtt kéri a megerősítést.

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

Annak megjelenítése, hogy mi történik, ha a parancsmag fut. A parancsmag nem fut.

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

Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters)című témakörben talál.

## BEMENETEK

### Nincs

## KIMENETEK

### System. Void

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Enable-AzDataCollection](./Enable-AzDataCollection.md)
