---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/update-azurermsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncSchema.md
ms.openlocfilehash: 710ae0ea93c7dc49597210d8890ebef04cc7c367
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679807"
---
# Update-AzureRmSqlSyncSchema

## Áttekintés
Frissítheti a Szinkronizáló sémát egy szinkronizálási tag-adatbázishoz vagy egy szinkronizáló központi adatbázishoz.
A legújabb adatbázis-séma a valós adatbázisból fog megjelenni, majd a szinkronizálási metaadat-adatbázis segítségével frissíti a sémát.
Ha a "SyncMemberName" érték van megadva, a program frissíti a tag adatbázis-sémát; Ha nem, akkor frissíti a központi adatbázis-sémát.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Update-AzureRmSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-PassThru]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
Az **Update-AzureRmSqlSyncSchema** parancsmag frissíti a Szinkronizáló sémát egy szinkronizáló vagy egy szinkronizáló központi adatbázis esetében.

## Példák

### Példa 1: a központi adatbázis szinkronizálási sémájának frissítése
```
PS C:\>Update-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
```

A parancs frissíti a központi adatbázis szinkronizálási sémáját a szinkronizálás csoport syncGroup01.

### 2. példa: a szinkronizálási séma frissítése a tagok adatbázisaiban
```
PS C:\>Update-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
```

Ez a parancs frissíti a tagsági adatbázis szinkronizálási sémáját a szinkronizálási tagok syncMember01

## PARAMÉTEREK

### -DatabaseName
Az Azure SQL-adatbázis neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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

### -PassThru
Meghatározza, hogy a szinkronizálási csoport visszaadja-e a parancsmagot

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

### -ResourceGroupName
Az erőforráscsoport neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Kiszolgálónév
Az Azure SQL Server neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SyncGroupName
A szinkronizálási csoport neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SyncMemberName
A szinkronizálási tag neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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

## KIMENETEK

### Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncGroupModel

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
