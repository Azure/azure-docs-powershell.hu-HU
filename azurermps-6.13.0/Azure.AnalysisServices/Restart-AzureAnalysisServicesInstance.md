---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/restart-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
ms.openlocfilehash: 496c0410808604303ab60d8ad4d989e838828bf7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492949"
---
# Restart-AzureAnalysisServicesInstance

## Áttekintés
Az Analysis Services Server példányának újraindítása az aktuálisan bejelentkezett környezetben, az Add-AzureAnalysisServicesAccount parancsban megadott módon

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Restart-AzureAnalysisServicesInstance -Instance <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
Az Restart-AzureAnalysisServicesInstance parancsmag az Azure Analysis Services-kiszolgáló egy példányát indítja el újra

## Példák

### Példa 1
```
PS C:\>Restart-AzureAnalysisServicesInstance
Instance: testserver
```

Ez a parancs elindítja a "TestServer" szervert a Add-AzureAnalysisServicesAccount parancsban megadott környezetben

## PARAMÉTEREK

### -Példány
Az Analysis Services-kiszolgálópéldány újraindításának neve

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

### -PassThru
Ez a beállítás akkor igaz, ha a parancs sikeres.

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

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

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
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### System. Boolean

## MEGJEGYZI
Alias: Restart-AzureAsInstance

## KAPCSOLÓDÓ HIVATKOZÁSOK
