---
title: Azure-beli szolgáltatásnév létrehozása az Azure PowerShell használatával
description: Megtudhatja, hogyan hozhat létre szolgáltatásneveket appjához vagy szolgáltatásához az Azure PowerShell használatával.
keywords: Azure PowerShell, Azure Active Directory, Azure Active directory, AD, RBAC
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: dd2e50a4fe5ee9061403e2b61ace74213b5c858e
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/23/2018
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="c79e1-104">Azure-beli szolgáltatásnév létrehozása az Azure PowerShell használatával</span><span class="sxs-lookup"><span data-stu-id="c79e1-104">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="c79e1-105">Ha az appját vagy szolgáltatását az Azure PowerShell-lel szeretné kezelni, egy Azure Active Directory (AAD) szolgáltatásnév alatt, és nem a saját hitelesítő adataival érdemes futtatnia.</span><span class="sxs-lookup"><span data-stu-id="c79e1-105">If you plan to manage your app or service with Azure PowerShell, you should run it under an Azure Active Directory (AAD) service principal, rather than your own credentials.</span></span> <span data-ttu-id="c79e1-106">Ez a témakör végigvezeti a szolgáltatásnevek Azure PowerShell-lel való létrehozásának folyamatán.</span><span class="sxs-lookup"><span data-stu-id="c79e1-106">This topic steps you through creating a security principal with Azure PowerShell.</span></span>

> [!NOTE]
> <span data-ttu-id="c79e1-107">Az Azure Portalon is létrehozhat szolgáltatásneveket.</span><span class="sxs-lookup"><span data-stu-id="c79e1-107">You can also create a service principal through the Azure portal.</span></span> <span data-ttu-id="c79e1-108">További részletekért lásd: [Active Directory-alkalmazás és -szolgáltatásnév létrehozása a portálon erőforrások eléréséhez](/azure/azure-resource-manager/resource-group-create-service-principal-portal).</span><span class="sxs-lookup"><span data-stu-id="c79e1-108">Read [Use portal to create Active Directory application and service principal that can access resources](/azure/azure-resource-manager/resource-group-create-service-principal-portal) for more details.</span></span>

## <a name="what-is-a-service-principal"></a><span data-ttu-id="c79e1-109">Mi az a szolgáltatásnév?</span><span class="sxs-lookup"><span data-stu-id="c79e1-109">What is a 'service principal'?</span></span>

<span data-ttu-id="c79e1-110">Az Azure-beli szolgáltatásnév egy biztonsági identitás, amellyel a felhasználó által létrehozott appok, szolgáltatások és automatizálási eszközök elérnek adott Azure-erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="c79e1-110">An Azure service principal is a security identity used by user-created apps, services, and automation tools to access specific Azure resources.</span></span> <span data-ttu-id="c79e1-111">Képzelje el úgy, mint egy „felhasználói identitást” (felhasználónév és jelszó vagy tanúsítvány) egy adott szerepkörrel és szigorúan szabályozott engedélyekkel.</span><span class="sxs-lookup"><span data-stu-id="c79e1-111">Think of it as a 'user identity' (username and password or certificate) with a specific role, and tightly controlled permissions.</span></span> <span data-ttu-id="c79e1-112">Az általános identitásoktól eltérően ez csak konkrét feladatok végrehajtására szolgál.</span><span class="sxs-lookup"><span data-stu-id="c79e1-112">It only needs to be able to do specific things, unlike a general user identity.</span></span> <span data-ttu-id="c79e1-113">Csak akkor javítja a biztonságot, ha csak a felügyeleti feladataihoz szükséges minimális engedélyeket osztja ki neki.</span><span class="sxs-lookup"><span data-stu-id="c79e1-113">It improves security if you only grant it the minimum permissions level needed to perform its management tasks.</span></span>

## <a name="verify-your-own-permission-level"></a><span data-ttu-id="c79e1-114">Saját jogosultsági szint ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="c79e1-114">Verify your own permission level</span></span>

