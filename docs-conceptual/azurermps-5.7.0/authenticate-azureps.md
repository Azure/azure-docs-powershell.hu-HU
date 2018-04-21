---
title: Bejelentkezés az Azure PowerShell-lel
description: Bejelentkezés az Azure PowerShell-lel
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: f07dee0eed106e39879d58ae06ff08b787faa531
ms.sourcegitcommit: 5f0013981fcea1d689649b9a2b2ffe84ae842e56
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2018
---
# <a name="log-in-with-azure-powershell"></a><span data-ttu-id="cfb34-103">Bejelentkezés az Azure PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="cfb34-103">Log in with Azure PowerShell</span></span>

<span data-ttu-id="cfb34-104">Az Azure PowerShell többféle bejelentkezési módszert támogat.</span><span class="sxs-lookup"><span data-stu-id="cfb34-104">Azure PowerShell supports multiple login methods.</span></span> <span data-ttu-id="cfb34-105">Első lépésként a legegyszerűbb módszer, ha interaktívan bejelentkezik a parancssoron.</span><span class="sxs-lookup"><span data-stu-id="cfb34-105">The simplest way to get started is to log in interactively at the command line.</span></span>

## <a name="interactive-log-in"></a><span data-ttu-id="cfb34-106">Interaktív bejelentkezés</span><span class="sxs-lookup"><span data-stu-id="cfb34-106">Interactive log in</span></span>

