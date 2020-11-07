---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 7C695E83-78AA-4008-91D6-D6B23BC96B92
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: d6c93a6ca54a67c13fcba54a11d9f30c61377e19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679671"
---
# Remove-AzureRmSiteRecoveryRecoveryPlan

## Áttekintés
Webhely-helyreállítási csomag eltávolítása a webhely-helyreállításból.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ByObject (alapértelmezett)
```
Remove-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Remove-AzureRmSiteRecoveryRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Remove-AzureRmSiteRecoveryRecoveryPlan** parancsmag eltávolítja a webhely-helyreállítási csomagot az Azure jelenlegi helyreállítási webhelyről.

## Példák

### 1. példa: helyreállítási terv eltávolítása
```
PS C:\>$RecoveryPlan = Get-AzureRmSiteRecoveryRecoveryPlan 
PS C:\> Remove-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan $RecoveryPlan
```

Az első parancs az Get-AzureRmSiteRecoveryRecoveryPlan parancsmagot használja a webhely-helyreállítási terv beszerzéséhez, majd a $RecoveryPlan változóban tárolja.

A második parancs eltávolítja az $RecoveryPlan helyreállítási tervét.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
Annak a helyreállítási tervnek a nevét adja meg, amelyre a parancsmag eltávolítja.

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryPlan
Azt a helyreállítási tervet adja meg, amelyre a parancsmag eltávolítja.

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByObject
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

### ASRRecoveryPlan
A ' RecoveryPlan ' paraméter az "ASRRecoveryPlan" típusú értéket fogadja el a csővezetékről

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmSiteRecoveryRecoveryPlan](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[Új – AzureRmSiteRecoveryRecoveryPlan](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[Update-AzureRmSiteRecoveryRecoveryPlan](./Update-AzureRmSiteRecoveryRecoveryPlan.md)


