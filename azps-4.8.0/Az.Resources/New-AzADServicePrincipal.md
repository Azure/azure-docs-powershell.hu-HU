---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: 3c96ab0cdcc25e0e1c9b4a343cd68420654d934c
ms.sourcegitcommit: 375232b84336ef5e13052504deaa43f5bd4b7f65
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/05/2020
ms.locfileid: "94303974"
---
# <span data-ttu-id="89169-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="89169-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="89169-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="89169-102">SYNOPSIS</span></span>
<span data-ttu-id="89169-103">Új Azure Active Directory-szolgáltató létrehozása.</span><span class="sxs-lookup"><span data-stu-id="89169-103">Creates a new Azure active directory service principal.</span></span>

## <span data-ttu-id="89169-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="89169-104">SYNTAX</span></span>

### <span data-ttu-id="89169-105">SimpleParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="89169-105">SimpleParameterSet (Default)</span></span>

```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89169-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="89169-106">ApplicationWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="89169-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="89169-107">ApplicationWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89169-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="89169-108">ApplicationWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89169-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="89169-109">ApplicationWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89169-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="89169-110">ApplicationWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89169-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="89169-111">DisplayNameWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="89169-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="89169-112">DisplayNameWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89169-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="89169-113">DisplayNameWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89169-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="89169-114">DisplayNameWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89169-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="89169-115">DisplayNameWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89169-116">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="89169-116">ApplicationObjectWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89169-117">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="89169-117">ApplicationObjectWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89169-118">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="89169-118">ApplicationObjectWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89169-119">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="89169-119">ApplicationObjectWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89169-120">Leírás</span><span class="sxs-lookup"><span data-stu-id="89169-120">DESCRIPTION</span></span>

<span data-ttu-id="89169-121">Új Azure Active Directory-szolgáltató létrehozása.</span><span class="sxs-lookup"><span data-stu-id="89169-121">Creates a new Azure active directory service principal.</span></span> <span data-ttu-id="89169-122">Az alapértelmezett paraméterérték a paraméterek alapértelmezett értékeit használja, ha azok nincsenek megadva.</span><span class="sxs-lookup"><span data-stu-id="89169-122">The default parameter set uses default values for parameters if they are not provided.</span></span> <span data-ttu-id="89169-123">Az alapértelmezett értékekről további információt az egyes paraméterek leírása című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="89169-123">For more information on default values, see the description for each parameter.</span></span> <span data-ttu-id="89169-124">Ezzel a parancsmaggal a **szerepkör** és a **hatókör** paraméterrel társíthat szerepkört a szolgáltatóhoz.</span><span class="sxs-lookup"><span data-stu-id="89169-124">This cmdlet has the ability to assign a role to the service principal with the **Role** and **Scope** parameters.</span></span> <span data-ttu-id="89169-125">Ha mindkettő nincs kihagyva, a közreműködői szerepkör a szolgáltatóhoz van társítva.</span><span class="sxs-lookup"><span data-stu-id="89169-125">If both are omitted, the contributor role is assigned to the service principal.</span></span> <span data-ttu-id="89169-126">A **szerepkör** és a **hatókör** paramétereinek alapértelmezett értékei az aktuális előfizetéshez **közreműködők** .</span><span class="sxs-lookup"><span data-stu-id="89169-126">The default values for the **Role** and **Scope** parameters are **Contributor** for the current subscription.</span></span> <span data-ttu-id="89169-127">A parancsmag létrehoz egy alkalmazást, és beállítja a tulajdonságait, ha nincs megadva ApplicationId.</span><span class="sxs-lookup"><span data-stu-id="89169-127">The cmdlet creates an application and sets its properties if an ApplicationId is not provided.</span></span> <span data-ttu-id="89169-128">Az alkalmazásspecifikus paraméterek frissítéséhez használja az [Update-AzADApplication](./update-azadapplication.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="89169-128">To update the application-specific parameters, use the [Update-AzADApplication](./update-azadapplication.md) cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="89169-129">Ha a **New-AzADServicePrincipal** parancs segítségével hoz létre egy egyszerű szolgáltatásnevet, a kimenet tartalmazza a védelemmel ellátott hitelesítő adatokat is.</span><span class="sxs-lookup"><span data-stu-id="89169-129">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="89169-130">Ügyeljen arra, hogy ne szerepeljenek ezek a hitelesítő adatok a kódban, vagy ellenőrizze a hitelesítő adatokat a forrás vezérlőben.</span><span class="sxs-lookup"><span data-stu-id="89169-130">Be sure that you do not include these credentials in your code or check the credentials into your source control.</span></span> <span data-ttu-id="89169-131">A [felügyelt identitások](/azure/active-directory/managed-identities-azure-resources/overview) használata helyett érdemes lehet használni a hitelesítő adatok használatát.</span><span class="sxs-lookup"><span data-stu-id="89169-131">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="89169-132">A **New-AzADServicePrincipal** alapértelmezés szerint a [munkatárs](/azure/role-based-access-control/built-in-roles#contributor) szerepkört rendeli hozzá az előfizetési tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="89169-132">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="89169-133">Ha csökkenteni szeretné a kiegyezéssel járó megbízó kockázatát, rendeljen hozzá egy specifikusabb szerepkört, és szűkítse a hatókört egy erőforrás vagy erőforrás csoportba.</span><span class="sxs-lookup"><span data-stu-id="89169-133">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="89169-134">További információért tekintse át [a szerepkör-hozzárendelés hozzáadásának lépéseit](/azure/role-based-access-control/role-assignments-steps) .</span><span class="sxs-lookup"><span data-stu-id="89169-134">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="89169-135">Példák</span><span class="sxs-lookup"><span data-stu-id="89169-135">EXAMPLES</span></span>

### <span data-ttu-id="89169-136">Példa 1: Simple AD Service Principal Creation</span><span class="sxs-lookup"><span data-stu-id="89169-136">Example 1: Simple AD service principal creation</span></span>

<span data-ttu-id="89169-137">Az alábbi példa létrehoz egy AD-szolgáltatót, amely a nem meghatározott paraméterek alapértelmezett értékeit használja.</span><span class="sxs-lookup"><span data-stu-id="89169-137">The following example creates an AD service principal using default values for parameters not specified.</span></span> <span data-ttu-id="89169-138">Mivel egy alkalmazás-azonosító nincs megadva, létrejön egy alkalmazás a szolgáltatási megbízó számára.</span><span class="sxs-lookup"><span data-stu-id="89169-138">Since an application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="89169-139">Mivel a **szerepkörhöz** vagy a **hatókörhöz** nincs megadva érték, a létrehozta a szolgáltató a jelenlegi előfizetés **közreműködői** szerepkörét kapja.</span><span class="sxs-lookup"><span data-stu-id="89169-139">Since no values are provided for **Role** or **Scope** , the created service principal is assigned the **contributor** role for the current subscription.</span></span>

```powershell
New-AzADServicePrincipal
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal
```

### <span data-ttu-id="89169-140">2. példa: egyszerű AD-szolgáltatás egyszerű létrehozása megadott szerepkörrel és alapértelmezett hatókörrel</span><span class="sxs-lookup"><span data-stu-id="89169-140">Example 2: Simple AD service principal creation with a specified role and default scope</span></span>

<span data-ttu-id="89169-141">Az alábbi példa létrehoz egy AD-szolgáltatót, amely a nem meghatározott paraméterek alapértelmezett értékeit használja.</span><span class="sxs-lookup"><span data-stu-id="89169-141">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="89169-142">Mivel az alkalmazás-azonosító nincs megadva, létrejön egy alkalmazás a szolgáltatási megbízó számára.</span><span class="sxs-lookup"><span data-stu-id="89169-142">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="89169-143">A Service Principal a jelenlegi előfizetéshez tartozó **olvasói** engedélyekkel jön létre, mivel a **hatókör** paraméter nem rendelkezik értékkel.</span><span class="sxs-lookup"><span data-stu-id="89169-143">The service principal is created with **Reader** permissions for the current subscription since no value is provided for the **Scope** parameter.</span></span>

```powershell
New-AzADServicePrincipal -Role Reader
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/00000000-0000-0000-0000-000000000000' to the new service principal.
```

### <span data-ttu-id="89169-144">3. példa: egyszerű AD-szolgáltatás – egyszerű létrehozás meghatározott hatókör és alapértelmezett szerepkörrel</span><span class="sxs-lookup"><span data-stu-id="89169-144">Example 3: Simple AD service principal creation with a specified scope and default role</span></span>

<span data-ttu-id="89169-145">Az alábbi példa létrehoz egy AD-szolgáltatót, amely a nem meghatározott paraméterek alapértelmezett értékeit használja.</span><span class="sxs-lookup"><span data-stu-id="89169-145">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="89169-146">Mivel az alkalmazás-azonosító nincs megadva, létrejön egy alkalmazás a szolgáltatási megbízó számára.</span><span class="sxs-lookup"><span data-stu-id="89169-146">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="89169-147">A szervizszerződés a megadott erőforráscsoport-tartomány **közreműködői** engedélyeivel jön létre, mivel a **role** paraméterhez nincs megadva érték.</span><span class="sxs-lookup"><span data-stu-id="89169-147">The service principal is created with **Contributor** permissions for the provided resource group scope since no value is provided for the **Role** parameter.</span></span>

```powershell
New-AzADServicePrincipal -Scope /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup' to the new service principal.
```

### <span data-ttu-id="89169-148">Példa 4: egyszerű AD-szolgáltatás egyszerű létrehozása megadott hatókörrel és szerepkörrel</span><span class="sxs-lookup"><span data-stu-id="89169-148">Example 4: Simple AD service principal creation with a specified scope and role</span></span>

<span data-ttu-id="89169-149">Az alábbi példa létrehoz egy AD-szolgáltatót, amely a nem meghatározott paraméterek alapértelmezett értékeit használja.</span><span class="sxs-lookup"><span data-stu-id="89169-149">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="89169-150">Mivel az alkalmazás-azonosító nincs megadva, létrejön egy alkalmazás a szolgáltatási megbízó számára.</span><span class="sxs-lookup"><span data-stu-id="89169-150">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="89169-151">A Service Principal a megadott erőforráscsoport-hatókörhöz tartozó **olvasói** engedélyekkel jön létre.</span><span class="sxs-lookup"><span data-stu-id="89169-151">The service principal is created with **Reader** permissions for the provided resource group scope.</span></span>

```powershell
New-AzADServicePrincipal -Role Reader -Scope /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup' to the new service principal.
```

### <span data-ttu-id="89169-152">Példa 5: új AD Service-szolgáltató létrehozása alkalmazásspecifikus AZONOSÍTÓval szerepkör-hozzárendeléssel</span><span class="sxs-lookup"><span data-stu-id="89169-152">Example 5: Create a new AD service principal using application ID with role assignment</span></span>

<span data-ttu-id="89169-153">Az alábbi példa létrehoz egy új AD-szolgáltatót az alkalmazáshoz a ' 00000000-0000-0000-0000-000000000000 ' AZONOSÍTÓJÚ alkalmazással.</span><span class="sxs-lookup"><span data-stu-id="89169-153">The following example creates a new AD service principal for the application with application ID '00000000-0000-0000-0000-000000000000'.</span></span> <span data-ttu-id="89169-154">Mivel a **szerepkörhöz** vagy a **hatókörhöz** nincs megadva érték, a létrehozta a szolgáltató a jelenlegi előfizetés **közreműködői** szerepkörét kapja.</span><span class="sxs-lookup"><span data-stu-id="89169-154">Since no values are provided for **Role** or **Scope** , the created service principal is assigned the **contributor** role for the current subscription.</span></span>

```powershell
New-AzADServicePrincipal -ApplicationId 00000000-0000-0000-0000-000000000000
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://my-temp-app}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : my-temp-app
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal
```

### <span data-ttu-id="89169-155">6. példa: új AD-szolgáltató létrehozása csővezetékek használatával</span><span class="sxs-lookup"><span data-stu-id="89169-155">Example 6: Create a new AD service principal using piping</span></span>

<span data-ttu-id="89169-156">Az alábbi példa beolvassa az "3ede3c26-b443-4e0b-9efc-b05e68338dc3" AZONOSÍTÓJÚ alkalmazást a [Get-AzADApplication](./get-azadapplication.md) parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="89169-156">The following example retrieves the application with object ID '3ede3c26-b443-4e0b-9efc-b05e68338dc3' using the [Get-AzADApplication](./get-azadapplication.md) cmdlet.</span></span> <span data-ttu-id="89169-157">Az eredmény az, hogy a `New-AzADServicePrincipal` parancsmag segítségével új ad-szolgáltatót hoz létre ahhoz az alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="89169-157">The results are piped to the `New-AzADServicePrincipal` cmdlet to create a new AD service principal for that application.</span></span>

```powershell
Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

