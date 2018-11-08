---
title: Bejelentkezés az Azure PowerShell-lel
description: Hogyan lehet bejelentkezni az Azure PowerShellbe felhasználóként, szolgáltatásnévként vagy az Azure-erőforrások felügyelt identitásaival.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: c19d9ade0f69f4af9f14c68ad22b327c27c8ccfd
ms.sourcegitcommit: 1f699b72bf544d92459da9d888cc0091f9415b65
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/06/2018
ms.locfileid: "50972162"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="460cc-103">Bejelentkezés az Azure PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="460cc-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="460cc-104">Az Azure PowerShell többféle hitelesítési módszert támogat.</span><span class="sxs-lookup"><span data-stu-id="460cc-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="460cc-105">Első lépésként a legegyszerűbb módszer, ha interaktívan bejelentkezik a parancssoron.</span><span class="sxs-lookup"><span data-stu-id="460cc-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="460cc-106">Interaktív bejelentkezés</span><span class="sxs-lookup"><span data-stu-id="460cc-106">Sign in interactively</span></span>

<span data-ttu-id="460cc-107">Az interaktív bejelentkezéshez használja a [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="460cc-107">To sign in interactively, use the [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet.</span></span>

```azurepowershell
Connect-AzureRmAccount
```

<span data-ttu-id="460cc-108">A parancsmag futtatásakor megnyílik egy párbeszédablak, amely az Azure-fiókhoz tartozó e-mail-cím és jelszó megadását kéri.</span><span class="sxs-lookup"><span data-stu-id="460cc-108">When run, this cmdlet will bring up a dialog box prompting you for your email address and password associated with your Azure account.</span></span> <span data-ttu-id="460cc-109">A hitelesítés csak az aktuális PowerShell-munkamenetre vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="460cc-109">This authentication lasts for the current PowerShell session.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="460cc-110">Az Azure PowerShell 6.3.0-s verziójától kezdve a hitelesítő adatok megoszlanak több PowerShell-munkamenet között, ha be van jelentkezve a Windowsba.</span><span class="sxs-lookup"><span data-stu-id="460cc-110">As of Azure PowerShell 6.3.0, your credentials are shared among multiple PowerShell sessions as long as you remain signed in to Windows.</span></span> <span data-ttu-id="460cc-111">További információért tekintse meg az [Állandó hitelesítő adatokat](context-persistence.md) ismertető cikket.</span><span class="sxs-lookup"><span data-stu-id="460cc-111">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="460cc-112">Bejelentkezés szolgáltatásnévvel</span><span class="sxs-lookup"><span data-stu-id="460cc-112">Sign in with a service principal</span></span>

<span data-ttu-id="460cc-113">A szolgáltatásnevek nem interaktív Azure-fiókok.</span><span class="sxs-lookup"><span data-stu-id="460cc-113">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="460cc-114">Más felhasználói fiókokhoz hasonlóan az ezekhez tartozó engedélyek kezelését is az Azure Active Directory végzi.</span><span class="sxs-lookup"><span data-stu-id="460cc-114">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="460cc-115">Az automatizálási szkriptek biztonságát úgy garantálhatjuk, ha a szolgáltatásnevek számára csak a szükséges engedélyeket adjuk meg.</span><span class="sxs-lookup"><span data-stu-id="460cc-115">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="460cc-116">Ha meg szeretné tudni, hogyan hozhat létre szolgáltatásnevet az Azure PowerShell-lel való használatra, tekintse meg az [Azure-beli szolgáltatásnév Azure PowerShell használatával történő létrehozásával](create-azure-service-principal-azureps.md) kapcsolatos szakaszt.</span><span class="sxs-lookup"><span data-stu-id="460cc-116">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="460cc-117">Szolgáltatásnévvel való bejelentkezéshez használja a `-ServicePrincipal` argumentumot a `Connect-AzureRmAccount` parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="460cc-117">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzureRmAccount` cmdlet.</span></span> <span data-ttu-id="460cc-118">Szüksége lesz a szolgáltatásnév alkalmazásazonosítójára, a bejelentkezési hitelesítő adatokra, és a szolgáltatásnévhez tartozó bérlőazonosítóra.</span><span class="sxs-lookup"><span data-stu-id="460cc-118">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="460cc-119">Annak érdekében, hogy a szolgáltatásnév hitelesítő adatait a megfelelő objektumként kapja meg, használja a [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="460cc-119">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="460cc-120">Ez a parancsmag megjelenít egy párbeszédpanelt, amelyben megadható a szolgáltatásnév felhasználói azonosítója és jelszava.</span><span class="sxs-lookup"><span data-stu-id="460cc-120">This cmdlet will display a dialog box to enter the service principal user ID and password into.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a><span data-ttu-id="460cc-121">Bejelentkezés Azure-beli Managed Service Identityvel</span><span class="sxs-lookup"><span data-stu-id="460cc-121">Sign in using an Azure Managed Service Identity</span></span>

<span data-ttu-id="460cc-122">A Azure-erőforrások felügyelt identitása az Azure Active Directory egy funkciója.</span><span class="sxs-lookup"><span data-stu-id="460cc-122">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="460cc-123">A felügyelt identitás szolgáltatásnevével bejelentkezhet, és beszerezhet egy csak alkalmazásra érvényes hozzáférési jogkivonatot az egyéb erőforrások eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="460cc-123">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="460cc-124">A felügyelt identitások csak az Azure-felhőben futó virtuális gépeken érhetők el.</span><span class="sxs-lookup"><span data-stu-id="460cc-124">Managed identities are only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="460cc-125">Az Azure-erőforrások felügyelt identitásairól [a hozzáférési jogkivonatok egy Azure-beli virtuális gép Azure-erőforrásainak felügyelt identitásaival való beszerzését ismertető részben](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token) talál.</span><span class="sxs-lookup"><span data-stu-id="460cc-125">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="460cc-126">Bejelentkezés felhőszolgáltatóként (CSP)</span><span class="sxs-lookup"><span data-stu-id="460cc-126">Sign in as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="460cc-127">A [felhőszolgáltatóként (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) történő bejelentkezéshez `-TenantId` használatára van szükség.</span><span class="sxs-lookup"><span data-stu-id="460cc-127">A [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) sign-in requires the use of `-TenantId`.</span></span> <span data-ttu-id="460cc-128">Ez a paraméter általában bérlőazonosítóként vagy tartománynévként is megadható,</span><span class="sxs-lookup"><span data-stu-id="460cc-128">Normally, this parameter can be provided as either a tenant ID or a domain name.</span></span> <span data-ttu-id="460cc-129">a felhőszolgáltatóként történő bejelentkezéshez azonban **bérlőazonosítót** kell megadni.</span><span class="sxs-lookup"><span data-stu-id="460cc-129">However, for CSP sign-in, it must be provided a **tenant ID**.</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="460cc-130">Bejelentkezés egy másik felhőbe</span><span class="sxs-lookup"><span data-stu-id="460cc-130">Sign in to another Cloud</span></span>

<span data-ttu-id="460cc-131">Az Azure Cloud Services által biztosított környezetek megfelelnek a regionális adatkezelési előírásoknak.</span><span class="sxs-lookup"><span data-stu-id="460cc-131">Azure cloud services offer environments compliant with regional data-handling regulations.</span></span>
<span data-ttu-id="460cc-132">Regionális felhőszolgáltatásban található fiókok esetében a környezetet az `-Environment` argumentummal való bejelentkezéskor kell beállítania.</span><span class="sxs-lookup"><span data-stu-id="460cc-132">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="460cc-133">Például ha a fiók a kínai felhőszolgáltatásban található:</span><span class="sxs-lookup"><span data-stu-id="460cc-133">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

<span data-ttu-id="460cc-134">Az alábbi paranccsal olvashatja be a rendelkezésre álló környezetek listáját:</span><span class="sxs-lookup"><span data-stu-id="460cc-134">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="460cc-135">További információ az Azure szerepkör-alapú hozzáférés kezeléséről</span><span class="sxs-lookup"><span data-stu-id="460cc-135">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="460cc-136">Az Azure-beli hitelesítésről és előfizetés-kezelésről a [fiókok, előfizetések és rendszergazdai szerepkörök kezeléséről](/azure/active-directory/role-based-access-control-configure) szóló cikkben talál további információt.</span><span class="sxs-lookup"><span data-stu-id="460cc-136">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="460cc-137">Azure PowerShell-parancsmagok a szerepkörök kezeléséhez:</span><span class="sxs-lookup"><span data-stu-id="460cc-137">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="460cc-138">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="460cc-138">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="460cc-139">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="460cc-139">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="460cc-140">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="460cc-140">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="460cc-141">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="460cc-141">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="460cc-142">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="460cc-142">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="460cc-143">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="460cc-143">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="460cc-144">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="460cc-144">Set-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Set-AzureRmRoleDefinition)
