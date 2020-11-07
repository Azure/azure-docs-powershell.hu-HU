---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationMongoDbCollectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
ms.openlocfilehash: aeb4c89ec4928118c5ebad05fe3c3602d88420ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671035"
---
# New-AzDataMigrationMongoDbCollectionSetting

## Áttekintés
Gyűjtemény-beállítás létrehozása az áttelepítéshez az mongoDb-áttelepítés szerint

## SZINTAXISA

```
New-AzDataMigrationMongoDbCollectionSetting -Name <Name> [-TargetRequestUnit <TargetRequestUnit>] [-CanDelete] [-ShardKey <ShardKey>]
```

## Leírás
A New-AzDataMigrationMongoDbCollectionSetting parancsmag létrehoz egy áttelepítési beállítás objektumot, amely az átviteli sebesség és a törlés működését adja meg.
A kimenet: a parancsmag egy kulcs érték párja a gyűjtemény nevével és a beállítás értékétől. A kimenet az adatbázis-szint áttelepítési beállításainak összeállításakor használatos.

## Példák

### Példa 1
```
PS C:\> $x = New-AzDataMigrationMongoDbCollectionSetting -Name myCollection -TargetRequestUnit 1000 -CanDelete -ShardKey "_id:-1,age:1,name"
PS C:\> $x

Name         Setting
----         -------
myCollection Microsoft.Azure.Management.DataMigration.Models.MongoDbCollectionSettings

PS C:\> $x.Setting

CanDelete ShardKey                                                               TargetRUs
--------- --------                                                               ---------
     True Microsoft.Azure.Management.DataMigration.Models.MongoDbShardKeySetting      1000

```

## PARAMÉTEREK

### -Name (név)
A gyűjtemény neve

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShardKey
A Szilánk-kulcsok pontosvesszővel elválasztott listája. A mongoDb Target esetében megadhatja a "ShardKeyName: Order" (": sorrend") bejárási sorrendjét, ahol a sorrend 1,-1 vagy üres az üzenetkivonat esetén (például "_id, e-mail:-1").

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetRequestUnit
A dedikált Collection Request Unit érték Ha nincs beállítva, a gyűjtemény az RU megosztott adatbázisát használja.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: RU

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CanDelete
Annak megállapítása, hogy a célérték törlésre kerül-e, ha a kapcsoló be van állítva, akkor a rendszer az áttelepítés után kitakarítja.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

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

### Microsoft. Azure. Command. DataMigration. models. MongoDbCollectionSetting>

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
