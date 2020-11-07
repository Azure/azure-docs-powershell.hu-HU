---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/submit-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Submit-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Submit-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 23c8f8baa2753382ef2ee91f62199966a4fb9c2d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836354"
---
# Submit-AzDataLakeAnalyticsJob

## Áttekintés
Feladatot küldhet el.

## SZINTAXISA

### SubmitUSqlJobWithScriptPath
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubmitUSqlJob
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubmitUSqlJobWithScriptPathAndRecurrence
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubmitUSqlJobWithRecurrence
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubmitUSqlJobWithScriptPathAndPipeline
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SubmitUSqlJobWithPipeline
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Submit-AzDataLakeAnalyticsJob** parancsmag az Azure Data-tó Analytics-feladatát továbbítja.

## Példák

### 1. példa: feladat elvégzése
```
PS C:\>Submit-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32
```

Ez a parancs egy adattói Analytics-feladatot küldött.

### 2. példa: feladatok elvégzése parancsfájl-paraméterekkel
```
PS C:\>$parameters = [ordered]@{}
$parameters["Department"] = "Sales"
$parameters["NumRecords"] = 1000
$parameters["StartDateTime"] = (Get-Date).AddDays(-14)
Submit-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32 -ScriptParameter $parameters
```

Az U-SQL-parancsfájlok paraméterei a fő egységprefixumokat felett jelennek meg, például: DEKLARÁLja a @Department String = "Sales" nevet. ÁLLAPÍTSA meg az @NumRecords int = 1000; A @StartDateTime datetime = New datetime (2017; 12; 6; 0; 0; 0; 0) deklarálása;

## PARAMÉTEREK

### -Fiók
Az adattó-fiók neve, amelybe a feladatot be fogja nyújtani.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AnalyticsUnits
A projekthez használandó Analytics-egységek. A parancsfájlokhoz tartozó további elemzési egységek általában gyorsabban futtathatják a parancsfájl-végrehajtási időt.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: DegreeOfParallelism

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CompileMode
A feladat során elvégzendő összeállítás típusa. Érvényes értékek: 
- Szemantikai (csak szemantikai vizsgálatokkal és a szükséges józan ellenőrzésekkel végezhető el)
- Teljes (teljes összeállítás)
- SingleBox (teljes összeállítás helyben végzett)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Semantic, Full, SingleBox

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CompileOnly
Jelzi, hogy a beküldésnek csak a feladatot kell kiépítenie, és nem kell végrehajtania, ha igaz értékre van állítva.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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

### -Name (név)
A elküldeni kívánt feladat rövid neve.

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

### -PipelineId
A feladat beküldését jelző azonosító a munkafolyamathoz kapcsolódó ismétlődő feladatok, valamint a munkafolyamathoz kapcsolódó munka része.

```yaml
Type: System.Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PipelineName
A projekthez társított pipeline számára választható felhasználóbarát név.

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PipelineUri
Egy opcionális URI, amely a csővezetékhez társított származó szolgáltatásra hivatkozik.

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Prioritás
A feladat prioritása. Ha nincs megadva, a prioritás a 1000. Az alacsonyabb számok magasabb prioritást jeleznek.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RecurrenceId
A feladat beküldését jelző azonosító egy olyan ismétlődő feladat része, amely ugyanazzal az ismétlődési AZONOSÍTÓval rendelkezik.

```yaml
Type: System.Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RecurrenceName
Választható rövid név a feladatok közötti ismétlődési korrelációhoz.

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RunId
Egy azonosító, amely azonosítja a folyamat adott futási közelítését.

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Futtatókörnyezet
Tetszés szerint állítsa be a projekthez használni kívánt futásidejű verziót. Ha nincs bekapcsolva, az alapértelmezett futásidejű érték van használatban.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Script
Parancsfájl végrehajtása (írt sor).

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJob, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithPipeline
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ScriptParameter
A projekthez tartozó parancsfájlok paraméterei (karakterlánc) az értékekhez (a bájtok, a sbyte, az int, a uint (vagy a UInt32), a Long, a ulong (vagy a UInt64), az float, a Double, a decimális, a short (vagy a Int16), a karakter, a karakterlánc, a DateTime, a bool, a GUID vagy a byte [] függvény

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScriptPath
A küldeni kívánt parancsfájl elérési útja.

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPath, SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithScriptPathAndPipeline
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### System. Management. Automation. SwitchParameter

### System. Int32

### System. Collections. IDictionary

### System. GUID

### System. null ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]

## KIMENETEK

### Microsoft. Azure. Management. DataLake. Analytics. models. JobInformation

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzDataLakeAnalyticsJob](./Get-AzDataLakeAnalyticsJob.md)

[Stop-AzDataLakeAnalyticsJob](./Stop-AzDataLakeAnalyticsJob.md)

[Várjon-AzDataLakeAnalyticsJob](./Wait-AzDataLakeAnalyticsJob.md)


