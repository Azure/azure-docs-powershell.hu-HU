---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: 3a410dfb43cc767b0a73086147042425d42764d1
ms.sourcegitcommit: e680033f216d86cd91a1dfdb8328d32f4c99d21a
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/02/2021
ms.locfileid: "99251624"
---
# <span data-ttu-id="36b96-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="36b96-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="36b96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36b96-102">SYNOPSIS</span></span>
<span data-ttu-id="36b96-103">Létrehoz egy új azure Active Directory szolgáltatásnévből.</span><span class="sxs-lookup"><span data-stu-id="36b96-103">Creates a new azure active directory service principal.</span></span>

## <span data-ttu-id="36b96-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="36b96-104">SYNTAX</span></span>

### <span data-ttu-id="36b96-105">SimpleParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="36b96-105">SimpleParameterSet (Default)</span></span>
```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36b96-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="36b96-106">ApplicationWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36b96-107">ApplicationWithPasswordPatlanParameterSet</span><span class="sxs-lookup"><span data-stu-id="36b96-107">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36b96-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="36b96-108">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36b96-109">ApplicationWithKeyPmirParameterSet</span><span class="sxs-lookup"><span data-stu-id="36b96-109">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36b96-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="36b96-110">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36b96-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="36b96-111">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36b96-112">DisplayNameWithPasswordPmirParameterSet</span><span class="sxs-lookup"><span data-stu-id="36b96-112">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36b96-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="36b96-113">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36b96-114">DisplayNameWithKeyPmirParameterSet</span><span class="sxs-lookup"><span data-stu-id="36b96-114">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36b96-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="36b96-115">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36b96-116">ApplicationObjectWithPasswordPmirParameterSet</span><span class="sxs-lookup"><span data-stu-id="36b96-116">ApplicationObjectWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36b96-117">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="36b96-117">ApplicationObjectWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36b96-118">ApplicationObjectWithKeyPmirParameterSet</span><span class="sxs-lookup"><span data-stu-id="36b96-118">ApplicationObjectWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36b96-119">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="36b96-119">ApplicationObjectWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36b96-120">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="36b96-120">DESCRIPTION</span></span>
<span data-ttu-id="36b96-121">Létrehoz egy új azure Active Directory szolgáltatásnévből.</span><span class="sxs-lookup"><span data-stu-id="36b96-121">Creates a new azure active directory service principal.</span></span> <span data-ttu-id="36b96-122">Az alapértelmezett paraméterkészlet alapértelmezett értékeket használ a paraméterekhez, ha a felhasználó nem biztosít számukra ilyen értéket.</span><span class="sxs-lookup"><span data-stu-id="36b96-122">The default parameter set uses default values for parameters if the user does not provide one for them.</span></span> <span data-ttu-id="36b96-123">A használt alapértelmezett értékekről az alábbi paraméterek leírásában olvashat bővebben.</span><span class="sxs-lookup"><span data-stu-id="36b96-123">For more information on the default values used, please see the description for the given parameters below.</span></span>
<span data-ttu-id="36b96-124">Ez a parancsmag képes szerepkört rendelni a egyszerű szolgáltatásnévhez a paraméterekkel és paraméterekkel; ha egyik paraméter sem áll rendelkezésre, a rendszer nem rendel szerepkört a `Role` `Scope` szolgáltatásnévhez.</span><span class="sxs-lookup"><span data-stu-id="36b96-124">This cmdlet has the ability to assign a role to the service principal with the `Role` and `Scope` parameters; if neither of these parameters are provided, no role will be assigned to the service principal.</span></span> <span data-ttu-id="36b96-125">A paraméterek és a közreműködői paraméterek alapértelmezett értékei a "Közreműködő" és az aktuális előfizetés ( megjegyzés: az alapértelmezett értékeket csak akkor használja a rendszer, ha a felhasználó a két paraméter egyikének értéket ad meg, a másiknak azonban `Role` `Scope` nem).</span><span class="sxs-lookup"><span data-stu-id="36b96-125">The default values for the `Role` and `Scope` parameters are "Contributor" and the current subscription, respectively (_note_: the defaults are only used when the user provides a value for one of the two parameters, but not the other).</span></span>
<span data-ttu-id="36b96-126">A parancsmag ezenkívül implicit módon létrehoz egy alkalmazást, és beállítja a tulajdonságait (ha az ApplicationId nincs megtéve).</span><span class="sxs-lookup"><span data-stu-id="36b96-126">The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span> <span data-ttu-id="36b96-127">Az alkalmazásspecifikus paraméterek frissítéséhez használja az Set-AzADApplication parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="36b96-127">In order to update the application specific parameters please use Set-AzADApplication cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="36b96-128">Amikor egyszerű szolgáltatást hoz létre a **New-AzADServicePrincipal** paranccsal, a kimenet azokat a hitelesítő adatokat tartalmazza, amelyek védelmét meg kell védenie.</span><span class="sxs-lookup"><span data-stu-id="36b96-128">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="36b96-129">Másik lehetőségként fontolja meg felügyelt [identitások használatát](/azure/active-directory/managed-identities-azure-resources/overview) a hitelesítő adatok használatának elkerülése érdekében.</span><span class="sxs-lookup"><span data-stu-id="36b96-129">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="36b96-130">A **New-AzADServicePrincipal** alapértelmezés szerint [](/azure/role-based-access-control/built-in-roles#contributor) hozzárendeli a közreműködői szerepkört a szolgáltatásnévhez az előfizetés hatókörében.</span><span class="sxs-lookup"><span data-stu-id="36b96-130">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="36b96-131">Ha csökkenteni szeretne egy feltört szolgáltatásnév kockázatát, rendeljen hozzá egy konkrétabb szerepkört, és szűkítse a hatókört egy erőforrás- vagy erőforráscsoportra.</span><span class="sxs-lookup"><span data-stu-id="36b96-131">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="36b96-132">További [információt a Lépések a szerepkör-hozzárendelés](/azure/role-based-access-control/role-assignments-steps) hozzáadásához.</span><span class="sxs-lookup"><span data-stu-id="36b96-132">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="36b96-133">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="36b96-133">EXAMPLES</span></span>

### <span data-ttu-id="36b96-134">1. példa – Egyszerű AD szolgáltatásnév létrehozása</span><span class="sxs-lookup"><span data-stu-id="36b96-134">Example 1 - Simple AD service principal creation</span></span>

```
PS C:\> New-AzADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="36b96-135">A fenti parancs létrehoz egy egyszerű AD-szolgáltatást, amely a nem megadott paraméterek alapértelmezett értékeit használja.</span><span class="sxs-lookup"><span data-stu-id="36b96-135">The above command creates an AD service principal using default values for parameters not provided.</span></span> <span data-ttu-id="36b96-136">Mivel nem adott meg alkalmazásazonosítót, a rendszer létrehozott egy alkalmazást a szolgáltatásnévhez.</span><span class="sxs-lookup"><span data-stu-id="36b96-136">Since an application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="36b96-137">Mivel nem adott meg értéket a szolgáltatáshoz, a létrehozott egyszerű `Role` `Scope` szolgáltatásnévnek nincs engedélye.</span><span class="sxs-lookup"><span data-stu-id="36b96-137">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="36b96-138">2. példa: Egyszerű AD szolgáltatásnév létrehozása megadott szerepkörrel és alapértelmezett hatókörrel</span><span class="sxs-lookup"><span data-stu-id="36b96-138">Example 2 - Simple AD service principal creation with a specified role and default scope</span></span>

