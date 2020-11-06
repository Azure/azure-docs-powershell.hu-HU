---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 69A26BF3-7FE7-41ED-8C21-C8DC72D09615
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: bd61b666dd321ec9007d413030cb899eeeb92778
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503164"
---
# Start-AzureRmSqlServerUpgrade

## Áttekintés
SQL-adatbázis kiszolgálójának frissítését indítja el.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Start-AzureRmSqlServerUpgrade -ServerVersion <String> [-ScheduleUpgradeAfterUtcDateTime <DateTime>]
 [-DatabaseCollection <RecommendedDatabaseProperties[]>]
 [-ElasticPoolCollection <UpgradeRecommendedElasticPoolProperties[]>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Start-AzureRmSqlServerUpgrade** parancsmag az Azure SQL Database Server 11-es verziójáról a 12-es verzióra való frissítést indítja el.
A frissítés előrehaladását az Get-AzureRmSqlServerUpgrade parancsmag segítségével figyelheti.

## Példák

### 1. példa: kiszolgáló frissítése
```
PS C:\>Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0
ResourceGroupName               : ResourceGroup01
ServerName                      : Server01
ServerVersion                   : 12.0
ScheduleUpgradeAfterUtcDateTime : 
DatabaseCollection              :
```

Ez a parancs frissíti a server01 nevű kiszolgálót, amely az erőforráscsoport TesourceGroup01 van hozzárendelve.

### 2. példa: a kiszolgáló frissítése az ütemezési idő és az adatbázis-javaslat használatával
```
PS C:\>$ScheduleTime = (Get-Date).AddMinutes(5).ToUniversalTime()
PS C:\> $DatabaseMap = New-Object -TypeName Microsoft.Azure.Management.Sql.Models.RecommendedDatabaseProperties
PS C:\> $DatabaseMap.Name = "contosodb"
PS C:\> $DatabaseMap.TargetEdition = "Standard"
PS C:\> $DatabaseMap.TargetServiceLevelObjective = "S0"
PS C:\> Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0 -ScheduleUpgradeAfterUtcDateTime $ScheduleTime -DatabaseCollection ($DatabaseMap)
```

Az első parancs öt perccel a jövőben hoz létre egy időpontot a Get-Date parancsmag használatával.
A parancs a dátumot az $ScheduleTime változóban tárolja.
További információért írja be a következőt: `Get-Help Get-Date` .

A második parancs létrehoz egy **RecommendedDatabaseProperties** objektumot, majd az adott objektumot az $DatabaseMap változóban tárolja.

A következő három parancs a $DatabaseMapban tárolt objektum tulajdonságainak értékét rendeli hozzá az értékekhez.

A végleges parancs frissíti a Server01 nevű meglévő kiszolgálót a 12,0-es verzióra.
A frissítés legkorábbi időpontja öt perc a parancs futtatása után, a $ScheduleTime változóban megadott módon.
A frissítés után az adatbázis-contosodb a normál kiadást fogja futtatni, és a szolgáltatási szint objektív S0 kell lennie.

## PARAMÉTEREK

### -DatabaseCollection
Itt adhatja meg a kiszolgáló frissítéséhez a parancsmag által használt **RecommendedDatabaseProperties** -objektumok tömbjét.

```yaml
Type: Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ElasticPoolCollection
A kiszolgálói frissítéshez használandó **UpgradeRecommendedElasticPoolProperties** -objektumok tömbjét adja meg.

```yaml
Type: Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.

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

### -ScheduleUpgradeAfterUtcDateTime
A kiszolgáló frissítéséhez a legkorábbi időpontot **datetime** -objektumként adja meg.
Adjon meg egy értéket a ISO8601 formátumban (az egyezményes világidő (UTC)).
További információért írja be a következőt: `Get-Help Get-Date` .

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kiszolgálónév
Itt adhatja meg annak a kiszolgálónak a nevét, amely a parancsmag frissítéseit tartalmazza.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerVersion
Azt a verziót adja meg, amelyre a parancsmag frissíti a kiszolgálót.
Az egyetlen érvényes érték az 12,0.

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

### Microsoft. Azure. Command. SQL. ServerUpgrade. Model. AzureSqlServerUpgradeModel

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmSqlServerUpgrade](./Get-AzureRmSqlServerUpgrade.md)

[Stop-AzureRmSqlServerUpgrade](./Stop-AzureRmSqlServerUpgrade.md)

[SQL-adatbázis dokumentációja](https://docs.microsoft.com/azure/sql-database/)


