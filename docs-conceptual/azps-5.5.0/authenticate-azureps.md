---
title: Bejelentkezés az Azure PowerShell-lel
description: Hogyan lehet bejelentkezni az Azure PowerShellbe felhasználóként, szolgáltatásnévként vagy az Azure-erőforrások felügyelt identitásaival.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/23/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 46e5e84b6718cc7a700ef2df4e82647e8cb60941
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100012751"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="246dd-103">Bejelentkezés az Azure PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="246dd-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="246dd-104">Az Azure PowerShell többféle hitelesítési módszert támogat.</span><span class="sxs-lookup"><span data-stu-id="246dd-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="246dd-105">Első lépésként a legegyszerűbb, ha az [Azure Cloud Shellt](/azure/cloud-shell/overview) használja, amely automatikusan belépteti.</span><span class="sxs-lookup"><span data-stu-id="246dd-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="246dd-106">Helyi telepítés esetén interaktívan jelentkezhet be a böngészőjén keresztül.</span><span class="sxs-lookup"><span data-stu-id="246dd-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="246dd-107">Automatizálási szkriptek írásakor az ajánlott módszer a [szolgáltatásnév](create-azure-service-principal-azureps.md) használata a szükséges engedélyekkel.</span><span class="sxs-lookup"><span data-stu-id="246dd-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="246dd-108">Egyéni használati esetekben az Azure-erőforrások biztonságát úgy őrizheti meg, ha a lehető legnagyobb mértékben korlátozza a bejelentkezési engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="246dd-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="246dd-109">A kezdetekkor az Azure által visszaadott első előfizetésbe lesz bejelentkezve, ha egynél több előfizetéshez rendelkezik hozzáféréssel.</span><span class="sxs-lookup"><span data-stu-id="246dd-109">Initially, you're signed into the first subscription Azure returns if you have access to more than one subscription.</span></span> <span data-ttu-id="246dd-110">Alapértelmezés szerint a futtatott parancsok ezen az előfizetésen lesznek végrehajtva.</span><span class="sxs-lookup"><span data-stu-id="246dd-110">Commands are run against this subscription by default.</span></span> <span data-ttu-id="246dd-111">Az adott munkamenethez tartozó aktív előfizetés módosításához használja a [Set-AzContext](/powershell/module/az.accounts/set-azcontext) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="246dd-111">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="246dd-112">Ha módosítani szeretné az aktív előfizetését, és szeretné, hogy ez az ugyanazon a rendszeren indított munkamenetek között rögzítve legyen, használja a [Select-AzContext](/powershell/module/az.accounts/select-azcontext) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="246dd-112">To change your active subscription and have it persist between sessions on the same system, use the [Select-AzContext](/powershell/module/az.accounts/select-azcontext) cmdlet.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="246dd-113">A hitelesítő adatok megoszlanak több PowerShell-munkamenet között, ha be van jelentkezve.</span><span class="sxs-lookup"><span data-stu-id="246dd-113">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="246dd-114">További információért tekintse meg az [Állandó hitelesítő adatokat](context-persistence.md) ismertető cikket.</span><span class="sxs-lookup"><span data-stu-id="246dd-114">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="246dd-115">Interaktív bejelentkezés</span><span class="sxs-lookup"><span data-stu-id="246dd-115">Sign in interactively</span></span>

