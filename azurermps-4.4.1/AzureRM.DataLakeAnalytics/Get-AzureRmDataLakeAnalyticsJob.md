---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 6a172de918e8b0675abaf01edf2ec198dae75b5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505076"
---
# Get-AzureRmDataLakeAnalyticsJob

## Áttekintés
Beolvashatja az adat-tó Analytics-munkáját.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### Az összes erőforrás-csoport és fiók (alapértelmezett)
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Adott JobInformation
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmDataLakeAnalyticsJob** parancsmag Azure Data-tó elemzési feladatát kapja.
Ha nem ad meg feladatot, ez a parancsmag minden feladatot beilleszt.

## Példák

### 1. példa: meghatározott feladat beszerzése
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

Ez a parancs a megadott AZONOSÍTÓval kapja a feladatot.

### 2. példa: a múlt héten benyújtott feladatok beszerzése
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

Ez a parancs a múlt héten benyújtott feladatokat kapja.

## PARAMÉTEREK

### -Fiók
Az adattó-Analytics-fiók nevét adja meg.

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

### -Include (include)
Azokat a beállításokat adja meg, amelyek jelzik, hogy milyen típusú további információkat kell beolvasni a feladatról.
A paraméter elfogadható értékei a következők:

- Nincs
- DebugInfo
- Statisztikák
- Minden

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData
Parameter Sets: Specific JobInformation
Aliases: 
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -JobId
A beolvasott feladat AZONOSÍTÓját adja meg.

```yaml
Type: System.Guid
Parameter Sets: Specific JobInformation
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Name (név)
A Feladatlista eredményének szűrésére használható nevet adja meg.
A paraméter elfogadható értékei a következők:

- Nincs
- DebugInfo
- Statisztikák
- Minden

```yaml
Type: System.String
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PipelineId
Egy olyan opcionális azonosító, amely csak a megadott csővezeték munkamennyiség részét adja eredményül.

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RecurrenceId
Egy olyan opcionális azonosító, amely csak a megadott ismétlődéshez tartozó feladatokat adja vissza.

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Result (eredmény)
A projekt eredményéhez tartozó eredményhalmaz-szűrőt adja meg.
A paraméter elfogadható értékei a következők:

- Nincs
- Lemondott
- Sikertelen
- Sikerességéről

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]
Parameter Sets: All In Resource Group and Account
Aliases: 
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -State (állami)
A projekt eredményéhez tartozó állapot-szűrőt adja meg.
A paraméter elfogadható értékei a következők:

- Elfogadott
- Új
- Összeállítása
- Ütemezés
- Várólistán töltött
- Kezdve
- Szünetel
- Fut
- Véget

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]
Parameter Sets: All In Resource Group and Account
Aliases: 
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubmittedAfter
A Dátumszűrő értékét adja meg.
Ezzel a paraméterrel szűrheti a tevékenységlista eredményét a megadott dátum után elküldött feladatokra.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubmittedBefore
A Dátumszűrő értékét adja meg.
Ezzel a paraméterrel szűrheti a tevékenységlista eredményét a megadott dátum előtt elküldött feladatokra.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Beküldő
A felhasználó e-mail-címét adja meg.
Ezzel a paraméterrel szűrheti a tevékenységlista eredményét egy adott felhasználó által elküldött munkákra.

```yaml
Type: System.String
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Top
Egy tetszőleges érték, amely a visszaadott feladatok számát jelzi. Az alapértelmezett érték a 500

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### GUID
A ' JobId ' paraméter a pipeline "GUID" típusú értékét adja meg.

## KIMENETEK

### JobInformation
A megadott projektfeladat adatai

### Lista<JobInformation>
A megadott adattó-fiókban lévő feladatok listája.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Stop-AzureRmDataLakeAnalyticsJob](./Stop-AzureRmDataLakeAnalyticsJob.md)

[Submit-AzureRmDataLakeAnalyticsJob](./Submit-AzureRmDataLakeAnalyticsJob.md)

[Várjon-AzureRmDataLakeAnalyticsJob](./Wait-AzureRmDataLakeAnalyticsJob.md)


