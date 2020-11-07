---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/move-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Move-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Move-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 5e6fb437833db3f4278335f67693d084c2d6d95b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672650"
---
# Move-AzureRmDataLakeStoreItem

## Áttekintés
Egy fájl vagy mappa áthelyezése vagy átnevezése az adattó áruházban.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Move-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Leírás
Az **Move-AzureRmDataLakeStoreItem** parancsmag az Adattó áruházban lévő fájlok vagy mappák áthelyezésére vagy átnevezésére.

## Példák

### 1. példa: elem áthelyezése és átnevezése
```
PS C:\>Move-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

Ez a parancs átnevezi az elemet File.txt RenamedFile.txt és egy másik mappába helyezi át.

## PARAMÉTEREK

### -Fiók
Az adattó-tároló fiók nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Destination (cél)
Az az adattó-tároló elérési útját adja meg, amelybe az elemet át szeretné helyezni, kezdve a legfelső szintű könyvtárral (/).

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Jelzi, hogy az adott művelet felülírja a célfájlba, ha már létezik.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path (elérési út)
Az áthelyezni vagy átnevezni kívánt elem az adattó-tároló elérési útját adja meg, kezdve a gyökérkönyvtárral (/).

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### karakterlánc
Az áthelyezett fájl vagy mappa teljes elérési útja.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmDataLakeStoreItem](./Get-AzureRmDataLakeStoreItem.md)

[Exportálás – AzureRmDataLakeStoreItem](./Export-AzureRmDataLakeStoreItem.md)

[Importálás – AzureRmDataLakeStoreItem](./Import-AzureRmDataLakeStoreItem.md)

[Új – AzureRmDataLakeStoreItem](./New-AzureRmDataLakeStoreItem.md)

[Remove-AzureRmDataLakeStoreItem](./Remove-AzureRmDataLakeStoreItem.md)

[Teszt-AzureRmDataLakeStoreItem](./Test-AzureRmDataLakeStoreItem.md)


