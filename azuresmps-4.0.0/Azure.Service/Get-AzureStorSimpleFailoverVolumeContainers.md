---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BABBA19E-5833-452C-9E36-811EAE7C20F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb326281058f0ff9280c4b87c0530241ece801e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015561"
---
# Get-AzureStorSimpleFailoverVolumeContainers

## Áttekintés
A kötet tároló csoportjának beolvasása az eszközök feladatátvételéhez.

## SZINTAXISA

### IdentifyById
```
Get-AzureStorSimpleFailoverVolumeContainers -DeviceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByName
```
Get-AzureStorSimpleFailoverVolumeContainers -DeviceName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureStorSimpleFailoverVolumeContainers** parancsmag a kötet-tároló csoportokat kapja meg az eszközök feladatátvételéhez.
Adjon át egyetlen **VolumeContainer** -csoportot vagy **VolumeContainer** -csoportot a **Start-AzureStorSimpleDeviceFailover** parancsmagba.
Csak azok a csoportok jogosultak a feladatátvételre, amelyek $True értékkel rendelkeznek a **IsDCGroupEligibleForDR** tulajdonságban.

## Példák

### 1. példa: feladatátvevő mennyiségi tárolók beszerzése
```
PS C:\>Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7"

DCGroup                    IneligibilityMessage          IsDCGroupEligibleForDR
-------                    --------------------          ----------------------
{VolumeContainer1889078...                                                 True
{VC_01}                    No cloud snapshot found                        False
{VolumeContainer7306959}   No cloud snapshot found                        False
{VolumeContainer407850151} No cloud snapshot found                        False
```

Ez a parancs feladatátvevő mennyiségi tárolókat kap.
Csak azok az DCGroups használhatók, amelyekben az **IsDCGroupEligibleForDR** tulajdonság $True értéke az eszközök feladatátvételéhez használható.

## PARAMÉTEREK

### -DeviceId
Annak a StorSimple-eszköznek a példány-AZONOSÍTÓját adja meg, amelyen a parancsmagot futtatni szeretné.

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
Annak a StorSimple-eszköznek a nevét adja meg, amelyen a parancsmagot futtatni szeretné.

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

## KIMENETEK

### IList\<DataContainerGroup\>
Ez a parancsmag a **VolumeContainer** -csoportok listáját számítja ki.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Start-AzureStorSimpleDeviceFailoverJob](./Start-AzureStorSimpleDeviceFailoverJob.md)

[Get-AzureStorSimpleDeviceVolumeContainer](./Get-AzureStorSimpleDeviceVolumeContainer.md)


