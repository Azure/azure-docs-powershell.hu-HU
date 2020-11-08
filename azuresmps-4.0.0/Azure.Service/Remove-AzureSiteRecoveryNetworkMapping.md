---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: BB36A434-6BE3-46BF-B10A-FCD6C766CB84
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87414a56778123053615bb36a06113e2b0b0633f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016110"
---
# Remove-AzureSiteRecoveryNetworkMapping

## Áttekintés
Eltávolít egy hálózati megfeleltetést egy webhely-helyreállítási boltozatból.

## SZINTAXISA

```
Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping <ASRNetworkMapping> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
A **Remove-AzureSiteRecoveryNetworkMapping** parancsmag eltávolít egy hálózati megfeleltetést az aktuális Azure webhely-helyreállítási boltozatból.

## Példák

### 1. példa: a hálózat és a helyreállítási hálózat közötti megfeleltetés eltávolítása
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[0]
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

Az első Command parancsmag a **Get-AzureSiteRecoveryServer** parancsmaggal kapja meg az aktuális Azure-webhely helyreállítási boltozatának kiszolgálóit.
A parancs a $Servers Array változóban tárolja a webhely-helyreállítási kiszolgálókat.

A második parancs az elsődleges hálózat és a helyreállítási hálózat közötti megfeleltetést kapja, majd a $NetworkMapping változóban tárolja.
A parancs a hálózati megfeleltetés elsődleges kiszolgálóját adja meg az $Servers első elemeként.
A parancs a helyreállítási hálózatnak azt a kiszolgálóját adja meg, amely a $Servers második eleme.

A végleges parancs eltávolítja a hálózati megfeleltetést a $NetworkMappingban.

### 2. példa: a megfeleltetés eltávolítása a hálózat és az Azure Virtual Machine-hálózat között
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -Azure
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

Az első Command parancsmag az aktuális webhely-helyreállítási boltozat kiszolgálóira kerül.
A parancs a $Servers Array változóban tárolja a webhely-helyreállítási kiszolgálókat.

A második parancs az elsődleges hálózat és egy Azure Virtual Machine-hálózat közötti megfeleltetést kapja, majd a $NetworkMapping változóban tárolja.
A parancs a hálózat elsődleges kiszolgálóját adja meg az $Servers első elemeként.
A parancs az *Azure* paramétert adja meg.
Ezért a parancs az Azure Virtual Machine-hálózathoz való megfeleltetést kapja.

A végleges parancs eltávolítja a hálózati megfeleltetést a $NetworkMappingban.

## PARAMÉTEREK

### -NetworkMapping
Az eltávolítandó hálózati megfeleltetést adja meg.

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureSiteRecoveryNetworkMapping](./Get-AzureSiteRecoveryNetworkMapping.md)

[Új – AzureSiteRecoveryNetworkMapping](./New-AzureSiteRecoveryNetworkMapping.md)

[Get-AzureSiteRecoveryServer](./Get-AzureSiteRecoveryServer.md)


