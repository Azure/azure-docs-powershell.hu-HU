---
Module Name: Az.Resources
Module Guid: ab3ca893-26fe-44b0-bd3c-8933df144d7b
Download Help Link: https://docs.microsoft.com/powershell/module/az.resources
Help Version: 5.5.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Az.Resources.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Az.Resources.md
ms.openlocfilehash: 7cf0104a2383f6e7e48be21ae5ffa947fd4d284b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929865"
---
# Az.Resources modul
## Leírás
Ez a témakör az Azure Resource Manager-parancsmagok súgótémakörét mutatja be.

## Az.Resources parancsmagok
### [Add-AzADGroupMember](Add-AzADGroupMember.md)
Hozzáad egy felhasználót egy meglévő AD-csoporthoz.

### [Export-AzResourceGroup](Export-AzResourceGroup.md)
Sablonként rögzít egy erőforráscsoportot, és fájlba menti.

### [Export-AzTemplateSpec](Export-AzTemplateSpec.md)
Sablon specifikációjának exportálása a helyi fájlrendszerbe

### [Get-AzADAppCredential](Get-AzADAppCredential.md)
Beolvassa az alkalmazáshoz társított hitelesítő adatok listáját.

### [Get-AzADApplication](Get-AzADApplication.md)
A meglévő Azure Active Directory-alkalmazások listája.

### [Get-AzADGroup](Get-AzADGroup.md)
Az Active Directory-csoportok szűrése.

### [Get-AzADGroupMember](Get-AzADGroupMember.md)
Az aktuális bérlői webhely AD-csoportjának tagjait sorolja fel.

### [Get-AzADServicePrincipal](Get-AzADServicePrincipal.md)
Szűri az active directory-szolgáltatásban használható egyszerű címtár-rendszereket.

### [Get-AzADSpCredential](Get-AzADSpCredential.md)
Beolvassa a szolgáltatásnévvel társított hitelesítő adatok listáját.

### [Get-AzADUser](Get-AzADUser.md)
Szűri az Active Directory-felhasználókat.

### [Get-AzDenyAssignment](Get-AzDenyAssignment.md)
Az Azure RBAC a megadott hatókörű hozzárendeléseket tiltja le.
Alapértelmezés szerint a kijelölt Azure-előfizetés összes elutasító hozzárendelését felsorolja.
A megfelelő paramétereket használva listában elutasíthatja egy adott felhasználó hozzárendelését, vagy elutasíthatja egy adott erőforráscsoport vagy erőforrás hozzárendelését.

### [Get-AzDeployment](Get-AzDeployment.md)
Üzembe helyezés

### [Get-AzDeploymentOperation](Get-AzDeploymentOperation.md)
Telepítési művelet

### [Get-AzDeploymentScript](Get-AzDeploymentScript.md)
Telepítési parancsfájlokat kap vagy sorol fel.

### [Get-AzDeploymentScriptLog](Get-AzDeploymentScriptLog.md)
Az üzembe helyezési parancsfájl végrehajtásának naplóját kapja.

### [Get-AzDeploymentWhatIfResult](Get-AzDeploymentWhatIfResult.md)
Egy ARM sablont What-If az előfizetés hatókörében való telepítés eredményéhez. 

### [Get-AzLocation](Get-AzLocation.md)
Lekérte az összes helyet és a támogatott erőforrás-szolgáltatókat az egyes helyekhez.

### [Get-AzManagedApplication](Get-AzManagedApplication.md)
Felügyelt alkalmazások lekérte

### [Get-AzManagedApplicationDefinition](Get-AzManagedApplicationDefinition.md)
Felügyelt alkalmazásdefiníciók lekérte

### [Get-AzManagementGroup](Get-AzManagementGroup.md)
Felügyeleti csoport(ak) lekérte

### [Get-AzManagementGroupDeployment](Get-AzManagementGroupDeployment.md)
Központi telepítés egy felügyeleti csoportnál

### [Get-AzManagementGroupDeploymentOperation](Get-AzManagementGroupDeploymentOperation.md)
Telepítési művelet a felügyeleti csoportok központi telepítéséhez

