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
ms.sourcegitcommit: b5635e291cdc324e66c936aa16c5772507fc78e8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/04/2019
ms.locfileid: "54055676"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="076fd-103">Bejelentkezés az Azure PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="076fd-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="076fd-104">Az Azure PowerShell többféle hitelesítési módszert támogat.</span><span class="sxs-lookup"><span data-stu-id="076fd-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="076fd-105">Első lépésként a legegyszerűbb, ha az [Azure Cloud Shellt](/azure/cloud-shell/overview) használja, amely automatikusan belépteti.</span><span class="sxs-lookup"><span data-stu-id="076fd-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="076fd-106">Helyi telepítés esetén interaktívan jelentkezhet be a böngészőjén keresztül.</span><span class="sxs-lookup"><span data-stu-id="076fd-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="076fd-107">Automatizálási szkriptek írásakor az ajánlott módszer a [szolgáltatásnév](create-azure-service-principal-azureps.md) használata a szükséges engedélyekkel.</span><span class="sxs-lookup"><span data-stu-id="076fd-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="076fd-108">Egyéni használati esetekben az Azure-erőforrások biztonságát úgy őrizheti meg, ha a lehető legnagyobb mértékben korlátozza a bejelentkezési engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="076fd-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="076fd-109">Bejelentkezés után a parancsokat a rendszer az alapértelmezett előfizetésen futtatja.</span><span class="sxs-lookup"><span data-stu-id="076fd-109">After signing in, commands are run against your default subscription.</span></span> <span data-ttu-id="076fd-110">Az adott munkamenethez tartozó aktív előfizetés módosításához használja a [Set-AzContext](/powershell/module/az.accounts/set-azcontext) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="076fd-110">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="076fd-111">Az Azure PowerShell-lel való bejelentkezéskor használt alapértelmezett előfizetés módosításához használja a [Set-AzDefault](/powershell/module/az.accounts/set-azdefault) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="076fd-111">To change the default subscription used when logging in with Azure PowerShell, use [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="076fd-112">A hitelesítő adatok megoszlanak több PowerShell-munkamenet között, ha be van jelentkezve.</span><span class="sxs-lookup"><span data-stu-id="076fd-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="076fd-113">További információért tekintse meg az [Állandó hitelesítő adatokat](context-persistence.md) ismertető cikket.</span><span class="sxs-lookup"><span data-stu-id="076fd-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="076fd-114">Interaktív bejelentkezés</span><span class="sxs-lookup"><span data-stu-id="076fd-114">Sign in interactively</span></span>

<span data-ttu-id="076fd-115">Az interaktív bejelentkezéshez használja a [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="076fd-115">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="076fd-116">A futtatáskor ez a parancsmag jogkivonatsztringet jelenít meg.</span><span class="sxs-lookup"><span data-stu-id="076fd-116">When run, this cmdlet will present a token string.</span></span> <span data-ttu-id="076fd-117">A bejelentkezéshez másolja ezt a sztringet a https://microsoft.com/devicelogin címbe egy böngészőben.</span><span class="sxs-lookup"><span data-stu-id="076fd-117">To sign in, copy this string and paste it into https://microsoft.com/devicelogin in a browser.</span></span> <span data-ttu-id="076fd-118">A rendszer ekkor hitelesíti a PowerShell-munkamenetet az Azure-hoz való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="076fd-118">Your PowerShell session will be authenticated to connect to Azure.</span></span>

## <a name="sign-in-with-credentials"></a><span data-ttu-id="076fd-119">Bejelentkezés hitelesítő adatokkal</span><span class="sxs-lookup"><span data-stu-id="076fd-119">Sign in with credentials</span></span>

<span data-ttu-id="076fd-120">Egy, az Azure-hoz való csatlakozásra jogosult `PSCredential` objektummal is bejelentkezhet.</span><span class="sxs-lookup"><span data-stu-id="076fd-120">You can also sign in with a `PSCredential` object authorized to connect to Azure.</span></span>
<span data-ttu-id="076fd-121">A hitelesítő objektum beszerzésének legegyszerűbb módszere a [Get-Credential](/powershell/module/Microsoft.PowerShell.Security/Get-Credential) parancsmag használata.</span><span class="sxs-lookup"><span data-stu-id="076fd-121">The easiest way to get a credential object is with the [Get-Credential](/powershell/module/Microsoft.PowerShell.Security/Get-Credential) cmdlet.</span></span> <span data-ttu-id="076fd-122">A futtatáskor ez a parancsmag egy felhasználónév/jelszó hitelesítőadat-párt fog kérni.</span><span class="sxs-lookup"><span data-stu-id="076fd-122">When run, this cmdlet will prompt you for a username/password credential pair.</span></span>

> [!Note]
> <span data-ttu-id="076fd-123">Ez a módszer nem működik Microsoft-fiókok, valamint az engedélyezett kéttényezős hitelesítéssel rendelkező fiókok esetében.</span><span class="sxs-lookup"><span data-stu-id="076fd-123">This approach doesn't work with Microsoft accounts or accounts that have two-factor authentication enabled.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
Connect-AzAccount -Credential $creds
```

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="076fd-124">Bejelentkezés szolgáltatásnévvel</span><span class="sxs-lookup"><span data-stu-id="076fd-124">Sign in with a service principal</span></span>

<span data-ttu-id="076fd-125">A szolgáltatásnevek nem interaktív Azure-fiókok.</span><span class="sxs-lookup"><span data-stu-id="076fd-125">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="076fd-126">Más felhasználói fiókokhoz hasonlóan az ezekhez tartozó engedélyek kezelését is az Azure Active Directory végzi.</span><span class="sxs-lookup"><span data-stu-id="076fd-126">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="076fd-127">Az automatizálási szkriptek biztonságát úgy garantálhatjuk, ha a szolgáltatásnevek számára csak a szükséges engedélyeket adjuk meg.</span><span class="sxs-lookup"><span data-stu-id="076fd-127">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="076fd-128">Ha meg szeretné tudni, hogyan hozhat létre szolgáltatásnevet az Azure PowerShell-lel való használatra, tekintse meg az [Azure-beli szolgáltatásnév Azure PowerShell használatával történő létrehozásával](create-azure-service-principal-azureps.md) kapcsolatos szakaszt.</span><span class="sxs-lookup"><span data-stu-id="076fd-128">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="076fd-129">Szolgáltatásnévvel való bejelentkezéshez használja a `-ServicePrincipal` argumentumot a `Connect-AzAccount` parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="076fd-129">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="076fd-130">Szüksége lesz a szolgáltatásnév alkalmazásazonosítójára, a bejelentkezési hitelesítő adatokra, és a szolgáltatásnévhez tartozó bérlőazonosítóra.</span><span class="sxs-lookup"><span data-stu-id="076fd-130">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="076fd-131">Annak érdekében, hogy a szolgáltatásnév hitelesítő adatait a megfelelő objektumként kapja meg, használja a [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="076fd-131">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="076fd-132">Ez a parancsmag a szolgáltatásnév felhasználói azonosítójának és jelszavának megadását kéri.</span><span class="sxs-lookup"><span data-stu-id="076fd-132">This cmdlet will present a prompt for the service principal user ID and password.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="076fd-133">Bejelentkezés felügyelt identitással</span><span class="sxs-lookup"><span data-stu-id="076fd-133">Sign in using a managed identity</span></span> 

<span data-ttu-id="076fd-134">A felügyelt identitások az Azure Active Directory funkciójaként érhetők el.</span><span class="sxs-lookup"><span data-stu-id="076fd-134">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="076fd-135">A felügyelt identitások Azure-ban futó erőforrásokhoz társított szolgáltatásnevek.</span><span class="sxs-lookup"><span data-stu-id="076fd-135">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="076fd-136">A felügyelt identitás szolgáltatásnevével bejelentkezhet, és beszerezhet egy csak alkalmazásra érvényes hozzáférési jogkivonatot az egyéb erőforrások eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="076fd-136">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="076fd-137">A felügyelt identitások csak az Azure-felhőkben futó erőforrásokon érhetők el.</span><span class="sxs-lookup"><span data-stu-id="076fd-137">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="076fd-138">Az Azure-erőforrások felügyelt identitásairól további információt [a hozzáférési jogkivonatok egy Azure-beli virtuális gép Azure-erőforrásainak felügyelt identitásaival való beszerzését ismertető részben](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token) talál.</span><span class="sxs-lookup"><span data-stu-id="076fd-138">To learn more about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="076fd-139">Bejelentkezés nem alapértelmezett bérlővel vagy felhőszolgáltatóként (CSP-ként)</span><span class="sxs-lookup"><span data-stu-id="076fd-139">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="076fd-140">Ha a fiókja egynél több bérlőhöz van társítva, kapcsolódáskor a bejelentkezéshez a `-TenantId` paramétert kell használni.</span><span class="sxs-lookup"><span data-stu-id="076fd-140">If your account is associated with more than one tenant, sign-in requires the use of the `-TenantId` parameter when connecting.</span></span> <span data-ttu-id="076fd-141">Ez a paraméter bármely egyéb bejelentkezési módszer esetében is használható.</span><span class="sxs-lookup"><span data-stu-id="076fd-141">This parameter will work with any other sign-in method.</span></span> <span data-ttu-id="076fd-142">Bejelentkezéskor a paraméter értéke a bérlő Azure-objektumazonosítója (bérlőazonosító) vagy a bérlő teljes tartományneve lehet.</span><span class="sxs-lookup"><span data-stu-id="076fd-142">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="076fd-143">[Felhőszolgáltatóként (CSP-ként)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) való bejelentkezés esetén a `-TenantId` értékének a bérlőazonosítónak **kell** lennie.</span><span class="sxs-lookup"><span data-stu-id="076fd-143">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/), the `-TenantId` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="076fd-144">Bejelentkezés egy másik felhőbe</span><span class="sxs-lookup"><span data-stu-id="076fd-144">Sign in to another Cloud</span></span>

<span data-ttu-id="076fd-145">Az Azure Cloud Services által biztosított környezetek megfelelnek a helyi szabályozásoknak.</span><span class="sxs-lookup"><span data-stu-id="076fd-145">Azure cloud services offer environments compliant with regional data-handling laws.</span></span>
<span data-ttu-id="076fd-146">Regionális felhőszolgáltatásban található fiókok esetében a környezetet az `-Environment` argumentummal való bejelentkezéskor kell beállítania.</span><span class="sxs-lookup"><span data-stu-id="076fd-146">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="076fd-147">Például ha a fiók a kínai felhőszolgáltatásban található:</span><span class="sxs-lookup"><span data-stu-id="076fd-147">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="076fd-148">Az alábbi paranccsal olvashatja be a rendelkezésre álló környezetek listáját:</span><span class="sxs-lookup"><span data-stu-id="076fd-148">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```