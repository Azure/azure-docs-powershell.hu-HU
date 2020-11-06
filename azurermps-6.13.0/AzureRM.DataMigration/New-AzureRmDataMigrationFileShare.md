---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationFileShare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationFileShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationFileShare.md
ms.openlocfilehash: b34665f9402186a1e07671e614d91fee59f565d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502115"
---
# New-AzureRmDataMigrationFileShare

## Áttekintés
Létrehozza az Azure adatbázis-áttelepítési szolgáltatás fájlmegosztásról objektumát, amely a helyi hálózati megosztást adja meg a forrás adatbázis biztonsági másolatának elkészítéséhez.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
New-AzureRmDataMigrationFileShare -Path <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A New-AzureRmDataMigrationFileShare parancsmag hozza létre a fájlmegosztásról objektumot, amely a helyi hálózati megosztást adja meg, amelyet az Azure adatbázis-áttelepítési szolgáltatás a forrás-adatbázis biztonsági másolatai készítéséhez használ Az SQL Server-példányt futtató szolgáltatásfiók írási jogosultsággal kell rendelkeznie ebben a hálózati megosztásban.

## Példák

### Példa 1
```
PS C:\> New-AzureRmDmsFileShare -Path $fileSharePath -Credential $fileShareCred

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. Management. DataMigration. models. MigrateSqlServerSqlDbDatabaseInput

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