### <span data-ttu-id="89169-158">7. példa: új AD Service Principal létrehozása a DisplayName és a jelszó hitelesítő adataival</span><span class="sxs-lookup"><span data-stu-id="89169-158">Example 7: Create a new AD service principal using DisplayName and password credential</span></span>

<span data-ttu-id="89169-159">Az alábbi példa új alkalmazást hoz létre a **ServicePrincipalName** név és a **StrongPassworld! 23** jelszóval.</span><span class="sxs-lookup"><span data-stu-id="89169-159">The following example creates a new application with the name **ServicePrincipalName** and a password of **StrongPassworld!23**.</span></span> <span data-ttu-id="89169-160">Ezt a szolgáltatást a létrehozta alkalmazás alapján hozza létre.</span><span class="sxs-lookup"><span data-stu-id="89169-160">It creates the service principal based on the created application.</span></span> <span data-ttu-id="89169-161">A program hozzáadja a kezdési és a befejezési dátumot a jelszó-hitelesítő adatokhoz.</span><span class="sxs-lookup"><span data-stu-id="89169-161">The start date and end date are added to the password credential.</span></span>

```powershell
$credentials = New-Object -TypeName Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{
  StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password='StrongPassworld!23'}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://ServicePrincipalName}
ApplicationId         : 00000000-0000-0000-0000-000000000000c
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 00000000-0000-0000-0000-000000000000
Type                  :
```