### [Get-AzManagementGroupDeploymentWhatIfResult](Get-AzManagementGroupDeploymentWhatIfResult.md)
Egy ARM sablont What-If a felügyeleti csoport hatókörében való telepítés eredményéhez. 

### [Get-AzPolicyAlias](Get-AzPolicyAlias.md)
Get-AzPolicyAlias beolvassa és kimenetként kinyeri az Azure-szolgáltató olyan erőforrástípusokat, amelyekhez aliasok vannak definiálva, és amelyek megfelelnek a megadott paraméterértéknek. Ha nem ad meg paramétereket, az aliast tartalmazó összes szolgáltató erőforrástípus kimenete lesz.
A -ListAvailable kapcsoló módosítja ezt a viselkedést úgy, hogy felsorolja az összes egyező erőforrástípust, beleértve az alias nélkülieket is.

### [Get-AzPolicyAssignment](Get-AzPolicyAssignment.md)
Házirend-hozzárendeléseket kap.

### [Get-AzPolicyDefinition](Get-AzPolicyDefinition.md)
Házirend-definíciókat kap.

### [Get-AzPolicySetDefinition](Get-AzPolicySetDefinition.md)
Házirend-definíciókat kap.

### [Get-AzProviderFeature](Get-AzProviderFeature.md)
Információkat kap az Azure-szolgáltató funkcióiról.

### [Get-AzProviderOperation](Get-AzProviderOperation.md)
Egy Azure-erőforrás-szolgáltató azure RBAC-n keresztül biztonságos műveleteit kapja meg.

### [Get-AzResource](Get-AzResource.md)
Erőforrásokat kap.

### [Get-AzResourceGroup](Get-AzResourceGroup.md)
Erőforráscsoportokat kap.

### [Get-AzResourceGroupDeployment](Get-AzResourceGroupDeployment.md)
Beveszi a telepítéseket egy erőforráscsoportban.

### [Get-AzResourceGroupDeploymentOperation](Get-AzResourceGroupDeploymentOperation.md)
Az erőforráscsoport üzembe helyezésének művelete

### [Get-AzResourceGroupDeploymentWhatIfResult](Get-AzResourceGroupDeploymentWhatIfResult.md)
Egy ARM sablont What-If az erőforráscsoport hatókörében való telepítés eredményéhez. 

### [Get-AzResourceLock](Get-AzResourceLock.md)
Erőforrás-zárolást kap.

### [Get-AzResourceProvider](Get-AzResourceProvider.md)
Erőforrás-szolgáltatót kap.

### [Get-AzRoleAssignment](Get-AzRoleAssignment.md)
A megadott hatókörű Azure RBAC-szerepkör-hozzárendelések listája.
Alapértelmezés szerint a kijelölt Azure-előfizetés összes szerepkör-hozzárendelését felsorolja.
A megfelelő paramétereket használva listába sorolja egy adott felhasználó hozzárendelését, illetve egy adott erőforráscsoport vagy erőforrás hozzárendelését.

### [Get-AzRoleDefinition](Get-AzRoleDefinition.md)
A hozzárendeléshez elérhető összes Azure RBAC-szerepkört sorolja fel.

### [Get-AzTag](Get-AzTag.md)
Előre definiált Azure-címkéket | Egy erőforrás vagy előfizetés teljes címkéit beveszi.

### [Get-AzTemplateSpec](Get-AzTemplateSpec.md)
Sablon specifikációi

### [Get-AzTenantDeployment](Get-AzTenantDeployment.md)
Üzembe helyezés bérlői hatókörben

### [Get-AzTenantDeploymentOperation](Get-AzTenantDeploymentOperation.md)
Telepítési művelet lekérte a bérlői webhely hatókörében való üzembe helyezést

### [Get-AzTenantDeploymentWhatIfResult](Get-AzTenantDeploymentWhatIfResult.md)
Egy ARM sablont What-If a bérlői webhelyen való telepítéshez. 

### [Invoke-AzResourceAction](Invoke-AzResourceAction.md)
Meghív egy műveletet egy erőforráson.

### [Move-AzResource](Move-AzResource.md)
Áthelyez egy erőforrást egy másik erőforráscsoportba vagy -előfizetésbe.

### [New-AzADAppCredential](New-AzADAppCredential.md)
Hitelesítő adatokat ad hozzá egy meglévő alkalmazáshoz.

