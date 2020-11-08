---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 6802F2E9-5925-4E92-AEB8-827B5A303617
online version: ''
schema: 2.0.0
ms.openlocfilehash: 153e30c03de7a0a5c404526bd06b9acb2f0678f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016217"
---
# New-AzureSiteRecoveryNetworkMapping

## Áttekintés
Társítást hoz létre a virtuális hálózatok között.

## SZINTAXISA

### EnterpriseToEnterprise
```
New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork <ASRNetwork> -RecoveryNetwork <ASRNetwork>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### EnterpriseToAzure
```
New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork <ASRNetwork> -AzureSubscriptionId <String>
 -AzureVMNetworkId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **New-AzureSiteRecoveryNetworkMapping** parancsmag létrehoz egy megfeleltetést két virtuális hálózat között, és egy Azure webhely-helyreállítási feladatot ad eredményül a követéshez.

## Példák

### 1. példa: megfeleltetés létrehozása a hálózat és a helyreállítási hálózat között
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $Networks = Get-AzureSiteRecoveryNetwork -Server $Servers[0]
PS C:\> New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork $Networks[0] -RecoveryNetwork $Networks[1]
```

Az első Command parancsmag a **Get-AzureSiteRecoveryServer** parancsmaggal kapja meg az aktuális Azure-webhely helyreállítási boltozatának kiszolgálóit.
A parancs a $Servers Array változóban tárolja a webhely-helyreállítási kiszolgálókat.

A második parancs a **Get-AzureSiteRecoveryNetwork** parancsmaggal kapja meg az első kiszolgálónak a webhely-helyreállítási hálózatát a $Servers tömbben.
A parancs a $Networks változóban tárolja a hálózatokat.

A végleges parancs az elsődleges hálózat és a helyreállítási hálózat között hoz létre megfeleltetést.
A parancs az elsődleges hálózatot az $Networks első elemeként adja meg.
A parancs a $Networks második elemeként adja meg a helyreállítási hálózatot.

## PARAMÉTEREK

### -AzureSubscriptionId
Az Azure-előfizetés AZONOSÍTÓját adja meg.

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureVMNetworkId
Az Azure virtuális hálózat AZONOSÍTÓját adja meg.

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrimaryNetwork
Az elsődleges hálózat objektumát adja meg.

```yaml
Type: ASRNetwork
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

### -RecoveryNetwork
A helyreállítási hálózat objektumát adja meg.

```yaml
Type: ASRNetwork
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

[Get-AzureSiteRecoveryNetworkMapping](./Get-AzureSiteRecoveryNetworkMapping.md)

[Get-AzureSiteRecoveryServer](./Get-AzureSiteRecoveryServer.md)

[Remove-AzureSiteRecoveryNetworkMapping](./Remove-AzureSiteRecoveryNetworkMapping.md)