### <span data-ttu-id="89169-162">8. példa: új AD-szolgáltató létrehozása a DisplayName és az egyszerű kulcs hitelesítő adataival</span><span class="sxs-lookup"><span data-stu-id="89169-162">Example 8: Create a new AD service principal using DisplayName and plain key credential</span></span>

<span data-ttu-id="89169-163">Az alábbi példa egy új alkalmazást hoz létre a name **ServicePrincipalName** és egy tanúsítvány **$CERT**. Létrehozza a szolgáltatásnevet a létrehozott alkalmazás alapján.</span><span class="sxs-lookup"><span data-stu-id="89169-163">The following example creates a new application with the name **ServicePrincipalName** and a certificate **$cert**. It creates the service principal based on the application created.</span></span> <span data-ttu-id="89169-164">A befejezési dátum hozzáadódik a legfontosabb hitelesítő adatokhoz.</span><span class="sxs-lookup"><span data-stu-id="89169-164">The end date is added to key credential.</span></span>

```powershell
$cert = 'public certificate as Base64 encoded string'
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert  -EndDate '2021-01-01'
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://ServicePrincipalName}
ApplicationId         : 00000000-0000-0000-0000-000000000000
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 00000000-0000-0000-0000-000000000000
Type                  :
```

## <span data-ttu-id="89169-165">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="89169-165">PARAMETERS</span></span>

