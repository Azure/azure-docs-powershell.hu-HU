---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 62f27b43158f8b01abc7be48cab93f4bb957258b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921657"
---
# Get-AzRecoveryServicesAsrVaultContext

## SYNOPSIS
A Helyreállítási szolgáltatások tárolóra vonatkozó ASR-tároló beállításainak adatait kapja meg.

## SZINTAXIS

```
Get-AzRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzRecoveryServicesAsrVaultContext parancsmag** asr tárolóbeállítási információkat kap a Helyreállítási szolgáltatások tárolóhoz.

## PÉLDÁK

### 1. példa
```
PS C:\> $VaultSettings = Get-AzRecoveryServicesAsrVaultContext
```

Az aktuálisan aktív (a PowerShell-munkamenetben) helyreállítási szolgáltatások tárolója ASR-tárolóbeállítását kapja meg.

## PARAMETERS

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

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Nincs

## KIMENETEK

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
