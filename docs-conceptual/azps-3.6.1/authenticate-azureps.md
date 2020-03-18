---
title: Bejelentkezés az Azure PowerShell-lel
description: Hogyan lehet bejelentkezni az Azure PowerShellbe felhasználóként, szolgáltatásnévként vagy az Azure-erőforrások felügyelt identitásaival.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/04/2019
ms.openlocfilehash: 0de487cc34593ceac05aa2077358d692470dc23e
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "79402748"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="f15b6-103">Bejelentkezés az Azure PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="f15b6-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="f15b6-104">Az Azure PowerShell többféle hitelesítési módszert támogat.</span><span class="sxs-lookup"><span data-stu-id="f15b6-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="f15b6-105">Első lépésként a legegyszerűbb, ha az [Azure Cloud Shellt](/azure/cloud-shell/overview) használja, amely automatikusan belépteti.</span><span class="sxs-lookup"><span data-stu-id="f15b6-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="f15b6-106">Helyi telepítés esetén interaktívan jelentkezhet be a böngészőjén keresztül.</span><span class="sxs-lookup"><span data-stu-id="f15b6-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="f15b6-107">Automatizálási szkriptek írásakor az ajánlott módszer a [szolgáltatásnév](create-azure-service-principal-azureps.md) használata a szükséges engedélyekkel.</span><span class="sxs-lookup"><span data-stu-id="f15b6-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="f15b6-108">Egyéni használati esetekben az Azure-erőforrások biztonságát úgy őrizheti meg, ha a lehető legnagyobb mértékben korlátozza a bejelentkezési engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="f15b6-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="f15b6-109">Bejelentkezés után a parancsokat a rendszer az alapértelmezett előfizetésen futtatja.</span><span class="sxs-lookup"><span data-stu-id="f15b6-109">After signing in, commands are run against your default subscription.</span></span> <span data-ttu-id="f15b6-110">Az adott munkamenethez tartozó aktív előfizetés módosításához használja a [Set-AzContext](/powershell/module/az.accounts/set-azcontext) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f15b6-110">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="f15b6-111">Az Azure PowerShell-lel való bejelentkezéskor használt alapértelmezett előfizetés módosításához használja a [Set-AzDefault](/powershell/module/az.accounts/set-azdefault) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f15b6-111">To change the default subscription used when logging in with Azure PowerShell, use [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="f15b6-112">A hitelesítő adatok megoszlanak több PowerShell-munkamenet között, ha be van jelentkezve.</span><span class="sxs-lookup"><span data-stu-id="f15b6-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="f15b6-113">További információért tekintse meg az [Állandó hitelesítő adatokat](context-persistence.md) ismertető cikket.</span><span class="sxs-lookup"><span data-stu-id="f15b6-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="f15b6-114">Interaktív bejelentkezés</span><span class="sxs-lookup"><span data-stu-id="f15b6-114">Sign in interactively</span></span>

<span data-ttu-id="f15b6-115">Az interaktív bejelentkezéshez használja a [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f15b6-115">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="f15b6-116">A futtatáskor ez a parancsmag jogkivonatsztringet jelenít meg.</span><span class="sxs-lookup"><span data-stu-id="f15b6-116">When run, this cmdlet will present a token string.</span></span> <span data-ttu-id="f15b6-117">A bejelentkezéshez másolja ezt a sztringet a https://microsoft.com/devicelogin címbe egy böngészőben.</span><span class="sxs-lookup"><span data-stu-id="f15b6-117">To sign in, copy this string and paste it into https://microsoft.com/devicelogin in a browser.</span></span> <span data-ttu-id="f15b6-118">A rendszer ekkor hitelesíti a PowerShell-munkamenetet az Azure-hoz való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="f15b6-118">Your PowerShell session will be authenticated to connect to Azure.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="f15b6-119">Az Active Directory engedélyezési folyamatának végrehajtásában történt módosítások miatt és biztonsági okokból a felhasználónévvel és jelszóval történő hitelesítés el lett távolítva az Azure PowerShellből.</span><span class="sxs-lookup"><span data-stu-id="f15b6-119">Username/password credential authorization has been removed in Azure PowerShell due to changes in Active Directory authorization implementations and security concerns.</span></span>
> <span data-ttu-id="f15b6-120">Ha az automatizálhatóság érdekében használta ezt a típusú hitelesítést, helyette [hozzon létre egy szolgáltatásnevet](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="f15b6-120">If you use credential authorization for automation purposes, instead [create a service principal](create-azure-service-principal-azureps.md).</span></span>

## <a name="sign-in-with-a-service-principal-a-namesp-signin"></a><span data-ttu-id="f15b6-121">Bejelentkezés szolgáltatásnévvel <a name="sp-signin"/></span><span class="sxs-lookup"><span data-stu-id="f15b6-121">Sign in with a service principal <a name="sp-signin"/></span></span>

<span data-ttu-id="f15b6-122">A szolgáltatásnevek nem interaktív Azure-fiókok.</span><span class="sxs-lookup"><span data-stu-id="f15b6-122">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="f15b6-123">Más felhasználói fiókokhoz hasonlóan az ezekhez tartozó engedélyek kezelését is az Azure Active Directory végzi.</span><span class="sxs-lookup"><span data-stu-id="f15b6-123">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="f15b6-124">Az automatizálási szkriptek biztonságát úgy garantálhatjuk, ha a szolgáltatásnevek számára csak a szükséges engedélyeket adjuk meg.</span><span class="sxs-lookup"><span data-stu-id="f15b6-124">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="f15b6-125">Ha meg szeretné tudni, hogyan hozhat létre szolgáltatásnevet az Azure PowerShell-lel való használatra, tekintse meg az [Azure-beli szolgáltatásnév Azure PowerShell használatával történő létrehozásával](create-azure-service-principal-azureps.md) kapcsolatos szakaszt.</span><span class="sxs-lookup"><span data-stu-id="f15b6-125">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="f15b6-126">Szolgáltatásnévvel való bejelentkezéshez használja a `-ServicePrincipal` argumentumot a `Connect-AzAccount` parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="f15b6-126">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="f15b6-127">Szüksége lesz a szolgáltatásnév alkalmazásazonosítójára, a bejelentkezési hitelesítő adatokra, és a szolgáltatásnévhez tartozó bérlőazonosítóra.</span><span class="sxs-lookup"><span data-stu-id="f15b6-127">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="f15b6-128">A szolgáltatásnévvel való bejelentkezés módja attól függ, hogy az jelszó- vagy tanúsítványalapú hitelesítésre van-e konfigurálva.</span><span class="sxs-lookup"><span data-stu-id="f15b6-128">How you sign in with a service principal will depend on whether it's configured for password-based or certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="f15b6-129">Jelszóalapú hitelesítés</span><span class="sxs-lookup"><span data-stu-id="f15b6-129">Password-based authentication</span></span>

<span data-ttu-id="f15b6-130">Annak érdekében, hogy a szolgáltatásnév hitelesítő adatait a megfelelő objektumként kapja meg, használja a [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f15b6-130">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="f15b6-131">Ez a parancsmag felhasználónév és jelszó megadását kéri.</span><span class="sxs-lookup"><span data-stu-id="f15b6-131">This cmdlet will present a prompt for a username and password.</span></span> <span data-ttu-id="f15b6-132">Felhasználónévként használja a szolgáltatásnév azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="f15b6-132">Use the service principal ID for the username.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="f15b6-133">Automatizálási forgatókönyvek esetén a hitelesítő adatokat egy felhasználónévből és egy biztonságos sztringből kell létrehoznia:</span><span class="sxs-lookup"><span data-stu-id="f15b6-133">For automation scenarios, you need to create credentials from a user name and secure string:</span></span>

```azurepowershell-interactive
$passwd = ConvertTo-SecureString <use a secure password here> -AsPlainText -Force
$pscredential = New-Object System.Management.Automation.PSCredential('service principal name/id', $passwd)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="f15b6-134">Győződjön meg róla, hogy a szolgáltatásnév-kapcsolatok automatizálásakor a jelszó tárolása megfelelően történik.</span><span class="sxs-lookup"><span data-stu-id="f15b6-134">Make sure that you use good password storage practices when automating service principal connections.</span></span>

### <a name="certificate-based-authentication"></a><span data-ttu-id="f15b6-135">Tanúsítványalapú hitelesítés</span><span class="sxs-lookup"><span data-stu-id="f15b6-135">Certificate-based authentication</span></span>

<span data-ttu-id="f15b6-136">A tanúsítványalapú hitelesítéshez az Azure PowerShellnek egy helyi tanúsítványtárolóból kell információkat lekérnie a tanúsítvány ujjlenyomata alapján.</span><span class="sxs-lookup"><span data-stu-id="f15b6-136">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ApplicationId $appId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="f15b6-137">Ha regisztrált alkalmazás helyett szolgáltatásnevet használ, adja hozzá a `-ServicePrincipal` argumentumot, és adja meg a szolgáltatásnév alkalmazásazonosítóját az `-ApplicationId` paraméter értékeként.</span><span class="sxs-lookup"><span data-stu-id="f15b6-137">When using a service principal instead of a registered application, add the `-ServicePrincipal` argument and provide the service principal's Application ID as the `-ApplicationId` parameter's value.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -ApplicationId $servicePrincipalId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="f15b6-138">A PowerShell 5.1-ben a tanúsítványtároló a [PKI](/powershell/module/pkiclient)-modullal felügyelhető és vizsgálható.</span><span class="sxs-lookup"><span data-stu-id="f15b6-138">In PowerShell 5.1, the certificate store can be managed and inspected with the [PKI](/powershell/module/pkiclient) module.</span></span> <span data-ttu-id="f15b6-139">A PowerShell Core 6.x és az újabb verziókban a folyamat ennél összetettebb.</span><span class="sxs-lookup"><span data-stu-id="f15b6-139">For PowerShell Core 6.x and later, the process is more complicated.</span></span> <span data-ttu-id="f15b6-140">Az alábbi szkriptek bemutatják, hogyan importálhat egy meglévő tanúsítványt a PowerShell által hozzáférhető tanúsítványtárolóba.</span><span class="sxs-lookup"><span data-stu-id="f15b6-140">The following scripts show you how to import an existing certificate into the certificate store accessible by PowerShell.</span></span>

#### <a name="import-a-certificate-in-powershell-51"></a><span data-ttu-id="f15b6-141">Tanúsítvány importálása PowerShell 5.1-ben</span><span class="sxs-lookup"><span data-stu-id="f15b6-141">Import a certificate in PowerShell 5.1</span></span>

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a><span data-ttu-id="f15b6-142">Tanúsítvány importálása PowerShell Core 6.x és újabb verziókban</span><span class="sxs-lookup"><span data-stu-id="f15b6-142">Import a certificate in PowerShell Core 6.x and later</span></span>

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

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="f15b6-143">Bejelentkezés felügyelt identitással</span><span class="sxs-lookup"><span data-stu-id="f15b6-143">Sign in using a managed identity</span></span>

<span data-ttu-id="f15b6-144">A felügyelt identitások az Azure Active Directory funkciójaként érhetők el.</span><span class="sxs-lookup"><span data-stu-id="f15b6-144">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="f15b6-145">A felügyelt identitások Azure-ban futó erőforrásokhoz társított szolgáltatásnevek.</span><span class="sxs-lookup"><span data-stu-id="f15b6-145">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="f15b6-146">A felügyelt identitás szolgáltatásnevével bejelentkezhet, és beszerezhet egy csak alkalmazásra érvényes hozzáférési jogkivonatot az egyéb erőforrások eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="f15b6-146">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="f15b6-147">A felügyelt identitások csak az Azure-felhőkben futó erőforrásokon érhetők el.</span><span class="sxs-lookup"><span data-stu-id="f15b6-147">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="f15b6-148">Ez a parancs a felügyelt identitás használatával kapcsolódik a gazdakörnyezethez.</span><span class="sxs-lookup"><span data-stu-id="f15b6-148">This command connects using the managed identity of the host environment.</span></span> <span data-ttu-id="f15b6-149">Ha például egy hozzárendelt felügyeletszolgáltatás-identitással rendelkező virtuális gépet használ, akkor a kód számára lehetővé válik a hozzárendelt identitással való bejelentkezés.</span><span class="sxs-lookup"><span data-stu-id="f15b6-149">For example, if executed on a VirtualMachine with an assigned Managed Service Identity, this allows the code to sign in using that assigned identity.</span></span>

```azurepowershell-interactive
 Connect-AzAccount -Identity 
```

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="f15b6-150">Bejelentkezés nem alapértelmezett bérlővel vagy felhőszolgáltatóként (CSP-ként)</span><span class="sxs-lookup"><span data-stu-id="f15b6-150">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="f15b6-151">Ha a fiókja egynél több bérlőhöz van társítva, kapcsolódáskor a bejelentkezéshez a `-Tenant` paramétert kell használni.</span><span class="sxs-lookup"><span data-stu-id="f15b6-151">If your account is associated with more than one tenant, sign-in requires the use of the `-Tenant` parameter when connecting.</span></span> <span data-ttu-id="f15b6-152">Ez a paraméter bármely bejelentkezési módszer esetében használható.</span><span class="sxs-lookup"><span data-stu-id="f15b6-152">This parameter will work with any sign-in method.</span></span> <span data-ttu-id="f15b6-153">Bejelentkezéskor a paraméter értéke a bérlő Azure-objektumazonosítója (bérlőazonosító) vagy a bérlő teljes tartományneve lehet.</span><span class="sxs-lookup"><span data-stu-id="f15b6-153">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="f15b6-154">[Felhőszolgáltatóként (CSP-ként)](https://azure.microsoft.com/offers/ms-azr-0145p/) való bejelentkezés esetén a `-Tenant` értékének a bérlőazonosítónak **kell** lennie.</span><span class="sxs-lookup"><span data-stu-id="f15b6-154">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), the `-Tenant` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="f15b6-155">Bejelentkezés egy másik felhőbe</span><span class="sxs-lookup"><span data-stu-id="f15b6-155">Sign in to another Cloud</span></span>

<span data-ttu-id="f15b6-156">Az Azure Cloud Services által biztosított környezetek megfelelnek a helyi szabályozásoknak.</span><span class="sxs-lookup"><span data-stu-id="f15b6-156">Azure cloud services offer environments compliant with regional data-handling laws.</span></span>
<span data-ttu-id="f15b6-157">Regionális felhőszolgáltatásban található fiókok esetében a környezetet az `-Environment` argumentummal való bejelentkezéskor kell beállítania.</span><span class="sxs-lookup"><span data-stu-id="f15b6-157">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="f15b6-158">Ez a paraméter bármely bejelentkezési módszer esetében használható.</span><span class="sxs-lookup"><span data-stu-id="f15b6-158">This parameter will work with any sign-in method.</span></span> <span data-ttu-id="f15b6-159">Például ha a fiók a kínai felhőszolgáltatásban található:</span><span class="sxs-lookup"><span data-stu-id="f15b6-159">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="f15b6-160">Az alábbi paranccsal olvashatja be a rendelkezésre álló környezetek listáját:</span><span class="sxs-lookup"><span data-stu-id="f15b6-160">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```
