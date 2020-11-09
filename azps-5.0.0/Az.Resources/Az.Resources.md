---
Module Name: Az.Resources
Module Guid: ab3ca893-26fe-44b0-bd3c-8933df144d7b
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.resources
Help Version: 5.5.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Az.Resources.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Az.Resources.md
ms.openlocfilehash: 25460ff58e2c3f2a493638cc7011e352d551280e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300593"
---
# Az erőforrások modul
## Leírás
Ez a témakör az Azure Resource Manager parancsmagokra vonatkozó súgótémaköröket jeleníti meg.

## Az. Resources parancsmagok
### [Add-AzADGroupMember](Add-AzADGroupMember.md)
Felhasználó felvétele egy meglévő HIRDETÉSCSOPORT-csoportba.

### [Exportálás – AzResourceGroup](Export-AzResourceGroup.md)
Egy erőforráscsoportot sablonként rögzít, és egy fájlba menti.

### [Get-AzADAppCredential](Get-AzADAppCredential.md)
Beolvassa az alkalmazáshoz társított hitelesítő adatok listáját.

### [Get-AzADApplication](Get-AzADApplication.md)
Felsorolja a meglévő Azure Active Directory-alkalmazásokat.

### [Get-AzADGroup](Get-AzADGroup.md)
Szűri az Active Directory-csoportokat.

### [Get-AzADGroupMember](Get-AzADGroupMember.md)
Az aktuális bérlői fiókban lévő HIRDETÉSCSOPORT tagjainak listája.

### [Get-AzADServicePrincipal](Get-AzADServicePrincipal.md)
Szűri az Active Directory-szolgáltatási résztvevőket.

### [Get-AzADSpCredential](Get-AzADSpCredential.md)
Lekérdezi a szolgáltatóhoz társított hitelesítő adatok listáját.

### [Get-AzADUser](Get-AzADUser.md)
Szűri az Active Directory felhasználóit.

### [Get-AzDenyAssignment](Get-AzDenyAssignment.md)
Felsorolja az Azure RBAC a feladatok elutasítását a megadott hatókörben.
Alapértelmezés szerint a kijelölt Azure-előfizetésben a megtagadási feladatokat sorolja fel.
A megfelelő paraméterekkel felsorolhatja az adott felhasználóhoz tartozó hozzárendeléseket, illetve megtagadhatja a feladatok megtagadását egy adott erőforráscsoport vagy erőforrás esetében.

### [Get-AzDeployment](Get-AzDeployment.md)
A központi telepítő beszerzése

### [Get-AzDeploymentOperation](Get-AzDeploymentOperation.md)
Üzembe állítási művelet

### [Get-AzDeploymentScript](Get-AzDeploymentScript.md)
Beolvashatja vagy listázhatja a központi telepítő parancsfájlokat.

### [Get-AzDeploymentScriptLog](Get-AzDeploymentScriptLog.md)
Beolvassa a központi telepítő parancsfájl-végrehajtás naplózását.

### [Get-AzDeploymentWhatIfResult](Get-AzDeploymentWhatIfResult.md)
Egy ARM-sablon beolvasása What-If eredmény a bevezetéshez az előfizetéses hatókörben. 

### [Get-AzLocation](Get-AzLocation.md)
Minden hely és a támogatott erőforrás-szolgáltatók beolvasása minden helyhez.

### [Get-AzManagedApplication](Get-AzManagedApplication.md)
Felügyelt alkalmazásokat kap

### [Get-AzManagedApplicationDefinition](Get-AzManagedApplicationDefinition.md)
Felügyelt alkalmazás-definíciók beolvasása

### [Get-AzManagementGroup](Get-AzManagementGroup.md)
Felügyeleti csoport (ok) beolvasása

### [Get-AzManagementGroupDeployment](Get-AzManagementGroupDeployment.md)
Bevezetés beszerzése felügyeleti csoporttal

### [Get-AzManagementGroupDeploymentOperation](Get-AzManagementGroupDeploymentOperation.md)
Üzembe állítási művelet beszerzése a felügyeleti csoport központi telepítéséhez

