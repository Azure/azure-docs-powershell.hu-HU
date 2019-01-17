---
title: Bejelentkezés az Azure PowerShell-lel
description: Hogyan lehet bejelentkezni az Azure PowerShellbe felhasználóként, szolgáltatásnévként vagy az Azure-erőforrások felügyelt identitásaival.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/29/2018
ms.openlocfilehash: 80c59a10666c6e3a01e6c33716fce40094fb14be
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/16/2019
ms.locfileid: "54342065"
---
# <a name="sign-in-with-azure-powershell"></a>Bejelentkezés az Azure PowerShell-lel

Az Azure PowerShell többféle hitelesítési módszert támogat. Első lépésként a legegyszerűbb, ha az [Azure Cloud Shellt](/azure/cloud-shell/overview) használja, amely automatikusan belépteti. Helyi telepítés esetén interaktívan jelentkezhet be a böngészőjén keresztül. Automatizálási szkriptek írásakor az ajánlott módszer a [szolgáltatásnév](create-azure-service-principal-azureps.md) használata a szükséges engedélyekkel. Egyéni használati esetekben az Azure-erőforrások biztonságát úgy őrizheti meg, ha a lehető legnagyobb mértékben korlátozza a bejelentkezési engedélyeket.

Bejelentkezés után a parancsokat a rendszer az alapértelmezett előfizetésen futtatja. Az adott munkamenethez tartozó aktív előfizetés módosításához használja a [Set-AzContext](/powershell/module/az.accounts/set-azcontext) parancsmagot. Az Azure PowerShell-lel való bejelentkezéskor használt alapértelmezett előfizetés módosításához használja a [Set-AzDefault](/powershell/module/az.accounts/set-azdefault) parancsmagot.

> [!IMPORTANT]
>
> A hitelesítő adatok megoszlanak több PowerShell-munkamenet között, ha be van jelentkezve.
> További információért tekintse meg az [Állandó hitelesítő adatokat](context-persistence.md) ismertető cikket.

## <a name="sign-in-interactively"></a>Interaktív bejelentkezés

Az interaktív bejelentkezéshez használja a [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) parancsmagot.

```azurepowershell-interactive
Connect-AzAccount
```

A futtatáskor ez a parancsmag jogkivonatsztringet jelenít meg. A bejelentkezéshez másolja ezt a sztringet a https://microsoft.com/devicelogin címbe egy böngészőben. A rendszer ekkor hitelesíti a PowerShell-munkamenetet az Azure-hoz való csatlakozáshoz.

## <a name="sign-in-with-credentials"></a>Bejelentkezés hitelesítő adatokkal

Egy, az Azure-hoz való csatlakozásra jogosult `PSCredential` objektummal is bejelentkezhet.
A hitelesítő objektum beszerzésének legegyszerűbb módszere a [Get-Credential](/powershell/module/Microsoft.PowerShell.Security/Get-Credential) parancsmag használata. A futtatáskor ez a parancsmag egy felhasználónév/jelszó hitelesítőadat-párt fog kérni.

> [!Note]
> Ez a módszer nem működik Microsoft-fiókok, valamint az engedélyezett kéttényezős hitelesítéssel rendelkező fiókok esetében.

```azurepowershell-interactive
$creds = Get-Credential
Connect-AzAccount -Credential $creds
```

## <a name="sign-in-with-a-service-principal"></a>Bejelentkezés szolgáltatásnévvel

A szolgáltatásnevek nem interaktív Azure-fiókok. Más felhasználói fiókokhoz hasonlóan az ezekhez tartozó engedélyek kezelését is az Azure Active Directory végzi. Az automatizálási szkriptek biztonságát úgy garantálhatjuk, ha a szolgáltatásnevek számára csak a szükséges engedélyeket adjuk meg.

Ha meg szeretné tudni, hogyan hozhat létre szolgáltatásnevet az Azure PowerShell-lel való használatra, tekintse meg az [Azure-beli szolgáltatásnév Azure PowerShell használatával történő létrehozásával](create-azure-service-principal-azureps.md) kapcsolatos szakaszt.

Szolgáltatásnévvel való bejelentkezéshez használja a `-ServicePrincipal` argumentumot a `Connect-AzAccount` parancsmaggal. Szüksége lesz a szolgáltatásnév alkalmazásazonosítójára, a bejelentkezési hitelesítő adatokra, és a szolgáltatásnévhez tartozó bérlőazonosítóra. Annak érdekében, hogy a szolgáltatásnév hitelesítő adatait a megfelelő objektumként kapja meg, használja a [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) parancsmagot. Ez a parancsmag a szolgáltatásnév felhasználói azonosítójának és jelszavának megadását kéri.

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-a-managed-identity"></a>Bejelentkezés felügyelt identitással 

A felügyelt identitások az Azure Active Directory funkciójaként érhetők el. A felügyelt identitások Azure-ban futó erőforrásokhoz társított szolgáltatásnevek. A felügyelt identitás szolgáltatásnevével bejelentkezhet, és beszerezhet egy csak alkalmazásra érvényes hozzáférési jogkivonatot az egyéb erőforrások eléréséhez. A felügyelt identitások csak az Azure-felhőkben futó erőforrásokon érhetők el.

Az Azure-erőforrások felügyelt identitásairól további információt [a hozzáférési jogkivonatok egy Azure-beli virtuális gép Azure-erőforrásainak felügyelt identitásaival való beszerzését ismertető részben](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token) talál.

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a>Bejelentkezés nem alapértelmezett bérlővel vagy felhőszolgáltatóként (CSP-ként)

Ha a fiókja egynél több bérlőhöz van társítva, kapcsolódáskor a bejelentkezéshez a `-TenantId` paramétert kell használni. Ez a paraméter bármely egyéb bejelentkezési módszer esetében is használható. Bejelentkezéskor a paraméter értéke a bérlő Azure-objektumazonosítója (bérlőazonosító) vagy a bérlő teljes tartományneve lehet.

[Felhőszolgáltatóként (CSP-ként)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) való bejelentkezés esetén a `-TenantId` értékének a bérlőazonosítónak **kell** lennie.

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a>Bejelentkezés egy másik felhőbe

Az Azure Cloud Services által biztosított környezetek megfelelnek a helyi szabályozásoknak.
Regionális felhőszolgáltatásban található fiókok esetében a környezetet az `-Environment` argumentummal való bejelentkezéskor kell beállítania.
Például ha a fiók a kínai felhőszolgáltatásban található:

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

Az alábbi paranccsal olvashatja be a rendelkezésre álló környezetek listáját:

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```