---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 185506BC-6155-4517-BCBD-BCDE7450C7A8
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8017c2947a8d046226a63b5ed07b3714c35b22c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016410"
---
# Start-AzureSiteRecoveryProtectionProfileDissociationJob

## Áttekintés
Disszociációs feladatot indít egy webhely-helyreállítási védelemmel ellátni kívánt replikációs házirendben.

## SZINTAXISA

### EnterpriseToAzure (alapértelmezett)
```
Start-AzureSiteRecoveryProtectionProfileDissociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### EnterpriseToEnterprise
```
Start-AzureSiteRecoveryProtectionProfileDissociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Start-AzureSiteRecoveryProtectionProfileDissociationJob** parancsmag disszociációs feladatot kezdeményez az Azure-webhely helyreállítási védelmi tárolója által társított replikációs házirendben.

## Példák

### 1. példa: védelmi profil szétválasztása
```
PS C:\> $ProtectionContainer01 = Get-AzureSiteRecoveryProtectionContainer -Id "5ba2ea95-856d-4033-9ca3-91e3e2c080b9"
PS C:\> $ProtectionContainer02 = Get-AzureSiteRecoveryProtectionContainer -Id "cf011f2a-aa19-443c-9f60-357f6b8afb77"
PS C:\> Start-AzureSiteRecoveryProtectionProfileDissociationJob -PrimaryProtectionContainer $ProtectionContainer01 -ProtectionProfile $ProtectionContainer01.AvailableProtectionProfiles[0] -RecoveryProtectionContainer $ProtectionContainer02
Name             : MyProtectionProfile
ID               : 51978b0f-9241-4153-9171-2e19344f0805
ClientRequestId  : bb6f3200-b7c6-4c6f-bcbc-a70bb9946f03-2015-01-30 02:55:55Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : 
Tasks            : {}
Errors           : {}
```

Az első parancs a **Get-AzureSiteRecoveryProtectionContainer** parancsmag használatával kap védelmi tárolót, és a tárolót a $ProtectionContainer 01 változóban tárolja.

A második parancs a védelmi tárolót kapja, majd a $ProtectionContainer 02 változóban tárolja.

A végleges parancs elválasztja az elsődleges védelmi tárolóként az $ProtectionContainer 01-ben tárolt tároló védelmi profilját.
A parancs elválasztja a $ProtectionContainer 02-ben tárolt tárolót a helyreállítási védelmi tárolóban.

## PARAMÉTEREK

### -PrimaryProtectionContainer
Az elsődleges védelmi tárolót adja meg.

```yaml
Type: ASRProtectionContainer
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

### -ProtectionProfile
Itt adhatja meg a védelemi profil beállításait a védett tárolókkal való társításhoz.
Itt adhatja meg a védett tárolók védelmi profiljának beállításait.
**ASRProtectionProfile** objektum beolvasásához használja az New-AzureSiteRecoveryProtectionProfileObject parancsmagot.

```yaml
Type: ASRProtectionProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RecoveryProtectionContainer
A helyreállítási védelmi tárolót adja meg.

```yaml
Type: ASRProtectionContainer
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

[Get-AzureSiteRecoveryProtectionContainer](./Get-AzureSiteRecoveryProtectionContainer.md)

[Új – AzureSiteRecoveryProtectionProfileObject](./New-AzureSiteRecoveryProtectionProfileObject.md)

[Start-AzureSiteRecoveryProtectionProfileAssociationJob](./Start-AzureSiteRecoveryProtectionProfileAssociationJob.md)


