---
Module Name: Az.KeyVault
Module Guid: D48CF693-4125-4D2D-8790-1514F44CE325
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.keyvault
Help Version: 4.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Az.KeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Az.KeyVault.md
ms.openlocfilehash: 68bbd1131ebd18046d6e974275eddcb75764960b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357249"
---
# Az.KeyVault modul
## Leírás
Ez a témakör az Azure Key Vault-parancsmagok súgótémakörét mutatja be.

## Az.KeyVault parancsmagok
### [Add-AzKeyVaultCertificate](Add-AzKeyVaultCertificate.md)
Hozzáad egy tanúsítványt egy kulcstárolóhoz.

### [Add-AzKeyVaultCertificateContact](Add-AzKeyVaultCertificateContact.md)
Névjegyet ad hozzá a tanúsítványértesítésekért.

### [Add-AzKeyVaultKey](Add-AzKeyVaultKey.md)
Kulcsot hoz létre egy kulcstárban, vagy kulcsot importál egy kulcstárba.

### [Add-AzKeyVaultManagedStorageAccount](Add-AzKeyVaultManagedStorageAccount.md)
Hozzáad egy meglévő Azure Storage-fiókot a megadott kulcstárolóhoz, hogy kulcsait a kulcstár szolgáltatás kezelnie kell.

### [Add-AzKeyVaultNetworkRule](Add-AzKeyVaultNetworkRule.md)
Hozzáad egy szabályt, amely az ügyfél internetcíme alapján korlátozza a kulcstárhoz való hozzáférést.

### [Backup-AzKeyVault](Backup-AzKeyVault.md)
Teljes biztonsági mentés felügyelt HSM-ről.

### [Backup-AzKeyVaultCertificate](Backup-AzKeyVaultCertificate.md)
Egy kulcstárolóban tárolt tanúsítvány biztonsági biztonsági ának biztonságira van berekedve.

### [Backup-AzKeyVaultKey](Backup-AzKeyVaultKey.md)
Kulcs biztonsági biztonsági hátramentve a kulcstárban.

### [Backup-AzKeyVaultManagedStorageAccount](Backup-AzKeyVaultManagedStorageAccount.md)
A KeyVault által felügyelt tárfiók biztonsági biztonsági létrehozása.

### [Backup-AzKeyVaultSecret](Backup-AzKeyVaultSecret.md)
Egy kulcstárban tárolt kulcsról biztonsági biztonsági ként biztonsági szerepet bevetve.

### [Export-AzKeyVaultSecurityDomain](Export-AzKeyVaultSecurityDomain.md)
Felügyelt HSM biztonsági tartományának adatait exportálja.

### [Get-AzKeyVault](Get-AzKeyVault.md)
Kulcstárat kap.

### [Get-AzKeyVaultCertificate](Get-AzKeyVaultCertificate.md)
Tanúsítványt kap egy kulcstárolóból.

### [Get-AzKeyVaultCertificateContact](Get-AzKeyVaultCertificateContact.md)
Egy kulcstároló tanúsítványértesítéseihez regisztrált névjegyeket kap.

### [Get-AzKeyVaultCertificateIssuer](Get-AzKeyVaultCertificateIssuer.md)
Tanúsítvány kibocsátóját kap egy kulcstárolóhoz.

### [Get-AzKeyVaultCertificateOperation](Get-AzKeyVaultCertificateOperation.md)
Tanúsítványművelet állapotát kapja meg.

### [Get-AzKeyVaultCertificatePolicy](Get-AzKeyVaultCertificatePolicy.md)
Egy kulcstárolóban tárolt tanúsítvány házirendje.

### [Get-AzKeyVaultKey](Get-AzKeyVaultKey.md)
Lekérte a kulcstár kulcsait.

### [Get-AzKeyVaultManagedHsm](Get-AzKeyVaultManagedHsm.md)
Felügyelt HSM-eket is lekért.

### [Get-AzKeyVaultManagedStorageAccount](Get-AzKeyVaultManagedStorageAccount.md)
Lekérte a kulcstár által kezelt Azure Storage-fiókokat.

### [Get-AzKeyVaultManagedStorageSasDefinition](Get-AzKeyVaultManagedStorageSasDefinition.md)
Lekérte a kulcstár által felügyelt TÁROLÓ SAS-definíciókat.

### [Get-AzKeyVaultRoleAssignment](Get-AzKeyVaultRoleAssignment.md)
Felügyelt HSM szerepkör-hozzárendelések lekérte vagy listába sorolja azokat. A megfelelő paramétereket használva listába sorolja fel egy adott felhasználó hozzárendelését vagy egy szerepkördefiníciót.

