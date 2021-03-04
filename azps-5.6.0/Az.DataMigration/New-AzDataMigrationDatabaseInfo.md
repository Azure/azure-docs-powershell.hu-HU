---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
ms.openlocfilehash: 2152835d997532b490a6be16bf329831071f2f87
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925929"
---
# New-AzDataMigrationDatabaseInfo

## SYNOPSIS
Létrehozza az Azure Adatbázis-áttelepítési szolgáltatás DatabaseInfo objektumát, amely megadja az áttelepítés adatbázis-forrását.

## SZINTAXIS

```
New-AzDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
A New-AzDataMigrationDatabaseInfo parancsmag létrehoz egy DatabaseInfo objektumot, amely megadja az áttelepíteni megfelelő forrásadatbázis-példányt. Az adatbázisnevet bemeneti paraméterként adja meg a rendszer.

## PÉLDÁK

### 1. példa
```
PS C:\> New-AzDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

Az előző példa új DatabaseInfo objektumot hoz létre az **AdventureWorks2016 forrásadatbázishoz.**
Ez a parancsfájl abból indul ki, hogy Már be van jelentkezve az Azure-fiókjába. A bejelentkezési állapotát a Get-AzSubscription meg.

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

### -SourceDatabaseName
Forrásadatbázis neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceDBName

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

### Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
