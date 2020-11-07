---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseUpgradeHint.md
ms.openlocfilehash: c0a917d2f5e10bb499ecf6fc698bee9a84d64363
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679322"
---
# Get-AzureRmSqlDatabaseUpgradeHint

## Áttekintés
Egy adatbázisra vonatkozó árazási szintű tippeket kap.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmSqlDatabaseUpgradeHint** parancsmag árazási szintű tippeket ad az Azure SQL-adatbázisok frissítéséhez.
Az olyan adatbázisokban, amelyek továbbra is a webes és az üzleti árak szintjein találhatók, az új alapszintű, normál vagy prémium árazási szintekre frissíthetik a célzást.

Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.

## Példák

### Példa 1: javaslatok kérése a kiszolgálón található összes adatbázishoz
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

Ez a parancs a Server01 nevű kiszolgálón található összes adatbázisra vonatkozó frissítési tippeket ad eredményül.

### 2. példa: javaslatok kérése adott adatbázishoz
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

Ez a parancs adott adatbázishoz tartozó frissítési tippeket ad eredményül.

### 3. példa: a rugalmas adatbázis-készletben nem szereplő összes adatbázisra vonatkozó ajánlás kérése
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

A parancs a rugalmas adatbázis-készletben nem szereplő összes adatbázisra vonatkozó frissítési tippeket ad eredményül.

## PARAMÉTEREK

### -DatabaseName
Annak az SQL-adatbázisnak a neve, amelyhez a parancsmag frissítési tippeket kap.
Ha nem ad meg adatbázist, ez a parancsmag tippeket ad a logikai kiszolgálón található összes adatbázishoz.

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

### -ExcludeElasticPoolCandidates
Azt jelzi, hogy a rugalmas adatbázis-készletben lévő adatbázisok ki vannak-e zárva a visszaadott ajánlásokból.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.

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
Itt adhatja meg annak az adatbázisnak a nevét, amelynek a parancsmagja a frissítési tippeket kapja.

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

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmSqlDatabaseExpanded](./Get-AzureRmSqlDatabaseExpanded.md)

[Get-AzureRmSqlElasticPoolRecommendation](./Get-AzureRmSqlElasticPoolRecommendation.md)