### [Get-AzManagementGroupDeploymentWhatIfResult](Get-AzManagementGroupDeploymentWhatIfResult.md)
ARM-sablont kap What-If eredmény a felügyeleti csoport hatókörének kiépítéséhez. 

### [Get-AzPolicyAlias](Get-AzPolicyAlias.md)
Get-AzPolicyAlias beolvassa és kinyeri az Azure-szolgáltató erőforrás-típusait, amelyek a megadott paraméter-értékekkel rendelkeznek. Ha nincs paraméter megadva, a rendszer minden olyan szolgáltatói erőforrástípust exportál, amely aliast tartalmaz.
A-ListAvailable kapcsoló a megfelelő erőforrástípusok (aliasok nélkül) megadásával módosítja ezt a problémát.

### [Get-AzPolicyAssignment](Get-AzPolicyAssignment.md)
Megkapja a házirend-hozzárendeléseket.

### [Get-AzPolicyDefinition](Get-AzPolicyDefinition.md)
Házirend-definíciókat kap.

### [Get-AzPolicySetDefinition](Get-AzPolicySetDefinition.md)
Kapja meg a házirend-definíciókat.

### [Get-AzProviderFeature](Get-AzProviderFeature.md)
Információkat kap az Azure Provider funkcióiról.

### [Get-AzProviderOperation](Get-AzProviderOperation.md)
Olyan Azure Resource Provider műveleteit kapja meg, amelyek az Azure RBAC segítségével biztonságossá tehetők.

### [Get-AzResource](Get-AzResource.md)
Erőforrásokat kap.

### [Get-AzResourceGroup](Get-AzResourceGroup.md)
Erőforrás-csoportok beolvasása

### [Get-AzResourceGroupDeployment](Get-AzResourceGroupDeployment.md)
Beilleszti a telepített erőforrásokat egy erőforrás-csoportban.

### [Get-AzResourceGroupDeploymentOperation](Get-AzResourceGroupDeploymentOperation.md)
Az erőforráscsoport-telepítő művelet beolvasása

### [Get-AzResourceGroupDeploymentWhatIfResult](Get-AzResourceGroupDeploymentWhatIfResult.md)
Egy ARM-sablon beolvasása What-If eredmény a bevezetéshez az erőforráscsoport hatókörében. 

### [Get-AzResourceLock](Get-AzResourceLock.md)
Erőforrás-zárolást kap.

### [Get-AzResourceProvider](Get-AzResourceProvider.md)
Erőforrás-szolgáltatót kap.

### [Get-AzRoleAssignment](Get-AzRoleAssignment.md)
Az Azure RBAC szerepkör-hozzárendeléseinek listája a megadott hatókörben.
Alapértelmezés szerint a kijelölt Azure-előfizetésben lévő összes szerepkör-hozzárendelést felsorolja.
A megfelelő paraméterekkel felsorolhatja a hozzárendeléseket egy adott felhasználóhoz, illetve felsorolhatja egy adott erőforráscsoport vagy erőforrás hozzárendeléseit.

### [Get-AzRoleDefinition](Get-AzRoleDefinition.md)
Felsorolja a hozzárendeléshez elérhető összes Azure RBAC szerepkört.

### [Get-AzTag](Get-AzTag.md)
Előre definiált Azure-címkéket kap | A teljes címkéket lekapja egy erőforrásra vagy előfizetésre.

### [Get-AzTenantDeployment](Get-AzTenantDeployment.md)
A központi bevezetés a bérlői hatókörben

### [Get-AzTenantDeploymentOperation](Get-AzTenantDeploymentOperation.md)
Üzembe állítási művelet beszerzése a bérlői hatókörben

### [Get-AzTenantDeploymentWhatIfResult](Get-AzTenantDeploymentWhatIfResult.md)
ARM-sablont kap, What-If a bérlői hatókörben való bevezetés eredményét adja eredményül. 

### [Meghívó-AzResourceAction](Invoke-AzResourceAction.md)
Egy erőforrás műveletét hívja fel.

### [Move-AzResource](Move-AzResource.md)
Erőforrás áthelyezése egy másik erőforrás-csoportba vagy előfizetésbe