### [Get-AzKeyVaultRoleDefinition](Get-AzKeyVaultRoleDefinition.md)
Egy adott felügyelt HSM szerepkördefinícióit adott hatókörben sorolja fel.

### [Get-AzKeyVaultSecret](Get-AzKeyVaultSecret.md)
Egy kulcstárban rejti el a titkos kulcsokat.

### [Import-AzKeyVaultCertificate](Import-AzKeyVaultCertificate.md)
Tanúsítványt importál egy kulcstárolóba.

### [Import-AzKeyVaultSecurityDomain](Import-AzKeyVaultSecurityDomain.md)
A korábban exportált biztonsági tartományadatok importálása felügyelt HSM-fájlba.

### [New-AzKeyVault](New-AzKeyVault.md)
Kulcstárat hoz létre.

### [New-AzKeyVaultCertificateAdministratorDetail](New-AzKeyVaultCertificateAdministratorDetail.md)
Létrehoz egy memória-tanúsítvány rendszergazdai részleteket tartalmazó objektumát.

### [New-AzKeyVaultCertificateOrganizationDetail](New-AzKeyVaultCertificateOrganizationDetail.md)
Létrehoz egy in-memory certificate organization details object.

### [New-AzKeyVaultCertificatePolicy](New-AzKeyVaultCertificatePolicy.md)
Memóriában létrehozott tanúsítvány-házirendobjektumot hoz létre.

### [New-AzKeyVaultManagedHsm](New-AzKeyVaultManagedHsm.md)
Felügyelt HSM-et hoz létre.

### [New-AzKeyVaultNetworkRuleSetObject](New-AzKeyVaultNetworkRuleSetObject.md)
Hozzon létre egy objektumot, amely a hálózati szabály beállításait képviseli.

### [New-AzKeyVaultRoleAssignment](New-AzKeyVaultRoleAssignment.md)
Hozzárendeli a megadott rbac szerepkört a megadott egyszerű felhasználóhoz a megadott hatókörben.

### [Remove-AzKeyVault](Remove-AzKeyVault.md)
Egy kulcstár törlése.

### [Remove-AzKeyVaultAccessPolicy](Remove-AzKeyVaultAccessPolicy.md)
Eltávolítja egy felhasználó vagy alkalmazás összes engedélyét egy kulcstárból.

### [Remove-AzKeyVaultCertificate](Remove-AzKeyVaultCertificate.md)
Eltávolít egy tanúsítványt egy kulcstárolóból.

### [Remove-AzKeyVaultCertificateContact](Remove-AzKeyVaultCertificateContact.md)
Törli a tanúsítványértesítéshez regisztrált névjegyet egy kulcstárolóból.

### [Remove-AzKeyVaultCertificateIssuer](Remove-AzKeyVaultCertificateIssuer.md)
Törli a tanúsítvány kibocsátóját egy kulcstárolóból.

### [Remove-AzKeyVaultCertificateOperation](Remove-AzKeyVaultCertificateOperation.md)
Egy tanúsítványművelet törlése egy kulcstárolóból.

### [Remove-AzKeyVaultKey](Remove-AzKeyVaultKey.md)
Kulcs törlése a kulcstárból.

### [Remove-AzKeyVaultManagedHsm](Remove-AzKeyVaultManagedHsm.md)
Felügyelt HSM törlése.

### [Remove-AzKeyVaultManagedStorageAccount](Remove-AzKeyVaultManagedStorageAccount.md)
Eltávolít egy kulcstár által felügyelt Azure Storage-fiókot és az összes hozzá tartozó SAS-definíciót.

### [Remove-AzKeyVaultManagedStorageSasDefinition](Remove-AzKeyVaultManagedStorageSasDefinition.md)
Eltávolít egy kulcstár által kezelt Azure Storage SAS-definíciókat.

### [Remove-AzKeyVaultNetworkRule](Remove-AzKeyVaultNetworkRule.md)
Eltávolít egy hálózati szabályt egy kulcstárból.

### [Remove-AzKeyVaultRoleAssignment](Remove-AzKeyVaultRoleAssignment.md)
Eltávolít egy szerepkör-hozzárendelést a megadott egyszerű felhasználóhoz, aki egy adott szerepkörhöz van hozzárendelve egy adott hatókörben.

### [Remove-AzKeyVaultSecret](Remove-AzKeyVaultSecret.md)
Egy kulcstárban tárolt titkos kulcsot töröl.

### [Restore-AzKeyVault](Restore-AzKeyVault.md)
A felügyelt HSM teljes visszaállítása biztonsági másolatból.