### <span data-ttu-id="89169-166">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="89169-166">-ApplicationId</span></span>

<span data-ttu-id="89169-167">Egy szolgáltató egyedi alkalmazásspecifikus azonosítója bérlői fiókban.</span><span class="sxs-lookup"><span data-stu-id="89169-167">The unique application ID for a service principal in a tenant.</span></span> <span data-ttu-id="89169-168">Miután létrehozta ezt a tulajdonságot, nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="89169-168">Once created this property cannot be changed.</span></span> <span data-ttu-id="89169-169">Ha egy meglévő alkalmazáshoz egy alkalmazás-azonosító nincs megadva, létrejön egy alkalmazás.</span><span class="sxs-lookup"><span data-stu-id="89169-169">If an application ID for an existing application is not specified, an application is created.</span></span>

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

### <span data-ttu-id="89169-170">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="89169-170">-ApplicationObject</span></span>

<span data-ttu-id="89169-171">Annak az alkalmazásnak az objektuma, amelybe a szolgáltatásnevet létrehozta.</span><span class="sxs-lookup"><span data-stu-id="89169-171">The object representing the application for which the service principal is created.</span></span>

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

### <span data-ttu-id="89169-172">-CertValue</span><span class="sxs-lookup"><span data-stu-id="89169-172">-CertValue</span></span>

