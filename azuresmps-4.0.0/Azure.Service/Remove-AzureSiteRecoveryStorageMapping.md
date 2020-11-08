---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 0A1FD05F-6573-46D8-8217-C7EA432F6742
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd8ccb634c313f487b6777a9fcb66d872b35510e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016109"
---
# Remove-AzureSiteRecoveryStorageMapping

## Áttekintés
Tároló-objektum megfeleltetésének eltávolítása a webhely-helyreállítási boltozathoz.

## SZINTAXISA

```
Remove-AzureSiteRecoveryStorageMapping -StorageMapping <ASRStorageMapping> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
A **Remove-AzureSiteRecoveryStorageMapping** parancsmag eltávolítja az aktuális Azure-webhely helyreállítási boltozatához tartozó tároló objektum megfeleltetését.

## Példák

### 1. példa: a hálózat és a helyreállítási hálózat közötti megfeleltetés eltávolítása
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $StorageMapping = Get-AzureSiteRecoveryStorageMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[1]
PS C:\> Remove-AzureSiteRecoveryStorageMapping -StorageMapping $StorageMapping
Get-AzureSiteRecoveryServerGet-AzureSiteRecoveryStorageMappingNew-AzureSiteRecoveryStorageMapping
```

Az első Command parancsmag a **Get-AzureSiteRecoveryServer** parancsmaggal kapja meg az aktuális Azure-webhely helyreállítási boltozatának kiszolgálóit.
A parancs a $Servers Array változóban tárolja a webhely-helyreállítási kiszolgálókat.

A második parancs beolvassa a megfeleltetést két tároló objektum között, majd a $StorageMapping változóban tárolja.
A parancs a hálózati megfeleltetés elsődleges kiszolgálóját adja meg az $Servers első elemeként.
A parancs a helyreállítási hálózatnak azt a kiszolgálóját adja meg, amely a $Servers második eleme.

A végleges parancs eltávolítja a megfeleltetést a $StorageMappingban.

## PARAMÉTEREK

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

### -StorageMapping
Hálózati megfeleltetést ad meg.
**ASRStorageMapping** beszerzéséhez használja a **Get-AzureSiteRecoveryStorage** parancsmagot.

```yaml
Type: ASRStorageMapping
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

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureSiteRecoveryStorage](./Get-AzureSiteRecoveryStorage.md)


