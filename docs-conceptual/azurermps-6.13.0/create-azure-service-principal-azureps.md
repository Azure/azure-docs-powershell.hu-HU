---
title: Azure-beli szolgáltatásnév létrehozása az Azure PowerShell használatával
description: Megtudhatja, hogyan hozhat létre szolgáltatásneveket appjához vagy szolgáltatásához az Azure PowerShell használatával.
keywords: Azure PowerShell, Azure Active Directory, Azure Active directory, AD, RBAC
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 38bb4345a9e4d2d9e450e74f99fb2c320c3ca4d8
ms.sourcegitcommit: bbd3f061cac3417ce588487c1ae4e0bc52c11d6a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/11/2019
ms.locfileid: "65534917"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="3e26c-104">Azure-beli szolgáltatásnév létrehozása az Azure PowerShell használatával</span><span class="sxs-lookup"><span data-stu-id="3e26c-104">Create an Azure service principal with Azure PowerShell</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="3e26c-105">Ha az appját vagy szolgáltatását az Azure PowerShell-lel szeretné kezelni, egy Azure Active Directory (AAD) szolgáltatásnév alatt, és nem a saját hitelesítő adataival érdemes futtatnia.</span><span class="sxs-lookup"><span data-stu-id="3e26c-105">If you plan to manage your app or service with Azure PowerShell, you should run it under an Azure Active Directory (AAD) service principal, rather than your own credentials.</span></span> <span data-ttu-id="3e26c-106">Ez a cikk végigvezeti a szolgáltatásnevek Azure PowerShell-lel való létrehozásának folyamatán.</span><span class="sxs-lookup"><span data-stu-id="3e26c-106">This article steps you through creating a security principal with Azure PowerShell.</span></span>

> [!NOTE]
> <span data-ttu-id="3e26c-107">Az Azure Portalon is létrehozhat szolgáltatásneveket.</span><span class="sxs-lookup"><span data-stu-id="3e26c-107">You can also create a service principal through the Azure portal.</span></span> <span data-ttu-id="3e26c-108">További részletekért lásd: [Active Directory-alkalmazás és -szolgáltatásnév létrehozása a portálon erőforrások eléréséhez](/azure/azure-resource-manager/resource-group-create-service-principal-portal).</span><span class="sxs-lookup"><span data-stu-id="3e26c-108">Read [Use portal to create Active Directory application and service principal that can access resources](/azure/azure-resource-manager/resource-group-create-service-principal-portal) for more details.</span></span>

## <a name="what-is-a-service-principal"></a><span data-ttu-id="3e26c-109">Mi az a szolgáltatásnév?</span><span class="sxs-lookup"><span data-stu-id="3e26c-109">What is a 'service principal'?</span></span>

<span data-ttu-id="3e26c-110">Az Azure-beli szolgáltatásnév egy biztonsági identitás, amellyel a felhasználó által létrehozott appok, szolgáltatások és automatizálási eszközök elérnek adott Azure-erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="3e26c-110">An Azure service principal is a security identity used by user-created apps, services, and automation tools to access specific Azure resources.</span></span> <span data-ttu-id="3e26c-111">Képzelje el úgy, mint egy „felhasználói identitást” (felhasználónév és jelszó vagy tanúsítvány) egy adott szerepkörrel és szigorúan szabályozott engedélyekkel.</span><span class="sxs-lookup"><span data-stu-id="3e26c-111">Think of it as a 'user identity' (username and password or certificate) with a specific role, and tightly controlled permissions.</span></span> <span data-ttu-id="3e26c-112">Az általános identitásoktól eltérően a szolgáltatásnév csak konkrét feladatok végrehajtására szolgál.</span><span class="sxs-lookup"><span data-stu-id="3e26c-112">A service principal should only need to do specific things, unlike a general user identity.</span></span> <span data-ttu-id="3e26c-113">Csak akkor javítja a biztonságot, ha csak a felügyeleti feladataihoz szükséges minimális engedélyeket osztja ki neki.</span><span class="sxs-lookup"><span data-stu-id="3e26c-113">It improves security if you only grant it the minimum permissions level needed to perform its management tasks.</span></span>

## <a name="verify-your-own-permission-level"></a><span data-ttu-id="3e26c-114">Saját jogosultsági szint ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="3e26c-114">Verify your own permission level</span></span>

<span data-ttu-id="3e26c-115">Először is megfelelő jogosultságokkal kell rendelkeznie mind az Azure Active Directoryban, mind az Azure-előfizetésén.</span><span class="sxs-lookup"><span data-stu-id="3e26c-115">First, you must have sufficient permissions in both your Azure Active Directory and your Azure subscription.</span></span> <span data-ttu-id="3e26c-116">Létre kell tudnia hozni alkalmazást az Active Directoryban, és ki kell tudnia osztani szerepköröket a szolgáltatásnévnek.</span><span class="sxs-lookup"><span data-stu-id="3e26c-116">You must be able to create an app in the Active Directory and assign a role to the service principal.</span></span>

