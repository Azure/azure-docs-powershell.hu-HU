---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7247CF85-78B0-4837-9162-F66077668A74
online version: ''
schema: 2.0.0
ms.openlocfilehash: d77dd294f386232f7db358696608aa47adceb1d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015902"
---
# New-AzureSchedulerStorageQueueJob

## Áttekintés
A tárolási műveleteket tartalmazó ütemező feladatot hoz létre.

## SZINTAXISA

### Szükséges
```
New-AzureSchedulerStorageQueueJob -Location <String> -JobCollectionName <String> -JobName <String>
 -StorageQueueAccount <String> -StorageQueueName <String> -SASToken <String> [-StorageQueueMessage <String>]
 [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionMethod <String>] [-ErrorActionURI <Uri>]
 [-ErrorActionRequestBody <String>] [-ErrorActionHeaders <Hashtable>] [-ErrorActionStorageAccount <String>]
 [-ErrorActionStorageQueue <String>] [-ErrorActionSASToken <String>] [-ErrorActionQueueMessageBody <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Ismétlődő
```
New-AzureSchedulerStorageQueueJob [-StorageQueueMessage <String>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionHeaders <Hashtable>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.
A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .

A **New-AzureSchedulerStorageQueueJob** parancsmag létrehoz egy olyan Feladatütemező-feladatot, amely Azure Storage művelettel rendelkezik.

## Példák

### Példa 1: egyszer futó tárolási feladat létrehozása
```
PS C:\> New-AzureSchedulerStorageQueueJob -JobCollectionName "JobCollection01" -JobName "Job01" -Location "North Central US" -StorageQueueAccount "ContosoStorageAccount" -StorageQueueName "ContosoStorageQueue" -SASToken "?sv=2012-02-12&si=samplePolicy%2F30%2F2014%206%3A37%3A36%20PM&sig=vLQEbSfZbTFh7q3YrzlxBeL%2BjiYKp0gE6lMJ0a5Nb4M%3D"
```

Ez a parancs létrehoz egy Feladatütemező tárolási feladatot a JobCollection01 nevű gyűjtemény részeként.
A parancs a tárolási fiókot, a várólista nevét és a SAS-tokent adja meg.
A feladat egyszer, azonnal fut.

### 2. példa: adott számú alkalommal futó tárterület létrehozása
```
PS C:\> New-AzureSchedulerStorageQueueJob -JobCollectionName "JobCollection01" -JobName "Job12" -Location "North Central US"-StorageQueueAccount "ContosoStorageAccount" -StorageQueueName "ContosoStorageQueue" -SASToken "?sv=2012-02-12&si=samplePolicy%2F30%2F2014%206%3A37%3A36%20PM&sig=vLQEbSfZbTFh7q3YrzlxBeL%2BjiYKp0gE6lMJ0a5Nb4M%3D" -ExecutionCount 20 -Frequency "Hour" -Interval 2
```

Ez a parancs létrehoz egy Feladatütemező tárolási feladatot a JobCollection01 nevű gyűjtemény részeként.
A parancs a tárolási fiókot, a várólista nevét és a SAS-tokent adja meg.
A feladat összesen 20 alkalommal, óránként kétszer fut.

## PARAMÉTEREK

### -A befejezési időpont
Időpontot ad meg **datetime** -objektumként a Feladatütemező számára a feladat kezdeményezésének befejezéséhez.
Ha egy **datetime** típusú objektumot szeretne beolvasni, használja a **Get-Date** parancsmagot.
További információért írja be a következőt: `Get-Help Get-Date` .

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ErrorActionHeaders
A fejléceket a hash-táblázatként adja meg.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ErrorActionMethod
A HTTP-és HTTPS-műveletek típusának megfelelő módszert adja meg.
Az érvényes értékek a következők: 

- BESZERZÉSE
- HELYEZNI
- POST
- FEJ
- TÖRLÉSE

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ErrorActionQueueMessageBody
A tárolási feladatok szövegtörzsét adja meg.

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ErrorActionRequestBody
A feladatok elvégzésére és KÖZZÉTÉTELére szolgáló szövegtörzset adja meg.

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ErrorActionSASToken
Megadja a tárterület-várólistához tartozó megosztott hozzáférés-aláírási (SA) tokent.

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ErrorActionStorageAccount
A tárolási fiók nevét adja meg.

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ErrorActionStorageQueue
A tárolási várólista nevét adja meg.

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ErrorActionURI
A hiba-feladathoz tartozó URI-azonosítóját adja meg.

```yaml
Type: Uri
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExecutionCount
A futtatott feladat előfordulásainak számát adja meg.
Alapértelmezés szerint a feladat határozatlan ideig ismétlődik.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Gyakoriság
A Feladatütemező maximális gyakoriságát adja meg.

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

### -Intervallum
A *gyakoriság* paraméterrel megadott gyakoriságú ismétlődési intervallumot adja meg.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobCollectionName
Annak a gyűjteménynek a nevét adja meg, amely a Feladatütemező feladatát tartalmazza.

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Feladatnév
A Feladatütemező feladatának nevét adja meg.

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -JobState
A Feladatütemező feladatához tartozó állapotot adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Hely
Annak a helynek a nevét adja meg, amely a felhőalapú szolgáltatást tárolja.
Az érvényes értékek a következők: 

- Bárhonnan Ázsia
- Bárhol Európában
- Bárhol vagyunk
- Kelet-ázsiai
- Kelet-amerikai
- Közép-amerikai Észak-amerikai
- Észak-Európa
- Dél-Közép-amerikai
- Dél-ázsiai
- Nyugat-Európa
- Nyugat-amerikai

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.
Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SASToken
A tárolási várólista biztonsági társítási jogkivonatát adja meg.

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Kezdő időpont
Időpontot ad meg **datetime** objektumként a kezdéshez.

```yaml
Type: DateTime
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageQueueAccount
A tárolási fiók nevét adja meg.

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageQueueMessage
A tárolási feladatok várólistájának üzenetét adja meg.

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

### -StorageQueueName
A tárolási várólista nevét adja meg.

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Set-AzureSchedulerStorageQueueJob](./Set-AzureSchedulerStorageQueueJob.md)