```
PS C:\> New-AzADServicePrincipal -Role Reader

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz' to the new service principal.
```

<span data-ttu-id="36b96-139">A fenti parancs létrehoz egy egyszerű AD-szolgáltatást, amely a nem megadott paraméterek alapértelmezett értékeit használja.</span><span class="sxs-lookup"><span data-stu-id="36b96-139">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="36b96-140">Mivel az alkalmazásazonosítót nem biztosította, a rendszer létrehozott egy alkalmazást a szolgáltatásnévhez.</span><span class="sxs-lookup"><span data-stu-id="36b96-140">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="36b96-141">A szolgáltatásnév "Olvasó" engedélyekkel lett létrehozva az aktuális előfizetés fölött (mivel a paraméterhez nem lett `Scope` megadva érték).</span><span class="sxs-lookup"><span data-stu-id="36b96-141">The service principal was created with "Reader" permissions over the current subscription (since no value was provided for the `Scope` parameter).</span></span>

### <span data-ttu-id="36b96-142">3. példa: Egyszerű AD szolgáltatásnév létrehozása meghatározott hatókörű és alapértelmezett szerepkörrel</span><span class="sxs-lookup"><span data-stu-id="36b96-142">Example 3 - Simple AD service principal creation with a specified scope and default role</span></span>

