---
title: Bejelentkezés az Azure PowerShell-lel
description: Hogyan lehet bejelentkezni az Azure PowerShellbe felhasználóként, szolgáltatásnévként vagy az Azure-erőforrások felügyelt identitásaival.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 9a93145f2abeea466a739775ca8ae7e337e78166
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/05/2018
ms.locfileid: "52826884"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="4dd42-103">Bejelentkezés az Azure PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="4dd42-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="4dd42-104">Az Azure PowerShell többféle hitelesítési módszert támogat.</span><span class="sxs-lookup"><span data-stu-id="4dd42-104">Azure PowerShell supports multiple authentication methods.</span></span> <span data-ttu-id="4dd42-105">Első lépésként a legegyszerűbb módszer, ha interaktívan bejelentkezik a parancssoron.</span><span class="sxs-lookup"><span data-stu-id="4dd42-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="4dd42-106">Interaktív bejelentkezés</span><span class="sxs-lookup"><span data-stu-id="4dd42-106">Sign in interactively</span></span>

<span data-ttu-id="4dd42-107">Az interaktív bejelentkezéshez használja a [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4dd42-107">To sign in interactively, use the [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount
```

<span data-ttu-id="4dd42-108">A parancsmag futtatásakor megnyílik egy párbeszédablak, amely az Azure-fiókhoz tartozó e-mail-cím és jelszó megadását kéri.</span><span class="sxs-lookup"><span data-stu-id="4dd42-108">When run, this cmdlet will bring up a dialog box prompting you for your email address and password associated with your Azure account.</span></span> <span data-ttu-id="4dd42-109">A hitelesítéskor a rendszer menti ezt az információt az aktuális PowerShell-munkamenethez, a párbeszédablak bezáródik, és Ön hozzáférhet az összes Azure PowerShell-parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="4dd42-109">When you authenticate, that information is saved for the current PowerShell session, the dialog is closed, and you have access to all of the Azure PowerShell cmdlets.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4dd42-110">Ez a bejelentkezés _csak_ az aktuális PowerShell-munkamenetre vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="4dd42-110">This sign in is for the current PowerShell session _only_.</span></span> <span data-ttu-id="4dd42-111">A több munkamenetre megőrzött hitelesítésről az [állandó hitelesítő adatokkal](context-persistence.md) kapcsolatos cikkből tájékozódhat.</span><span class="sxs-lookup"><span data-stu-id="4dd42-111">To persist authentication across multiple sessions, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="4dd42-112">Bejelentkezés szolgáltatásnévvel</span><span class="sxs-lookup"><span data-stu-id="4dd42-112">Sign in with a service principal</span></span>

<span data-ttu-id="4dd42-113">A szolgáltatásnevek használatával nem interaktív fiókokat hozhat létre az erőforrások kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="4dd42-113">Service principals provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="4dd42-114">A szolgáltatásnevek olyan felhasználói fiókokhoz hasonlóak, amelyekre szabályokat alkalmazhat az Azure Active Directory használatával.</span><span class="sxs-lookup"><span data-stu-id="4dd42-114">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span> <span data-ttu-id="4dd42-115">Az automatizálási szkriptek biztonságának növelése érdekében csak a minimálisan szükséges engedélyeket adja meg a szolgáltatásneveknek.</span><span class="sxs-lookup"><span data-stu-id="4dd42-115">By granting the minimum permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

<span data-ttu-id="4dd42-116">Ha létre kíván hozni szolgáltatásnevet az Azure PowerShell-lel való használatra, tekintse meg az [Azure-beli szolgáltatásnév Azure PowerShell használatával történő létrehozásával](create-azure-service-principal-azureps.md) kapcsolatos szakaszt.</span><span class="sxs-lookup"><span data-stu-id="4dd42-116">If you need to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="4dd42-117">Szolgáltatásnévvel való bejelentkezéshez használja a `-ServicePrincipal` argumentumot a `Connect-AzureRmAccount` parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="4dd42-117">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzureRmAccount` cmdlet.</span></span> <span data-ttu-id="4dd42-118">Szüksége lesz a szolgáltatásnév alkalmazásazonosítójára, a bejelentkezési hitelesítő adatokra, és a szolgáltatásnévhez tartozó bérlőazonosítóra.</span><span class="sxs-lookup"><span data-stu-id="4dd42-118">You will also need the service princpal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="4dd42-119">Annak érdekében, hogy a szolgáltatásnév hitelesítő adatait a megfelelő objektumként kapja meg, használja a [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4dd42-119">In order to get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="4dd42-120">Ez a parancsmag megjelenít egy párbeszédpanelt, amelyben megadható a szolgáltatásnév felhasználói azonosítója és jelszava.</span><span class="sxs-lookup"><span data-stu-id="4dd42-120">This cmdlet will display a dialog box to enter the service principal user ID and password into.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-managed-identities-for-azure-resources"></a><span data-ttu-id="4dd42-121">Bejelentkezés az Azure-erőforrások felügyelt identitásaival</span><span class="sxs-lookup"><span data-stu-id="4dd42-121">Sign in using managed identities for Azure resources</span></span>

<span data-ttu-id="4dd42-122">A Azure-erőforrások felügyelt identitása az Azure Active Directory egy funkciója.</span><span class="sxs-lookup"><span data-stu-id="4dd42-122">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="4dd42-123">A felügyelt identitás szolgáltatásnevével bejelentkezhet, és beszerezhet egy csak alkalmazásra érvényes hozzáférési jogkivonatot az egyéb erőforrások eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="4dd42-123">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="4dd42-124">A felügyelt identitások csak az Azure-felhőben futó virtuális gépeken érhetők el.</span><span class="sxs-lookup"><span data-stu-id="4dd42-124">Managed identities are only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="4dd42-125">Az Azure-erőforrások felügyelt identitásairól [a hozzáférési jogkivonatok egy Azure-beli virtuális gép Azure-erőforrásainak felügyelt identitásaival való beszerzését ismertető részben](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token) talál.</span><span class="sxs-lookup"><span data-stu-id="4dd42-125">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="4dd42-126">Bejelentkezés egy másik felhőbe</span><span class="sxs-lookup"><span data-stu-id="4dd42-126">Sign in to another Cloud</span></span>

<span data-ttu-id="4dd42-127">Az Azure Cloud Services különböző környezeteket biztosít, amelyek igazodnak az egyes régiók adatkezelési szabályzataihoz.</span><span class="sxs-lookup"><span data-stu-id="4dd42-127">Azure cloud services provide different environments that adhere to the data-handling regulations of various regions.</span></span> <span data-ttu-id="4dd42-128">Ha az Azure-fiókja az egyik ilyen régióhoz társított felhőben található, bejelentkezéskor meg kell adnia a környezetet.</span><span class="sxs-lookup"><span data-stu-id="4dd42-128">If your Azure account is in a cloud associated with one of these regions, you need to specify the environment when you sign in.</span></span> <span data-ttu-id="4dd42-129">Például ha a fiók a kínai felhőszolgáltatásban található, a regisztrálás az alábbi paranccsal történik:</span><span class="sxs-lookup"><span data-stu-id="4dd42-129">For example, if you account is in the China cloud you sign on using the following command:</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

<span data-ttu-id="4dd42-130">Az alábbi paranccsal olvashatja be a rendelkezésre álló környezetek listáját:</span><span class="sxs-lookup"><span data-stu-id="4dd42-130">Use the following command to get a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="4dd42-131">További információ az Azure szerepkör-alapú hozzáférés kezeléséről</span><span class="sxs-lookup"><span data-stu-id="4dd42-131">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="4dd42-132">Az Azure-beli hitelesítésről és előfizetés-kezelésről a [fiókok, előfizetések és rendszergazdai szerepkörök kezeléséről](/azure/active-directory/role-based-access-control-configure) szóló cikkben talál további információt.</span><span class="sxs-lookup"><span data-stu-id="4dd42-132">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="4dd42-133">Azure PowerShell-parancsmagok a szerepkörök kezeléséhez:</span><span class="sxs-lookup"><span data-stu-id="4dd42-133">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="4dd42-134">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="4dd42-134">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="4dd42-135">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="4dd42-135">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="4dd42-136">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="4dd42-136">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="4dd42-137">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="4dd42-137">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="4dd42-138">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="4dd42-138">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="4dd42-139">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="4dd42-139">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="4dd42-140">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="4dd42-140">Set-AzureRmRoleDefinition</span></span>](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