<span data-ttu-id="c79e1-115">Először is megfelelő jogosultságokkal kell rendelkeznie mind az Azure Active Directoryban, mind az Azure-előfizetésén.</span><span class="sxs-lookup"><span data-stu-id="c79e1-115">First, you must have sufficient permissions in both your Azure Active Directory and your Azure subscription.</span></span> <span data-ttu-id="c79e1-116">Pontosabban, létre kell tudnia hozni appot az Active Directoryban, és ki kell tudnia osztani szerepköröket a szolgáltatásnévnek.</span><span class="sxs-lookup"><span data-stu-id="c79e1-116">Specifically, you must be able to create an app in the Active Directory, and assign a role to the service principal.</span></span>

<span data-ttu-id="c79e1-117">A legegyszerűbben a portálon ellenőrizheti, hogy rendelkezik-e megfelelő jogosultságokkal.</span><span class="sxs-lookup"><span data-stu-id="c79e1-117">The easiest way to check whether your account has adequate permissions is through the portal.</span></span> <span data-ttu-id="c79e1-118">Lásd [Szükséges jogosultságok ellenőrzése a portálon](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span><span class="sxs-lookup"><span data-stu-id="c79e1-118">See [Check required permission in portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span></span>

## <a name="create-a-service-principal-for-your-app"></a><span data-ttu-id="c79e1-119">Szolgáltatásnév létrehozása az app számára</span><span class="sxs-lookup"><span data-stu-id="c79e1-119">Create a service principal for your app</span></span>

<span data-ttu-id="c79e1-120">Miután bejelentkezett Azure-fiókjába, létrehozhatja a szolgáltatásnevet.</span><span class="sxs-lookup"><span data-stu-id="c79e1-120">Once you are signed into your Azure account, you can create the service principal.</span></span> <span data-ttu-id="c79e1-121">A következő módszerek egyikének rendelkezésre kell állnia az üzembe helyezett app azonosításához:</span><span class="sxs-lookup"><span data-stu-id="c79e1-121">You must have one of the following ways to identify your deployed app:</span></span>

* <span data-ttu-id="c79e1-122">Az üzembe helyezett app egyedi neve (a következő példákban ez a „MyDemoWebApp”), vagy</span><span class="sxs-lookup"><span data-stu-id="c79e1-122">The unique name of your deployed app, such as "MyDemoWebApp" in the following examples, or</span></span>
* <span data-ttu-id="c79e1-123">az alkalmazásazonosító, az üzembe helyezett alkalmazással, szolgáltatással vagy objektummal társított egyedi GUID</span><span class="sxs-lookup"><span data-stu-id="c79e1-123">the Application ID, the unique GUID associated with your deployed app, service, or object</span></span>

### <a name="get-information-about-your-application"></a><span data-ttu-id="c79e1-124">Az alkalmazás adatainak lekérése</span><span class="sxs-lookup"><span data-stu-id="c79e1-124">Get information about your application</span></span>

<span data-ttu-id="c79e1-125">Az alkalmazással kapcsolatos információkat a `Get-AzureRmADApplication` parancsmaggal derítheti fel.</span><span class="sxs-lookup"><span data-stu-id="c79e1-125">The `Get-AzureRmADApplication` cmdlet can be used to discover information about your application.</span></span>

```powershell
Get-AzureRmADApplication -DisplayNameStartWith MyDemoWebApp
```

```
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

### <a name="create-a-service-principal-for-your-application"></a><span data-ttu-id="c79e1-126">Szolgáltatásnév létrehozása az alkalmazás számára</span><span class="sxs-lookup"><span data-stu-id="c79e1-126">Create a service principal for your application</span></span>

<span data-ttu-id="c79e1-127">A szolgáltatásnév a `New-AzureRmADServicePrincipal` parancsmaggal hozható létre.</span><span class="sxs-lookup"><span data-stu-id="c79e1-127">The `New-AzureRmADServicePrincipal` cmdlet is used to create the service principal.</span></span>

```powershell
Add-Type -Assembly System.Web
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
New-AzureRmADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4 -Password $password
```

```
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
MyDemoWebApp                   ServicePrincipal               698138e7-d7b6-4738-a866-b4e3081a69e4
```

### <a name="get-information-about-the-service-principal"></a><span data-ttu-id="c79e1-128">A szolgáltatásnév adatainak lekérése</span><span class="sxs-lookup"><span data-stu-id="c79e1-128">Get information about the service principal</span></span>

```powershell
$svcprincipal = Get-AzureRmADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```

### <a name="sign-in-using-the-service-principal"></a><span data-ttu-id="c79e1-129">Bejelentkezés a szolgáltatásnévvel</span><span class="sxs-lookup"><span data-stu-id="c79e1-129">Sign in using the service principal</span></span>

<span data-ttu-id="c79e1-130">Most már bejelentkezhet az app új szolgáltatásnevével a megadott *appId* és *jelszó* használatával.</span><span class="sxs-lookup"><span data-stu-id="c79e1-130">You can now sign in as the new service principal for your app using the *appId* and *password* you provided.</span></span> <span data-ttu-id="c79e1-131">Meg kell adnia fiókja bérlőazonosítóját.</span><span class="sxs-lookup"><span data-stu-id="c79e1-131">You need to supply the Tenant Id for your account.</span></span> <span data-ttu-id="c79e1-132">A bérlőazonosító akkor jelenik meg, ha a saját hitelesítő adataival bejelentkezik az Azure-ba.</span><span class="sxs-lookup"><span data-stu-id="c79e1-132">Your Tenant Id is displayed when you sign into Azure with your personal credentials.</span></span>

```powershell
$cred = Get-Credential -UserName $svcprincipal.ApplicationId -Message "Enter Password"
Login-AzureRmAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="c79e1-133">Futtassa ezt a parancsot egy új PowerShell-munkamenetből.</span><span class="sxs-lookup"><span data-stu-id="c79e1-133">Run this command from a new PowerShell session.</span></span> <span data-ttu-id="c79e1-134">Sikeres bejelentkezés után az alábbihoz hasonló kimenet jelenik meg:</span><span class="sxs-lookup"><span data-stu-id="c79e1-134">After a successfully signing on you see output something like this:</span></span>

```
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

<span data-ttu-id="c79e1-135">Gratulálunk!</span><span class="sxs-lookup"><span data-stu-id="c79e1-135">Congratulations!</span></span> <span data-ttu-id="c79e1-136">Ezekkel a hitelesítő adatokkal futtathatja az appját.</span><span class="sxs-lookup"><span data-stu-id="c79e1-136">You can use these credentials to run your app.</span></span> <span data-ttu-id="c79e1-137">Ezután be kell állítania a szolgáltatásnév jogosultságait.</span><span class="sxs-lookup"><span data-stu-id="c79e1-137">Next, you need to adjust the permissions of the service principal.</span></span>

## <a name="managing-roles"></a><span data-ttu-id="c79e1-138">Szerepkörök kezelése</span><span class="sxs-lookup"><span data-stu-id="c79e1-138">Managing roles</span></span>

> [!NOTE]
> <span data-ttu-id="c79e1-139">Az Azure szerepköralapú hozzáférés-vezérlése (RBAC) a felhasználói nevek és szolgáltatásnevek szerepköreinek meghatározására és kezelésére szolgáló modell.</span><span class="sxs-lookup"><span data-stu-id="c79e1-139">Azure Role-Based Access Control (RBAC) is a model for defining and managing roles for user and service principals.</span></span> <span data-ttu-id="c79e1-140">A szerepkörökhöz jogosultságkészletek vannak társítva, amelyek meghatározzák az egyszerű entitás által olvasható, elérhető, írható és kezelhető erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="c79e1-140">Roles have sets of permissions associated with them, which determine the resources a principal can read, access, write, or manage.</span></span> <span data-ttu-id="c79e1-141">További információkért az RBAC-ról és a szerepkörökről: [RBAC: Beépített szerepkörök](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="c79e1-141">For more information on RBAC and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="c79e1-142">Az Azure PowerShell a következő parancsmagokat kínálja a szerepkör-hozzárendelések kezeléséhez:</span><span class="sxs-lookup"><span data-stu-id="c79e1-142">Azure PowerShell provides the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="c79e1-143">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c79e1-143">Get-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/get-azurermroleassignment)
* [<span data-ttu-id="c79e1-144">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c79e1-144">New-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/new-azurermroleassignment)
* [<span data-ttu-id="c79e1-145">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c79e1-145">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/remove-azurermroleassignment)

<span data-ttu-id="c79e1-146">A szolgáltatásnevek alapértelmezett szerepköre a **Közreműködő**.</span><span class="sxs-lookup"><span data-stu-id="c79e1-146">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="c79e1-147">Mivel azonban ez széles körű engedélyekkel rendelkezik, nem feltétlenül ez a legjobb választás, attól függően, hogy az app milyen mértékben használja az Azure-szolgáltatásokat.</span><span class="sxs-lookup"><span data-stu-id="c79e1-147">It may not be the best choice depending on the scope of your app's interactions with Azure services, given its broad permissions.</span></span>
<span data-ttu-id="c79e1-148">Az **Olvasó** szerepkör sokkal korlátozóbb, és jó választás lehet a csak olvasó appokhoz.</span><span class="sxs-lookup"><span data-stu-id="c79e1-148">The **Reader** role is more restrictive and can be a good choice for read-only apps.</span></span> <span data-ttu-id="c79e1-149">A szerepkör-specifikus engedélyek részleteit megtekintheti az Azure Portalon, és létrehozhat saját szerepköröket is.</span><span class="sxs-lookup"><span data-stu-id="c79e1-149">You can view details on role-specific permissions or create custom ones through the Azure portal.</span></span>

<span data-ttu-id="c79e1-150">Esetünkben az **Olvasó** szerepkört adjuk hozzá a példához, és töröljük a **Közreműködő** szerepkört:</span><span class="sxs-lookup"><span data-stu-id="c79e1-150">In this example, we add the **Reader** role to our prior example, and delete the **Contributor** one:</span></span>

```powershell
New-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
```

```
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/818892f2-d075-46a1-a3a2-3a4e1a12fcd5
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : b24988ac-6180-42a0-ab88-20f7382dd24c
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

```powershell
Remove-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

<span data-ttu-id="c79e1-151">Az aktuálisan hozzárendelt szerepkörök megtekintése:</span><span class="sxs-lookup"><span data-stu-id="c79e1-151">To view the current roles assigned:</span></span>

```powershell
Get-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
```

```
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/0906bbd8-9982-4c03-8dae-aeaae8b13f9e
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : acdd72a7-3385-48ef-bd42-f606fba81ae7
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

<span data-ttu-id="c79e1-152">Egyéb Azure PowerShell-parancsmagok a szerepkörök kezeléséhez:</span><span class="sxs-lookup"><span data-stu-id="c79e1-152">Other Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="c79e1-153">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c79e1-153">Get-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="c79e1-154">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c79e1-154">New-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="c79e1-155">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c79e1-155">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="c79e1-156">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c79e1-156">Set-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Set-AzureRmRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a><span data-ttu-id="c79e1-157">Szolgáltatásnév hitelesítő adatainak módosítása</span><span class="sxs-lookup"><span data-stu-id="c79e1-157">Change the credentials of the security principal</span></span>

<span data-ttu-id="c79e1-158">A jogosultságok rendszeres áttekintése és a jelszavak cseréje ajánlott biztonsági eljárás.</span><span class="sxs-lookup"><span data-stu-id="c79e1-158">It's a good security practice to review the permissions and update the password regularly.</span></span> <span data-ttu-id="c79e1-159">Az app változása esetén is érdemes lehet módosítani a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="c79e1-159">You may also want to manage and modify the security credentials as your app changes.</span></span> <span data-ttu-id="c79e1-160">A szolgáltatásnév jelszava például módosítható egy új jelszó létrehozásával és a korábbi törlésével.</span><span class="sxs-lookup"><span data-stu-id="c79e1-160">For example, we can change the password of the service principal by creating a new password and removing the old one.</span></span>

### <a name="add-a-new-password-for-the-service-principal"></a><span data-ttu-id="c79e1-161">Új jelszó hozzáadása a szolgáltatásnévhez</span><span class="sxs-lookup"><span data-stu-id="c79e1-161">Add a new password for the service principal</span></span>

```powershell
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
New-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -Password $password
```

```
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="c79e1-162">A szolgáltatásnév hitelesítő adatainak listázása</span><span class="sxs-lookup"><span data-stu-id="c79e1-162">Get a list of credentials for the service principal</span></span>

```powershell
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a><span data-ttu-id="c79e1-163">A régi jelszó törlése a szolgáltatásnévből</span><span class="sxs-lookup"><span data-stu-id="c79e1-163">Remove the old password from the service principal</span></span>

```powershell
Remove-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="c79e1-164">A szolgáltatásnév hitelesítőadat-listájának ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="c79e1-164">Verify the list of credentials for the service principal</span></span>

```powershell
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```
