---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: a0572e73d270a37b3c705018a38b4a88fe88d1e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503435"
---
# Get-AzureRmRecoveryServicesVaultSettingsFile

## Áttekintés
Megkapja az Azure webhely-helyreállítási Vault beállítási fájlját.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ForSite
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> -SiteIdentifier <String>
 -SiteFriendlyName <String> [[-Path] <String>] [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByDefault
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-SiteRecovery]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ForBackupVaultType
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmRecoveryServicesVaultSettingsFile** parancsmag az Azure-webhely helyreállítási boltozatának beállítási fájlját kapja meg.

## Példák

### 1. példa: Windows Server-vagy DPM-gép regisztrálása az Azure Backup szolgáltatáshoz
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

Az első parancs a TestVault nevű boltozatot kapja, majd a $Vault 01 változóban tárolja.
A második parancs beállítja a $CredsPath változót a C:\Downloads.-ra.
Az utolsó parancs az Azure biztonsági másolat $CredsPath hitelesítő adataival kapja meg $Vault 01 rendszerhez tartozó Vault hitelesítő adatait tartalmazó fájlt.

### 2. példa:
```
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

A parancs beolvassa a Vault hitelesítő adatait tartalmazó fájlt $Vault 01 a Vault típusú siteRecovery.

### 3. példa: Windows Server-vagy DPM-gép regisztrálása az Azure Backup szolgáltatáshoz
```
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

A parancs a $Vault 01-es számú Vault hitelesítő adatait tartalmazó fájlt kapja meg.

## PARAMÉTEREK

### -Backup
Jelzi, hogy a Vault hitelesítőadat-fájl az Azure Backup alkalmazásra érvényes.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForBackupVaultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -Path (elérési út)
Az Azure webhely-helyreállítási Vault-beállítások fájljának elérési útját adja meg.
Ezt a fájlt az Azure site Recovery Vault portálról töltheti le, és helyileg tárolhatja.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteFriendlyName
A webhely felhasználóbarát nevét adja meg.
Akkor használja ezt a paramétert, ha a Hyper-V-webhelyhez tartozó Vault-hitelesítő adatokat tölti le.

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteIdentifier
A webhely azonosítóját adja meg.
Akkor használja ezt a paramétert, ha a Hyper-V-webhelyhez tartozó Vault-hitelesítő adatokat tölti le.

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteRecovery
Jelzi, hogy a Vault hitelesítőadat-fájl az Azure-webhely helyreállítása esetén érvényes.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForSite, ByDefault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Boltozat
Az Azure webhely-helyreállítási boltozat objektumát adja meg.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. Azure. Command. RecoveryServices. ARSVault
Paraméterek: Vault (ByValue)

## KIMENETEK

### Microsoft. Azure. Command. RecoveryServices. VaultSettingsFilePath

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmRecoveryServicesVault](./Get-AzureRmRecoveryServicesVault.md)

[Új – AzureRmRecoveryServicesVault](./New-AzureRmRecoveryServicesVault.md)

[Remove-AzureRmRecoveryServicesVault](./Remove-AzureRmRecoveryServicesVault.md)


