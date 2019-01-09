---
title: Bejelentkezés az Azure PowerShell-lel
description: Hogyan lehet bejelentkezni az Azure PowerShellbe felhasználóként, szolgáltatásnévként vagy az Azure-erőforrások felügyelt identitásaival.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/29/2018
ms.openlocfilehash: 8b085720aeabe26c1293ece193e050b31f99a693
ms.sourcegitcommit: ae81b08a45d8729fc8d40156422e3eb2e94de8c7
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/27/2018
ms.locfileid: "53786679"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="5b1f5-103">Bejelentkezés az Azure PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="5b1f5-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="5b1f5-104">Az Azure PowerShell többféle hitelesítési módszert támogat.</span><span class="sxs-lookup"><span data-stu-id="5b1f5-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="5b1f5-105">Első lépésként a legegyszerűbb módszer, ha interaktívan bejelentkezik a parancssoron.</span><span class="sxs-lookup"><span data-stu-id="5b1f5-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="5b1f5-106">Interaktív bejelentkezés</span><span class="sxs-lookup"><span data-stu-id="5b1f5-106">Sign in interactively</span></span>

<span data-ttu-id="5b1f5-107">Az interaktív bejelentkezéshez használja a [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5b1f5-107">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="5b1f5-108">A futtatáskor ez a parancsmag jogkivonatsztringet jelenít meg.</span><span class="sxs-lookup"><span data-stu-id="5b1f5-108">When run, this cmdlet will present a token string.</span></span> <span data-ttu-id="5b1f5-109">A bejelentkezéshez másolja ezt a sztringet a https://microsoft.com/devicelogin címbe egy böngészőben.</span><span class="sxs-lookup"><span data-stu-id="5b1f5-109">To log in, copy this string and paste it into https://microsoft.com/devicelogin in a browser.</span></span> <span data-ttu-id="5b1f5-110">A rendszer ekkor hitelesíti a PowerShell-munkamenetet az Azure-hoz való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="5b1f5-110">Your PowerShell session will then be authenticated to connect to Azure.</span></span> <span data-ttu-id="5b1f5-111">A hitelesítés csak az aktuális PowerShell-munkamenetre vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="5b1f5-111">This authentication lasts for the current PowerShell session.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="5b1f5-112">A hitelesítő adatok megoszlanak több PowerShell-munkamenet között, ha be van jelentkezve.</span><span class="sxs-lookup"><span data-stu-id="5b1f5-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="5b1f5-113">További információért tekintse meg az [Állandó hitelesítő adatokat](context-persistence.md) ismertető cikket.</span><span class="sxs-lookup"><span data-stu-id="5b1f5-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="5b1f5-114">Bejelentkezés szolgáltatásnévvel</span><span class="sxs-lookup"><span data-stu-id="5b1f5-114">Sign in with a service principal</span></span>

<span data-ttu-id="5b1f5-115">A szolgáltatásnevek nem interaktív Azure-fiókok.</span><span class="sxs-lookup"><span data-stu-id="5b1f5-115">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="5b1f5-116">Más felhasználói fiókokhoz hasonlóan az ezekhez tartozó engedélyek kezelését is az Azure Active Directory végzi.</span><span class="sxs-lookup"><span data-stu-id="5b1f5-116">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="5b1f5-117">Az automatizálási szkriptek biztonságát úgy garantálhatjuk, ha a szolgáltatásnevek számára csak a szükséges engedélyeket adjuk meg.</span><span class="sxs-lookup"><span data-stu-id="5b1f5-117">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="5b1f5-118">Ha meg szeretné tudni, hogyan hozhat létre szolgáltatásnevet az Azure PowerShell-lel való használatra, tekintse meg az [Azure-beli szolgáltatásnév Azure PowerShell használatával történő létrehozásával](create-azure-service-principal-azureps.md) kapcsolatos szakaszt.</span><span class="sxs-lookup"><span data-stu-id="5b1f5-118">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="5b1f5-119">Szolgáltatásnévvel való bejelentkezéshez használja a `-ServicePrincipal` argumentumot a `Connect-AzAccount` parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="5b1f5-119">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="5b1f5-120">Szüksége lesz a szolgáltatásnév alkalmazásazonosítójára, a bejelentkezési hitelesítő adatokra, és a szolgáltatásnévhez tartozó bérlőazonosítóra.</span><span class="sxs-lookup"><span data-stu-id="5b1f5-120">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="5b1f5-121">Annak érdekében, hogy a szolgáltatásnév hitelesítő adatait a megfelelő objektumként kapja meg, használja a [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5b1f5-121">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="5b1f5-122">Ez a parancsmag a szolgáltatásnév felhasználói azonosítójának és jelszavának megadását kéri.</span><span class="sxs-lookup"><span data-stu-id="5b1f5-122">This cmdlet will present a prompt for the service principal user ID and password.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a><span data-ttu-id="5b1f5-123">Bejelentkezés Azure-beli Managed Service Identityvel</span><span class="sxs-lookup"><span data-stu-id="5b1f5-123">Sign in using an Azure Managed Service Identity</span></span>

<span data-ttu-id="5b1f5-124">A Azure-erőforrások felügyelt identitása az Azure Active Directory egy funkciója.</span><span class="sxs-lookup"><span data-stu-id="5b1f5-124">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="5b1f5-125">A felügyelt identitás szolgáltatásnevével bejelentkezhet, és beszerezhet egy csak alkalmazásra érvényes hozzáférési jogkivonatot az egyéb erőforrások eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="5b1f5-125">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="5b1f5-126">A felügyelt identitások csak az Azure-felhőben futó virtuális gépeken érhetők el.</span><span class="sxs-lookup"><span data-stu-id="5b1f5-126">Managed identities are only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="5b1f5-127">Az Azure-erőforrások felügyelt identitásairól [a hozzáférési jogkivonatok egy Azure-beli virtuális gép Azure-erőforrásainak felügyelt identitásaival való beszerzését ismertető részben](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token) talál.</span><span class="sxs-lookup"><span data-stu-id="5b1f5-127">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="5b1f5-128">Bejelentkezés felhőszolgáltatóként (CSP)</span><span class="sxs-lookup"><span data-stu-id="5b1f5-128">Sign in as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="5b1f5-129">A [felhőszolgáltatóként (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) történő bejelentkezéshez `-TenantId` használatára van szükség.</span><span class="sxs-lookup"><span data-stu-id="5b1f5-129">A [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) sign-in requires the use of `-TenantId`.</span></span> <span data-ttu-id="5b1f5-130">Ez a paraméter általában bérlőazonosítóként vagy tartománynévként is megadható,</span><span class="sxs-lookup"><span data-stu-id="5b1f5-130">Normally, this parameter can be provided as either a tenant ID or a domain name.</span></span> <span data-ttu-id="5b1f5-131">a felhőszolgáltatóként történő bejelentkezéshez azonban **bérlőazonosítót** kell megadni.</span><span class="sxs-lookup"><span data-stu-id="5b1f5-131">However, for CSP sign-in, it must be provided a **tenant ID**.</span></span>

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="5b1f5-132">Bejelentkezés egy másik felhőbe</span><span class="sxs-lookup"><span data-stu-id="5b1f5-132">Sign in to another Cloud</span></span>

<span data-ttu-id="5b1f5-133">Az Azure Cloud Services által biztosított környezetek megfelelnek a regionális adatkezelési előírásoknak.</span><span class="sxs-lookup"><span data-stu-id="5b1f5-133">Azure cloud services offer environments compliant with regional data-handling regulations.</span></span>
<span data-ttu-id="5b1f5-134">Regionális felhőszolgáltatásban található fiókok esetében a környezetet az `-Environment` argumentummal való bejelentkezéskor kell beállítania.</span><span class="sxs-lookup"><span data-stu-id="5b1f5-134">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="5b1f5-135">Például ha a fiók a kínai felhőszolgáltatásban található:</span><span class="sxs-lookup"><span data-stu-id="5b1f5-135">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="5b1f5-136">Az alábbi paranccsal olvashatja be a rendelkezésre álló környezetek listáját:</span><span class="sxs-lookup"><span data-stu-id="5b1f5-136">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="5b1f5-137">További információ az Azure szerepkör-alapú hozzáférés kezeléséről</span><span class="sxs-lookup"><span data-stu-id="5b1f5-137">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="5b1f5-138">Az Azure-beli hitelesítésről és előfizetés-kezelésről a [fiókok, előfizetések és rendszergazdai szerepkörök kezeléséről](/azure/active-directory/role-based-access-control-configure) szóló cikkben talál további információt.</span><span class="sxs-lookup"><span data-stu-id="5b1f5-138">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="5b1f5-139">Azure PowerShell-parancsmagok a szerepkörök kezeléséhez:</span><span class="sxs-lookup"><span data-stu-id="5b1f5-139">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="5b1f5-140">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5b1f5-140">Get-AzRoleAssignment</span></span>](/powershell/module/az.Resources/Get-azRoleAssignment)
* [<span data-ttu-id="5b1f5-141">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="5b1f5-141">Get-AzRoleDefinition</span></span>](/powershell/module/az.Resources/Get-azRoleDefinition)
* [<span data-ttu-id="5b1f5-142">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5b1f5-142">New-AzRoleAssignment</span></span>](/powershell/module/az.Resources/New-azRoleAssignment)
* [<span data-ttu-id="5b1f5-143">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="5b1f5-143">New-AzRoleDefinition</span></span>](/powershell/module/az.Resources/New-azRoleDefinition)
* [<span data-ttu-id="5b1f5-144">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5b1f5-144">Remove-AzRoleAssignment</span></span>](/powershell/module/az.Resources/Remove-azRoleAssignment)
* [<span data-ttu-id="5b1f5-145">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="5b1f5-145">Remove-AzRoleDefinition</span></span>](/powershell/module/az.Resources/Remove-azRoleDefinition)
* [<span data-ttu-id="5b1f5-146">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="5b1f5-146">Set-AzRoleDefinition</span></span>](/powershell/module/az.Resources/Set-azRoleDefinition)