### [Restore-AzKeyVaultCertificate](Restore-AzKeyVaultCertificate.md)
Visszaállít egy tanúsítványt egy biztonsági másolatból egy kulcstárolóban.

### [Restore-AzKeyVaultKey](Restore-AzKeyVaultKey.md)
Kulcsot hoz létre egy kulcstárban egy biztonságimentett kulcsból.

### [Restore-AzKeyVaultManagedStorageAccount](Restore-AzKeyVaultManagedStorageAccount.md)
Visszaállít egy felügyelt tárfiókot egy kulcstárolóban egy biztonsági másolatból.

### [Restore-AzKeyVaultSecret](Restore-AzKeyVaultSecret.md)
Egy titkos kulcsot hoz létre egy kulcstárban egy biztonságimentett titkos kulcsból.

### [Set-AzKeyVaultAccessPolicy](Set-AzKeyVaultAccessPolicy.md)
Megadja vagy módosítja egy felhasználó, alkalmazás vagy biztonsági csoport meglévő engedélyét, hogy műveleteket hajtson végre egy kulcstárban.

### [Set-AzKeyVaultCertificateIssuer](Set-AzKeyVaultCertificateIssuer.md)
Egy kulcstárolóban beállítja a tanúsítvány kibocsátóját.

### [Set-AzKeyVaultCertificatePolicy](Set-AzKeyVaultCertificatePolicy.md)
Létrehozza vagy frissíti egy tanúsítvány házirendét egy kulcstárolóban.

### [Set-AzKeyVaultManagedStorageSasDefinition](Set-AzKeyVaultManagedStorageSasDefinition.md)
Egy megosztott hozzáférés-aláírás (SAS) definícióját állítja be egy adott, kulcstárolóval felügyelt Azure Storage-fiók kulcstárával.

### [Set-AzKeyVaultSecret](Set-AzKeyVaultSecret.md)
Titkos kulcsot hoz létre vagy frissítéseket hoz létre egy kulcstárban.

### [Stop-AzKeyVaultCertificateOperation](Stop-AzKeyVaultCertificateOperation.md)
Visszavon egy tanúsítványműveletet a kulcstárolóban.

### [Undo-AzKeyVaultCertificateRemoval](Undo-AzKeyVaultCertificateRemoval.md)
Egy kulcstároló törölt tanúsítványát aktív állapotba visszaállítja.

### [Undo-AzKeyVaultKeyRemoval](Undo-AzKeyVaultKeyRemoval.md)
Egy kulcstár törölt kulcsát aktív állapotba visszaállítja.

### [Undo-AzKeyVaultManagedStorageAccountRemoval](Undo-AzKeyVaultManagedStorageAccountRemoval.md)
Helyreállít egy korábban törölt KeyVault-felügyelt tárfiókot.

### [Undo-AzKeyVaultManagedStorageSasDefinitionRemoval](Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md)
Helyreállít egy korábban törölt KeyVault-felügyelt tárTERÜLET SAS-definícióját.

### [Undo-AzKeyVaultRemoval](Undo-AzKeyVaultRemoval.md)
Helyreállít egy törölt kulcstárat egy aktív állapotba.

### [Undo-AzKeyVaultSecretRemoval](Undo-AzKeyVaultSecretRemoval.md)
Egy kulcstár törölt titkos kulcsát aktív állapotba helyreállítja.

### [Update-AzKeyVault](Update-AzKeyVault.md)
Frissítse egy Azure-kulcstár állapotát.

### [Update-AzKeyVaultCertificate](Update-AzKeyVaultCertificate.md)
Módosítja egy tanúsítvány szerkeszthető attribútumát.

### [Update-AzKeyVaultKey](Update-AzKeyVaultKey.md)
Frissíti egy kulcskulcs attribútumát egy kulcstárban.

### [Update-AzKeyVaultManagedHsm](Update-AzKeyVaultManagedHsm.md)
Frissítse egy Azure által felügyelt HSM állapotát.

### [Update-AzKeyVaultManagedStorageAccount](Update-AzKeyVaultManagedStorageAccount.md)
Frissítheti egy kulcstár által felügyelt Azure Storage-fiók szerkeszthető attribútumát.

### [Update-AzKeyVaultManagedStorageAccountKey](Update-AzKeyVaultManagedStorageAccountKey.md)
A kulcstár által felügyelt Azure Storage-fiók megadott kulcsának újragenerálása.

### [Update-AzKeyVaultNetworkRuleSet](Update-AzKeyVaultNetworkRuleSet.md)
Frissíti a hálózati szabálykészletet egy kulcstárban.

### [Update-AzKeyVaultSecret](Update-AzKeyVaultSecret.md)
Frissíti egy titkos kulcs attribútumát egy kulcstárban.