### [New-AzADApplication](New-AzADApplication.md)
Létrehoz egy új Azure Active Directory-alkalmazást.

### [New-AzADGroup](New-AzADGroup.md)
Új Active Directory-csoportot hoz létre.

### [New-AzADServicePrincipal](New-AzADServicePrincipal.md)
Új Azure Active Directory-szolgáltatásnév létrehozása.

### [New-AzADSpCredential](New-AzADSpCredential.md)
Hitelesítő adatokat ad hozzá egy meglévő egyszerű szolgáltatásnévhez.

### [New-AzADUser](New-AzADUser.md)
Új Active Directory-felhasználót hoz létre.

### [New-AzDeployment](New-AzDeployment.md)
Telepítés létrehozása

### [New-AzManagedApplication](New-AzManagedApplication.md)
Azure által felügyelt alkalmazást hoz létre.

### [New-AzManagedApplicationDefinition](New-AzManagedApplicationDefinition.md)
Felügyelt alkalmazásdefiníciót hoz létre.

### [New-AzManagementGroup](New-AzManagementGroup.md)
Felügyeleti csoportot hoz létre

### [New-AzManagementGroupDeployment](New-AzManagementGroupDeployment.md)
Központi telepítés létrehozása egy felügyeleti csoportban

### [New-AzManagementGroupSubscription](New-AzManagementGroupSubscription.md)
Előfizetés hozzáadása felügyeleti csoporthoz.

### [New-AzPolicyAssignment](New-AzPolicyAssignment.md)
Házirend-hozzárendelést hoz létre.

### [New-AzPolicyDefinition](New-AzPolicyDefinition.md)
Házirenddefiníciót hoz létre.

### [New-AzPolicySetDefinition](New-AzPolicySetDefinition.md)
Házirendkészlet-definíciót hoz létre.

### [New-AzResource](New-AzResource.md)
Létrehoz egy erőforrást.

### [New-AzResourceGroup](New-AzResourceGroup.md)
Létrehoz egy Azure-erőforráscsoportot.

### [New-AzResourceGroupDeployment](New-AzResourceGroupDeployment.md)
Hozzáad egy Azure-telepítést egy erőforráscsoporthoz.

### [New-AzResourceLock](New-AzResourceLock.md)
Erőforrászárolást hoz létre.

### [New-AzRoleAssignment](New-AzRoleAssignment.md)
Hozzárendeli a megadott rbac szerepkört a megadott egyszerű felhasználóhoz a megadott hatókörben.

### [New-AzRoleDefinition](New-AzRoleDefinition.md)
Egyéni szerepkört hoz létre az Azure RBAC-ban.
Adjon meg JSON szerepkördefiníciós fájlt vagy PSRoleDefinition objektumot bemenetként.
Először a Get-AzRoleDefinition paranccsal hozzon létre egy alaptervi szerepkör-definíciós objektumot.
Ezután szükség szerint módosítsa a tulajdonságait.
Végül ezzel a paranccsal szerepkördefiníció használatával hozhat létre egyéni szerepkört.

### [New-AzTag](New-AzTag.md)
Előre definiált Azure-címkét hoz létre, vagy értékeket ad hozzá egy meglévő | Létrehozza vagy frissíti a címkék teljes készletét egy erőforráson vagy előfizetésen.

### [New-AzTemplateSpec](New-AzTemplateSpec.md)
Létrehoz egy új sablon specifikációt.

### [New-AzTenantDeployment](New-AzTenantDeployment.md)
Üzembe helyezés létrehozása bérlői hatókörben

### [Register-AzProviderFeature](Register-AzProviderFeature.md)
Regisztrál egy Azure-szolgáltató funkciót a fiókjában.

### [Register-AzResourceProvider](Register-AzResourceProvider.md)
Regisztrál egy erőforrás-szolgáltatót.

### [Remove-AzADAppCredential](Remove-AzADAppCredential.md)
Eltávolít egy hitelesítő adatokat egy alkalmazásból.

### [Remove-AzADApplication](Remove-AzADApplication.md)
Törli az Azure Active Directory-alkalmazást.

### [Remove-AzADGroup](Remove-AzADGroup.md)
Egy Active Directory-csoportot töröl.

