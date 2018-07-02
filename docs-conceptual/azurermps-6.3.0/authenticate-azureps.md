---
title: Bejelentkezés az Azure PowerShell-lel
description: Hogyan lehet bejelentkezni az Azure PowerShellbe felhasználóként, szolgáltatásnévként vagy MSI-ként.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: e2eb6767d16dd15529b35b7a4134f4dcdd257d60
ms.sourcegitcommit: 5a5b6dd216d5f805204244146cf6f88ad2f34fb4
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/19/2018
ms.locfileid: "36237729"
---
# <a name="sign-in-with-azure-powershell"></a>Bejelentkezés az Azure PowerShell-lel

Az Azure PowerShell többféle bejelentkezési módszert támogat. Első lépésként a legegyszerűbb módszer, ha interaktívan bejelentkezik a parancssoron.

## <a name="sign-in-interactively"></a>Interaktív bejelentkezés

Az interaktív bejelentkezéshez használja a [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) parancsmagot.

```azurepowershell
Connect-AzureRmAccount
```

A parancsmag futtatásakor megnyílik egy párbeszédablak, amely az Azure-fiókhoz tartozó e-mail-cím és jelszó megadását kéri. A hitelesítéskor a rendszer menti ezt az információt az aktuális PowerShell-munkamenethez, a párbeszédablak bezáródik, és Ön hozzáférhet az összes Azure PowerShell-parancsmaghoz.

> [!IMPORTANT]
> Ez a bejelentkezés _csak_ az aktuális PowerShell-munkamenetre vonatkozik. A több munkamenetre megőrzött bejelentkezésről az [állandó hitelesítő adatokkal](context-persistence.md) kapcsolatos cikkből tájékozódhat.

## <a name="sign-in-with-a-service-principal"></a>Bejelentkezés szolgáltatásnévvel

A szolgáltatásnevek használatával nem interaktív fiókokat hozhat létre az erőforrások kezeléséhez. A szolgáltatásnevek olyan felhasználói fiókokhoz hasonlóak, amelyekre szabályokat alkalmazhat az Azure Active Directory használatával. Az automatizálási szkriptek biztonságának növelése érdekében csak a minimálisan szükséges engedélyeket adja meg a szolgáltatásneveknek.

Ha létre kíván hozni szolgáltatásnevet az Azure PowerShell-lel való használatra, tekintse meg az [Azure-beli szolgáltatásnév Azure PowerShell használatával történő létrehozásával](create-azure-service-principal-azureps.md) kapcsolatos szakaszt.

Szolgáltatásnévvel való bejelentkezéshez használja a `-ServicePrincipal` argumentumot a `Connect-AzureRmAccount` parancsmaggal. Szüksége lesz a szolgáltatásnév alkalmazásazonosítójára, a bejelentkezési hitelesítő adatokra, és a szolgáltatásnévhez tartozó bérlőazonosítóra. Annak érdekében, hogy a szolgáltatásnév hitelesítő adatait a megfelelő objektumként kapja meg, használja a [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) parancsmagot. Ez a parancsmag megjelenít egy párbeszédpanelt, amelyben megadható a szolgáltatásnév felhasználói azonosítója és jelszava.

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-vm-managed-service-identity"></a>Bejelentkezés Azure-beli virtuális gépek Managed Service Identityjével

A Felügyeltszolgáltatás-identitás (MSI) az Azure Active Directory előzetes verzióként elérhető funkciója. Az MSI szolgáltatásnevekkel bejelentkezhet, és beszerezhet egy csak alkalmazásra érvényes hozzáférési jogkivonatot az egyéb erőforrások eléréséhez. Az MSI csak az Azure-felhőben futó virtuális gépeken érhető el.

További információ az MSI-ről: [Az Azure-beli virtuális gépek felügyeltszolgáltatás-identitásának (MSI) használata bejelentkezéshez és jogkivonat beszerzéséhez](/azure/active-directory/msi-how-to-get-access-token-using-msi).

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
* [Set-AzureRmRoleDefinition](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
