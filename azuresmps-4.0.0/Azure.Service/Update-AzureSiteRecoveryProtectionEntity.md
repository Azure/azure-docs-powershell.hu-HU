---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 16146A0D-4605-489A-8259-A37BEAC98306
online version: ''
schema: 2.0.0
ms.openlocfilehash: 664c9af9373120f293153a1bbdc65d1a82637631
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016015"
---
# Update-AzureSiteRecoveryProtectionEntity

## Áttekintés
A védelmi entitások tulajdonságait frissíti az Azure webhely-helyreállításban.

## SZINTAXISA

```
Update-AzureSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Az **Update-AzureSiteRecoveryProtectionEntity** parancsmag az Azure webhely-helyreállításban (például a virtuális gép tulajdonosának adatai) frissíti a védelmi entitások tulajdonságait.
Ezt a parancsmagot csak a Virtual Machine monitor (VMM) támogatja, hogy VMM a védett védelmi entitásokat.

## Példák

### Példa 1: védelmi entitás frissítése
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container
PS C:\> Update-AzureSiteRecoveryProtectionEntity -ProtectionEntity $ProtectionEntity
           Name             : 
           ID               : 680ffe0f-6236-465e-8c94-81242fa67e6d
           ClientRequestId  : 2c47e6ce-1460-4187-8a0f-b9073735fa38-2014-12-30 06:44:40Z-P
           State            : NotStarted
           StateDescription : NotStarted
           StartTime        : 
           EndTime          : 
           AllowedActions   : {}
           Tasks            : {}
           Errors           : {}
```

Az első parancs a **Get-AzureSiteRecoveryProtectionContainer** parancsmag használatával kap védett tárolót, majd az objektumot a $Container változóban tárolja.

A második parancs a **Get-AzureSiteRecoveryProtectionEntity** parancsmaggal a $Container tárolt tárolóhoz tartozó védett virtuális gépet kapja, majd a $ProtectionEntity változóban tárolja.

A végleges parancs frissíti a védelmi entitást a $ProtectionEntityban.

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

### -ProtectionEntity
A frissítendő védelmi entitást adja meg.
Ha **ASRProtectionEntity** objektumot szeretne beolvasni, használja a **Get-AzureSiteRecoveryProtectionEntity** parancsmagot.

```yaml
Type: ASRProtectionEntity
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WaitForCompletion
Azt jelzi, hogy ez a parancsmag a művelet befejezését várja, mielőtt a vezérlőt visszaadja a Windows PowerShell-konzolnak.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureSiteRecoveryProtectionContainer](./Get-AzureSiteRecoveryProtectionContainer.md)

[Get-AzureSiteRecoveryProtectionEntity](./Get-AzureSiteRecoveryProtectionEntity.md)

[Set-AzureSiteRecoveryProtectionEntity](./Set-AzureSiteRecoveryProtectionEntity.md)