### [Remove-AzADGroupMember](Remove-AzADGroupMember.md)
Eltávolít egy felhasználót egy AD-csoportból.

### [Remove-AzADServicePrincipal](Remove-AzADServicePrincipal.md)
Az Azure Active Directory szolgáltatásnév törlése.

### [Remove-AzADSpCredential](Remove-AzADSpCredential.md)
Eltávolítja a hitelesítő adatokat egy egyszerű szolgáltatásnévből.

### [Remove-AzADUser](Remove-AzADUser.md)
Egy Active Directory-felhasználó törlése.

### [Remove-AzDeployment](Remove-AzDeployment.md)
Eltávolítja a telepítést és a kapcsolódó műveleteket.

### [Remove-AzDeploymentScript](Remove-AzDeploymentScript.md)
Eltávolít egy telepítési parancsfájlt és a hozzá tartozó erőforrásokat.

### [Remove-AzManagedApplication](Remove-AzManagedApplication.md)
Felügyelt alkalmazás eltávolítása

### [Remove-AzManagedApplicationDefinition](Remove-AzManagedApplicationDefinition.md)
Felügyelt alkalmazásdefiníció eltávolítása

### [Remove-AzManagementGroup](Remove-AzManagementGroup.md)
Felügyeleti csoport eltávolítása

### [Remove-AzManagementGroupDeployment](Remove-AzManagementGroupDeployment.md)
Egy központi telepítés eltávolítása egy felügyeleti csoportnál és a kapcsolódó műveleteknél

### [Remove-AzManagementGroupSubscription](Remove-AzManagementGroupSubscription.md)
Eltávolít egy előfizetést egy felügyeleti csoportból.

### [Remove-AzPolicyAssignment](Remove-AzPolicyAssignment.md)
Eltávolít egy házirend-hozzárendelést.

### [Remove-AzPolicyDefinition](Remove-AzPolicyDefinition.md)
Eltávolít egy házirenddefiníciót.

### [Remove-AzPolicySetDefinition](Remove-AzPolicySetDefinition.md)
Eltávolít egy házirendkészlet-definíciót.

### [Remove-AzResource](Remove-AzResource.md)
Eltávolít egy erőforrást.

### [Remove-AzResourceGroup](Remove-AzResourceGroup.md)
Eltávolít egy erőforráscsoportot.

### [Remove-AzResourceGroupDeployment](Remove-AzResourceGroupDeployment.md)
Eltávolítja az erőforráscsoport-telepítést és a kapcsolódó műveleteket.

### [Remove-AzResourceLock](Remove-AzResourceLock.md)
Eltávolítja az erőforrászárolást.

### [Remove-AzRoleAssignment](Remove-AzRoleAssignment.md)
Eltávolít egy szerepkör-hozzárendelést a megadott egyszerű felhasználóhoz, aki egy adott szerepkörhöz van hozzárendelve egy adott hatókörben.

### [Remove-AzRoleDefinition](Remove-AzRoleDefinition.md)
Töröl egy egyéni szerepkört az Azure RBAC-ban.
A törölt szerepkört a szerepkör Azonosító tulajdonságával lehet megadni.
A törlés sikertelen lesz, ha az egyéni szerepkörben már vannak szerepkör-hozzárendelések.

### [Remove-AzTag](Remove-AzTag.md)
Az előre definiált Azure-címkék vagy -| Törli egy erőforrás vagy előfizetés címkéinek teljes készletét.

### [Remove-AzTemplateSpec](Remove-AzTemplateSpec.md)
Sablon specifikációjának eltávolítása

### [Remove-AzTenantDeployment](Remove-AzTenantDeployment.md)
Eltávolítja a telepítést a bérlő hatókörében és a kapcsolódó műveleteket.

### [Save-AzDeploymentScriptLog](Save-AzDeploymentScriptLog.md)
Az üzembe helyezési parancsfájl végrehajtásának naplóját lemezre menti.

### [Save-AzDeploymentTemplate](Save-AzDeploymentTemplate.md)
Egy telepítősablont fájlba ment.

### [Save-AzManagementGroupDeploymentTemplate](Save-AzManagementGroupDeploymentTemplate.md)
Egy telepítősablont fájlba ment.

