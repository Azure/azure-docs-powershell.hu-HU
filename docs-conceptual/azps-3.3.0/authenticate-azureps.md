---
title: Bejelentkezés az Azure PowerShell-lel
description: Hogyan lehet bejelentkezni az Azure PowerShellbe felhasználóként, szolgáltatásnévként vagy az Azure-erőforrások felügyelt identitásaival.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/04/2019
ms.openlocfilehash: 614cce77deb4390ea158a48ae2d48b7b983224f2
ms.sourcegitcommit: 2d0c3ffaa5246f680784fa7e15b0d2536c27ff80
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/07/2020
ms.locfileid: "75720918"
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

> [!IMPORTANT]
>
> Az Active Directory engedélyezési folyamatának végrehajtásában történt módosítások miatt és biztonsági okokból a felhasználónévvel és jelszóval történő hitelesítés el lett távolítva az Azure PowerShellből.
> Ha az automatizálhatóság érdekében használta ezt a típusú hitelesítést, helyette [hozzon létre egy szolgáltatásnevet](create-azure-service-principal-azureps.md).

## <a name="sign-in-with-a-service-principal-a-namesp-signin"></a>Bejelentkezés szolgáltatásnévvel <a name="sp-signin"/>

A szolgáltatásnevek nem interaktív Azure-fiókok. Más felhasználói fiókokhoz hasonlóan az ezekhez tartozó engedélyek kezelését is az Azure Active Directory végzi. Az automatizálási szkriptek biztonságát úgy garantálhatjuk, ha a szolgáltatásnevek számára csak a szükséges engedélyeket adjuk meg.

Ha meg szeretné tudni, hogyan hozhat létre szolgáltatásnevet az Azure PowerShell-lel való használatra, tekintse meg az [Azure-beli szolgáltatásnév Azure PowerShell használatával történő létrehozásával](create-azure-service-principal-azureps.md) kapcsolatos szakaszt.

Szolgáltatásnévvel való bejelentkezéshez használja a `-ServicePrincipal` argumentumot a `Connect-AzAccount` parancsmaggal. Szüksége lesz a szolgáltatásnév alkalmazásazonosítójára, a bejelentkezési hitelesítő adatokra, és a szolgáltatásnévhez tartozó bérlőazonosítóra. A szolgáltatásnévvel való bejelentkezés módja attól függ, hogy az jelszó- vagy tanúsítványalapú hitelesítésre van-e konfigurálva.

### <a name="password-based-authentication"></a>Jelszóalapú hitelesítés

Annak érdekében, hogy a szolgáltatásnév hitelesítő adatait a megfelelő objektumként kapja meg, használja a [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) parancsmagot. Ez a parancsmag felhasználónév és jelszó megadását kéri. Felhasználónévként használja a szolgáltatásnév azonosítóját.

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

Automatizálási forgatókönyvek esetén a hitelesítő adatokat egy felhasználónévből és egy biztonságos sztringből kell létrehoznia:

```azurepowershell-interactive
$passwd = ConvertTo-SecureString <use a secure password here> -AsPlainText -Force
$pscredential = New-Object System.Management.Automation.PSCredential('service principal name/id', $passwd)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

Győződjön meg róla, hogy a szolgáltatásnév-kapcsolatok automatizálásakor a jelszó tárolása megfelelően történik.

### <a name="certificate-based-authentication"></a>Tanúsítványalapú hitelesítés

A tanúsítványalapú hitelesítéshez az Azure PowerShellnek egy helyi tanúsítványtárolóból kell információkat lekérnie a tanúsítvány ujjlenyomata alapján.

```azurepowershell-interactive
Connect-AzAccount -ApplicationId $appId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

Ha regisztrált alkalmazás helyett szolgáltatásnevet használ, adja hozzá a `-ServicePrincipal` argumentumot, és adja meg a szolgáltatásnév azonosítóját az `-ApplicationId` paraméter értékeként.

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -ApplicationId $servicePrincipalId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

A PowerShell 5.1-ben a tanúsítványtároló a [PKI](/powershell/module/pkiclient)-modullal felügyelhető és vizsgálható. A PowerShell Core 6.x és az újabb verziókban a folyamat ennél összetettebb. Az alábbi szkriptek bemutatják, hogyan importálhat egy meglévő tanúsítványt a PowerShell által hozzáférhető tanúsítványtárolóba.

#### <a name="import-a-certificate-in-powershell-51"></a>Tanúsítvány importálása PowerShell 5.1-ben

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a>Tanúsítvány importálása PowerShell Core 6.x és újabb verziókban

```azurepowershell-interactive
# Import a PFX
$storeName = [System.Security.Cryptography.X509Certificates.StoreName]::My 
$storeLocation = [System.Security.Cryptography.X509Certificates.StoreLocation]::CurrentUser 
$store = [System.Security.Cryptography.X509Certificates.X509Store]::new($storeName, $storeLocation) 
$certPath = <path to certificate>
$credentials = Get-Credential -Message "Provide PFX private key password"
$flag = [System.Security.Cryptography.X509Certificates.X509KeyStorageFlags]::Exportable 
$certificate = [System.Security.Cryptography.X509Certificates.X509Certificate2]::new($certPath, $credentials.Password, $flag) 
$store.Open([System.Security.Cryptography.X509Certificates.OpenFlags]::ReadWrite) 
$store.Add($Certificate) 
$store.Close()
```

## <a name="sign-in-using-a-managed-identity"></a>Bejelentkezés felügyelt identitással

A felügyelt identitások az Azure Active Directory funkciójaként érhetők el. A felügyelt identitások Azure-ban futó erőforrásokhoz társított szolgáltatásnevek. A felügyelt identitás szolgáltatásnevével bejelentkezhet, és beszerezhet egy csak alkalmazásra érvényes hozzáférési jogkivonatot az egyéb erőforrások eléréséhez. A felügyelt identitások csak az Azure-felhőkben futó erőforrásokon érhetők el.

Ez a parancs a felügyelt identitás használatával kapcsolódik a gazdakörnyezethez. Ha például egy hozzárendelt felügyeletszolgáltatás-identitással rendelkező virtuális gépet használ, akkor a kód számára lehetővé válik a hozzárendelt identitással való bejelentkezés.

```azurepowershell-interactive
 Connect-AzAccount -Identity 
```

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a>Bejelentkezés nem alapértelmezett bérlővel vagy felhőszolgáltatóként (CSP-ként)

Ha a fiókja egynél több bérlőhöz van társítva, kapcsolódáskor a bejelentkezéshez a `-Tenant` paramétert kell használni. Ez a paraméter bármely bejelentkezési módszer esetében használható. Bejelentkezéskor a paraméter értéke a bérlő Azure-objektumazonosítója (bérlőazonosító) vagy a bérlő teljes tartományneve lehet.

[Felhőszolgáltatóként (CSP-ként)](https://azure.microsoft.com/offers/ms-azr-0145p/) való bejelentkezés esetén a `-Tenant` értékének a bérlőazonosítónak **kell** lennie.

```azurepowershell-interactive
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a>Bejelentkezés egy másik felhőbe

Az Azure Cloud Services által biztosított környezetek megfelelnek a helyi szabályozásoknak.
Regionális felhőszolgáltatásban található fiókok esetében a környezetet az `-Environment` argumentummal való bejelentkezéskor kell beállítania.
Ez a paraméter bármely bejelentkezési módszer esetében használható. Például ha a fiók a kínai felhőszolgáltatásban található:

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

Az alábbi paranccsal olvashatja be a rendelkezésre álló környezetek listáját:

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```