```
PS C:\> New-AzADServicePrincipal -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="36b96-143">A fenti parancs létrehoz egy egyszerű AD-szolgáltatást, amely a nem megadott paraméterek alapértelmezett értékeit használja.</span><span class="sxs-lookup"><span data-stu-id="36b96-143">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="36b96-144">Mivel az alkalmazásazonosítót nem biztosította, a rendszer létrehozott egy alkalmazást a szolgáltatásnévhez.</span><span class="sxs-lookup"><span data-stu-id="36b96-144">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="36b96-145">A szolgáltatásnév "Közreműködői" engedélyekkel lett létrehozva (mivel a paraméterhez nem lett megadva `Role` érték) a megadott erőforráscsoport hatóköre alapján.</span><span class="sxs-lookup"><span data-stu-id="36b96-145">The service principal was created with "Contributor" permissions (since no value was provided for the `Role` parameter) over the provided resource group scope.</span></span>

### <span data-ttu-id="36b96-146">4. példa : Egyszerű AD szolgáltatásnév létrehozása meghatározott hatókörű és szerepkörű szolgáltatásnévvel</span><span class="sxs-lookup"><span data-stu-id="36b96-146">Example 4 - Simple AD service principal creation with a specified scope and role</span></span>

```
PS C:\> New-AzADServicePrincipal -Role Reader -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="36b96-147">A fenti parancs létrehoz egy egyszerű AD-szolgáltatást, amely a nem megadott paraméterek alapértelmezett értékeit használja.</span><span class="sxs-lookup"><span data-stu-id="36b96-147">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="36b96-148">Mivel az alkalmazásazonosítót nem biztosította, a rendszer létrehozott egy alkalmazást a szolgáltatásnévhez.</span><span class="sxs-lookup"><span data-stu-id="36b96-148">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="36b96-149">A szolgáltatásnév "Olvasó" engedélyekkel lett létrehozva a megadott erőforráscsoport hatókörében.</span><span class="sxs-lookup"><span data-stu-id="36b96-149">The service principal was created with "Reader" permissions over the provided resource group scope.</span></span>

### <span data-ttu-id="36b96-150">5. példa : Új AD szolgáltatásnév létrehozása szerepkör-hozzárendeléssel használt alkalmazásazonosító használatával</span><span class="sxs-lookup"><span data-stu-id="36b96-150">Example 5 - Create a new AD service principal using application id with role assignment</span></span>

