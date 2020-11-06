---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9574CEB5-B699-4606-8C5E-CE2C0D01092D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
ms.openlocfilehash: 740077def0ba0eccb1d962b88317fadb3c5c897c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492878"
---
# New-AzureRmBackupRetentionPolicyObject

## Áttekintés
Biztonsági adatmegőrzési házirendet hoz létre.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### DailyRetentionParamSet
```
New-AzureRmBackupRetentionPolicyObject [-DailyRetention] -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WeeklyRetentionParamSet
```
New-AzureRmBackupRetentionPolicyObject [-WeeklyRetention] -DaysOfWeek <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### MonthlyRetentionInDailyFormatParamSet
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### MonthlyRetentionInWeeklyFormatParamSet
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### YearlyRetentionInDailyFormatParamSet
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -MonthsOfYear <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### YearlyRetentionInWeeklyFormatParamSet
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -MonthsOfYear <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **New-AzureRmBackupRetentionPolicyObject** parancsmag egy Azure Backup adatmegőrzési házirendet hoz létre.
Az adatmegőrzési házirend azt határozza meg, hogy a biztonsági mentés mennyi ideig tart a helyreállítási pont.
Az adatmegőrzés típusai a következők: 
- Napi 
- Heti 
- Havi 
- Évente hozzon létre egy adatmegőrzési házirendet a használni kívánt adatmegőrzési típusokhoz.
A biztonságimásolat-házirend legalább egy adatmegőrzési házirendhez van társítva.
Biztonsági házirend létrehozásához használja az New-AzureRmBackupProtectionPolicy parancsmagot.
Ehelyett adatmegőrzési házirendet adhat meg az Enable-AzureRmBackupProtection parancsmaghoz.

## Példák

### Példa 1: adatmegőrzési szabály létrehozása a napi adatmegőrzéshez
```
PS C:\>$Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Daily
RetentionType      Retention          RetentionTimes
-------------      ---------          --------------
Daily              30
```

Az első parancs adatmegőrzési házirendet hoz létre a napi adatmegőrzési 30 napra, majd a $Daily változóban tárolja.
A második parancs a $Daily tartalmát jeleníti meg.

### 2. példa: havi adatmegőrzési házirend létrehozása
```
PS C:\>$Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $Monthly | select *
RetentionFormat : Daily
DaysOfMonth     : {10, 20}
WeekNumber      : 
DaysOfWeek      : 
RetentionType   : Monthly
Retention       : 12
RetentionTimes  :
```

Az első parancs olyan adatmegőrzési házirendet hoz létre, amely minden hónap tizedik és huszadik részéről tizenkét hónapig őrzi meg a biztonsági másolatot.
A parancs az adatmegőrzési házirendet a $Monthly változóban tárolja.
A második parancs a $Monthly tartalmát jeleníti meg.

## PARAMÉTEREK

### -DailyRetention
Jelzi, hogy ez a parancsmag napi adatmegőrzési házirendet hoz létre.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyRetentionParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DaysOfMonth
A hónap azon napjait adja meg, amely meghatározza, hogy mely helyreállítási pontok biztonsági mentése megmaradjon és mennyi ideig.
A paraméter elfogadható értékei a következők: 1 – 28 és az utolsó egész szám.
Adja meg ezt a paramétert, ha a *DailyRetention* , az *MonthlyRetentionInDailyFormat* és a *YearlyRetentionInDailyFormat* paramétert adja meg.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: MonthlyRetentionInDailyFormatParamSet, YearlyRetentionInDailyFormatParamSet
Aliases:
Accepted values: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DaysOfWeek
A hét napjainak tömbjét adja meg.
A parancsmag azon napjai, amelyek meghatározzák, hogy mely helyreállítási pontok őrzik meg a biztonsági mentést és mennyi ideig.
A paraméter elfogadható értékei a következők:
- Hétfő 
- Kedd 
- Szerda 
- Csütörtök 
- Péntek 
- Szombat 
- Vasárnap: ezt a paramétert akkor adja meg, ha a *WeeklyRetention* , az *MonthlyRetentionInWeeklyFormat* és a *YearlyRetentionInWeeklyFormat* paramétert adja meg.
Győződjön meg arról, hogy a hét napja a biztonsági mentéshez és a visszatartás beállításhoz van igazítva.
Ha például a biztonsági másolat szombaton van beállítva, az adatmegőrzési házirendeknek a szombaton is szerepelniük kell.

```yaml
Type: System.String[]
Parameter Sets: WeeklyRetentionParamSet, MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### -MonthlyRetentionInDailyFormat
Azt jelzi, hogy ez a parancsmag napi formátumban hoz létre havi házirendet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MonthlyRetentionInDailyFormatParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonthlyRetentionInWeeklyFormat
Jelzi, hogy ez a parancsmag havi szabályokat hoz létre heti formátumban.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonthsOfYear
Itt adhatja meg, hogy az év mely hónapjaiban legyenek a biztonsági másolatok évente megmaradó helyreállítási pontok.
A paraméter elfogadható értékei a következők: hónapok (például január vagy február) nevei.

```yaml
Type: System.String[]
Parameter Sets: YearlyRetentionInDailyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases:
Accepted values: January, February, March, April, May, June, July, August, September, October, November, December

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Adatmegőrzés
Az adatmegőrzési időszakot napokban, hónapokban vagy években adja meg, hogy mely biztonsági másolat tárolja a biztonsági mentési pontot.
Az egység attól függ, hogy az adott parancsmag napi, havi vagy éves adatmegőrzési beállítást jelöl-e ki.
Ha például a *DailyRetention* paramétert adja meg, a parancsmag a jelenlegi paramétert több napra értelmezi.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WeeklyRetention
Jelzi, hogy ez a parancsmag heti adatmegőrzési házirendet hoz létre.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyRetentionParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WeekNumber
Itt adhatja meg a hónap hetet, amely meghatározza, hogy mely helyreállítási pontok biztonsági mentése megmaradjon és mennyi ideig.
A paraméter elfogadható értékei a következők:
- Első 
- Második 
- Harmadik 
- Negyedik 
- Utolsó

```yaml
Type: System.String[]
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases:
Accepted values: First, Second, Third, Fourth, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -YearlyRetentionInDailyFormat
Jelzi, hogy ez a parancsmag éves adatmegőrzési házirendet hoz létre napi formátumban.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: YearlyRetentionInDailyFormatParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -YearlyRetentionInWeeklyFormat
Jelzi, hogy ez a parancsmag éves adatmegőrzési szabályt hoz létre heti formátumban.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: YearlyRetentionInWeeklyFormatParamSet
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

### Microsoft. Azure. Command. AzureBackup. models. AzureRMBackupRetentionPolicy

## MEGJEGYZI
* Nincs

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Enable-AzureRmBackupProtection](./Enable-AzureRmBackupProtection.md)

[Új – AzureRmBackupProtectionPolicy](./New-AzureRmBackupProtectionPolicy.md)