1. <span data-ttu-id="cfb34-107">Gépelje be: `Connect-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="cfb34-107">Type `Connect-AzureRmAccount`.</span></span> <span data-ttu-id="cfb34-108">Egy párbeszédpanel jelenik meg, amelyen meg kell adnia Azure-beli hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="cfb34-108">You will get dialog box asking for your Azure credentials.</span></span>

2. <span data-ttu-id="cfb34-109">Írja be a fiókjához tartozó e-mail-címet és jelszót.</span><span class="sxs-lookup"><span data-stu-id="cfb34-109">Type the email address and password associated with your account.</span></span> <span data-ttu-id="cfb34-110">Az Azure hitelesíti és menti a hitelesítő adatokat, majd bezárja az ablakot.</span><span class="sxs-lookup"><span data-stu-id="cfb34-110">Azure authenticates and saves the credential information, and then closes the window.</span></span>

## <a name="log-in-with-a-service-principal"></a><span data-ttu-id="cfb34-111">Bejelentkezés szolgáltatásnévvel</span><span class="sxs-lookup"><span data-stu-id="cfb34-111">Log in with a service principal</span></span>

<span data-ttu-id="cfb34-112">A szolgáltatásnevek használatával nem interaktív fiókokat hozhat létre az erőforrások kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="cfb34-112">Service principals provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="cfb34-113">A szolgáltatásnevek olyan felhasználói fiókokhoz hasonlóak, amelyekre szabályokat alkalmazhat az Azure Active Directory használatával.</span><span class="sxs-lookup"><span data-stu-id="cfb34-113">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span> <span data-ttu-id="cfb34-114">Az automatizálási szkriptek biztonságának növelése érdekében csak a minimálisan szükséges engedélyeket adja meg a szolgáltatásneveknek.</span><span class="sxs-lookup"><span data-stu-id="cfb34-114">By granting the minimum permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

1. <span data-ttu-id="cfb34-115">Ha még nem rendelkezik szolgáltatásnévvel, akkor [hozzon létre egyet](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="cfb34-115">If you don't already have a service principal, [create one](create-azure-service-principal-azureps.md).</span></span>

2. <span data-ttu-id="cfb34-116">Jelentkezzen be a szolgáltatásnévvel.</span><span class="sxs-lookup"><span data-stu-id="cfb34-116">Log in with the service principal.</span></span>

    ```powershell
    Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
    ```

    <span data-ttu-id="cfb34-117">A bérlőazonosító megismeréséhez jelentkezzen be interaktívan, és kérje le az előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="cfb34-117">To get your TenantId, log in interactively and then get the TenantId from your subscription.</span></span>

    ```powershell
    Get-AzureRmSubscription
    ```

    ```
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Production Subscription
    CurrentStorageAccount :
    ```

### <a name="log-in-using-an-azure-vm-managed-service-identity"></a><span data-ttu-id="cfb34-118">Bejelentkezés Azure-beli virtuális gépek felügyeltszolgáltatás-identitásaival</span><span class="sxs-lookup"><span data-stu-id="cfb34-118">Log in using an Azure VM Managed Service Identity</span></span>

<span data-ttu-id="cfb34-119">A Felügyeltszolgáltatás-identitás (MSI) az Azure Active Directory előzetes verzióként elérhető funkciója.</span><span class="sxs-lookup"><span data-stu-id="cfb34-119">Managed Service Identity (MSI) is a preview feature of Azure Active Directory.</span></span> <span data-ttu-id="cfb34-120">Az MSI szolgáltatásnevekkel bejelentkezhet, és beszerezhet egy csak alkalmazásra érvényes hozzáférési jogkivonatot az egyéb erőforrások eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="cfb34-120">You can use an MSI service principal for sign-in, and acquire an app-only access token to access other resources.</span></span>

<span data-ttu-id="cfb34-121">További információ az MSI-ről: [Az Azure-beli virtuális gépek felügyeltszolgáltatás-identitásának (MSI) használata bejelentkezéshez és jogkivonat beszerzéséhez](/azure/active-directory/msi-how-to-get-access-token-using-msi).</span><span class="sxs-lookup"><span data-stu-id="cfb34-121">For more information about MSI, see [How to use an Azure VM Managed Service Identity (MSI) for sign-in and token acquisition](/azure/active-directory/msi-how-to-get-access-token-using-msi).</span></span>

## <a name="log-in-to-another-cloud"></a><span data-ttu-id="cfb34-122">Bejelentkezés egy másik felhőbe</span><span class="sxs-lookup"><span data-stu-id="cfb34-122">Log in to another Cloud</span></span>

<span data-ttu-id="cfb34-123">Az Azure-beli felhőszolgáltatások különböző környezeteket biztosítanak, amelyek igazodnak az egyes kormányzatok adatkezelési szabályzataihoz.</span><span class="sxs-lookup"><span data-stu-id="cfb34-123">Azure cloud services provide different environments that adhere to the data-handling regulations of various governments.</span></span> <span data-ttu-id="cfb34-124">Ha az Azure-fiók valamelyik kormányzati felhőben található, bejelentkezéskor meg kell adnia a környezetet.</span><span class="sxs-lookup"><span data-stu-id="cfb34-124">If your Azure account is in one the government clouds, you need to specify the environment when you sign in.</span></span> <span data-ttu-id="cfb34-125">Például ha a fiók a kínai felhőszolgáltatásban található, a regisztrálás az alábbi paranccsal történik:</span><span class="sxs-lookup"><span data-stu-id="cfb34-125">For example, if you account is in the China cloud you sign on using the following command:</span></span>

```powershell
Connect-AzureRmAccount -Environment AzureChinaCloud
```

<span data-ttu-id="cfb34-126">Az alábbi paranccsal olvashatja be a rendelkezésre álló környezetek listáját:</span><span class="sxs-lookup"><span data-stu-id="cfb34-126">Use the following command to get a list of available environments:</span></span>

```powershell
Get-AzureRmEnvironment | Select-Object Name
```

```
Name
----
AzureCloud
AzureChinaCloud
AzureUSGovernment
AzureGermanCloud
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="cfb34-127">További információ az Azure szerepkör-alapú hozzáférés kezeléséről</span><span class="sxs-lookup"><span data-stu-id="cfb34-127">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="cfb34-128">Az Azure-beli hitelesítésről és előfizetés-kezelésről a [fiókok, előfizetések és rendszergazdai szerepkörök kezeléséről](/azure/active-directory/role-based-access-control-configure) szóló cikkben talál további információt.</span><span class="sxs-lookup"><span data-stu-id="cfb34-128">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="cfb34-129">Azure PowerShell-parancsmagok a szerepkörök kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="cfb34-129">Azure PowerShell cmdlets for role management</span></span>

* [<span data-ttu-id="cfb34-130">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="cfb34-130">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="cfb34-131">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="cfb34-131">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="cfb34-132">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="cfb34-132">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="cfb34-133">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="cfb34-133">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="cfb34-134">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="cfb34-134">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="cfb34-135">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="cfb34-135">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="cfb34-136">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="cfb34-136">Set-AzureRmRoleDefinition</span></span>](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
