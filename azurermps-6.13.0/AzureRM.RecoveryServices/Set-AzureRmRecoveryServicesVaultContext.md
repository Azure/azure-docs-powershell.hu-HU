---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/set-azurermrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
ms.openlocfilehash: 0989bdcc14a9f7e3cbd65af11aea843cdd0ec6e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492767"
---
# Set-AzureRmRecoveryServicesVaultContext

## Áttekintés
Beállítja a boltozat kontextusát.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Set-AzureRmRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **set-AzureRmRecoveryServicesVaultContext** parancsmag az Azure webhely-helyreállítási szolgáltatások boltozat-környezetét állítja be.

## Példák

### Példa 1
```
PS C:\> Set-AzureRmRecoveryServicesVaultContext -Vault $vault
```

Beállítja a boltozat kontextusát.

## PARAMÉTEREK

### -Boltozat
A boltozat nevét adja meg.
A boltozatnak **AzureRmRecoveryServicesVault** objektumnak kell lennie.

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. Azure. Command. RecoveryServices. ARSVault
Paraméterek: Vault (ByValue)

## KIMENETEK

### System. Void

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
