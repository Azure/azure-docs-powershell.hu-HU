---
title: Bejelentkezés az Azure PowerShell-lel
description: Hogyan lehet bejelentkezni az Azure PowerShellbe felhasználóként, szolgáltatásnévként vagy az Azure-erőforrások felügyelt identitásaival.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/18/2020
ms.openlocfilehash: f82a9e373806f2f071ae59f6aee7e0a0bd4ea13d
ms.sourcegitcommit: 747769a143ddebff39e78c2cc62a182401adddb9
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/23/2020
ms.locfileid: "85268187"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="91b20-103">Bejelentkezés az Azure PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="91b20-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="91b20-104">Az Azure PowerShell többféle hitelesítési módszert támogat.</span><span class="sxs-lookup"><span data-stu-id="91b20-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="91b20-105">Első lépésként a legegyszerűbb, ha az [Azure Cloud Shellt](/azure/cloud-shell/overview) használja, amely automatikusan belépteti.</span><span class="sxs-lookup"><span data-stu-id="91b20-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="91b20-106">Helyi telepítés esetén interaktívan jelentkezhet be a böngészőjén keresztül.</span><span class="sxs-lookup"><span data-stu-id="91b20-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="91b20-107">Automatizálási szkriptek írásakor az ajánlott módszer a [szolgáltatásnév](create-azure-service-principal-azureps.md) használata a szükséges engedélyekkel.</span><span class="sxs-lookup"><span data-stu-id="91b20-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="91b20-108">Egyéni használati esetekben az Azure-erőforrások biztonságát úgy őrizheti meg, ha a lehető legnagyobb mértékben korlátozza a bejelentkezési engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="91b20-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="91b20-109">Bejelentkezés után a parancsokat a rendszer az alapértelmezett előfizetésen futtatja.</span><span class="sxs-lookup"><span data-stu-id="91b20-109">After signing in, commands are run against your default subscription.</span></span> <span data-ttu-id="91b20-110">Az adott munkamenethez tartozó aktív előfizetés módosításához használja a [Set-AzContext](/powershell/module/az.accounts/set-azcontext) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="91b20-110">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="91b20-111">Az Azure PowerShell-lel való bejelentkezéskor használt alapértelmezett előfizetés módosításához használja a [Set-AzDefault](/powershell/module/az.accounts/set-azdefault) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="91b20-111">To change the default subscription used when logging in with Azure PowerShell, use [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="91b20-112">A hitelesítő adatok megoszlanak több PowerShell-munkamenet között, ha be van jelentkezve.</span><span class="sxs-lookup"><span data-stu-id="91b20-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="91b20-113">További információért tekintse meg az [Állandó hitelesítő adatokat](context-persistence.md) ismertető cikket.</span><span class="sxs-lookup"><span data-stu-id="91b20-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="91b20-114">Interaktív bejelentkezés</span><span class="sxs-lookup"><span data-stu-id="91b20-114">Sign in interactively</span></span>

<span data-ttu-id="91b20-115">Az interaktív bejelentkezéshez használja a [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="91b20-115">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="91b20-116">A PowerShell 6-os vagy újabb verziójának futtatásakor ez a parancsmag jogkivonatsztringet jelenít meg.</span><span class="sxs-lookup"><span data-stu-id="91b20-116">When run from PowerShell version 6 and higher, this cmdlet presents a token string.</span></span> <span data-ttu-id="91b20-117">A bejelentkezéshez másolja és illessze be ezt a sztringet a [microsoft.com/devicelogin](https://microsoft.com/devicelogin) helyre egy webböngészőben.</span><span class="sxs-lookup"><span data-stu-id="91b20-117">To sign in, copy this string and paste it into [microsoft.com/devicelogin](https://microsoft.com/devicelogin) in a web browser.</span></span> <span data-ttu-id="91b20-118">A rendszer ekkor hitelesíti a PowerShell-munkamenetet az Azure-hoz való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="91b20-118">Your PowerShell session will be authenticated to connect to Azure.</span></span> <span data-ttu-id="91b20-119">Megadhatja a `UseDeviceAuthentication` paramétert úgy, hogy jogkivonatsztringet fogadjon a Windows PowerShellen.</span><span class="sxs-lookup"><span data-stu-id="91b20-119">You can specify the `UseDeviceAuthentication` parameter to receive a token string on Windows PowerShell.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="91b20-120">Az Active Directory engedélyezési folyamatának végrehajtásában történt módosítások miatt és biztonsági okokból a felhasználónévvel és jelszóval történő hitelesítés el lett távolítva az Azure PowerShellből.</span><span class="sxs-lookup"><span data-stu-id="91b20-120">Username/password credential authorization has been removed in Azure PowerShell due to changes in Active Directory authorization implementations and security concerns.</span></span> <span data-ttu-id="91b20-121">Ha az automatizálhatóság érdekében használta ezt a típusú hitelesítést, helyette [hozzon létre egy szolgáltatásnevet](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="91b20-121">If you use credential authorization for automation purposes, instead [create a service principal](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="91b20-122">Használhatja a [Get-AzContext](/powershell/module/az.accounts/get-azcontext) parancsmagot a bérlőazonosító tárolásához egy változóban, mert a cikk két ezt követő szakaszában szükség lesz rá.</span><span class="sxs-lookup"><span data-stu-id="91b20-122">Use the [Get-AzContext](/powershell/module/az.accounts/get-azcontext) cmdlet to store your tenant ID in a variable to be used in the next two sections of this article.</span></span>

```azurepowershell-interactive
$tenantId = (Get-AzContext).Tenant.Id
```

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="91b20-123">Bejelentkezés szolgáltatásnévvel <a name="sp-signin"/></span><span class="sxs-lookup"><span data-stu-id="91b20-123">Sign in with a service principal <a name="sp-signin"/></span></span>

<span data-ttu-id="91b20-124">A szolgáltatásnevek nem interaktív Azure-fiókok.</span><span class="sxs-lookup"><span data-stu-id="91b20-124">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="91b20-125">Más felhasználói fiókokhoz hasonlóan az ezekhez tartozó engedélyek kezelését is az Azure Active Directory végzi.</span><span class="sxs-lookup"><span data-stu-id="91b20-125">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="91b20-126">Az automatizálási szkriptek biztonságát úgy garantálhatjuk, ha a szolgáltatásnevek számára csak a szükséges engedélyeket adjuk meg.</span><span class="sxs-lookup"><span data-stu-id="91b20-126">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="91b20-127">Ha meg szeretné tudni, hogyan hozhat létre szolgáltatásnevet az Azure PowerShell-lel való használatra, tekintse meg az [Azure-beli szolgáltatásnév Azure PowerShell használatával történő létrehozásával](create-azure-service-principal-azureps.md) kapcsolatos szakaszt.</span><span class="sxs-lookup"><span data-stu-id="91b20-127">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="91b20-128">Szolgáltatásnévvel való bejelentkezéshez használja a `-ServicePrincipal` argumentumot a `Connect-AzAccount` parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="91b20-128">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="91b20-129">Szüksége lesz a szolgáltatásnév alkalmazásazonosítójára, a bejelentkezési hitelesítő adatokra, és a szolgáltatásnévhez tartozó bérlőazonosítóra.</span><span class="sxs-lookup"><span data-stu-id="91b20-129">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="91b20-130">A szolgáltatásnévvel való bejelentkezés módja attól függ, hogy az jelszó- vagy tanúsítványalapú hitelesítésre van-e konfigurálva.</span><span class="sxs-lookup"><span data-stu-id="91b20-130">How you sign in with a service principal depends on whether it's configured for password-based or certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="91b20-131">Jelszóalapú hitelesítés</span><span class="sxs-lookup"><span data-stu-id="91b20-131">Password-based authentication</span></span>

<span data-ttu-id="91b20-132">Hozzon létre egy szolgáltatásnevet, hogy használhassa ennek a szakasznak a példáiban.</span><span class="sxs-lookup"><span data-stu-id="91b20-132">Create a service principal to be used in the examples in this section.</span></span> <span data-ttu-id="91b20-133">További információ a szolgáltatásnevek létrehozásával kapcsolatban: [Azure-beli szolgáltatásnév létrehozása az Azure PowerShell használatával](/powershell/azure/create-azure-service-principal-azureps).</span><span class="sxs-lookup"><span data-stu-id="91b20-133">For more information on creating service principals, see [Create an Azure service principal with Azure PowerShell](/powershell/azure/create-azure-service-principal-azureps).</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="91b20-134">Annak érdekében, hogy a szolgáltatásnév hitelesítő adatait a megfelelő objektumként kapja meg, használja a [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="91b20-134">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="91b20-135">Ez a parancsmag felhasználónév és jelszó megadását kéri.</span><span class="sxs-lookup"><span data-stu-id="91b20-135">This cmdlet presents a prompt for a username and password.</span></span> <span data-ttu-id="91b20-136">Használja a szolgáltatásnév `applicationID` azonosítóját felhasználónévként, és konvertálja annak `secret` paraméterét egyszerű szöveggé a jelszóhoz.</span><span class="sxs-lookup"><span data-stu-id="91b20-136">Use the service principal's `applicationID` for the username and convert its `secret` to plain text for the password.</span></span>

```azurepowershell-interactive
# Retrieve the plain text password for use with `Get-Credential` in the next command.
$sp.secret | ConvertFrom-SecureString -AsPlainText

$pscredential = Get-Credential -UserName $sp.ApplicationId
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="91b20-137">Automatizálási forgatókönyvek esetén a hitelesítő adatokat egy szolgáltatásnév `applicationId` és `secret` paramétereiből kell létrehozni:</span><span class="sxs-lookup"><span data-stu-id="91b20-137">For automation scenarios, you need to create credentials from a service principal's `applicationId` and `secret`:</span></span>

```azurepowershell-interactive
$pscredential = New-Object -TypeName System.Management.Automation.PSCredential($sp.ApplicationId, $sp.Secret)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="91b20-138">Győződjön meg róla, hogy a szolgáltatásnév-kapcsolatok automatizálásakor a jelszó tárolása megfelelően történik.</span><span class="sxs-lookup"><span data-stu-id="91b20-138">Make sure that you use good password storage practices when automating service principal connections.</span></span>

### <a name="certificate-based-authentication"></a><span data-ttu-id="91b20-139">Tanúsítványalapú hitelesítés</span><span class="sxs-lookup"><span data-stu-id="91b20-139">Certificate-based authentication</span></span>

<span data-ttu-id="91b20-140">A tanúsítványalapú hitelesítéshez az Azure PowerShellnek egy helyi tanúsítványtárolóból kell információkat lekérnie a tanúsítvány ujjlenyomata alapján.</span><span class="sxs-lookup"><span data-stu-id="91b20-140">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ApplicationId $appId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="91b20-141">Ha regisztrált alkalmazás helyett szolgáltatásnevet használ, adja hozzá a `-ServicePrincipal` argumentumot, és adja meg a szolgáltatásnév alkalmazásazonosítóját az `-ApplicationId` paraméter értékeként.</span><span class="sxs-lookup"><span data-stu-id="91b20-141">When using a service principal instead of a registered application, add the `-ServicePrincipal` argument and provide the service principal's Application ID as the `-ApplicationId` parameter's value.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -ApplicationId $servicePrincipalId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="91b20-142">A PowerShell 5.1-ben a tanúsítványtároló a [PKI](/powershell/module/pkiclient)-modullal felügyelhető és vizsgálható.</span><span class="sxs-lookup"><span data-stu-id="91b20-142">In PowerShell 5.1, the certificate store can be managed and inspected with the [PKI](/powershell/module/pkiclient) module.</span></span> <span data-ttu-id="91b20-143">A PowerShell Core 6.x és az újabb verziókban a folyamat ennél összetettebb.</span><span class="sxs-lookup"><span data-stu-id="91b20-143">For PowerShell Core 6.x and later, the process is more complicated.</span></span> <span data-ttu-id="91b20-144">Az alábbi szkriptek bemutatják, hogyan importálhat egy meglévő tanúsítványt a PowerShell által hozzáférhető tanúsítványtárolóba.</span><span class="sxs-lookup"><span data-stu-id="91b20-144">The following scripts show you how to import an existing certificate into the certificate store accessible by PowerShell.</span></span>

#### <a name="import-a-certificate-in-powershell-51"></a><span data-ttu-id="91b20-145">Tanúsítvány importálása PowerShell 5.1-ben</span><span class="sxs-lookup"><span data-stu-id="91b20-145">Import a certificate in PowerShell 5.1</span></span>

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a><span data-ttu-id="91b20-146">Tanúsítvány importálása PowerShell Core 6.x és újabb verziókban</span><span class="sxs-lookup"><span data-stu-id="91b20-146">Import a certificate in PowerShell Core 6.x and later</span></span>

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

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="91b20-147">Bejelentkezés felügyelt identitással</span><span class="sxs-lookup"><span data-stu-id="91b20-147">Sign in using a managed identity</span></span>

<span data-ttu-id="91b20-148">A felügyelt identitások az Azure Active Directory funkciójaként érhetők el.</span><span class="sxs-lookup"><span data-stu-id="91b20-148">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="91b20-149">A felügyelt identitások Azure-ban futó erőforrásokhoz társított szolgáltatásnevek.</span><span class="sxs-lookup"><span data-stu-id="91b20-149">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="91b20-150">A felügyelt identitás szolgáltatásnevével bejelentkezhet, és beszerezhet egy csak alkalmazásra érvényes hozzáférési jogkivonatot az egyéb erőforrások eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="91b20-150">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="91b20-151">A felügyelt identitások csak az Azure-felhőkben futó erőforrásokon érhetők el.</span><span class="sxs-lookup"><span data-stu-id="91b20-151">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="91b20-152">Ebben a példában a kapcsolódás a gazdakörnyezet felügyelt identitásával történik.</span><span class="sxs-lookup"><span data-stu-id="91b20-152">This example connects using the managed identity of the host environment.</span></span> <span data-ttu-id="91b20-153">Ha például egy hozzárendelt felügyeletszolgáltatás-identitással rendelkező virtuális gépet használ, akkor a kód számára lehetővé válik a hozzárendelt identitással való bejelentkezés.</span><span class="sxs-lookup"><span data-stu-id="91b20-153">For example, if executed on a VirtualMachine with an assigned Managed Service Identity, this allows the code to sign in using that assigned identity.</span></span>

```azurepowershell-interactive
 Connect-AzAccount -Identity
```

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="91b20-154">Bejelentkezés nem alapértelmezett bérlővel vagy felhőszolgáltatóként (CSP-ként)</span><span class="sxs-lookup"><span data-stu-id="91b20-154">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="91b20-155">Ha a fiókja egynél több bérlőhöz van társítva, kapcsolódáskor a bejelentkezéshez a `-Tenant` paramétert kell megadni.</span><span class="sxs-lookup"><span data-stu-id="91b20-155">If your account is associated with more than one tenant, sign-in requires the `-Tenant` parameter to be specified when connecting.</span></span> <span data-ttu-id="91b20-156">Ez a paraméter bármely bejelentkezési módszer esetében használható.</span><span class="sxs-lookup"><span data-stu-id="91b20-156">This parameter works with any sign-in method.</span></span> <span data-ttu-id="91b20-157">Bejelentkezéskor a paraméter értéke a bérlő Azure-objektumazonosítója (bérlőazonosító) vagy a bérlő teljes tartományneve lehet.</span><span class="sxs-lookup"><span data-stu-id="91b20-157">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="91b20-158">[Felhőszolgáltatóként (CSP-ként)](https://azure.microsoft.com/offers/ms-azr-0145p/) való bejelentkezés esetén a `-Tenant` értékének a bérlőazonosítónak **kell** lennie.</span><span class="sxs-lookup"><span data-stu-id="91b20-158">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), the `-Tenant` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="91b20-159">Bejelentkezés egy másik felhőbe</span><span class="sxs-lookup"><span data-stu-id="91b20-159">Sign in to another Cloud</span></span>

<span data-ttu-id="91b20-160">Az Azure Cloud Services által biztosított környezetek megfelelnek a helyi szabályozásoknak.</span><span class="sxs-lookup"><span data-stu-id="91b20-160">Azure cloud services offer environments compliant with regional data-handling laws.</span></span> <span data-ttu-id="91b20-161">Regionális felhőszolgáltatásban található fiókok esetében a környezetet az `-Environment` argumentummal való bejelentkezéskor kell beállítania.</span><span class="sxs-lookup"><span data-stu-id="91b20-161">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span> <span data-ttu-id="91b20-162">Ez a paraméter bármely bejelentkezési módszer esetében használható.</span><span class="sxs-lookup"><span data-stu-id="91b20-162">This parameter works with any sign-in method.</span></span> <span data-ttu-id="91b20-163">Például ha a fiók a kínai felhőszolgáltatásban található:</span><span class="sxs-lookup"><span data-stu-id="91b20-163">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="91b20-164">Az alábbi paranccsal olvashatja be a rendelkezésre álló környezetek listáját:</span><span class="sxs-lookup"><span data-stu-id="91b20-164">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object -Property Name
```
