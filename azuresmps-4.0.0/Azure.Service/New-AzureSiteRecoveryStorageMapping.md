---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2D09422F-82B1-4243-B835-8BF223A6F936
online version: ''
schema: 2.0.0
ms.openlocfilehash: a6f02f333601172341de4fe8a0bf629037f712a5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015975"
---
# New-AzureSiteRecoveryStorageMapping

## Áttekintés
Az Azure Storage Object és a helyreállítási tároló objektum között megfeleltetést hoz létre.

## SZINTAXISA

```
New-AzureSiteRecoveryStorageMapping -PrimaryStorage <ASRStorage> -RecoveryStorage <ASRStorage>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **New-AzureSiteRecoveryStorageMapping** parancsmag létrehoz egy megfeleltetést az Azure webhely-helyreállítási felügyelt elsődleges Azure Storage Object és a helyreállítási tároló objektum között.

## Példák

### 1. példa: megfeleltetés létrehozása tárolási objektum és helyreállítási tároló objektum között
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $Storages = Get-AzureSiteRecoveryStorage -Server $Servers[0]
PS C:\> New-AzureSiteRecoveryStorageMapping -PrimaryStorage $Storages[0] -RecoveryStorage $Storages[1]
```

Az első Command parancsmag a **Get-AzureSiteRecoveryServer** parancsmaggal kapja meg az aktuális Azure-webhely helyreállítási boltozatának kiszolgálóit.
A parancs a $Servers Array változóban tárolja a webhely-helyreállítási kiszolgálókat.

A második parancs beolvassa a webhely-helyreállítási tárterületet az $Servers tömb első kiszolgálójára, majd a $Storages tárolja.

A végleges parancs az elsődleges hálózat és a helyreállítási hálózat között hoz létre megfeleltetést.
A parancs az elsődleges tárterület-objektumot az $Storages első elemeként adja meg.
A parancs a helyreállítási tárterület objektumot a $Storages második elemeként adja meg.

## PARAMÉTEREK

### -PrimaryStorage
A helyreállítási tárterülethez rendelhető elsődleges tárterületet adja meg.
**ASRStorage** objektum beolvasásához használja az Get-AzureSiteRecoveryStorage parancsmagot.

```yaml
Type: ASRStorage
Parameter Sets: (All)
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

### -RecoveryStorage
A helyreállítási tárterület objektumot adja meg.
Ez a parancsmag az elsődleges tárterületet az a tárterület-objektumhoz rendeli, amelyet a paraméter határoz meg.
**ASRStorage** -objektum beszerzéséhez használja a **Get-AzureSiteRecoveryStorage**.

```yaml
Type: ASRStorage
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureSiteRecoveryStorage](./Get-AzureSiteRecoveryStorage.md)

[Get-AzureSiteRecoveryStorageMapping](./Get-AzureSiteRecoveryStorageMapping.md)

[Remove-AzureSiteRecoveryStorageMapping](./Remove-AzureSiteRecoveryStorageMapping.md)