<span data-ttu-id="246dd-116">Az interaktív bejelentkezéshez használja a [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="246dd-116">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="246dd-117">Az Az PowerShell-modul 5.0.0-s verziójától kezdve ez a parancsmag alapértelmezés szerint interaktív böngésző-alapú bejelentkezési utasítást jelenít meg.</span><span class="sxs-lookup"><span data-stu-id="246dd-117">Beginning with Az PowerShell module version 5.0.0, this cmdlet presents an interactive browser based login prompt by default.</span></span> <span data-ttu-id="246dd-118">Megadhatja a `UseDeviceAuthentication` paramétert egy olyan jogkivonatsztring fogadásához, amely korábban a PowerShell 6-os vagy újabb verziójának alapértelmezett értéke volt.</span><span class="sxs-lookup"><span data-stu-id="246dd-118">You can specify the `UseDeviceAuthentication` parameter to receive a token string which was previously the default for PowerShell version 6 and higher.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="246dd-119">Az Active Directory engedélyezési folyamatának végrehajtásában történt módosítások miatt és biztonsági okokból a felhasználónévvel és jelszóval történő hitelesítés el lett távolítva az Azure PowerShellből.</span><span class="sxs-lookup"><span data-stu-id="246dd-119">Username/password credential authorization has been removed in Azure PowerShell due to changes in Active Directory authorization implementations and security concerns.</span></span> <span data-ttu-id="246dd-120">Ha az automatizálhatóság érdekében használta ezt a típusú hitelesítést, helyette [hozzon létre egy szolgáltatásnevet](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="246dd-120">If you use credential authorization for automation purposes, instead [create a service principal](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="246dd-121">Használhatja a [Get-AzContext](/powershell/module/az.accounts/get-azcontext) parancsmagot a bérlőazonosító tárolásához egy változóban, mert a cikk két ezt követő szakaszában szükség lesz rá.</span><span class="sxs-lookup"><span data-stu-id="246dd-121">Use the [Get-AzContext](/powershell/module/az.accounts/get-azcontext) cmdlet to store your tenant ID in a variable to be used in the next two sections of this article.</span></span>

```azurepowershell-interactive
$tenantId = (Get-AzContext).Tenant.Id
```

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="246dd-122">Bejelentkezés szolgáltatásnévvel <a name="sp-signin"/></span><span class="sxs-lookup"><span data-stu-id="246dd-122">Sign in with a service principal <a name="sp-signin"/></span></span>

<span data-ttu-id="246dd-123">A szolgáltatásnevek nem interaktív Azure-fiókok.</span><span class="sxs-lookup"><span data-stu-id="246dd-123">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="246dd-124">Más felhasználói fiókokhoz hasonlóan az ezekhez tartozó engedélyek kezelését is az Azure Active Directory végzi.</span><span class="sxs-lookup"><span data-stu-id="246dd-124">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="246dd-125">Az automatizálási szkriptek biztonságát úgy garantálhatjuk, ha a szolgáltatásnevek számára csak a szükséges engedélyeket adjuk meg.</span><span class="sxs-lookup"><span data-stu-id="246dd-125">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="246dd-126">Ha meg szeretné tudni, hogyan hozhat létre szolgáltatásnevet az Azure PowerShell-lel való használatra, tekintse meg az [Azure-beli szolgáltatásnév Azure PowerShell használatával történő létrehozásával](create-azure-service-principal-azureps.md) kapcsolatos szakaszt.</span><span class="sxs-lookup"><span data-stu-id="246dd-126">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="246dd-127">Szolgáltatásnévvel való bejelentkezéshez használja a `-ServicePrincipal` argumentumot a `Connect-AzAccount` parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="246dd-127">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="246dd-128">Szüksége lesz a szolgáltatásnév alkalmazásazonosítójára, a bejelentkezési hitelesítő adatokra, és a szolgáltatásnévhez tartozó bérlőazonosítóra.</span><span class="sxs-lookup"><span data-stu-id="246dd-128">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="246dd-129">A szolgáltatásnévvel való bejelentkezés módja attól függ, hogy az jelszó- vagy tanúsítványalapú hitelesítésre van-e konfigurálva.</span><span class="sxs-lookup"><span data-stu-id="246dd-129">How you sign in with a service principal depends on whether it's configured for password-based or certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="246dd-130">Jelszóalapú hitelesítés</span><span class="sxs-lookup"><span data-stu-id="246dd-130">Password-based authentication</span></span>

<span data-ttu-id="246dd-131">Hozzon létre egy szolgáltatásnevet, hogy használhassa ennek a szakasznak a példáiban.</span><span class="sxs-lookup"><span data-stu-id="246dd-131">Create a service principal to be used in the examples in this section.</span></span> <span data-ttu-id="246dd-132">További információ a szolgáltatásnevek létrehozásával kapcsolatban: [Azure-beli szolgáltatásnév létrehozása az Azure PowerShell használatával](/powershell/azure/create-azure-service-principal-azureps).</span><span class="sxs-lookup"><span data-stu-id="246dd-132">For more information on creating service principals, see [Create an Azure service principal with Azure PowerShell](/powershell/azure/create-azure-service-principal-azureps).</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="246dd-133">Annak érdekében, hogy a szolgáltatásnév hitelesítő adatait a megfelelő objektumként kapja meg, használja a [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="246dd-133">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="246dd-134">Ez a parancsmag felhasználónév és jelszó megadását kéri.</span><span class="sxs-lookup"><span data-stu-id="246dd-134">This cmdlet presents a prompt for a username and password.</span></span> <span data-ttu-id="246dd-135">Használja a szolgáltatásnév `applicationID` azonosítóját felhasználónévként, és konvertálja annak `secret` paraméterét egyszerű szöveggé a jelszóhoz.</span><span class="sxs-lookup"><span data-stu-id="246dd-135">Use the service principal's `applicationID` for the username and convert its `secret` to plain text for the password.</span></span>

```azurepowershell-interactive
# Retrieve the plain text password for use with `Get-Credential` in the next command.
$sp.secret | ConvertFrom-SecureString -AsPlainText

$pscredential = Get-Credential -UserName $sp.ApplicationId
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="246dd-136">Automatizálási forgatókönyvek esetén a hitelesítő adatokat egy szolgáltatásnév `applicationId` és `secret` paramétereiből kell létrehozni:</span><span class="sxs-lookup"><span data-stu-id="246dd-136">For automation scenarios, you need to create credentials from a service principal's `applicationId` and `secret`:</span></span>

```azurepowershell-interactive
$pscredential = New-Object -TypeName System.Management.Automation.PSCredential($sp.ApplicationId, $sp.Secret)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="246dd-137">Győződjön meg róla, hogy a szolgáltatásnév-kapcsolatok automatizálásakor a jelszó tárolása megfelelően történik.</span><span class="sxs-lookup"><span data-stu-id="246dd-137">Make sure that you use good password storage practices when automating service principal connections.</span></span>

### <a name="certificate-based-authentication"></a><span data-ttu-id="246dd-138">Tanúsítványalapú hitelesítés</span><span class="sxs-lookup"><span data-stu-id="246dd-138">Certificate-based authentication</span></span>

<span data-ttu-id="246dd-139">A tanúsítványalapú hitelesítéshez az Azure PowerShellnek egy helyi tanúsítványtárolóból kell információkat lekérnie a tanúsítvány ujjlenyomata alapján.</span><span class="sxs-lookup"><span data-stu-id="246dd-139">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ApplicationId $appId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="246dd-140">Ha regisztrált alkalmazás helyett szolgáltatásnevet használ, adja hozzá a `-ServicePrincipal` argumentumot, és adja meg a szolgáltatásnév alkalmazásazonosítóját az `-ApplicationId` paraméter értékeként.</span><span class="sxs-lookup"><span data-stu-id="246dd-140">When using a service principal instead of a registered application, add the `-ServicePrincipal` argument and provide the service principal's Application ID as the `-ApplicationId` parameter's value.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -ApplicationId $servicePrincipalId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="246dd-141">A PowerShell 5.1-ben a tanúsítványtároló a [PKI](/powershell/module/pkiclient)-modullal felügyelhető és vizsgálható.</span><span class="sxs-lookup"><span data-stu-id="246dd-141">In PowerShell 5.1, the certificate store can be managed and inspected with the [PKI](/powershell/module/pkiclient) module.</span></span> <span data-ttu-id="246dd-142">A PowerShell Core 6.x és az újabb verziókban a folyamat ennél összetettebb.</span><span class="sxs-lookup"><span data-stu-id="246dd-142">For PowerShell Core 6.x and later, the process is more complicated.</span></span> <span data-ttu-id="246dd-143">Az alábbi szkriptek bemutatják, hogyan importálhat egy meglévő tanúsítványt a PowerShell által hozzáférhető tanúsítványtárolóba.</span><span class="sxs-lookup"><span data-stu-id="246dd-143">The following scripts show you how to import an existing certificate into the certificate store accessible by PowerShell.</span></span>

#### <a name="import-a-certificate-in-powershell-51"></a><span data-ttu-id="246dd-144">Tanúsítvány importálása PowerShell 5.1-ben</span><span class="sxs-lookup"><span data-stu-id="246dd-144">Import a certificate in PowerShell 5.1</span></span>

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a><span data-ttu-id="246dd-145">Tanúsítvány importálása PowerShell Core 6.x és újabb verziókban</span><span class="sxs-lookup"><span data-stu-id="246dd-145">Import a certificate in PowerShell Core 6.x and later</span></span>

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

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="246dd-146">Bejelentkezés felügyelt identitással</span><span class="sxs-lookup"><span data-stu-id="246dd-146">Sign in using a managed identity</span></span>

<span data-ttu-id="246dd-147">A felügyelt identitások az Azure Active Directory funkciójaként érhetők el.</span><span class="sxs-lookup"><span data-stu-id="246dd-147">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="246dd-148">A felügyelt identitások Azure-ban futó erőforrásokhoz társított szolgáltatásnevek.</span><span class="sxs-lookup"><span data-stu-id="246dd-148">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="246dd-149">A felügyelt identitás szolgáltatásnevével bejelentkezhet, és beszerezhet egy csak alkalmazásra érvényes hozzáférési jogkivonatot az egyéb erőforrások eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="246dd-149">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="246dd-150">A felügyelt identitások csak az Azure-felhőkben futó erőforrásokon érhetők el.</span><span class="sxs-lookup"><span data-stu-id="246dd-150">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="246dd-151">Ebben a példában a kapcsolódás a gazdakörnyezet felügyelt identitásával történik.</span><span class="sxs-lookup"><span data-stu-id="246dd-151">This example connects using the managed identity of the host environment.</span></span> <span data-ttu-id="246dd-152">Ha például egy hozzárendelt felügyeletszolgáltatás-identitással rendelkező virtuális gépet használ, akkor a kód számára lehetővé válik a hozzárendelt identitással való bejelentkezés.</span><span class="sxs-lookup"><span data-stu-id="246dd-152">For example, if executed on a VirtualMachine with an assigned Managed Service Identity, this allows the code to sign in using that assigned identity.</span></span>

```azurepowershell-interactive
 Connect-AzAccount -Identity
```

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="246dd-153">Bejelentkezés nem alapértelmezett bérlővel vagy felhőszolgáltatóként (CSP-ként)</span><span class="sxs-lookup"><span data-stu-id="246dd-153">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="246dd-154">Ha a fiókja egynél több bérlőhöz van társítva, kapcsolódáskor a bejelentkezéshez a `-Tenant` paramétert kell megadni.</span><span class="sxs-lookup"><span data-stu-id="246dd-154">If your account is associated with more than one tenant, sign-in requires the `-Tenant` parameter to be specified when connecting.</span></span> <span data-ttu-id="246dd-155">Ez a paraméter bármely bejelentkezési módszer esetében használható.</span><span class="sxs-lookup"><span data-stu-id="246dd-155">This parameter works with any sign-in method.</span></span> <span data-ttu-id="246dd-156">Bejelentkezéskor a paraméter értéke a bérlő Azure-objektumazonosítója (bérlőazonosító) vagy a bérlő teljes tartományneve lehet.</span><span class="sxs-lookup"><span data-stu-id="246dd-156">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="246dd-157">[Felhőszolgáltatóként (CSP-ként)](https://azure.microsoft.com/offers/ms-azr-0145p/) való bejelentkezés esetén a `-Tenant` értékének a bérlőazonosítónak **kell** lennie.</span><span class="sxs-lookup"><span data-stu-id="246dd-157">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), the `-Tenant` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="246dd-158">Bejelentkezés egy másik felhőbe</span><span class="sxs-lookup"><span data-stu-id="246dd-158">Sign in to another Cloud</span></span>

<span data-ttu-id="246dd-159">Az Azure Cloud Services által biztosított környezetek megfelelnek a helyi szabályozásoknak.</span><span class="sxs-lookup"><span data-stu-id="246dd-159">Azure cloud services offer environments compliant with regional data-handling laws.</span></span> <span data-ttu-id="246dd-160">Regionális felhőszolgáltatásban található fiókok esetében a környezetet az `-Environment` argumentummal való bejelentkezéskor kell beállítania.</span><span class="sxs-lookup"><span data-stu-id="246dd-160">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span> <span data-ttu-id="246dd-161">Ez a paraméter bármely bejelentkezési módszer esetében használható.</span><span class="sxs-lookup"><span data-stu-id="246dd-161">This parameter works with any sign-in method.</span></span> <span data-ttu-id="246dd-162">Például ha a fiók a kínai felhőszolgáltatásban található:</span><span class="sxs-lookup"><span data-stu-id="246dd-162">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="246dd-163">Az alábbi paranccsal olvashatja be a rendelkezésre álló környezetek listáját:</span><span class="sxs-lookup"><span data-stu-id="246dd-163">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object -Property Name
```
