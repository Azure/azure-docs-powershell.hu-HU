---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationFileShare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
ms.openlocfilehash: c0b88b60127162d895eeb642269240b699836d4f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010916"
---
# New-AzDataMigrationFileShare

## Áttekintés
Létrehozza az Azure adatbázis-áttelepítési szolgáltatás fájlmegosztásról objektumát, amely a helyi hálózati megosztást adja meg a forrás adatbázis biztonsági másolatának elkészítéséhez.

## SZINTAXISA

```
New-AzDataMigrationFileShare -Path <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A New-AzDataMigrationFileShare parancsmag hozza létre a fájlmegosztásról objektumot, amely a helyi hálózati megosztást adja meg, amelyet az Azure adatbázis-áttelepítési szolgáltatás a forrás-adatbázis biztonsági másolatai készítéséhez használ Az SQL Server-példányt futtató szolgáltatásfiók írási jogosultsággal kell rendelkeznie ebben a hálózati megosztásban.

## Példák

### Példa 1
```
PS C:\> New-AzDmsFileShare -Path $fileSharePath -Credential $fileShareCred

UserName    Password     Path
--------    --------     ----
domain\user testadmin123 \\fileshare\folder1
```

## PARAMÉTEREK

### -Hitelesítő adatok
Hitelesítő adatok a fájlmegosztás eléréséhez.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Path (elérési út)
Fájlmegosztási elérési út.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. Management. DataMigration. models. MigrateSqlServerSqlDbDatabaseInput

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