```
PS C:\> New-AzADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="36b96-151">Létrehoz egy új AD-szolgáltatásnév a (34a28ad2-dec4-4a41-bc3b-d22ddf90000e) azonosítójú alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="36b96-151">Creates a new AD service principal for the application with application id '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span></span> <span data-ttu-id="36b96-152">Mivel nem adott meg értéket a szolgáltatáshoz, a létrehozott egyszerű `Role` `Scope` szolgáltatásnévnek nincs engedélye.</span><span class="sxs-lookup"><span data-stu-id="36b96-152">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="36b96-153">6. példa: Új AD szolgáltatásnév létrehozása pipázás használatával</span><span class="sxs-lookup"><span data-stu-id="36b96-153">Example 6 - Create a new AD service principal using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

<span data-ttu-id="36b96-154">A (3ede3c26-b443-4e0b-9efc-b05e68338dc3) objektumazonosítóval és a New-AzADServicePrincipal-parancsmaghoz vezető új AD-szolgáltatásnév létrehozásához szükségescsöveket használja.</span><span class="sxs-lookup"><span data-stu-id="36b96-154">Gets the application with object id '3ede3c26-b443-4e0b-9efc-b05e68338dc3' and pipes that to the New-AzADServicePrincipal cmdlet to create a new AD service principal for that application.</span></span>

### <span data-ttu-id="36b96-155">7. példa: Új AD szolgáltatásnév létrehozása a DisplayName és a jelszó használatával</span><span class="sxs-lookup"><span data-stu-id="36b96-155">Example 7 - Create a new AD service principal using DisplayName and password credential</span></span>

```
PS C:\> $credentials = New-Object -TypeName Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password="StrongPassworld!23"}
PS C:\> $sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials

