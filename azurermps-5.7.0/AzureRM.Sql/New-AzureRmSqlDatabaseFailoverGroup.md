---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 71f4796e33ec512f9d0aa2eb27f78ba615eefef1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492124"
---
# New-AzureRmSqlDatabaseFailoverGroup

## Áttekintés
A parancs létrehoz egy új Azure SQL-adatbázis feladatátvételi csoportját.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
New-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> -FailoverGroupName <String>
 [-PartnerResourceGroupName <String>] -PartnerServerName <String> [-FailoverPolicy <FailoverPolicy>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
Új Azure SQL adatbázis-feladatátvételi csoportot hoz létre a megadott kiszolgálókhoz.

Két Azure SQL-adatbázis TDS végpontokat hoz létre a FailoverGroupName. SqlDatabaseDnsSuffix (például FailoverGroupName.database.windows.net) és a FailoverGroupName. középfokú. SqlDatabaseDnsSuffix. Ezek a végpontok akkor használhatók, ha az elsődleges és a másodlagos kiszolgálókhoz csatlakoznak a feladatátvétel csoportban. Ha az elsődleges kiszolgálót áramkimaradás okozta, akkor a végpontok és adatbázisok automatikus feladatátvételét a feladatátvételi csoport feladatátvételi házirendje és türelmi időszaka határozza meg.

Az újonnan létrehozott feladatátvevő csoportok nem tartalmaznak adatbázisokat. Ha meg szeretné határozni egy feladatátvételi csoport adatbázis-készletét, használja a "AzureRmSqlDatabaseToFailoverGroup" és a "Remove-AzureRmSqlDatabaseFromFailoverGroup" parancsmagot.

A feladatátvevő csoportok funkció előnézete során a "-GracePeriodWithDataLossHours" paraméterben csak az 1 óra feletti vagy azzal egyenlő értékek támogatottak.

## Példák

### Példa 1
```
C:\> $failoverGroup = New-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -PartnerServerName secondaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

Ez a parancs létrehoz egy új feladatátvételi csoportot, amelyben az "automatikus" feladatátvételi házirend két kiszolgáló ugyanazon erőforráscsoport-kiszolgálón található.

### 2. példa
```
C:\> $failoverGroup = New-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg1 -ServerName primaryserver -PartnerResourceGroupName rg2 -PartnerServerName secondaryserver1 -FailoverGroupName fg -FailoverPolicy Manual
```

Ez a parancs létrehoz egy új feladatátvételi csoportot, amelyben a feladatátvételi házirend "kézi", két különböző erőforráscsoport kiszolgálói esetén használható.

## PARAMÉTEREK

### -AllowReadOnlyFailoverToPrimary
Azt, hogy a másodlagos kiszolgálón lévő leállás esetén az írásvédett végpont automatikus feladatátvételét kell-e elindítani. Ez a funkció még nem támogatott.

```yaml
Type: AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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

### -FailoverGroupName
A létrehozandó Azure SQL adatbázis-feladatátvételi csoport neve.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FailoverPolicy
Az Azure SQL-adatbázis feladatátvételi csoportjának feladatátvételi házirendje.

```yaml
Type: FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: Automatic
Accept pipeline input: False
Accept wildcard characters: False
```

### -GracePeriodWithDataLossHours
Az automatikus feladatátvétel kezdeményezésének gyakorisága, ha áramkimaradás történik az elsődleges kiszolgálón, és a feladatátvétel nem hajtható végre adatvesztés nélkül.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerResourceGroupName
Az Azure SQL-adatbázis feladatátvételi csoportjának másodlagos erőforráscsoport neve.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerServerName
Az Azure SQL-adatbázis feladatátvételi csoportjának másodlagos kiszolgálójának neve.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforráscsoport neve.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Kiszolgálónév
A feladatátvételi csoport elsődleges Azure SQL-adatbázis-kiszolgálójának neve.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

## KIMENETEK

### System. Object (rendszer. objektum)

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Set-AzureRmSqlDatabaseFailoverGroup](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[Get-AzureRmSqlDatabaseFailoverGroup](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[Add-AzureRmSqlDatabaseToFailoverGroup](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[Remove-AzureRmSqlDatabaseFromFailoverGroup](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[Switch-AzureRmSqlDatabaseFailoverGroup](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[Remove-AzureRmSqlDatabaseFailoverGroup](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[SQL-adatbázis dokumentációja](https://docs.microsoft.com/azure/sql-database/)