### [Save-AzResourceGroupDeploymentTemplate](Save-AzResourceGroupDeploymentTemplate.md)
Fájlba menti az erőforráscsoport-telepítő sablont.

### [Save-AzTenantDeploymentTemplate](Save-AzTenantDeploymentTemplate.md)
Egy telepítősablont fájlba ment.

### [Set-AzManagedApplication](Set-AzManagedApplication.md)
Felügyelt alkalmazás frissítései

### [Set-AzManagedApplicationDefinition](Set-AzManagedApplicationDefinition.md)
Felügyelt alkalmazásdefiníció frissítése

### [Set-AzPolicyAssignment](Set-AzPolicyAssignment.md)
Egy házirend-hozzárendelést módosít.

### [Set-AzPolicyDefinition](Set-AzPolicyDefinition.md)
Módosítja a házirenddefiníciót.

### [Set-AzPolicySetDefinition](Set-AzPolicySetDefinition.md)
Házirendkészlet-definíciót módosít

### [Set-AzResource](Set-AzResource.md)
Módosít egy erőforrást.

### [Set-AzResourceGroup](Set-AzResourceGroup.md)
Módosít egy erőforráscsoportot.

### [Set-AzResourceLock](Set-AzResourceLock.md)
Módosítja az erőforrás zárolását.

### [Set-AzRoleAssignment](Set-AzRoleAssignment.md)
Szerepkör-hozzárendelés frissítése

### [Set-AzRoleDefinition](Set-AzRoleDefinition.md)
Módosít egy egyéni szerepkört az Azure RBAC-ban.
Adja meg a módosított szerepkör-definíciót JSON-fájlként vagy PSRoleDefinition formátumban.
Először a Get-AzRoleDefinition paranccsal olvassa be a módosítani kívánt egyéni szerepkört.
Ezután módosítsa a módosítani kívánt tulajdonságokat.
Végül ezzel a paranccsal mentse a szerepkördefiníciót.

### [Set-AzTemplateSpec](Set-AzTemplateSpec.md)
Módosítja a sablon specifikációját.

### [Stop-AzDeployment](Stop-AzDeployment.md)
Futó telepítés megszakítása

### [Stop-AzManagementGroupDeployment](Stop-AzManagementGroupDeployment.md)
Futó telepítés megszakítása egy felügyeleti csoportban

### [Stop-AzResourceGroupDeployment](Stop-AzResourceGroupDeployment.md)
Erőforráscsoport-telepítés megszakítása.

### [Stop-AzTenantDeployment](Stop-AzTenantDeployment.md)
Futó telepítés megszakítása bérlői hatókörben

### [Test-AzDeployment](Test-AzDeployment.md)
Egy központi telepítés ellenőrzése.

### [Test-AzManagementGroupDeployment](Test-AzManagementGroupDeployment.md)
Egy felügyeleti csoport központi telepítésének ellenőrzése.

### [Test-AzResourceGroupDeployment](Test-AzResourceGroupDeployment.md)
Erőforráscsoport-telepítés ellenőrzése.

### [Test-AzTenantDeployment](Test-AzTenantDeployment.md)
Egy központi telepítést ellenőriz bérlői hatókörben.

### [Unregister-AzProviderFeature](Unregister-AzProviderFeature.md)
Az Azure-szolgáltatói szolgáltatások regisztrációjának a regisztrációját a fiókjában.

### [Unregister-AzResourceProvider](Unregister-AzResourceProvider.md)
Erőforrás-szolgáltató regisztrációjának a visszaszava.

### [Update-AzADApplication](Update-AzADApplication.md)
Egy meglévő Azure Active Directory-alkalmazás frissítése.

### [Update-AzADServicePrincipal](Update-AzADServicePrincipal.md)
Egy meglévő Azure Active Directory-szolgáltatásnév frissítése.

### [Update-AzADUser](Update-AzADUser.md)
Egy meglévő Active Directory-felhasználó frissítése.

### [Update-AzManagementGroup](Update-AzManagementGroup.md)
Felügyeleti csoport frissítése

### [Update-AzTag](Update-AzTag.md)
Szelektíven frissíti egy erőforrás vagy előfizetés címkéinek készletét.
