---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationMongoDbCollectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
ms.openlocfilehash: 4e0082d742aff54ba4d4b57d4e148e249ab8ecf7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387560"
---
# New-AzDataMigrationMongoDbCollectionSetting

## SYNOPSIS
Gyűjteménybeállítás létrehozása a mongóDb-áttelepítéshez

## SZINTAXIS

```
New-AzDataMigrationMongoDbCollectionSetting -Name <Name> [-TargetRequestUnit <TargetRequestUnit>] [-CanDelete] [-ShardKey <ShardKey>]
```

## LEÍRÁS
A New-AzDataMigrationMongoDbCollectionSetting parancsmag létrehoz egy áttelepítési beállításobjektumot, amely megadja az átviteli sebességet és a törlés viselkedését.
A parancsmag kimenete a kulcsérték pár a gyűjtemény nevével és a beállítás értékével. A kimenet az adatbázisszintű áttelepítési beállítások összeállításához használatos.

## PÉLDÁK

### 1. példa
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

## PARAMETERS

### -Name
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
A shard billentyűk vesszővel elválasztott listája. A mongoDb célhoz megadhatja a "ShardKeyName:Order" shard billentyű sorrendjét, ahol a sorrend 1, -1 vagy üres a kivonatoláshoz, például "_id;email:-1".

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
A dedikált gyűjteménykérési egység értéke. Ha nincs beállítva, akkor a gyűjtemény megosztott adatbázist (RU) használ.

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
Ha a kapcsoló be van állítva, akkor törlődnek-e a céladatok az áttelepítéskor

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Nincs

## KIMENETEK

### Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting>

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
