---
title: Azure-beli szolgáltatásnév létrehozása az Azure PowerShell használatával
description: Megtudhatja, hogyan hozhat létre szolgáltatásneveket appjához vagy szolgáltatásához az Azure PowerShell használatával.
keywords: Azure PowerShell, Azure Active Directory, Azure Active directory, AD, RBAC
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 3e1c5ad280bdb29ce479dd0a478d0ed58237f969
ms.sourcegitcommit: 797c18f93aaa495ef005993b2e202d7378588dfa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/19/2018
ms.locfileid: "53594955"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="df354-104">Azure-beli szolgáltatásnév létrehozása az Azure PowerShell használatával</span><span class="sxs-lookup"><span data-stu-id="df354-104">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="df354-105">Ha az appját vagy szolgáltatását az Azure PowerShell-lel szeretné kezelni, egy Azure Active Directory (AAD) szolgáltatásnév alatt, és nem a saját hitelesítő adataival érdemes futtatnia.</span><span class="sxs-lookup"><span data-stu-id="df354-105">If you plan to manage your app or service with Azure PowerShell, you should run it under an Azure Active Directory (AAD) service principal, rather than your own credentials.</span></span> <span data-ttu-id="df354-106">Ez a cikk végigvezeti a szolgáltatásnevek Azure PowerShell-lel való létrehozásának folyamatán.</span><span class="sxs-lookup"><span data-stu-id="df354-106">This article steps you through creating a security principal with Azure PowerShell.</span></span>

## <a name="what-is-a-service-principal"></a><span data-ttu-id="df354-107">Mi az a szolgáltatásnév?</span><span class="sxs-lookup"><span data-stu-id="df354-107">What is a service principal?</span></span>

<span data-ttu-id="df354-108">Az Azure-beli szolgáltatásnév egy biztonsági identitás, amellyel a felhasználó által létrehozott appok, szolgáltatások és automatizálási eszközök elérnek adott Azure-erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="df354-108">An Azure service principal is a security identity used by user-created apps, services, and automation tools to access specific Azure resources.</span></span> <span data-ttu-id="df354-109">A szolgáltatásnevekhez a feladataikhoz kapcsolódó speciális engedélyek vannak rendelve, így jobban szabályozható a biztonság.</span><span class="sxs-lookup"><span data-stu-id="df354-109">Service principals are assigned specific permissions related to their tasks, giving you better security control.</span></span> <span data-ttu-id="df354-110">Ez abban tér el az általános identitásoktól, hogy azok általában bármely módosítás elvégzésére jogosultak.</span><span class="sxs-lookup"><span data-stu-id="df354-110">This is unlike a general user identity, which is usually authorized to make any changes.</span></span>

## <a name="verify-your-own-permission-level"></a><span data-ttu-id="df354-111">Saját jogosultsági szint ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="df354-111">Verify your own permission level</span></span>

<span data-ttu-id="df354-112">Először is megfelelő jogosultságokkal kell rendelkeznie mind az Azure Active Directoryban, mind az Azure-előfizetésén.</span><span class="sxs-lookup"><span data-stu-id="df354-112">First, you must have sufficient permissions in both your Azure Active Directory and your Azure subscription.</span></span> <span data-ttu-id="df354-113">Létre kell tudnia hozni alkalmazást az Active Directoryban, és ki kell tudnia osztani szerepköröket a szolgáltatásnévnek.</span><span class="sxs-lookup"><span data-stu-id="df354-113">You must be able to create an app in the Active Directory and assign a role to the service principal.</span></span>