### [Új – AzADAppCredential](New-AzADAppCredential.md)
Hitelesítő adatok hozzáadása egy meglévő alkalmazáshoz.

### [Új – AzADApplication](New-AzADApplication.md)
Új Azure Active Directory-alkalmazást hoz létre.

### [Új – AzADGroup](New-AzADGroup.md)
Új Active Directory-csoport létrehozása

### [Új – AzADServicePrincipal](New-AzADServicePrincipal.md)
Új Azure Active Directory-szolgáltató létrehozása.

### [Új – AzADSpCredential](New-AzADSpCredential.md)
Hitelesítő adatok hozzáadása egy meglévő szolgáltatási megbízóhoz.

### [Új – AzADUser](New-AzADUser.md)
Új Active Directory-felhasználó létrehozása.

### [Új – AzDeployment](New-AzDeployment.md)
Központi telepítő létrehozása

### [Új – AzManagedApplication](New-AzManagedApplication.md)
Azure-felügyelt alkalmazást hoz létre.

### [Új – AzManagedApplicationDefinition](New-AzManagedApplicationDefinition.md)
Felügyelt alkalmazás-definíciót hoz létre.

### [Új – AzManagementGroup](New-AzManagementGroup.md)
Felügyeleti csoport létrehozása

### [Új – AzManagementGroupDeployment](New-AzManagementGroupDeployment.md)
Bevezetés létrehozása felügyeleti csoportban

### [Új – AzManagementGroupSubscription](New-AzManagementGroupSubscription.md)
Előfizetést ad hozzá egy felügyeleti csoporthoz.

### [Új – AzPolicyAssignment](New-AzPolicyAssignment.md)
Házirend-hozzárendelést hoz létre.

### [Új – AzPolicyDefinition](New-AzPolicyDefinition.md)
Házirend-definíciót hoz létre.

### [Új – AzPolicySetDefinition](New-AzPolicySetDefinition.md)
Házirend-készlet definícióját hozza létre.

### [Új – AzResource](New-AzResource.md)
Létrehoz egy erőforrást.

### [Új – AzResourceGroup](New-AzResourceGroup.md)
Azure-erőforráscsoportot hoz létre.

### [Új – AzResourceGroupDeployment](New-AzResourceGroupDeployment.md)
Azure-bevezetést ad hozzá egy erőforrás-csoporthoz.

### [Új – AzResourceLock](New-AzResourceLock.md)
Erőforrás-zárolást hoz létre.

### [Új – AzRoleAssignment](New-AzRoleAssignment.md)
A megadott RBAC szerepkör hozzárendelése a megadott hatókörhöz.

### [Új – AzRoleDefinition](New-AzRoleDefinition.md)
Egyéni szerepkör létrehozása az Azure RBAC-ban.
JSON-Szerepdefiníció vagy PSRoleDefinition-objektum megadása bemenetként.
Első lépésként a Get-AzRoleDefinition parancs segítségével hozzon létre egy eredeti szerepkör-definíciós objektumot.
Ezután szükség szerint módosítsa a tulajdonságait.
Végül ezt a parancsot használva egyéni szerepkört hozhat létre a szerepkör-definícióval.

### [Új – AzTag](New-AzTag.md)
Előre definiált Azure címkét hoz létre, vagy hozzáadott értékeket egy meglévő címkéhez | A teljes címkéket létrehoz vagy frissít egy erőforrásban vagy előfizetésben.

### [Új – AzTenantDeployment](New-AzTenantDeployment.md)
Bevezetés létrehozása bérlői hatókörben

### [Register-AzProviderFeature](Register-AzProviderFeature.md)
A fiók Azure Provider szolgáltatását regisztrálja.

### [Register-AzResourceProvider](Register-AzResourceProvider.md)
Erőforrás-szolgáltató regisztrálása.

### [Remove-AzADAppCredential](Remove-AzADAppCredential.md)
Hitelesítő adatok eltávolítása egy alkalmazásból.

### [Remove-AzADApplication](Remove-AzADApplication.md)
Törli az Azure Active Directory-alkalmazást.