ServicePrincipalNames : {exxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxc, http://ServicePrincipalName}
ApplicationId         : exxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxcc
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 6xxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxb
Type                  :
```

<span data-ttu-id="36b96-156">Létrehoz egy új alkalmazást a "ServicePrincipalName" névvel és a "StrongPassworld!23" jelszóval, és létrehozza az egyszerű szolgáltatásnevet az éppen létrehozott alkalmazás alapján.</span><span class="sxs-lookup"><span data-stu-id="36b96-156">Creates a new application with name "ServicePrincipalName" and password "StrongPassworld!23" and creates the service principal based on the application just created.</span></span> <span data-ttu-id="36b96-157">A rendszer hozzáadja a kezdő dátumot és a záró dátumot a jelszó hitelesítő adataihoz.</span><span class="sxs-lookup"><span data-stu-id="36b96-157">The start date and end date are added to password credential.</span></span>

### <span data-ttu-id="36b96-158">8. példa: Új AD szolgáltatásnév létrehozása a DisplayName és az egyszerű kulcs hitelesítő adataival</span><span class="sxs-lookup"><span data-stu-id="36b96-158">Example 8 - Create a new AD service principal using DisplayName and plain key credential</span></span>

```
PS C:\> $cert = <public certificate as base64-encoded string>
PS C:\> $sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert  -EndDate "2021-01-01"

ServicePrincipalNames : {cxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxx6, http://ServicePrincipalName}
ApplicationId         : cxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxx6
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : cxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxc
Type                  :
```

<span data-ttu-id="36b96-159">Létrehoz egy új alkalmazást "ServicePrincipalName" és certifcate "$cert" névvel, és létrehozza a szolgáltatásnevet az éppen létrehozott alkalmazás alapján.</span><span class="sxs-lookup"><span data-stu-id="36b96-159">Creates a new application with name "ServicePrincipalName" and certifcate "$cert" and creates the service principal based on the application just created.</span></span> <span data-ttu-id="36b96-160">A rendszer hozzáadja a záró dátumot a kulcs hitelesítő adataihoz.</span><span class="sxs-lookup"><span data-stu-id="36b96-160">The end date is added to key credential.</span></span>

## <span data-ttu-id="36b96-161">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36b96-161">PARAMETERS</span></span>

### <span data-ttu-id="36b96-162">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="36b96-162">-ApplicationId</span></span>
<span data-ttu-id="36b96-163">A bérlői webhelyen egy egyszerű szolgáltatásnév egyedi alkalmazásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="36b96-163">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="36b96-164">A tulajdonság létrehozása után ezt a tulajdonságot nem lehet módosítani.</span><span class="sxs-lookup"><span data-stu-id="36b96-164">Once created this property cannot be changed.</span></span>
<span data-ttu-id="36b96-165">Ha nincs megadva alkalmazásazonosító, létrejön egy.</span><span class="sxs-lookup"><span data-stu-id="36b96-165">If an application id is not specified, one will be generated.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationWithoutCredentialParameterSet, ApplicationWithPasswordPlainParameterSet, ApplicationWithPasswordCredentialParameterSet, ApplicationWithKeyPlainParameterSet, ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b96-166">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="36b96-166">-ApplicationObject</span></span>
<span data-ttu-id="36b96-167">Az az objektum, amely azt az alkalmazást képviseli, amelyhez a szolgáltatásnév létre van hozva.</span><span class="sxs-lookup"><span data-stu-id="36b96-167">The object representing the application for which the service principal is created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36b96-168">-CertValue</span><span class="sxs-lookup"><span data-stu-id="36b96-168">-CertValue</span></span>
<span data-ttu-id="36b96-169">Az "aszimmetrikus" hitelesítőadat-típus értéke.</span><span class="sxs-lookup"><span data-stu-id="36b96-169">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="36b96-170">A 64-es alapkódolt tanúsítványt képviseli.</span><span class="sxs-lookup"><span data-stu-id="36b96-170">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36b96-171">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36b96-171">-DefaultProfile</span></span>
<span data-ttu-id="36b96-172">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="36b96-172">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b96-173">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="36b96-173">-DisplayName</span></span>
<span data-ttu-id="36b96-174">A szolgáltatásnév rövid neve.</span><span class="sxs-lookup"><span data-stu-id="36b96-174">The friendly name of the service principal.</span></span> <span data-ttu-id="36b96-175">Ha nincs megjelölve megjelenítendő név, ez az érték alapértelmezés szerint az "azure-powershell-MM-dd-yyyy-HH-mm-mm-mm", ahol az utótag az alkalmazás létrehozásának ideje.</span><span class="sxs-lookup"><span data-stu-id="36b96-175">If a display name is not provided, this value will default to 'azure-powershell-MM-dd-yyyy-HH-mm-ss', where the suffix is the time of application creation.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DisplayNameWithoutCredentialParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithPasswordCredentialParameterSet, DisplayNameWithKeyPlainParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b96-176">-EndDate</span><span class="sxs-lookup"><span data-stu-id="36b96-176">-EndDate</span></span>
<span data-ttu-id="36b96-177">A hitelesítő adatok használatának tényleges záró dátuma.</span><span class="sxs-lookup"><span data-stu-id="36b96-177">The effective end date of the credential usage.</span></span>
<span data-ttu-id="36b96-178">Az alapértelmezett záró dátum egy év a mai naptól.</span><span class="sxs-lookup"><span data-stu-id="36b96-178">The default end date value is one year from today.</span></span> <span data-ttu-id="36b96-179">Az "aszimmetrikus" típusú hitelesítő adatoknál ezt az X509-tanúsítvány érvényességének dátumán vagy azt megelőzően kell megadni.</span><span class="sxs-lookup"><span data-stu-id="36b96-179">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b96-180">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="36b96-180">-KeyCredential</span></span>
<span data-ttu-id="36b96-181">Az alkalmazáshoz társított kulcs hitelesítő adatok gyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="36b96-181">The collection of key credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationObjectWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36b96-182">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="36b96-182">-PasswordCredential</span></span>
<span data-ttu-id="36b96-183">Az alkalmazáshoz társított jelszó-hitelesítő adatok gyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="36b96-183">The collection of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationObjectWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36b96-184">-Szerepkör</span><span class="sxs-lookup"><span data-stu-id="36b96-184">-Role</span></span>
<span data-ttu-id="36b96-185">Az egyszerű szolgáltatásnév szerepköre a hatókörben.</span><span class="sxs-lookup"><span data-stu-id="36b96-185">The role that the service principal has over the scope.</span></span> <span data-ttu-id="36b96-186">Ha a megadott érték meg van jelölve, de nincs megjelölve érték, akkor alapértelmezés szerint a `Scope` `Role` `Role` "Közreműködő" szerepkört használja.</span><span class="sxs-lookup"><span data-stu-id="36b96-186">If a value for `Scope` is provided, but no value is provided for `Role`, then `Role` will default to the 'Contributor' role.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b96-187">-Scope</span><span class="sxs-lookup"><span data-stu-id="36b96-187">-Scope</span></span>
<span data-ttu-id="36b96-188">Az a tartomány, amelyhez a egyszerű szolgáltatásnév rendelkezik engedélyekkel.</span><span class="sxs-lookup"><span data-stu-id="36b96-188">The scope that the service principal has permissions on.</span></span> <span data-ttu-id="36b96-189">Ha a megadott érték meg van jelölve, de nincs megjelölve érték, akkor az alapértelmezett érték az `Role` `Scope` aktuális `Scope` előfizetés.</span><span class="sxs-lookup"><span data-stu-id="36b96-189">If a value for `Role` is provided, but no value is provided for `Scope`, then `Scope` will default to the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b96-190">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="36b96-190">-SkipAssignment</span></span>
<span data-ttu-id="36b96-191">Ha be van állítva, a rendszer kihagyja az egyszerű szolgáltatásnév alapértelmezett szerepkör-hozzárendelésének létrehozását.</span><span class="sxs-lookup"><span data-stu-id="36b96-191">If set, will skip creating the default role assignment for the service principal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b96-192">-StartDate</span><span class="sxs-lookup"><span data-stu-id="36b96-192">-StartDate</span></span>
<span data-ttu-id="36b96-193">A hitelesítő adatok használatának tényleges kezdő dátuma.</span><span class="sxs-lookup"><span data-stu-id="36b96-193">The effective start date of the credential usage.</span></span>
<span data-ttu-id="36b96-194">A kezdő dátum alapértelmezett értéke a mai nap.</span><span class="sxs-lookup"><span data-stu-id="36b96-194">The default start date value is today.</span></span> <span data-ttu-id="36b96-195">Az "aszimmetrikus" típusú hitelesítő adatoknál ezt az X509-tanúsítvány érvényességének dátumán vagy azt követően kell megadni.</span><span class="sxs-lookup"><span data-stu-id="36b96-195">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b96-196">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36b96-196">-Confirm</span></span>
<span data-ttu-id="36b96-197">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="36b96-197">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b96-198">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36b96-198">-WhatIf</span></span>
<span data-ttu-id="36b96-199">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="36b96-199">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36b96-200">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="36b96-200">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b96-201">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36b96-201">CommonParameters</span></span>
<span data-ttu-id="36b96-202">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36b96-202">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36b96-203">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36b96-203">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36b96-204">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36b96-204">INPUTS</span></span>

### <span data-ttu-id="36b96-205">System.Guid</span><span class="sxs-lookup"><span data-stu-id="36b96-205">System.Guid</span></span>

### <span data-ttu-id="36b96-206">System.String</span><span class="sxs-lookup"><span data-stu-id="36b96-206">System.String</span></span>

### <span data-ttu-id="36b96-207">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="36b96-207">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="36b96-208">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span><span class="sxs-lookup"><span data-stu-id="36b96-208">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="36b96-209">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span><span class="sxs-lookup"><span data-stu-id="36b96-209">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="36b96-210">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="36b96-210">System.DateTime</span></span>

## <span data-ttu-id="36b96-211">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36b96-211">OUTPUTS</span></span>

### <span data-ttu-id="36b96-212">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="36b96-212">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="36b96-213">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="36b96-213">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="36b96-214">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="36b96-214">NOTES</span></span>
<span data-ttu-id="36b96-215">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, telepítés</span><span class="sxs-lookup"><span data-stu-id="36b96-215">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="36b96-216">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36b96-216">RELATED LINKS</span></span>

[<span data-ttu-id="36b96-217">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="36b96-217">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="36b96-218">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="36b96-218">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="36b96-219">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="36b96-219">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="36b96-220">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="36b96-220">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="36b96-221">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="36b96-221">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="36b96-222">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="36b96-222">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="36b96-223">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="36b96-223">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