<span data-ttu-id="df354-114">A legegyszerűbben a portálon ellenőrizheti, hogy rendelkezik-e megfelelő jogosultságokkal.</span><span class="sxs-lookup"><span data-stu-id="df354-114">The easiest way to check whether your account has the right permissions is through the portal.</span></span> <span data-ttu-id="df354-115">Lásd [Szükséges jogosultságok ellenőrzése a portálon](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span><span class="sxs-lookup"><span data-stu-id="df354-115">See [Check required permission in portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span></span>

## <a name="create-a-service-principal-for-your-app"></a><span data-ttu-id="df354-116">Szolgáltatásnév létrehozása az app számára</span><span class="sxs-lookup"><span data-stu-id="df354-116">Create a service principal for your app</span></span>

<span data-ttu-id="df354-117">Miután bejelentkezett Azure-fiókjába, létrehozhatja a szolgáltatásnevet.</span><span class="sxs-lookup"><span data-stu-id="df354-117">Once signed in to your Azure account, you can create the service principal.</span></span> <span data-ttu-id="df354-118">A következő módszerek egyikének rendelkezésre kell állnia az üzembe helyezett app azonosításához:</span><span class="sxs-lookup"><span data-stu-id="df354-118">You must have one of the following ways to identify your deployed app:</span></span>

* <span data-ttu-id="df354-119">Az üzembe helyezett alkalmazás egyedi neve – a következő példákban ez a MyDemoWebApp</span><span class="sxs-lookup"><span data-stu-id="df354-119">The unique name of your deployed app, such as "MyDemoWebApp" in the following examples</span></span>
* <span data-ttu-id="df354-120">Az alkalmazásazonosító, az üzembe helyezett alkalmazáshoz, szolgáltatáshoz vagy objektumhoz társított egyedi GUID</span><span class="sxs-lookup"><span data-stu-id="df354-120">The Application ID, the unique GUID associated with your deployed app, service, or object</span></span>

### <a name="get-information-about-your-application"></a><span data-ttu-id="df354-121">Az alkalmazás adatainak lekérése</span><span class="sxs-lookup"><span data-stu-id="df354-121">Get information about your application</span></span>

<span data-ttu-id="df354-122">Az alkalmazással kapcsolatos információkat a `Get-AzADApplication` parancsmaggal kérheti le.</span><span class="sxs-lookup"><span data-stu-id="df354-122">The `Get-AzADApplication` cmdlet can be used to get information about your application.</span></span>

```azurepowershell-interactive
$app = Get-AzADApplication -DisplayNameStartWith MyDemoWebApp
$app
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

### <a name="create-a-service-principal-for-your-application"></a><span data-ttu-id="df354-123">Szolgáltatásnév létrehozása az alkalmazás számára</span><span class="sxs-lookup"><span data-stu-id="df354-123">Create a service principal for your application</span></span>

<span data-ttu-id="df354-124">A szolgáltatásnév a `New-AzADServicePrincipal` parancsmaggal hozható létre.</span><span class="sxs-lookup"><span data-stu-id="df354-124">The `New-AzADServicePrincipal` cmdlet is used to create the service principal.</span></span>

```azurepowershell-interactive
$servicePrincipal = New-AzADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4
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

<span data-ttu-id="df354-125">Itt használhatja közvetlenül a `$servicePrincipal.Secret` tulajdonságot a `Connect-AzAccount` argumentumaként (lásd a „Bejelentkezés a szolgáltatásnévvel” című részt) vagy átalakíthatja ezt a `SecureString` típusú sztringet egyszerű szöveges sztringgé:</span><span class="sxs-lookup"><span data-stu-id="df354-125">From here, you can either directly use the `$servicePrincipal.Secret` property as an argument to `Connect-AzAccount` (see "Sign in using the service principal"), or you can convert this `SecureString` to a plain text string:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($servicePrincipal.Secret)
$password = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
[Runtime.InteropServices.Marshal]::ZeroFreeBSTR($BSTR)
```

### <a name="sign-in-using-the-service-principal"></a><span data-ttu-id="df354-126">Bejelentkezés a szolgáltatásnévvel</span><span class="sxs-lookup"><span data-stu-id="df354-126">Sign in using the service principal</span></span>

<span data-ttu-id="df354-127">Most már bejelentkezhet az alkalmazás új szolgáltatásnevével a megadott `appId` és a létrehozott `password`</span><span class="sxs-lookup"><span data-stu-id="df354-127">You can now sign in as the new service principal for your app using the `appId` you provided and `password` that was</span></span>  
<span data-ttu-id="df354-128">használatával.</span><span class="sxs-lookup"><span data-stu-id="df354-128">generated.</span></span> <span data-ttu-id="df354-129">Szüksége lesz a szolgáltatásnévhez tartozó bérlőazonosítóra is.</span><span class="sxs-lookup"><span data-stu-id="df354-129">You also need the Tenant ID for the service principal.</span></span> <span data-ttu-id="df354-130">A bérlőazonosító akkor jelenik meg, ha a saját hitelesítő adataival bejelentkezik az Azure-ba.</span><span class="sxs-lookup"><span data-stu-id="df354-130">Your Tenant ID is displayed when you sign into Azure with your personal credentials.</span></span> <span data-ttu-id="df354-131">Szolgáltatásnévvel való bejelentkezéshez használja a következő parancsokat:</span><span class="sxs-lookup"><span data-stu-id="df354-131">To sign in with a service principal, use the commands:</span></span>

```azurepowershell-interactive
$cred = New-Object System.Management.Automation.PSCredential ("00c01aaa-1603-49fc-b6df-b78c4e5138b4", $servicePrincipal.Secret)
Connect-AzAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="df354-132">Sikeres bejelentkezés után az alábbihoz hasonló kimenet jelenik meg:</span><span class="sxs-lookup"><span data-stu-id="df354-132">After a successful sign-in you see output like:</span></span>

```output
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

<span data-ttu-id="df354-133">Gratulálunk!</span><span class="sxs-lookup"><span data-stu-id="df354-133">Congratulations!</span></span> <span data-ttu-id="df354-134">Ezekkel a hitelesítő adatokkal futtathatja az appját.</span><span class="sxs-lookup"><span data-stu-id="df354-134">You can use these credentials to run your app.</span></span> <span data-ttu-id="df354-135">Ezután be kell állítania a szolgáltatásnév jogosultságait.</span><span class="sxs-lookup"><span data-stu-id="df354-135">Next, you need to adjust the permissions of the service principal.</span></span>

## <a name="managing-roles"></a><span data-ttu-id="df354-136">Szerepkörök kezelése</span><span class="sxs-lookup"><span data-stu-id="df354-136">Managing roles</span></span>

> [!NOTE]
> <span data-ttu-id="df354-137">Az Azure szerepköralapú hozzáférés-vezérlése (RBAC) a felhasználói nevek és szolgáltatásnevek szerepköreinek meghatározására és kezelésére szolgáló modell.</span><span class="sxs-lookup"><span data-stu-id="df354-137">Azure Role-Based Access Control (RBAC) is a model for defining and managing roles for user and service principals.</span></span> <span data-ttu-id="df354-138">A szerepkörökhöz jogosultságkészletek vannak társítva, amelyek meghatározzák az egyszerű entitás által olvasható, elérhető, írható és kezelhető erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="df354-138">Roles have sets of permissions associated with them, which determine the resources a principal can read, access, write, or manage.</span></span> <span data-ttu-id="df354-139">További információ az RBAC-ról és a szerepkörökről: [RBAC: Beépített szerepkörök](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="df354-139">For more information on RBAC and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="df354-140">Az Azure PowerShell a következő parancsmagokat kínálja a szerepkör-hozzárendelések kezeléséhez:</span><span class="sxs-lookup"><span data-stu-id="df354-140">Azure PowerShell provides the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="df354-141">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="df354-141">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
* [<span data-ttu-id="df354-142">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="df354-142">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
* [<span data-ttu-id="df354-143">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="df354-143">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="df354-144">A szolgáltatásnevek alapértelmezett szerepköre a **Közreműködő**.</span><span class="sxs-lookup"><span data-stu-id="df354-144">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="df354-145">Mivel azonban ez széles körű engedélyekkel rendelkezik, nem feltétlenül ez a legjobb választás, attól függően, hogy az app milyen mértékben használja az Azure-szolgáltatásokat.</span><span class="sxs-lookup"><span data-stu-id="df354-145">It may not be the best choice depending on the scope of your app's interactions with Azure services, given its broad permissions.</span></span>
<span data-ttu-id="df354-146">Az **Olvasó** szerepkör sokkal korlátozóbb, és jó választás lehet a csak olvasó appokhoz.</span><span class="sxs-lookup"><span data-stu-id="df354-146">The **Reader** role is more restrictive and can be a good choice for read-only apps.</span></span> <span data-ttu-id="df354-147">A szerepkör-specifikus engedélyek részleteit megtekintheti az Azure Portalon, és létrehozhat saját szerepköröket is.</span><span class="sxs-lookup"><span data-stu-id="df354-147">You can view details on role-specific permissions or create custom ones through the Azure portal.</span></span>

<span data-ttu-id="df354-148">Esetünkben az **Olvasó** szerepkört adjuk hozzá a példához, és töröljük a **Közreműködő** szerepkört:</span><span class="sxs-lookup"><span data-stu-id="df354-148">In this example, we add the **Reader** role to our prior example, and delete the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
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
Remove-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

<span data-ttu-id="df354-149">Az aktuálisan hozzárendelt szerepkörök megtekintése:</span><span class="sxs-lookup"><span data-stu-id="df354-149">To view the current roles assigned:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
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

<span data-ttu-id="df354-150">Egyéb Azure PowerShell-parancsmagok a szerepkörök kezeléséhez:</span><span class="sxs-lookup"><span data-stu-id="df354-150">Other Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="df354-151">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="df354-151">Get-AzRoleDefinition</span></span>](/powershell/module/az.resources/Get-azRoleDefinition)
* [<span data-ttu-id="df354-152">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="df354-152">New-AzRoleDefinition</span></span>](/powershell/module/az.resources/New-azRoleDefinition)
* [<span data-ttu-id="df354-153">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="df354-153">Remove-AzRoleDefinition</span></span>](/powershell/module/az.resources/Remove-azRoleDefinition)
* [<span data-ttu-id="df354-154">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="df354-154">Set-AzRoleDefinition</span></span>](/powershell/module/az.resources/Set-azRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a><span data-ttu-id="df354-155">Szolgáltatásnév hitelesítő adatainak módosítása</span><span class="sxs-lookup"><span data-stu-id="df354-155">Change the credentials of the security principal</span></span>

<span data-ttu-id="df354-156">A jogosultságok rendszeres áttekintése és a jelszavak cseréje ajánlott biztonsági eljárás.</span><span class="sxs-lookup"><span data-stu-id="df354-156">It's a good security practice to review the permissions and update the password regularly.</span></span> <span data-ttu-id="df354-157">Az app változása esetén is érdemes lehet módosítani a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="df354-157">You may also want to manage and modify the security credentials as your app changes.</span></span> <span data-ttu-id="df354-158">A szolgáltatásnév jelszava például módosítható egy új jelszó létrehozásával és a korábbi törlésével.</span><span class="sxs-lookup"><span data-stu-id="df354-158">For example, we can change the password of the service principal by creating a new password and removing the old one.</span></span>

### <a name="add-a-new-password-for-the-service-principal"></a><span data-ttu-id="df354-159">Új jelszó hozzáadása a szolgáltatásnévhez</span><span class="sxs-lookup"><span data-stu-id="df354-159">Add a new password for the service principal</span></span>

```azurepowershell-interactive
New-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
Secret    : System.Security.SecureString
StartDate : 11/16/2018 12:38:23 AM
EndDate   : 11/16/2019 12:38:23 AM
KeyId     : 6f801c3e-6fcd-42b9-be8e-320b17ba1d36
Type      : Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="df354-160">A szolgáltatásnév hitelesítő adatainak listázása</span><span class="sxs-lookup"><span data-stu-id="df354-160">Get a list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a><span data-ttu-id="df354-161">A régi jelszó törlése a szolgáltatásnévből</span><span class="sxs-lookup"><span data-stu-id="df354-161">Remove the old password from the service principal</span></span>

```azurepowershell-interactive
Remove-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```output
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="df354-162">A szolgáltatásnév hitelesítőadat-listájának ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="df354-162">Verify the list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-information-about-the-service-principal"></a><span data-ttu-id="df354-163">A szolgáltatásnév adatainak lekérése</span><span class="sxs-lookup"><span data-stu-id="df354-163">Get information about the service principal</span></span>

```azurepowershell-interactive
$svcprincipal = Get-AzADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```output
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```