### [Remove-AzADGroup](Remove-AzADGroup.md)
Active Directory-csoport törlése

### [Remove-AzADGroupMember](Remove-AzADGroupMember.md)
Felhasználó eltávolítása egy HIRDETÉSCSOPORT-csoportból.

### [Remove-AzADServicePrincipal](Remove-AzADServicePrincipal.md)
Az Azure Active Directory Service Principal törlése

### [Remove-AzADSpCredential](Remove-AzADSpCredential.md)
Hitelesítő adatok eltávolítása egy egyszerű szolgáltatótól.

### [Remove-AzADUser](Remove-AzADUser.md)
Active Directory-felhasználó törlése

### [Remove-AzDeployment](Remove-AzDeployment.md)
A telepített példányok és a hozzájuk kapcsolódó műveletek eltávolítása

### [Remove-AzDeploymentScript](Remove-AzDeploymentScript.md)
Eltávolítja a telepítő parancsfájlt és a hozzá tartozó erőforrásokat.

### [Remove-AzManagedApplication](Remove-AzManagedApplication.md)
Felügyelt alkalmazás eltávolítása

### [Remove-AzManagedApplicationDefinition](Remove-AzManagedApplicationDefinition.md)
Felügyelt alkalmazás definíciójának eltávolítása

### [Remove-AzManagementGroup](Remove-AzManagementGroup.md)
Felügyeleti csoport eltávolítása

### [Remove-AzManagementGroupDeployment](Remove-AzManagementGroupDeployment.md)
A központi felügyelet eltávolítása a felügyeleti csoportokban és a hozzájuk kapcsolódó műveletekben

### [Remove-AzManagementGroupSubscription](Remove-AzManagementGroupSubscription.md)
Új előfizetés eltávolítása egy felügyeleti csoportból.

### [Remove-AzPolicyAssignment](Remove-AzPolicyAssignment.md)
Házirend-hozzárendelés eltávolítása

### [Remove-AzPolicyDefinition](Remove-AzPolicyDefinition.md)
Házirend-definíció eltávolítása.

### [Remove-AzPolicySetDefinition](Remove-AzPolicySetDefinition.md)
Házirend-készlet definíciójának eltávolítása

### [Remove-AzResource](Remove-AzResource.md)
Eltávolít egy erőforrást.

### [Remove-AzResourceGroup](Remove-AzResourceGroup.md)
Erőforráscsoport eltávolítása

### [Remove-AzResourceGroupDeployment](Remove-AzResourceGroupDeployment.md)
Egy erőforráscsoport-telepítő és az ahhoz kapcsolódó műveletek eltávolítása.

### [Remove-AzResourceLock](Remove-AzResourceLock.md)
Erőforrás-zárolás eltávolítása.

### [Remove-AzRoleAssignment](Remove-AzRoleAssignment.md)
Eltávolítja a szerepkör-hozzárendelést a meghatározott megbízóhoz, aki egy bizonyos hatókörben meghatározott szerepkörhöz van rendelve.

### [Remove-AzRoleDefinition](Remove-AzRoleDefinition.md)
Egyéni szerepkör törlése az Azure RBAC-ban.
A törlendő szerepkör a szerepkör ID tulajdonságával van megadva.
A törlés meghiúsul, ha a meglévő szerepkör-hozzárendelések az egyéni szerepkörre vonatkoznak.

### [Remove-AzTag](Remove-AzTag.md)
Előre definiált Azure-címkék vagy-értékek törlése | A teljes címkék törlése egy erőforrásra vagy előfizetésre

### [Remove-AzTenantDeployment](Remove-AzTenantDeployment.md)
A bevezetést eltávolítja a bérlői hatókörben és az esetleges kapcsolódó műveletekben

### [Mentés-AzDeploymentScriptLog](Save-AzDeploymentScriptLog.md)
Menti a telepítő parancsfájl-végrehajtás naplóját a lemezre.

### [Mentés-AzDeploymentTemplate](Save-AzDeploymentTemplate.md)
Egy központi telepítő sablont ment a fájlra.

### [Mentés-AzManagementGroupDeploymentTemplate](Save-AzManagementGroupDeploymentTemplate.md)
Egy központi telepítő sablont ment a fájlra.

