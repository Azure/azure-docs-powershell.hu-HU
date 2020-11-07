---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 59a5cbde2bde2c2cbe5834f73199c7b86791d247
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672424"
---
# New-AzureRmRecoveryServicesAsrRecoveryPlan

## Áttekintés
ASR-helyreállítási csomagot hoz létre.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### EnterpriseToEnterprise (alapértelmezett)
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric>
 -RecoveryFabric <ASRFabric> -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### EnterpriseToAzure
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByRPFile
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Path <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **New-AzureRmRecoveryServicesAsrRecoveryPlan** parancsmag az Azure webhely-helyreállítási helyreállítási csomagot hoz létre a helyreállítási szolgáltatások pincéjében.

A helyreállítási terv az alkalmazásba tartozó virtuális gépeket egy egységbe gyűjti, amely lehetővé teszi számukra a helyreállítást.

## Példák

### Példa 1
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

Elindítja a helyreállítási terv létrehozása műveletet a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.

## PARAMÉTEREK

### -Azure
Váltson paramétert, és adja meg, hogy a helyreállítási terv helyreállítási helye Azure-e.

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

### -FailoverDeploymentModel
Megadja a helyreállítási csomag részét képező replikációs telepítő modellt (klasszikus vagy erőforrás-kezelő) a replikációs védelemmel ellátott elemek között.

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A helyreállítási terv neve.

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path (elérési út)
A helyreállítási terv definíciója JSON-fájl elérési útját adja meg. A helyreállítási terv definíciója: a JSON segítségével létrehozhatja a helyreállítási tervet.

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrimaryFabric
A helyreállítási csomag részét képező, a replikációs védelemmel ellátott elemek elsődleges ASR-szövetéhez tartozó ASR-szövet objektumot adja meg.

```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryFabric
A helyreállítási csomag részét képező replikációs helyreállítási anyaghoz tartozó ASR-szövet objektum.

```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationProtectedItem
A helyreállítási terv első csoportjához hozzáadni kívánt replikációs védelemmel ellátott elemek listája.

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
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

### Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem []

## KIMENETEK

### System. Object (rendszer. objektum)

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmRecoveryServicesAsrRecoveryPlan](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[Remove-AzureRmRecoveryServicesAsrRecoveryPlan](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[Update-AzureRmRecoveryServicesAsrRecoveryPlan](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)


