---
title: Bejelentkezés az Azure PowerShell-lel
description: Hogyan lehet bejelentkezni az Azure PowerShellbe felhasználóként, szolgáltatásnévként vagy MSI-ként.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 20194ac2282d602ba61bf130791edac9f4ffae6c
ms.sourcegitcommit: afae9f2f091b21ed07d5aec1c249cf859a8b89a4
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/09/2018
ms.locfileid: "39653865"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="56917-103">Bejelentkezés az Azure PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="56917-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="56917-104">Az Azure PowerShell többféle hitelesítési módszert támogat.</span><span class="sxs-lookup"><span data-stu-id="56917-104">Azure PowerShell supports multiple authentication methods.</span></span> <span data-ttu-id="56917-105">Első lépésként a legegyszerűbb módszer, ha interaktívan bejelentkezik a parancssoron.</span><span class="sxs-lookup"><span data-stu-id="56917-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="56917-106">Interaktív bejelentkezés</span><span class="sxs-lookup"><span data-stu-id="56917-106">Sign in interactively</span></span>

<span data-ttu-id="56917-107">Az interaktív bejelentkezéshez használja a [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="56917-107">To sign in interactively, use the [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet.</span></span>

```azurepowershell
Connect-AzureRmAccount
```

<span data-ttu-id="56917-108">A parancsmag futtatásakor megnyílik egy párbeszédablak, amely az Azure-fiókhoz tartozó e-mail-cím és jelszó megadását kéri.</span><span class="sxs-lookup"><span data-stu-id="56917-108">When run, this cmdlet will bring up a dialog box prompting you for your email address and password associated with your Azure account.</span></span> <span data-ttu-id="56917-109">A hitelesítéskor a rendszer menti ezt az információt az aktuális PowerShell-munkamenethez, a párbeszédablak bezáródik, és Ön hozzáférhet az összes Azure PowerShell-parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="56917-109">When you authenticate, that information is saved for the current PowerShell session, the dialog is closed, and you have access to all of the Azure PowerShell cmdlets.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="56917-110">Az Azure PowerShell 6.3.0-s verziójától kezdve a hitelesítő adatok megoszlanak több PowerShell-munkamenet között, ha be van jelentkezve a Windowsba.</span><span class="sxs-lookup"><span data-stu-id="56917-110">As of Azure PowerShell 6.3.0, your credentials are shared among multiple PowerShell sessions as long as you remain signed in to Windows.</span></span> <span data-ttu-id="56917-111">További információért tekintse meg az [Állandó hitelesítő adatokat](context-persistence.md) ismertető cikket.</span><span class="sxs-lookup"><span data-stu-id="56917-111">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="56917-112">Bejelentkezés szolgáltatásnévvel</span><span class="sxs-lookup"><span data-stu-id="56917-112">Sign in with a service principal</span></span>

<span data-ttu-id="56917-113">A szolgáltatásnevek használatával nem interaktív fiókokat hozhat létre az erőforrások kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="56917-113">Service principals provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="56917-114">A szolgáltatásnevek olyan felhasználói fiókokhoz hasonlóak, amelyekre szabályokat alkalmazhat az Azure Active Directory használatával.</span><span class="sxs-lookup"><span data-stu-id="56917-114">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span> <span data-ttu-id="56917-115">Az automatizálási szkriptek biztonságának növelése érdekében csak a minimálisan szükséges engedélyeket adja meg a szolgáltatásneveknek.</span><span class="sxs-lookup"><span data-stu-id="56917-115">By granting the minimum permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

<span data-ttu-id="56917-116">Ha létre kíván hozni szolgáltatásnevet az Azure PowerShell-lel való használatra, tekintse meg az [Azure-beli szolgáltatásnév Azure PowerShell használatával történő létrehozásával](create-azure-service-principal-azureps.md) kapcsolatos szakaszt.</span><span class="sxs-lookup"><span data-stu-id="56917-116">If you need to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="56917-117">Szolgáltatásnévvel való bejelentkezéshez használja a `-ServicePrincipal` argumentumot a `Connect-AzureRmAccount` parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="56917-117">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzureRmAccount` cmdlet.</span></span> <span data-ttu-id="56917-118">Szüksége lesz a szolgáltatásnév alkalmazásazonosítójára, a bejelentkezési hitelesítő adatokra, és a szolgáltatásnévhez tartozó bérlőazonosítóra.</span><span class="sxs-lookup"><span data-stu-id="56917-118">You will also need the service princpal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="56917-119">Annak érdekében, hogy a szolgáltatásnév hitelesítő adatait a megfelelő objektumként kapja meg, használja a [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="56917-119">In order to get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="56917-120">Ez a parancsmag megjelenít egy párbeszédpanelt, amelyben megadható a szolgáltatásnév felhasználói azonosítója és jelszava.</span><span class="sxs-lookup"><span data-stu-id="56917-120">This cmdlet will display a dialog box to enter the service principal user ID and password into.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-vm-managed-service-identity"></a><span data-ttu-id="56917-121">Bejelentkezés Azure-beli virtuális gépek Managed Service Identityjével</span><span class="sxs-lookup"><span data-stu-id="56917-121">Sign in using an Azure VM Managed Service Identity</span></span>

<span data-ttu-id="56917-122">A Felügyeltszolgáltatás-identitás (MSI) az Azure Active Directory előzetes verzióként elérhető funkciója.</span><span class="sxs-lookup"><span data-stu-id="56917-122">Managed Service Identity (MSI) is a preview feature of Azure Active Directory.</span></span> <span data-ttu-id="56917-123">Az MSI szolgáltatásnevekkel bejelentkezhet, és beszerezhet egy csak alkalmazásra érvényes hozzáférési jogkivonatot az egyéb erőforrások eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="56917-123">You can use an MSI service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="56917-124">Az MSI csak az Azure-felhőben futó virtuális gépeken érhető el.</span><span class="sxs-lookup"><span data-stu-id="56917-124">MSI is only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="56917-125">További információ az MSI-ről: [Az Azure-beli virtuális gépek felügyeltszolgáltatás-identitásának (MSI) használata bejelentkezéshez és jogkivonat beszerzéséhez](/azure/active-directory/msi-how-to-get-access-token-using-msi).</span><span class="sxs-lookup"><span data-stu-id="56917-125">For more information about MSI, see [How to use an Azure VM Managed Service Identity (MSI) for sign-in and token acquisition](/azure/active-directory/msi-how-to-get-access-token-using-msi).</span></span>

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="56917-126">Bejelentkezés egy másik felhőbe</span><span class="sxs-lookup"><span data-stu-id="56917-126">Sign in to another Cloud</span></span>

<span data-ttu-id="56917-127">Az Azure Cloud Services különböző környezeteket biztosít, amelyek igazodnak az egyes régiók adatkezelési szabályzataihoz.</span><span class="sxs-lookup"><span data-stu-id="56917-127">Azure cloud services provide different environments that adhere to the data-handling regulations of various regions.</span></span> <span data-ttu-id="56917-128">Ha az Azure-fiókja az egyik ilyen régióhoz társított felhőben található, bejelentkezéskor meg kell adnia a környezetet.</span><span class="sxs-lookup"><span data-stu-id="56917-128">If your Azure account is in a cloud associated with one of these regions, you need to specify the environment when you sign in.</span></span> <span data-ttu-id="56917-129">Például ha a fiók a kínai felhőszolgáltatásban található, a regisztrálás az alábbi paranccsal történik:</span><span class="sxs-lookup"><span data-stu-id="56917-129">For example, if you account is in the China cloud you sign on using the following command:</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

<span data-ttu-id="56917-130">Az alábbi paranccsal olvashatja be a rendelkezésre álló környezetek listáját:</span><span class="sxs-lookup"><span data-stu-id="56917-130">Use the following command to get a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="56917-131">További információ az Azure szerepkör-alapú hozzáférés kezeléséről</span><span class="sxs-lookup"><span data-stu-id="56917-131">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="56917-132">Az Azure-beli hitelesítésről és előfizetés-kezelésről a [fiókok, előfizetések és rendszergazdai szerepkörök kezeléséről](/azure/active-directory/role-based-access-control-configure) szóló cikkben talál további információt.</span><span class="sxs-lookup"><span data-stu-id="56917-132">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="56917-133">Azure PowerShell-parancsmagok a szerepkörök kezeléséhez:</span><span class="sxs-lookup"><span data-stu-id="56917-133">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="56917-134">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="56917-134">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="56917-135">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="56917-135">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="56917-136">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="56917-136">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="56917-137">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="56917-137">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="56917-138">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="56917-138">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="56917-139">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="56917-139">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="56917-140">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="56917-140">Set-AzureRmRoleDefinition</span></span>](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
