---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: ad22cbe1cb17e69358ef386b478fe929abe415b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672425"
---
# Import-AzureRmRecoveryServicesAsrVaultSettingsFile

## Áttekintés
Importálja a megadott ASR-tároló beállítási fájlját a boltozat környezetének (PowerShell-munkamenet-környezet) beállításához a PowerShell-munkamenetben a további ASR-műveletekhez. 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Import-AzureRmRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
Az **import-AzureRmRecoveryServicesAsrVaultSettingsFile** parancsmag importálja az Azure-webhely helyreállítási Vault-beállításait tartalmazó fájlt. A Vault-beállítások fájl az aktuális munkamenetben a következő Azure-webhely-helyreállítási műveletek boltozat-környezetének beállítására szolgál.

## Példák

### Példa 1
```
PS C:\> $VaultSettings = Import-AzureRmRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

Importálja a megadott helyreállítási szolgáltatások Vault-beállítási fájlját, és az importált boltozat beállításait adja eredményül.

## PARAMÉTEREK

### -Path (elérési út)
Az ASR-boltozat beállítási fájljának elérési útját adja meg.
Ez a fájl letölthető a helyreállítási szolgáltatások Vault-portálról, és helyben tárolható.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### System. String

## KIMENETEK

### Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRVaultSettings

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmRecoveryServicesAsrVaultSettingsFile](./Get-AzureRmRecoveryServicesAsrVaultSettingsFile.md)