<span data-ttu-id="89169-173">Az aszimmetrikus hitelesítőadat-típus értéke.</span><span class="sxs-lookup"><span data-stu-id="89169-173">The value of the asymmetric credential type.</span></span> <span data-ttu-id="89169-174">A Base64 kódolású tanúsítványt képviseli.</span><span class="sxs-lookup"><span data-stu-id="89169-174">It represents the Base64 encoded certificate.</span></span>

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

### <span data-ttu-id="89169-175">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89169-175">-DefaultProfile</span></span>

<span data-ttu-id="89169-176">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="89169-176">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89169-177">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="89169-177">-DisplayName</span></span>

<span data-ttu-id="89169-178">A szolgáltatás megbízójának rövid neve.</span><span class="sxs-lookup"><span data-stu-id="89169-178">The friendly name of the service principal.</span></span> <span data-ttu-id="89169-179">Ha a megjelenítendő név nem látható, akkor ez az érték alapértelmezés szerint az **Azure-PowerShell-hh-nn-éééé-hh-hh-hh-mm-mm** , ahol az utótag az alkalmazás létrehozásának időpontja.</span><span class="sxs-lookup"><span data-stu-id="89169-179">If a display name is not provided, this value will default to **azure-powershell-MM-dd-yyyy-HH-mm-ss** where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="89169-180">-EndDate</span><span class="sxs-lookup"><span data-stu-id="89169-180">-EndDate</span></span>

<span data-ttu-id="89169-181">A hitelesítő adatok használatának tényleges befejezési dátuma.</span><span class="sxs-lookup"><span data-stu-id="89169-181">The effective end date of the credential usage.</span></span> <span data-ttu-id="89169-182">Az alapértelmezett befejezési dátum értéke egy év a mai naptól számítva.</span><span class="sxs-lookup"><span data-stu-id="89169-182">The default end date value is one year from today.</span></span>
<span data-ttu-id="89169-183">Aszimmetrikus típusú hitelesítő adatok esetén ezt be kell állítani a X509 tanúsítvány érvényességi dátumának be vagy azt megelőzőre.</span><span class="sxs-lookup"><span data-stu-id="89169-183">For an asymmetric type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="89169-184">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="89169-184">-KeyCredential</span></span>

<span data-ttu-id="89169-185">Az alkalmazáshoz társított legfontosabb hitelesítő adatok gyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="89169-185">The collection of key credentials associated with the application.</span></span>

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

### <span data-ttu-id="89169-186">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="89169-186">-PasswordCredential</span></span>

<span data-ttu-id="89169-187">Az alkalmazáshoz társított jelszó-hitelesítő adatok gyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="89169-187">The collection of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="89169-188">-Role (szerepkör)</span><span class="sxs-lookup"><span data-stu-id="89169-188">-Role</span></span>

