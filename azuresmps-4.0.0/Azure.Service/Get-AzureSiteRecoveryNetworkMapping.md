---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: F6C01C25-655C-4798-9826-F7CB168181C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: bc8b7dc7e23a98111e75c2b2c9c079f010e3c5dc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015590"
---
# Get-AzureSiteRecoveryNetworkMapping

## Áttekintés
A webhely-helyreállítási boltozat hálózati megfeleltetéseit kapja.

## SZINTAXISA

### EnterpriseToEnterprise
```
Get-AzureSiteRecoveryNetworkMapping -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### EnterpriseToAzure
```
Get-AzureSiteRecoveryNetworkMapping -PrimaryServer <ASRServer> [-Azure] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureSiteRecoveryNetworkMapping** parancsmag információkat kap az Azure webhely-helyreállítási hálózati megfeleltetésekről az aktuális webhely-helyreállítási boltozathoz.

## Példák

### Példa 1: a hálózat és a helyreállítási hálózat közötti megfeleltetés beszerzése
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[0]
PrimaryServerId     : 774859b0-1966-48cc-9df7-759c441b7a8c
PrimaryNetworkId    : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
PrimaryNetworkName  : phase2RecoveryVMNetwork
RecoveryServerId    : 774859b0-1966-48cc-9df7-759c441b7a8c
RecoveryNetworkId   : d903e2c6-3141-4cef-bfe1-04616cd43cbb
RecoveryNetworkName : phase2PrimaryVMNetwork
PairingStatus       : OK
```

Az első Command parancsmag a **Get-AzureSiteRecoveryServer** parancsmaggal kapja meg az aktuális Azure-webhely helyreállítási boltozatának kiszolgálóit.
A parancs a $Servers Array változóban tárolja a webhely-helyreállítási kiszolgálókat.

A második parancs az elsődleges hálózat és a helyreállítási hálózat közötti megfeleltetést kapja.
A parancs a hálózati megfeleltetés elsődleges kiszolgálóját adja meg az $Servers első elemeként.
A parancs a helyreállítási hálózatnak azt a kiszolgálóját adja meg, amely a $Servers második eleme.

### 2. példa: a megfeleltetés beszerzése a hálózat és az Azure virtuális gép hálózata között
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetworkMapping -Azure -PrimaryServer $Servers[0] 
PrimaryServerId     : 774859b0-1966-48cc-9df7-759c441b7a8c
PrimaryNetworkId    : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
PrimaryNetworkName  : phase2RecoveryVMNetwork
RecoveryServerId    : 21a9403c-6ec1-44f2-b744-b4e50b792387
RecoveryNetworkId   : ecb3a462-664f-4f57-873e-d09b5925e1a1
RecoveryNetworkName : AzureVMNetwork
PairingStatus       : OK
```

Az első Command parancsmag az aktuális webhely-helyreállítási boltozat kiszolgálóira kerül.
A parancs a $Servers Array változóban tárolja a kiszolgálókat.

A második parancs az elsődleges hálózat és az Azure Virtual Machine-hálózat közötti megfeleltetést kapja.
A parancs a hálózat elsődleges kiszolgálóját adja meg az $Servers első elemeként.
A parancs az *Azure* paramétert adja meg.
Ezért a parancs az Azure Virtual Machine-hálózathoz való megfeleltetést kapja.

## PARAMÉTEREK

### -Azure
Azt jelzi, hogy ez a parancsmag hálózati megfeleltetéseket kap az elsődleges kiszolgálón az Azure virtuális hálózatokhoz rendelt hálózatokhoz.

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrimaryServer
Itt adhatja meg azt az elsődleges kiszolgálót, amelyhez megfeleltetéseket szeretne kapni.

```yaml
Type: ASRServer
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

### -RecoveryServer
Azt a helyreállítási kiszolgálót adja meg, amelyhez megfeleltetéseket szeretne kapni.

```yaml
Type: ASRServer
Parameter Sets: EnterpriseToEnterprise
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

[Új – AzureSiteRecoveryNetworkMapping](./New-AzureSiteRecoveryNetworkMapping.md)

[Remove-AzureSiteRecoveryNetworkMapping](./Remove-AzureSiteRecoveryNetworkMapping.md)