<span data-ttu-id="3e26c-117">A legegyszerűbben a portálon ellenőrizheti, hogy rendelkezik-e megfelelő jogosultságokkal.</span><span class="sxs-lookup"><span data-stu-id="3e26c-117">The easiest way to check whether your account has the right permissions is through the portal.</span></span> <span data-ttu-id="3e26c-118">Lásd [Szükséges jogosultságok ellenőrzése a portálon](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span><span class="sxs-lookup"><span data-stu-id="3e26c-118">See [Check required permission in portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span></span>

## <a name="create-a-service-principal-for-your-app"></a><span data-ttu-id="3e26c-119">Szolgáltatásnév létrehozása az app számára</span><span class="sxs-lookup"><span data-stu-id="3e26c-119">Create a service principal for your app</span></span>

<span data-ttu-id="3e26c-120">Miután bejelentkezett Azure-fiókjába, létrehozhatja a szolgáltatásnevet.</span><span class="sxs-lookup"><span data-stu-id="3e26c-120">Once signed in to your Azure account, you can create the service principal.</span></span> <span data-ttu-id="3e26c-121">A következő módszerek egyikének rendelkezésre kell állnia az üzembe helyezett app azonosításához:</span><span class="sxs-lookup"><span data-stu-id="3e26c-121">You must have one of the following ways to identify your deployed app:</span></span>

* <span data-ttu-id="3e26c-122">Az üzembe helyezett app egyedi neve (a következő példákban ez a „MyDemoWebApp”), vagy</span><span class="sxs-lookup"><span data-stu-id="3e26c-122">The unique name of your deployed app, such as "MyDemoWebApp" in the following examples, or</span></span>
* <span data-ttu-id="3e26c-123">az alkalmazásazonosító, az üzembe helyezett alkalmazással, szolgáltatással vagy objektummal társított egyedi GUID</span><span class="sxs-lookup"><span data-stu-id="3e26c-123">the Application ID, the unique GUID associated with your deployed app, service, or object</span></span>

### <a name="get-information-about-your-application"></a><span data-ttu-id="3e26c-124">Az alkalmazás adatainak lekérése</span><span class="sxs-lookup"><span data-stu-id="3e26c-124">Get information about your application</span></span>

<span data-ttu-id="3e26c-125">Az alkalmazással kapcsolatos információkat a `Get-AzureRmADApplication` parancsmaggal kérheti le.</span><span class="sxs-lookup"><span data-stu-id="3e26c-125">The `Get-AzureRmADApplication` cmdlet can be used to get information about your application.</span></span>

```azurepowershell-interactive
Get-AzureRmADApplication -DisplayNameStartWith MyDemoWebApp
```

```output
DisplayName             : MyDemoWebApp
ObjectId                : 775f64cd-0ec8-4b9b-b69a-8b8946022d9f
IdentifierUris          : {http://MyDemoWebApp}
HomePage                : http://www.contoso.com
Type                    : Application
ApplicationId           : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
AvailableToOtherTenants : False
AppPermissions          :
ReplyUrls               : {}
```

### <a name="create-a-service-principal-for-your-application"></a><span data-ttu-id="3e26c-126">Szolgáltatásnév létrehozása az alkalmazás számára</span><span class="sxs-lookup"><span data-stu-id="3e26c-126">Create a service principal for your application</span></span>

<span data-ttu-id="3e26c-127">A szolgáltatásnév a `New-AzureRmADServicePrincipal` parancsmaggal hozható létre.</span><span class="sxs-lookup"><span data-stu-id="3e26c-127">The `New-AzureRmADServicePrincipal` cmdlet is used to create the service principal.</span></span>

```azurepowershell-interactive
$servicePrincipal = New-AzureRmADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4
```

```output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00c01aaa-1603-49fc-b6df-b78c4e5138b4, http://MyDemoWebApp}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
AdfsId                :
Type                  : ServicePrincipal
```

<span data-ttu-id="3e26c-128">Itt használhatja közvetlenül a $servicePrincipal.Secret tulajdonságot a Connect-AzureRmAccount parancsmaggal (lásd az alábbi, „Bejelentkezés a szolgáltatásnévvel” című részt) vagy átalakíthatja ezt a SecureString típusú sztringet egyszerű szöveges sztringgé későbbi használatra:</span><span class="sxs-lookup"><span data-stu-id="3e26c-128">From here, you can either directly use the $servicePrincipal.Secret property in Connect-AzureRmAccount (see "Sign in using the service principal" below), or you can convert this SecureString to a plain text string for later usage:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($servicePrincipal.Secret)
$password = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
[Runtime.InteropServices.Marshal]::ZeroFreeBSTR($BSTR)
```

### <a name="sign-in-using-the-service-principal"></a><span data-ttu-id="3e26c-129">Bejelentkezés a szolgáltatásnévvel</span><span class="sxs-lookup"><span data-stu-id="3e26c-129">Sign in using the service principal</span></span>

<span data-ttu-id="3e26c-130">Most már bejelentkezhet az alkalmazás új szolgáltatásnevével az automatikusan létrehozott *appId* és *jelszó* használatával.</span><span class="sxs-lookup"><span data-stu-id="3e26c-130">You can now sign in as the new service principal for your app using the *appId* you provided and *password* that was automatically generated.</span></span> <span data-ttu-id="3e26c-131">Szüksége lesz a szolgáltatásnévhez tartozó bérlőazonosítóra is.</span><span class="sxs-lookup"><span data-stu-id="3e26c-131">You also need the Tenant ID for the service principal.</span></span> <span data-ttu-id="3e26c-132">A bérlőazonosító akkor jelenik meg, ha a saját hitelesítő adataival bejelentkezik az Azure-ba.</span><span class="sxs-lookup"><span data-stu-id="3e26c-132">Your Tenant ID is displayed when you sign into Azure with your personal credentials.</span></span> <span data-ttu-id="3e26c-133">Szolgáltatásnévvel való bejelentkezéshez használja a következő parancsokat:</span><span class="sxs-lookup"><span data-stu-id="3e26c-133">To sign in with a service principal, use the following commands:</span></span>

```azurepowershell-interactive
$cred = New-Object System.Management.Automation.PSCredential ("00c01aaa-1603-49fc-b6df-b78c4e5138b4", $servicePrincipal.Secret)
Connect-AzureRmAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="3e26c-134">Sikeres bejelentkezés után az alábbihoz hasonló kimenet jelenik meg:</span><span class="sxs-lookup"><span data-stu-id="3e26c-134">After a successful sign-in you see output like:</span></span>

```output
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

<span data-ttu-id="3e26c-135">Gratulálunk!</span><span class="sxs-lookup"><span data-stu-id="3e26c-135">Congratulations!</span></span> <span data-ttu-id="3e26c-136">Ezekkel a hitelesítő adatokkal futtathatja az appját.</span><span class="sxs-lookup"><span data-stu-id="3e26c-136">You can use these credentials to run your app.</span></span> <span data-ttu-id="3e26c-137">Ezután be kell állítania a szolgáltatásnév jogosultságait.</span><span class="sxs-lookup"><span data-stu-id="3e26c-137">Next, you need to adjust the permissions of the service principal.</span></span>

## <a name="managing-roles"></a><span data-ttu-id="3e26c-138">Szerepkörök kezelése</span><span class="sxs-lookup"><span data-stu-id="3e26c-138">Managing roles</span></span>

> [!NOTE]
> <span data-ttu-id="3e26c-139">Az Azure szerepköralapú hozzáférés-vezérlése (RBAC) a felhasználói nevek és szolgáltatásnevek szerepköreinek meghatározására és kezelésére szolgáló modell.</span><span class="sxs-lookup"><span data-stu-id="3e26c-139">Azure Role-Based Access Control (RBAC) is a model for defining and managing roles for user and service principals.</span></span> <span data-ttu-id="3e26c-140">A szerepkörökhöz jogosultságkészletek vannak társítva, amelyek meghatározzák az egyszerű entitás által olvasható, elérhető, írható és kezelhető erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="3e26c-140">Roles have sets of permissions associated with them, which determine the resources a principal can read, access, write, or manage.</span></span> <span data-ttu-id="3e26c-141">További információ az RBAC-ról és a szerepkörökről: [RBAC: Beépített szerepkörök](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="3e26c-141">For more information on RBAC and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="3e26c-142">Az Azure PowerShell a következő parancsmagokat kínálja a szerepkör-hozzárendelések kezeléséhez:</span><span class="sxs-lookup"><span data-stu-id="3e26c-142">Azure PowerShell provides the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="3e26c-143">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="3e26c-143">Get-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/get-azurermroleassignment)
* [<span data-ttu-id="3e26c-144">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="3e26c-144">New-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/new-azurermroleassignment)
* [<span data-ttu-id="3e26c-145">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="3e26c-145">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/remove-azurermroleassignment)

<span data-ttu-id="3e26c-146">A szolgáltatásnevek alapértelmezett szerepköre a **Közreműködő**.</span><span class="sxs-lookup"><span data-stu-id="3e26c-146">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="3e26c-147">Mivel azonban ez széles körű engedélyekkel rendelkezik, nem feltétlenül ez a legjobb választás, attól függően, hogy az app milyen mértékben használja az Azure-szolgáltatásokat.</span><span class="sxs-lookup"><span data-stu-id="3e26c-147">It may not be the best choice depending on the scope of your app's interactions with Azure services, given its broad permissions.</span></span>
<span data-ttu-id="3e26c-148">Az **Olvasó** szerepkör sokkal korlátozóbb, és jó választás lehet a csak olvasó appokhoz.</span><span class="sxs-lookup"><span data-stu-id="3e26c-148">The **Reader** role is more restrictive and can be a good choice for read-only apps.</span></span> <span data-ttu-id="3e26c-149">A szerepkör-specifikus engedélyek részleteit megtekintheti az Azure Portalon, és létrehozhat saját szerepköröket is.</span><span class="sxs-lookup"><span data-stu-id="3e26c-149">You can view details on role-specific permissions or create custom ones through the Azure portal.</span></span>

<span data-ttu-id="3e26c-150">Esetünkben az **Olvasó** szerepkört adjuk hozzá a példához, és töröljük a **Közreműködő** szerepkört:</span><span class="sxs-lookup"><span data-stu-id="3e26c-150">In this example, we add the **Reader** role to our prior example, and delete the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/818892f2-d075-46a1-a3a2-3a4e1a12fcd5
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : b24988ac-6180-42a0-ab88-20f7382dd24c
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

```azurepowershell-interactive
Remove-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

<span data-ttu-id="3e26c-151">Az aktuálisan hozzárendelt szerepkörök megtekintése:</span><span class="sxs-lookup"><span data-stu-id="3e26c-151">To view the current roles assigned:</span></span>

```azurepowershell-interactive
Get-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/0906bbd8-9982-4c03-8dae-aeaae8b13f9e
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : acdd72a7-3385-48ef-bd42-f606fba81ae7
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

<span data-ttu-id="3e26c-152">Egyéb Azure PowerShell-parancsmagok a szerepkörök kezeléséhez:</span><span class="sxs-lookup"><span data-stu-id="3e26c-152">Other Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="3e26c-153">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3e26c-153">Get-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="3e26c-154">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3e26c-154">New-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="3e26c-155">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3e26c-155">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="3e26c-156">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3e26c-156">Set-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Set-AzureRmRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a><span data-ttu-id="3e26c-157">Szolgáltatásnév hitelesítő adatainak módosítása</span><span class="sxs-lookup"><span data-stu-id="3e26c-157">Change the credentials of the security principal</span></span>

<span data-ttu-id="3e26c-158">A jogosultságok rendszeres áttekintése és a jelszavak cseréje ajánlott biztonsági eljárás.</span><span class="sxs-lookup"><span data-stu-id="3e26c-158">It's a good security practice to review the permissions and update the password regularly.</span></span> <span data-ttu-id="3e26c-159">Az app változása esetén is érdemes lehet módosítani a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="3e26c-159">You may also want to manage and modify the security credentials as your app changes.</span></span> <span data-ttu-id="3e26c-160">A szolgáltatásnév jelszava például módosítható egy új jelszó létrehozásával és a korábbi törlésével.</span><span class="sxs-lookup"><span data-stu-id="3e26c-160">For example, we can change the password of the service principal by creating a new password and removing the old one.</span></span>

### <a name="add-a-new-password-for-the-service-principal"></a><span data-ttu-id="3e26c-161">Új jelszó hozzáadása a szolgáltatásnévhez</span><span class="sxs-lookup"><span data-stu-id="3e26c-161">Add a new password for the service principal</span></span>

```azurepowershell-interactive
New-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
Secret    : System.Security.SecureString
StartDate : 11/16/2018 12:38:23 AM
EndDate   : 11/16/2019 12:38:23 AM
KeyId     : 6f801c3e-6fcd-42b9-be8e-320b17ba1d36
Type      : Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="3e26c-162">A szolgáltatásnév hitelesítő adatainak listázása</span><span class="sxs-lookup"><span data-stu-id="3e26c-162">Get a list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a><span data-ttu-id="3e26c-163">A régi jelszó törlése a szolgáltatásnévből</span><span class="sxs-lookup"><span data-stu-id="3e26c-163">Remove the old password from the service principal</span></span>

```azurepowershell-interactive
Remove-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```output
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="3e26c-164">A szolgáltatásnév hitelesítőadat-listájának ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="3e26c-164">Verify the list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-information-about-the-service-principal"></a><span data-ttu-id="3e26c-165">A szolgáltatásnév adatainak lekérése</span><span class="sxs-lookup"><span data-stu-id="3e26c-165">Get information about the service principal</span></span>

```azurepowershell-interactive
$svcprincipal = Get-AzureRmADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```output
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```
