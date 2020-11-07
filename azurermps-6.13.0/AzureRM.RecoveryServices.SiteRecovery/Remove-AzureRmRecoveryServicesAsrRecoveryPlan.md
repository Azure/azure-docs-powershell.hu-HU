---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: b3bedc5c521736ff702f5e7378b4c401a42bce5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672104"
---
# Remove-AzureRmRecoveryServicesAsrRecoveryPlan

## Áttekintés
Törli a megadott ASR-helyreállítási csomagot a helyreállítási szolgáltatások boltozatból.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ByObject (alapértelmezett)
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** parancsmag törli a megadott helyreállítási csomagot a helyreállítási szolgáltatások boltozatból.

## Példák

### Példa 1
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

Elindítja a megadott helyreállítási terv törlését, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.

## PARAMÉTEREK

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
A bemeneti objektum a parancsmag: az ASR-helyreállítási terv objektuma, amely megfelel a törlendő helyreállítási tervnek.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (név)
A törlendő helyreállítási terv nevét adja meg.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut. A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryPlan

## KIMENETEK

### System. Object (rendszer. objektum)

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmRecoveryServicesAsrRecoveryPlan](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[Új – AzureRmRecoveryServicesAsrRecoveryPlan](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[Update-AzureRmRecoveryServicesAsrRecoveryPlan](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)


