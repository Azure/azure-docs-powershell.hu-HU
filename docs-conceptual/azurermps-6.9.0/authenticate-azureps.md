---
title: Bejelentkezés az Azure PowerShell-lel
description: Hogyan lehet bejelentkezni az Azure PowerShellbe felhasználóként, szolgáltatásnévként vagy az Azure-erőforrások felügyelt identitásaival.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 2a118e1aa8b6755ef5769f44429427d22532780d
ms.sourcegitcommit: 6c38e86e16da99f65cd183c63e34f7176b121ab8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/04/2018
ms.locfileid: "47425244"
---
# <a name="sign-in-with-azure-powershell"></a>Bejelentkezés az Azure PowerShell-lel

Az Azure PowerShell többféle hitelesítési módszert támogat. Első lépésként a legegyszerűbb módszer, ha interaktívan bejelentkezik a parancssoron.

## <a name="sign-in-interactively"></a>Interaktív bejelentkezés

Az interaktív bejelentkezéshez használja a [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) parancsmagot.

```azurepowershell
Connect-AzureRmAccount
```

A parancsmag futtatásakor megnyílik egy párbeszédablak, amely az Azure-fiókhoz tartozó e-mail-cím és jelszó megadását kéri. A hitelesítés csak az aktuális PowerShell-munkamenetre vonatkozik.

> [!IMPORTANT]
> Az Azure PowerShell 6.3.0-s verziójától kezdve a hitelesítő adatok megoszlanak több PowerShell-munkamenet között, ha be van jelentkezve a Windowsba. További információért tekintse meg az [Állandó hitelesítő adatokat](context-persistence.md) ismertető cikket.

## <a name="sign-in-with-a-service-principal"></a>Bejelentkezés szolgáltatásnévvel

A szolgáltatásnevek nem interaktív Azure-fiókok. Más felhasználói fiókokhoz hasonlóan az ezekhez tartozó engedélyek kezelését is az Azure Active Directory végzi. Az automatizálási szkriptek biztonságát úgy garantálhatjuk, ha a szolgáltatásnevek számára csak a szükséges engedélyeket adjuk meg.

Ha meg szeretné tudni, hogyan hozhat létre szolgáltatásnevet az Azure PowerShell-lel való használatra, tekintse meg az [Azure-beli szolgáltatásnév Azure PowerShell használatával történő létrehozásával](create-azure-service-principal-azureps.md) kapcsolatos szakaszt.

Szolgáltatásnévvel való bejelentkezéshez használja a `-ServicePrincipal` argumentumot a `Connect-AzureRmAccount` parancsmaggal. Szüksége lesz a szolgáltatásnév alkalmazásazonosítójára, a bejelentkezési hitelesítő adatokra, és a szolgáltatásnévhez tartozó bérlőazonosítóra. Annak érdekében, hogy a szolgáltatásnév hitelesítő adatait a megfelelő objektumként kapja meg, használja a [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) parancsmagot. Ez a parancsmag megjelenít egy párbeszédpanelt, amelyben megadható a szolgáltatásnév felhasználói azonosítója és jelszava.

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a>Bejelentkezés Azure-beli Managed Service Identityvel

A Azure-erőforrások felügyelt identitása az Azure Active Directory egy funkciója. A felügyelt identitás szolgáltatásnevével bejelentkezhet, és beszerezhet egy csak alkalmazásra érvényes hozzáférési jogkivonatot az egyéb erőforrások eléréséhez. A felügyelt identitások csak az Azure-felhőben futó virtuális gépeken érhetők el.

Az Azure-erőforrások felügyelt identitásairól [a hozzáférési jogkivonatok egy Azure-beli virtuális gép Azure-erőforrásainak felügyelt identitásaival való beszerzését ismertető részben](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token) talál.

## <a name="sign-in-to-another-cloud"></a>Bejelentkezés egy másik felhőbe

Az Azure Cloud Services által biztosított környezetek megfelelnek a regionális adatkezelési előírásoknak.
Regionális felhőszolgáltatásban található fiókok esetében a környezetet az `-Environment` argumentummal való bejelentkezéskor kell beállítania.
Például ha a fiók a kínai felhőszolgáltatásban található:

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
