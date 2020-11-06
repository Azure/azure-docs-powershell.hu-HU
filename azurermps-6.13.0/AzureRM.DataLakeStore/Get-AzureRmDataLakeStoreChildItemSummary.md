---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azureatalakestorechilditemsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreChildItemSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreChildItemSummary.md
ms.openlocfilehash: 83fb8b3ea5fdf9ad63983d2a3a3d23d402fbb5a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502960"
---
# Get-AzureRmDataLakeStoreChildItemSummary

## Áttekintés
A megadott elérési úton lévő teljes méret, fájlok és könyvtárak összegzése

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmDataLakeStoreChildItemSummary [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmDataLakeStoreChildItemSummary** lekéri egy adott útvonal tartalmi összegzését. A fájl, a könyvtárak és a megadott elérési út alatti fájlok teljes méretének kiszámítása.

## Példák

### Példa 1: mappa tartalmi összegzésének beszerzése
```
PS C:\> Get-AzureRmDataLakeStoreChildItemSummary -Account ContosoADL -Path /a -Concurrency 128
```

Felsorolja a teljes könyvtárak számát, a fájlok és a/a. alatti méretet.

## PARAMÉTEREK

### -Fiók
Az adattó áruházbeli fiókja a FileSystem művelet végrehajtásához

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Párhuzamosság
A párhuzamosan feldolgozott fájlok/könyvtárak számát jelzi.
Az alapértelmezett beállítás a rendszerspecifikáción alapuló legjobb munkamennyiségként fog kiszámításra.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path (elérési út)
A megadott adattó-fiók útvonala, amelyet le kell olvasnia.
A "/Folder/file.txt" formátumban lehet fájl vagy mappa, ahol az első "/" a DNS a fájlrendszer gyökerét jelzi.

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### System. String

### Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance

### System. Int32

## KIMENETEK

### Microsoft. Azure. Command. DataLakeStore. models. DataLakeStoreChildItemSummary

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
