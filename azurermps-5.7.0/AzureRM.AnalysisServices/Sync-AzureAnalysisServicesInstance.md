---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/sync-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
ms.openlocfilehash: f3fb2377fd78db4b330afd39a8691f958597f07a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493797"
---
# Sync-AzureAnalysisServicesInstance

## Áttekintés

A megadott adatbázis szinkronizálása az Analysis Services-kiszolgáló meghatározott példányán az Add-AzureAnalysisServicesAccount parancsban megadott, a jelenleg bejelentkezett környezetben található összes lekérdezés scaleout-példányához

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Sync-AzureAnalysisServicesInstance [-Instance] <String> [-Database] <String> [-Passthru]
```

## Leírás

A Sync-AzureAnalysisServicesInstance parancsmag az Analysis Services Server meghatározott példányának egy adott adatbázisát szinkronizálja az aktuálisan bejelentkezett scaleout-példányokkal az Add-AzureAnalysisServicesAccount parancsban megadott módon.

## Példák

### Példa 1

```
PS C:\>Sync-AzureAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

Ez a parancs szinkronizálja a SalesOrders nevű adatbázist a "contoso" nevű kiszolgálón a környezet westus.asazure.windows.net, feltéve, hogy a felhasználó bejelentkezett erre a környezetre Add-AzureAnalysisServicesAccount parancs segítségével.

## PARAMÉTEREK

### -Példány

Az Analysis Services-kiszolgálópéldány újraindításának neve

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Database (adatbázis)

A szinkronizálandó adatbázis identitása

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru

Ez a beállítás akkor igaz, ha a parancs sikeres.

```yaml
Type: Switch
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### System. Boolean

## MEGJEGYZI

Alias: Sync-AzureAsInstance

## KAPCSOLÓDÓ HIVATKOZÁSOK
