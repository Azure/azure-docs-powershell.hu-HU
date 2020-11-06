---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: fbd2f518d3bdcf64599e32b55cdb9f416c29be21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504788"
---
# Get-AzureRmRecoveryServicesAsrReplicationProtectedItem

## Áttekintés
Beolvassa az Azure webhely-helyreállítási replikációval védett elemek tulajdonságait.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ByObject (alapértelmezett)
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### ByObjectWithName
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

### ByObjectWithFriendlyName
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

### ByProtectableItemObject
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [<CommonParameters>]
```

## Leírás
A **Get-AzureRmRecoveryServicesAsrReplicationProtectedItem** parancsmag a megadott ASR-védelmi tárolóból az összes vagy a megadott ASR-replikációs védett elem tulajdonságait kapja.

## Példák

### Példa 1
```
PS C:\> $ReplicationProtectedItems = Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer $PrimaryContainer
```

A megadott ASR-védelmi tárolóban lévő összes replikációs védelemmel ellátott elem felsorolása.

## PARAMÉTEREK

### -Típusú megjelenített
A beolvasott replikációs védett elem rövid nevét adja meg.

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A beolvasott replikációs védett elem nevét adja meg.

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProtectableItem
Egy ASR-védelemmel ellátott elem objektumot ad meg. A parancsmag a megadott ASR-védelemmel ellátott, a megadott ASR-védelemmel ellátott elemnek megfelelő, ha az elem védett.

```yaml
Type: ASRProtectableItem
Parameter Sets: ByProtectableItemObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ProtectionContainer
A replikációs védelemmel ellátott védett elemnek megfelelő ASR-védelmi tároló objektumot adja meg. 

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject, ByObjectWithName, ByObjectWithFriendlyName
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

### Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRProtectionContainer
Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRProtectableItem

## KIMENETEK

### System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 4.0.0.0, Culture = semleges, PublicKeyToken = null]]

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureRmRecoveryServicesAsrReplicationProtectedItem](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[Set-AzureRmRecoveryServicesAsrReplicationProtectedItem](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
