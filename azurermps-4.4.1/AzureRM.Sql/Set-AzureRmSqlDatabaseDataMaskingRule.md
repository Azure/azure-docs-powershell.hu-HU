---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 1a26cc83bfd42ba63f2ae914ea6c288b862ccaf5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493314"
---
# Set-AzureRmSqlDatabaseDataMaskingRule

## Áttekintés
Egy adatbázis adatmaszkolási szabályának tulajdonságait állítja be.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Set-AzureRmSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Leírás
A **set-AzureRmSqlDatabaseDataMaskingRule** parancsmag adatmaszkolási szabályt állít be egy Azure SQL-adatbázishoz.
A parancsmag használatához adja meg a *ResourceGroupName* , a *kiszolgálónév* , a *databasename* és az *RuleId* paramétert a szabály meghatározásához.
A *SchemaName* , az *Táblanév* és a *ColumnName* bármelyik paraméterét megadhatja a szabály átcélzásához.
Adja meg a *MaskingFunction* paramétert az adatmaszkolás módjának módosításához.

Ha megad egy szám vagy szöveg értékét a *MaskingFunction* , megadhatja a *NumberFrom* és az *NumberTo* paramétert a szám maszkolásához, illetve a szöveg maszkolásához használt *PrefixSize* , *ReplacementString* és *SuffixSize* paramétereket.
Ha a parancs sikeres, és ha a *PassThru* paramétert adja meg, a parancsmag egy olyan objektumot ad eredményül, amely leírja az adatmaszkolási szabály tulajdonságait és a szabályok azonosítóját.
A **ResourceGroupName** , a **kiszolgálónév** , a **databasename** és a **RuleId** nem csak a szabály-azonosítókat tartalmazzák.

Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.

## Példák

### Példa 1: adatmaszkolási szabály tartományának módosítása az adatbázisban
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

Ez a parancs módosítja az adatmaszkolási szabályokat az azonosító Rule17.
Ez a szabály a kiszolgáló Server01 Database01 nevű adatbázisban működik.
Ez a parancs módosítja annak az intervallumnak a szegélyét, amelyben a véletlenszerűen kiválasztott szám a maszkolt érték lesz.
Az új címtartomány 23 és 42 között van.

## PARAMÉTEREK

### -ColumnName
A maszkolási szabály által célzott oszlop nevét adja meg.

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

### -DatabaseName
Az adatbázis nevét adja meg.

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

### -MaskingFunction
A szabály által használt maszkolás függvényt adja meg.
A paraméter elfogadható értékei a következők:

- Alapértelmezett
- A kitakarás
- Szöveg
- Szám
- SocialSecurityNumber
- CreditCardNumber
- E-mail

Az alapértelmezett érték az alapértelmezett.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NumberFrom
Annak az intervallumnak az alsó határát adja meg, amelyből egy véletlenszerű érték van kijelölve.
Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez megadja a szám értékét.
Az alapértelmezett érték a 0.

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NumberTo
Annak az intervallumnak a felső határát adja meg, amelyből egy véletlenszerű érték van kijelölve.
Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez megadja a szám értékét.
Az alapértelmezett érték a 0.

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.
Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.

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

### -PrefixSize
Itt adhatja meg, hogy a program hány karaktert tartalmaz a nem maszkolt szöveg elején.
Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez adja meg a szöveg értékét.
Az alapértelmezett érték a 0.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ReplacementString
A nem maszkolt szöveg végén található karakterek számát adja meg.
Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez adja meg a szöveg értékét.
Az alapértelmezett érték a 0.

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

### -SchemaName
A séma nevét adja meg.

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

### -Kiszolgálónév
Az adatbázist tároló kiszolgáló nevét adja meg.

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

### -SuffixSize
A nem maszkolt szöveg végén található karakterek számát adja meg.
Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez adja meg a szöveg értékét.
Az alapértelmezett érték a 0.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Táblanév
A maszkolt oszlopot tartalmazó adatbázis-tábla nevét adja meg.

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

###  
Nincs

## KIMENETEK

### Microsoft. Azure. Command. SQL. Security. Model. DatabaseDataMaskingRuleModel

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmSqlDatabaseDataMaskingRule](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[Új – AzureRmSqlDatabaseDataMaskingRule](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[Remove-AzureRmSqlDatabaseDataMaskingRule](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[SQL-adatbázis dokumentációja](https://docs.microsoft.com/azure/sql-database/)