### [Mentés-AzResourceGroupDeploymentTemplate](Save-AzResourceGroupDeploymentTemplate.md)
Egy erőforráscsoport-telepítő sablont ment a fájlba.

### [Mentés-AzTenantDeploymentTemplate](Save-AzTenantDeploymentTemplate.md)
Egy központi telepítő sablont ment a fájlra.

### [Set-AzManagedApplication](Set-AzManagedApplication.md)
A felügyelt alkalmazások frissítése

### [Set-AzManagedApplicationDefinition](Set-AzManagedApplicationDefinition.md)
A felügyelt alkalmazások definíciójának frissítése

### [Set-AzPolicyAssignment](Set-AzPolicyAssignment.md)
Házirend-hozzárendelés módosítása

### [Set-AzPolicyDefinition](Set-AzPolicyDefinition.md)
Módosította a házirend-definíciót.

### [Set-AzPolicySetDefinition](Set-AzPolicySetDefinition.md)
Házirend-készlet definíciójának módosítása

### [Set-AzResource](Set-AzResource.md)
Módosítja az erőforrást.

### [Set-AzResourceGroup](Set-AzResourceGroup.md)
Egy erőforráscsoport módosítása

### [Set-AzResourceLock](Set-AzResourceLock.md)
Módosítja az erőforrás-zárolást.

### [Set-AzRoleAssignment](Set-AzRoleAssignment.md)
Szerepkör-hozzárendelés frissítése

### [Set-AzRoleDefinition](Set-AzRoleDefinition.md)
Egyéni szerepkör módosítása az Azure RBAC-ban.
A módosított szerepkör definíciójának megadása JSON-fájlként vagy PSRoleDefinition.
Először használja a Get-AzRoleDefinition parancsot a módosítani kívánt egyéni szerepkör beolvasásához.
Ezután módosítsa a módosítani kívánt tulajdonságokat.
Végül mentse a szerepkör-definíciót a parancs segítségével.

### [Stop-AzDeployment](Stop-AzDeployment.md)
Futó példány visszavonása

### [Stop-AzManagementGroupDeployment](Stop-AzManagementGroupDeployment.md)
Futó telepített példány lemondása felügyeleti csoportban

### [Stop-AzResourceGroupDeployment](Stop-AzResourceGroupDeployment.md)
Erőforráscsoport-telepítő lemondása

### [Stop-AzTenantDeployment](Stop-AzTenantDeployment.md)
Futó telepített példány lemondása a bérlői hatókörben

### [Teszt-AzDeployment](Test-AzDeployment.md)
Ellenőrzi a központi telepítőt.

### [Teszt-AzManagementGroupDeployment](Test-AzManagementGroupDeployment.md)
Egy felügyeleti csoportban ellenőrzi a bevezetést.

### [Teszt-AzResourceGroupDeployment](Test-AzResourceGroupDeployment.md)
Egy erőforráscsoport-telepítő érvényesítése.

### [Teszt-AzTenantDeployment](Test-AzTenantDeployment.md)
A bevezetést a bérlői hatókörben ellenőrzi.

### [Regisztráció törlése – AzProviderFeature](Unregister-AzProviderFeature.md)
Az Azure szolgáltató funkció regisztrációjának megszüntetése a fiókban.

### [Regisztráció törlése – AzResourceProvider](Unregister-AzResourceProvider.md)
Az erőforrás-szolgáltató regisztrációjának megszüntetése

### [Update-AzADApplication](Update-AzADApplication.md)
Frissít egy meglévő Azure Active Directory-alkalmazást.

### [Update-AzADServicePrincipal](Update-AzADServicePrincipal.md)
Frissít egy meglévő Azure Active Directory-szolgáltatót.

### [Update-AzADUser](Update-AzADUser.md)
Frissít egy meglévő Active Directory-felhasználót.

### [Update-AzManagementGroup](Update-AzManagementGroup.md)
Felügyeleti csoport frissítése

### [Update-AzTag](Update-AzTag.md)
Szelektíven frissíti egy erőforrás vagy előfizetés címkéit.