<span data-ttu-id="89169-189">Annak a szerepkörnek a szerepe, amelyet a szolgáltató a hatókör felett tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="89169-189">The role that the service principal has over the scope.</span></span> <span data-ttu-id="89169-190">Ha nincs megadva érték, akkor a **szerepkör** alapértelmezés szerint a **közreműködői** szerepkört kapja.</span><span class="sxs-lookup"><span data-stu-id="89169-190">If no value is provided, **Role** defaults to the **Contributor** role.</span></span>

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

### <span data-ttu-id="89169-191">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="89169-191">-Scope</span></span>

<span data-ttu-id="89169-192">Az a hatókör, amelyre a szolgáltatónak van engedélye.</span><span class="sxs-lookup"><span data-stu-id="89169-192">The scope that the service principal has permissions for.</span></span> <span data-ttu-id="89169-193">Ha nincs megadva érték, akkor az alapértelmezett hatókör az aktuális előfizetéshez **tartozik** .</span><span class="sxs-lookup"><span data-stu-id="89169-193">If no value is provided, **Scope** defaults to the current subscription.</span></span>

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

### <span data-ttu-id="89169-194">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="89169-194">-SkipAssignment</span></span>

<span data-ttu-id="89169-195">Ha be van állítva, ugorjon az alapértelmezett szerepkör-hozzárendelés létrehozásához a szolgáltatónál.</span><span class="sxs-lookup"><span data-stu-id="89169-195">If set, skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="89169-196">-StartDate</span><span class="sxs-lookup"><span data-stu-id="89169-196">-StartDate</span></span>

<span data-ttu-id="89169-197">A hitelesítő adatok használatának tényleges kezdési dátuma.</span><span class="sxs-lookup"><span data-stu-id="89169-197">The effective start date of the credential usage.</span></span> <span data-ttu-id="89169-198">A kezdő dátum alapértelmezett értéke ma.</span><span class="sxs-lookup"><span data-stu-id="89169-198">The default start date value is today.</span></span> <span data-ttu-id="89169-199">Aszimmetrikus típusú hitelesítő adatok esetében ezt be kell állítani a X509 tanúsítvány érvényességi dátumának be vagy mögé.</span><span class="sxs-lookup"><span data-stu-id="89169-199">For an asymmetric type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="89169-200">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="89169-200">-Confirm</span></span>

<span data-ttu-id="89169-201">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="89169-201">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89169-202">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89169-202">-WhatIf</span></span>

<span data-ttu-id="89169-203">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="89169-203">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="89169-204">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="89169-204">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89169-205">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89169-205">CommonParameters</span></span>
<span data-ttu-id="89169-206">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="89169-206">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89169-207">További információt a [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="89169-207">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>
## <span data-ttu-id="89169-208">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="89169-208">INPUTS</span></span>

### <span data-ttu-id="89169-209">System. GUID</span><span class="sxs-lookup"><span data-stu-id="89169-209">System.Guid</span></span>

### <span data-ttu-id="89169-210">System. String</span><span class="sxs-lookup"><span data-stu-id="89169-210">System.String</span></span>

### <span data-ttu-id="89169-211">Microsoft. Azure. Command. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="89169-211">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="89169-212">Microsoft. Azure. Command. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="89169-212">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="89169-213">Microsoft. Azure. Command. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="89169-213">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="89169-214">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="89169-214">System.DateTime</span></span>

## <span data-ttu-id="89169-215">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89169-215">OUTPUTS</span></span>

### <span data-ttu-id="89169-216">Microsoft. Azure. Command. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="89169-216">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="89169-217">Microsoft. Azure. Command. Resources. modellek. Authorization. PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="89169-217">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="89169-218">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="89169-218">NOTES</span></span>

<span data-ttu-id="89169-219">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="89169-219">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="89169-220">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89169-220">RELATED LINKS</span></span>

[<span data-ttu-id="89169-221">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="89169-221">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="89169-222">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="89169-222">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="89169-223">Új – AzADApplication</span><span class="sxs-lookup"><span data-stu-id="89169-223">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="89169-224">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="89169-224">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="89169-225">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="89169-225">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="89169-226">Új – AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="89169-226">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="89169-227">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="89169-227">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)
