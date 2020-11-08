---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: E4F6D096-E265-49CF-AA73-E9C807F8383B
online version: ''
schema: 2.0.0
ms.openlocfilehash: b0207d4b7eddfe56a8e4e86aac6899d19c10f44e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015556"
---
# Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan

## Áttekintés
A régebbi tárolók áttelepítési terveit kapja.

## SZINTAXISA

```
Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan [-LegacyConfigId <String>]
 [-LegacyContainerNames <String[]>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-AzureStorSimpleLEgacyVolumeContainerMigrationPlan** parancsmag a régi tárolók áttelepítési terveit kapja.
Adja meg az áttelepítési tervet a régi konfiguráció AZONOSÍTÓjának megfelelően.
Ha az áttelepítési terv még folyamatban van, ez a parancsmag az áttelepítési terv állapotát kapja meg.
Ha az áttelepítési terv befejeződött, ez a parancsmag a régi tárolók készletének tényleges áttelepítési tervét adja eredményül.
Ha nem adja meg a *LegacyConfigId* paramétert, ez a parancsmag a konfigurációs azonosítók listáját adja eredményül.

## Példák

### Példa 1: a terv állapotának beszerzése
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "f16463bd-94a9-4c3c-91c2-7a3ba7120087" -LegacyContainerNames "OneSDKAzureCloud"
VERBOSE: 2015-04-08 13:48:05 ClientRequestId: 51e413fd-c2c9-4108-88cd-a0e792eab80a_PS
VERBOSE: 2015-04-08 13:48:05 ClientRequestId: 4c6398ef-35a0-4d1c-931e-d9d45599a97a_PS
VERBOSE: 2015-04-08 13:48:17 ClientRequestId: ef7a7e35-6dff-46cd-9df3-cb5fa25d149e_PS
VERBOSE: Request Id : fd7e502f273885468f633a44567bcb3f, HttpResponse OK
VERBOSE: List of volume containers: 


LegacyConfigId                    : f16463bd-94a9-4c3c-91c2-7a3ba7120087
DeviceName                        : ARUNKM-N4
MigrationTimeEstimationCompleted  : CloudConfigurationName        : OneSDKAzureCloud
                                    EstimatedTimeForLatestBackup  : 15Minutes
                                    EstimatedTimeForAllBackups    : 15Minutes
                                    These estimates are assuming 20 MBps bandwidth. Refer to migration guide to re-calculate for lower bandwidths. 



MigrationTimeEstimationInProgress : None
MigrationTimeEstimationFailed     : None
MigrationTimeEstimationNotStarted : None
```

Ez a parancs megkapja az áttelepítési terv állapotát.
Az állapot a feltételezett sávszélességet, a becsült időt és a kapcsolódó információkat tartalmazza.

### 2. példa: meglévő csomagok azonosítóinak beolvasása
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
VERBOSE: 2015-04-08 13:46:51 ClientRequestId: 813da56c-0cfc-4325-80db-08ef32bdde1e_PS
VERBOSE: 2015-04-08 13:46:51 ClientRequestId: 9e7cf244-1894-490a-be02-749834a99318_PS
VERBOSE: List of LegacyConfig Ids on the resource: 

LegacyConfigId                                              DeviceName
--------------                                              ----------
1e1f10a0-3dff-4249-b847-4930061cd87a                        ARUNKM-N4
26d4096d-49b6-4102-b188-0446ece73c8b                        ARUNKM-N4
```

Ez a parancs az áttelepítési tervek minden konfigurációs azonosítóját megkapja.

## PARAMÉTEREK

### -LegacyConfigId
A régi készülék konfigurációjának egyedi AZONOSÍTÓját adja meg.

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

### -LegacyContainerNames
A kötet-tárolók azon neveinek tömbje, amelyekhez ez a parancsmag áttelepítési tervet kap.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Egy Azure-profilt ad meg.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### MigrationPlanMsg
Ez a parancsmag egy olyan **MigrationPlanMsg** -objektumot ad eredményül, amely az áttelepítési terv feladatának állapotát tartalmazza, a sávszélességet a másodpercenként megabitben, a becsült időt percekben jeleníti meg.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan](./Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


