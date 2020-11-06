---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 070DA86E-9EA4-4777-9D53-64B58B4401B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/import-azurermsiterecoveryvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
ms.openlocfilehash: 11233414250377331f75e3e8b69f262a0f3a0537
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502383"
---
# Import-AzureRmSiteRecoveryVaultSettingsFile

## Áttekintés
Webhely-helyreállítási Vault-beállítási fájl importálása

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Import-AzureRmSiteRecoveryVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
Az **import-AzureRmSiteRecoveryVaultSettingsFile** parancsmag az Azure webhely-helyreállítási tároló beállítási fájljába importálja az aktuális munkamenetben az azt követő helyreállítási műveletekhez tartozó Vault-környezet beállítását.

## Példák

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

### -Path (elérési út)
A webhely-helyreállítási boltozat beállítási fájljának elérési útját adja meg.
Ez a fájl letölthető a webhely-helyreállítási Vault portálról, és helyben tárolható.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### Microsoft. Azure. Command. SiteRecovery. ASRVaultSettings

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmSiteRecoveryVaultSettingsFile](./Get-AzureRmSiteRecoveryVaultSettingsFile.md)
