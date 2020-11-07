---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: e5bb8a19cb616c9696ec224d8f1d9d25678d9e47
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669717"
---
# Get-AzRecoveryServicesAsrVaultContext

## Áttekintés
Megkapja az ASR-tároló beállításait a helyreállítási szolgáltatások boltozatához.

## SZINTAXISA

```
Get-AzRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzRecoveryServicesAsrVaultContext** PARANCSMAG az ASR Vault-beállításokkal kapcsolatos információkat kapja a helyreállítási szolgáltatások boltozatával kapcsolatban.

## Példák

### Példa 1
```
PS C:\> $VaultSettings = Get-AzRecoveryServicesAsrVaultContext
```

Beolvassa az ASR-tároló beállításait a jelenleg aktív (a PowerShell-munkamenetben) helyreállítási szolgáltatások pincéjében.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRVaultSettings

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
