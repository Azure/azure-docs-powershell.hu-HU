---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 53580FF1-D905-40FD-A5F0-D5FBCD036E0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: a51fd8210d2fe7fb224ed43650a354e383ed4e54
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015776"
---
# Start-AzureStorSimpleDeviceFailoverJob

## Áttekintés
A kötet-tároló csoportok feladatátvételi műveletét kezdeményezi.

## SZINTAXISA

### Üres (alapértelmezett)
```
Start-AzureStorSimpleDeviceFailoverJob
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyById
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceId <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByName
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceName <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceName <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Start-AzureStorSimpleDeviceFailoverJob** parancsmag egy vagy több mennyiségi tároló csoport feladatátvételi műveletét kezdeményezi egyik eszközről a másikra.

## Példák

### 1. példa: feladatátvételi feladat indítása névvel ellátott eszközön és elnevezett céleszköz
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Start-AzureStorSimpleDeviceFailoverJob -DeviceName "ChewD_App7" -TargetDeviceName "Fuller05" -Force
a3d902be-8ffb-42a4-bbf8-0a1b30db71b2_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

Ez a parancs a **Get-AzureStorSimpleFailoverVolumeContainers** parancsmag használatával kapja meg a ChewD_App7 nevű eszköz feladatátvevő mennyiségi tárolóit.
A parancs átadja az eredményeket a **Where-Object** parancsmagnak, amely a **IsDCGroupEligibleForDR** tulajdonságtól $True eltérő értéket tartalmazó tárolókat visz le.
További információért írja be a következőt: `Get-Help Where-Object` .
Az aktuális parancsmag feladatátvételi feladatokat indít a fennmaradó feladatátvevő mennyiségi tárolókban.
A parancs az eszköz nevét és a céleszköz nevét adja meg.
A parancs a parancsmag által elindított feladat példányának AZONOSÍTÓját számítja ki.

### 2. példa: feladatátvételi feladat indítása eszközhöz és az AZONOSÍTÓval megadott céleszköz
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Select-Object -First 1 | Start-AzureStorSimpleDeviceFailoverJob -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925" -TargetDeviceId "0ee59ae9-0293-46e2-ae56-bc308c8e5520" -Force
4c5ac0d0-4b66-465c-98f5-aec90505ad12_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

Ez a parancs a **Get-AzureStorSimpleFailoverVolumeContainers** használatával megkapja a ChewD_App7 nevű eszköz feladatátvevő mennyiségi tárolóit.
A parancs a találatokat a **Where-Object** értékre adja át, amely a **IsDCGroupEligibleForDR** tulajdonságtól eltérő értékkel rendelkező $Trueokat adja eredményül.
A parancsmag átadja az eredményeket a **Select-Object** parancsmagnak, amely kijelöli az első objektumot, amelyet az aktuális parancsmagnak szeretne továbbítani.
További információért írja be a következőt: `Get-Help Select-Object` .
Az aktuális parancsmag a kijelölt feladatátvevő mennyiségi tárolóhoz tartozó feladatátvételi feladatokat indítja el.
A parancs az eszköz AZONOSÍTÓját és a céleszköz AZONOSÍTÓját adja meg.
A parancs a parancsmag által elindított feladat példányának AZONOSÍTÓját számítja ki.

## PARAMÉTEREK

### -DeviceId
Annak az StorSimple-eszköznek a példány-AZONOSÍTÓját adja meg, amelyen a mennyiségi tároló csoport létezik.

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Annak a StorSimple-eszköznek a nevét adja meg, amelyen a mennyiségi tároló csoport létezik.

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.

```yaml
Type: SwitchParameter
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

### -TargetDeviceId
Annak az StorSimple-eszköznek a példány-AZONOSÍTÓját adja meg, amelyre a parancsmag a mennyiségi tároló csoporton keresztül nem ér el.

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDeviceName
Annak a StorSimple-eszköznek a nevét adja meg, amelyre a parancsmag a mennyiségi tároló csoporton keresztül nem képes.

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VolumecontainerGroups
Azon mennyiségi tároló-csoportok listáját adja meg, amelyeket a parancsmag a másik eszközre nem ér át.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Lista\<DataContainerGroup\>
A kötet-tároló csoportok listáját áthelyezheti erre a parancsmagra.

## KIMENETEK

### Karakterlánc

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureStorSimpleFailoverVolumeContainers](./Get-AzureStorSimpleFailoverVolumeContainers.md)


