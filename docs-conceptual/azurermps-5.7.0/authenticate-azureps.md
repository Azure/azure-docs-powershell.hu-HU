---
title: Bejelentkezés az Azure PowerShell-lel
description: Hogyan lehet bejelentkezni az Azure PowerShellbe felhasználóként, szolgáltatásnévként vagy az Azure-erőforrások felügyelt identitásaival.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 326d4402b4f58f29c14129f32f5b5ffda2d762fa
ms.sourcegitcommit: 038cb42a3bd8c009bc57c8c1c252e66fa170c84b
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/24/2020
ms.locfileid: "92523427"
---
# <a name="sign-in-with-azure-powershell"></a>Bejelentkezés az Azure PowerShell-lel

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

Az Azure PowerShell többféle hitelesítési módszert támogat. Első lépésként a legegyszerűbb módszer, ha interaktívan bejelentkezik a parancssoron.

## <a name="sign-in-interactively"></a>Interaktív bejelentkezés

Az interaktív bejelentkezéshez használja a [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) parancsmagot.

```azurepowershell-interactive
Connect-AzureRmAccount
```

A parancsmag futtatásakor megnyílik egy párbeszédablak, amely az Azure-fiókhoz tartozó e-mail-cím és jelszó megadását kéri. A hitelesítéskor a rendszer menti ezt az információt az aktuális PowerShell-munkamenethez, a párbeszédablak bezáródik, és Ön hozzáférhet az összes Azure PowerShell-parancsmaghoz.

> [!IMPORTANT]
> Ez a bejelentkezés _csak_ az aktuális PowerShell-munkamenetre vonatkozik. A több munkamenetre megőrzött hitelesítésről az [állandó hitelesítő adatokkal](context-persistence.md) kapcsolatos cikkből tájékozódhat.

## <a name="sign-in-with-a-service-principal"></a>Bejelentkezés szolgáltatásnévvel

A szolgáltatásnevek használatával nem interaktív fiókokat hozhat létre az erőforrások kezeléséhez. A szolgáltatásnevek olyan felhasználói fiókokhoz hasonlóak, amelyekre szabályokat alkalmazhat az Azure Active Directory használatával. Az automatizálási szkriptek biztonságának növelése érdekében csak a minimálisan szükséges engedélyeket adja meg a szolgáltatásneveknek.

Ha létre kíván hozni szolgáltatásnevet az Azure PowerShell-lel való használatra, tekintse meg az [Azure-beli szolgáltatásnév Azure PowerShell használatával történő létrehozásával](create-azure-service-principal-azureps.md) kapcsolatos szakaszt.

Szolgáltatásnévvel való bejelentkezéshez használja a `-ServicePrincipal` argumentumot a `Connect-AzureRmAccount` parancsmaggal. Szüksége lesz a szolgáltatásnév alkalmazásazonosítójára, a bejelentkezési hitelesítő adatokra, és a szolgáltatásnévhez tartozó bérlőazonosítóra. Annak érdekében, hogy a szolgáltatásnév hitelesítő adatait a megfelelő objektumként kapja meg, használja a [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) parancsmagot. Ez a parancsmag megjelenít egy párbeszédpanelt, amelyben megadható a szolgáltatásnév felhasználói azonosítója és jelszava.

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-managed-identities-for-azure-resources"></a>Bejelentkezés az Azure-erőforrások felügyelt identitásaival

A Azure-erőforrások felügyelt identitása az Azure Active Directory egy funkciója. A felügyelt identitás szolgáltatásnevével bejelentkezhet, és beszerezhet egy csak alkalmazásra érvényes hozzáférési jogkivonatot az egyéb erőforrások eléréséhez. A felügyelt identitások csak az Azure-felhőben futó virtuális gépeken érhetők el.

Az Azure-erőforrások felügyelt identitásairól [a hozzáférési jogkivonatok egy Azure-beli virtuális gép Azure-erőforrásainak felügyelt identitásaival való beszerzését ismertető részben](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token) talál.

## <a name="sign-in-to-another-cloud"></a>Bejelentkezés egy másik felhőbe

Az Azure Cloud Services különböző környezeteket biztosít, amelyek igazodnak az egyes régiók adatkezelési szabályzataihoz. Ha az Azure-fiókja az egyik ilyen régióhoz társított felhőben található, bejelentkezéskor meg kell adnia a környezetet. Például ha a fiók a kínai felhőszolgáltatásban található, a regisztrálás az alábbi paranccsal történik:

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

Az alábbi paranccsal olvashatja be a rendelkezésre álló környezetek listáját:

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a>További információ az Azure szerepkör-alapú hozzáférés kezeléséről

Az Azure-beli hitelesítésről és előfizetés-kezelésről a [fiókok, előfizetések és rendszergazdai szerepkörök kezeléséről](/azure/active-directory/role-based-access-control-configure) szóló cikkben talál további információt.

Azure PowerShell-parancsmagok a szerepkörök kezeléséhez:

* [Get-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [Get-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [New-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [New-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [Remove-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [Remove-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [Set-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Set-AzureRmRoleDefinition)
