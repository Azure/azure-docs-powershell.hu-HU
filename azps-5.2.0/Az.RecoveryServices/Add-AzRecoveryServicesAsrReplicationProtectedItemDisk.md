---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/add-azrecoveryservicesasrreplicationprotecteditemdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: ab8c2bb74f381be898dc243ddd010462f8158ed2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333330"
---
# Add-AzRecoveryServicesAsrReplicationProtectedItemDisk

## SYNOPSIS
Vegye fel a lemezt a már védett Azure virtuális gép védelme érdekében.

## SZINTAXIS

```
Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
Az **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** parancsmag hozzáadja a lemezt a már védett Azure virtuális gép védelme érdekében.

## PÉLDÁK

### 1. példa
```powershell
PS C:> Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

Indítsa el a műveletet adott lemezkonfiguráció hozzáadásához a védelem érdekében.

### 2. példa
```powershell
PS C:> $ReplicationProtectedItem |Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

Indítsa el a műveletet adott lemezkonfiguráció hozzáadásához a védelem érdekében. Piping input replication protected item.

## PARAMETERS

### -AzureToAzureDiskReplicationConfiguration
Az Azure–Azure katasztrófa-helyreállítási forgatókönyv lemezvédelemhez használt lemezkonfigurációja.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
A parancsmag bemeneti objektuma: A ASR replikációs védett elemobjektuma, amely megfelel az új lemeznek.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WaitForCompletion
Várakozás a befejezésre

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

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
A parancsmag futtatásakor a program megjeleníti, hogy mi történik.
A parancsmag nem fut.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Nincs

## KIMENETEK

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
