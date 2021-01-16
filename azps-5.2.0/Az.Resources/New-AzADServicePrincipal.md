---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: 6d268c2378c93bcfb98e64c654880e8055bcede8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358061"
---
# <span data-ttu-id="41d13-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="41d13-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="41d13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41d13-102">SYNOPSIS</span></span>
<span data-ttu-id="41d13-103">Új Azure Active Directory-szolgáltatásnév létrehozása.</span><span class="sxs-lookup"><span data-stu-id="41d13-103">Creates a new Azure active directory service principal.</span></span>

## <span data-ttu-id="41d13-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="41d13-104">SYNTAX</span></span>

### <span data-ttu-id="41d13-105">SimpleParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="41d13-105">SimpleParameterSet (Default)</span></span>

```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41d13-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="41d13-106">ApplicationWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="41d13-107">ApplicationWithPasswordPmirParameterSet</span><span class="sxs-lookup"><span data-stu-id="41d13-107">ApplicationWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41d13-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="41d13-108">ApplicationWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41d13-109">ApplicationWithKeyPmirParameterSet</span><span class="sxs-lookup"><span data-stu-id="41d13-109">ApplicationWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41d13-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="41d13-110">ApplicationWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41d13-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="41d13-111">DisplayNameWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="41d13-112">DisplayNameWithPasswordPmirParameterSet</span><span class="sxs-lookup"><span data-stu-id="41d13-112">DisplayNameWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41d13-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="41d13-113">DisplayNameWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41d13-114">DisplayNameWithKeyPmirParameterSet</span><span class="sxs-lookup"><span data-stu-id="41d13-114">DisplayNameWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41d13-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="41d13-115">DisplayNameWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41d13-116">ApplicationObjectWithPasswordPmirParameterSet</span><span class="sxs-lookup"><span data-stu-id="41d13-116">ApplicationObjectWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41d13-117">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="41d13-117">ApplicationObjectWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41d13-118">ApplicationObjectWithKeyPmirParameterSet</span><span class="sxs-lookup"><span data-stu-id="41d13-118">ApplicationObjectWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41d13-119">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="41d13-119">ApplicationObjectWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41d13-120">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="41d13-120">DESCRIPTION</span></span>

<span data-ttu-id="41d13-121">Új Azure Active Directory-szolgáltatásnév létrehozása.</span><span class="sxs-lookup"><span data-stu-id="41d13-121">Creates a new Azure active directory service principal.</span></span> <span data-ttu-id="41d13-122">Az alapértelmezett paraméterkészlet alapértelmezett értékeket használ a paraméterekhez, ha nincsenek megadva.</span><span class="sxs-lookup"><span data-stu-id="41d13-122">The default parameter set uses default values for parameters if they are not provided.</span></span> <span data-ttu-id="41d13-123">Az alapértelmezett értékekről további információt az egyes paraméterek leírásában láthat.</span><span class="sxs-lookup"><span data-stu-id="41d13-123">For more information on default values, see the description for each parameter.</span></span> <span data-ttu-id="41d13-124">Ez a parancsmag szerepkört rendelhet a egyszerű szolgáltatásnévhez a **Szerepkör** és a Hatókör **paraméterrel.**</span><span class="sxs-lookup"><span data-stu-id="41d13-124">This cmdlet has the ability to assign a role to the service principal with the **Role** and **Scope** parameters.</span></span> <span data-ttu-id="41d13-125">Ha mindkettőt nem ad meg, a közreműködői szerepkört a rendszer a szolgáltatásnévhez rendeli hozzá.</span><span class="sxs-lookup"><span data-stu-id="41d13-125">If both are omitted, the contributor role is assigned to the service principal.</span></span> <span data-ttu-id="41d13-126">A szerepkör és  a  hatókör paramétereinek alapértelmezett értékei **az** aktuális előfizetés közreműködői.</span><span class="sxs-lookup"><span data-stu-id="41d13-126">The default values for the **Role** and **Scope** parameters are **Contributor** for the current subscription.</span></span> <span data-ttu-id="41d13-127">A parancsmag létrehoz egy alkalmazást, és beállítja a tulajdonságait, ha nem ad meg ApplicationId-et.</span><span class="sxs-lookup"><span data-stu-id="41d13-127">The cmdlet creates an application and sets its properties if an ApplicationId is not provided.</span></span> <span data-ttu-id="41d13-128">Az alkalmazásspecifikus paraméterek frissítéséhez használja az [Update-AzADApplication](./update-azadapplication.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="41d13-128">To update the application-specific parameters, use the [Update-AzADApplication](./update-azadapplication.md) cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="41d13-129">Amikor egyszerű szolgáltatást hoz létre a **New-AzADServicePrincipal** paranccsal, a kimenet azokat a hitelesítő adatokat tartalmazza, amelyek védelmét meg kell védenie.</span><span class="sxs-lookup"><span data-stu-id="41d13-129">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="41d13-130">Győződjön meg arról, hogy ezeket a hitelesítő adatokat nem veszi fel a kódba, vagy ellenőrizze a hitelesítő adatokat a forrásvezérlőben.</span><span class="sxs-lookup"><span data-stu-id="41d13-130">Be sure that you do not include these credentials in your code or check the credentials into your source control.</span></span> <span data-ttu-id="41d13-131">Másik lehetőségként fontolja meg felügyelt [identitások használatát](/azure/active-directory/managed-identities-azure-resources/overview) a hitelesítő adatok használatának elkerülése érdekében.</span><span class="sxs-lookup"><span data-stu-id="41d13-131">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="41d13-132">A **New-AzADServicePrincipal** alapértelmezés szerint [](/azure/role-based-access-control/built-in-roles#contributor) hozzárendeli a közreműködői szerepkört a szolgáltatásnévhez az előfizetés hatókörében.</span><span class="sxs-lookup"><span data-stu-id="41d13-132">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="41d13-133">Ha csökkenteni szeretne egy feltört szolgáltatásnév kockázatát, rendeljen hozzá egy konkrétabb szerepkört, és szűkítse a hatókört egy erőforráshoz vagy erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="41d13-133">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="41d13-134">További [információért lásd: Lépések szerepkör-hozzárendelés](/azure/role-based-access-control/role-assignments-steps) hozzáadásához.</span><span class="sxs-lookup"><span data-stu-id="41d13-134">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="41d13-135">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="41d13-135">EXAMPLES</span></span>

### <span data-ttu-id="41d13-136">1. példa: Egyszerű AD szolgáltatásnév létrehozása</span><span class="sxs-lookup"><span data-stu-id="41d13-136">Example 1: Simple AD service principal creation</span></span>

<span data-ttu-id="41d13-137">Az alábbi példa létrehoz egy egyszerű AD-szolgáltatást, amely a nem megadott paraméterek alapértelmezett értékeit használja.</span><span class="sxs-lookup"><span data-stu-id="41d13-137">The following example creates an AD service principal using default values for parameters not specified.</span></span> <span data-ttu-id="41d13-138">Mivel nem adott meg alkalmazásazonosítót, a rendszer létrehoz egy alkalmazást a szolgáltatásnévhez.</span><span class="sxs-lookup"><span data-stu-id="41d13-138">Since an application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="41d13-139">Mivel a szerepkör  vagy a hatókör nem tartalmaz értékeket, a létrehozott egyszerű szolgáltatásnév lesz az aktuális előfizetés közreműködői szerepköre. </span><span class="sxs-lookup"><span data-stu-id="41d13-139">Since no values are provided for **Role** or **Scope**, the created service principal is assigned the **contributor** role for the current subscription.</span></span>

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

### <span data-ttu-id="41d13-140">2. példa: Egyszerű AD szolgáltatásnév létrehozása meghatározott szerepkörrel és alapértelmezett hatókörrel</span><span class="sxs-lookup"><span data-stu-id="41d13-140">Example 2: Simple AD service principal creation with a specified role and default scope</span></span>

<span data-ttu-id="41d13-141">Az alábbi példa létrehoz egy egyszerű AD-szolgáltatást, amely a nem megadott paraméterek alapértelmezett értékeit használja.</span><span class="sxs-lookup"><span data-stu-id="41d13-141">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="41d13-142">Mivel az alkalmazásazonosító nincs megtéve, a rendszer létrehoz egy alkalmazást a szolgáltatásnévhez.</span><span class="sxs-lookup"><span data-stu-id="41d13-142">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="41d13-143">A szolgáltatásnév az aktuális előfizetés **olvasói** engedélyekkel jön létre, mivel a Scope paraméterhez nincs **megadva** érték.</span><span class="sxs-lookup"><span data-stu-id="41d13-143">The service principal is created with **Reader** permissions for the current subscription since no value is provided for the **Scope** parameter.</span></span>

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

### <span data-ttu-id="41d13-144">3. példa: Egyszerű AD szolgáltatásnév létrehozása meghatározott hatókörű és alapértelmezett szerepkörrel</span><span class="sxs-lookup"><span data-stu-id="41d13-144">Example 3: Simple AD service principal creation with a specified scope and default role</span></span>

<span data-ttu-id="41d13-145">Az alábbi példa létrehoz egy egyszerű AD-szolgáltatást, amely a nem megadott paraméterek alapértelmezett értékeit használja.</span><span class="sxs-lookup"><span data-stu-id="41d13-145">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="41d13-146">Mivel az alkalmazásazonosító nincs megtéve, a rendszer létrehoz egy alkalmazást a szolgáltatásnévhez.</span><span class="sxs-lookup"><span data-stu-id="41d13-146">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="41d13-147">A szolgáltatásnév közreműködői **engedélyekkel** jön létre a megadott erőforráscsoport hatókörében, mivel a Szerepkör paraméterhez nincs **megadva** érték.</span><span class="sxs-lookup"><span data-stu-id="41d13-147">The service principal is created with **Contributor** permissions for the provided resource group scope since no value is provided for the **Role** parameter.</span></span>

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

### <span data-ttu-id="41d13-148">4. példa: Egyszerű AD szolgáltatásnév létrehozása meghatározott hatókörrel és szerepkörrel</span><span class="sxs-lookup"><span data-stu-id="41d13-148">Example 4: Simple AD service principal creation with a specified scope and role</span></span>

<span data-ttu-id="41d13-149">Az alábbi példa létrehoz egy egyszerű AD-szolgáltatást, amely a nem megadott paraméterek alapértelmezett értékeit használja.</span><span class="sxs-lookup"><span data-stu-id="41d13-149">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="41d13-150">Mivel az alkalmazásazonosító nincs megtéve, a rendszer létrehoz egy alkalmazást a szolgáltatásnévhez.</span><span class="sxs-lookup"><span data-stu-id="41d13-150">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="41d13-151">A szolgáltatásnév **olvasói** engedélyekkel jön létre a megadott erőforráscsoport hatókörében.</span><span class="sxs-lookup"><span data-stu-id="41d13-151">The service principal is created with **Reader** permissions for the provided resource group scope.</span></span>

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

### <span data-ttu-id="41d13-152">5. példa: Új AD szolgáltatásnév létrehozása szerepkör-hozzárendeléssel használt alkalmazásazonosító használatával</span><span class="sxs-lookup"><span data-stu-id="41d13-152">Example 5: Create a new AD service principal using application ID with role assignment</span></span>

<span data-ttu-id="41d13-153">Az alábbi példa létrehoz egy új AD szolgáltatásnévből az alkalmazáshoz a következő azonosítóval: "000000000-0000-0000-0000000000000".</span><span class="sxs-lookup"><span data-stu-id="41d13-153">The following example creates a new AD service principal for the application with application ID '00000000-0000-0000-0000-000000000000'.</span></span> <span data-ttu-id="41d13-154">Mivel a szerepkör  vagy a hatókör nem tartalmaz értékeket, a létrehozott egyszerű szolgáltatásnév lesz az aktuális előfizetés közreműködői szerepköre. </span><span class="sxs-lookup"><span data-stu-id="41d13-154">Since no values are provided for **Role** or **Scope**, the created service principal is assigned the **contributor** role for the current subscription.</span></span>

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

### <span data-ttu-id="41d13-155">6. példa: Új AD szolgáltatásnév létrehozása pipázás használatával</span><span class="sxs-lookup"><span data-stu-id="41d13-155">Example 6: Create a new AD service principal using piping</span></span>

<span data-ttu-id="41d13-156">Az alábbi példa beolvassa az alkalmazást a [Get-AzADApplication](./get-azadapplication.md) parancsmaggal a "3ede3c26-b443-4e0b-9efc-b05e68338dc3" objektumazonosítóval.</span><span class="sxs-lookup"><span data-stu-id="41d13-156">The following example retrieves the application with object ID '3ede3c26-b443-4e0b-9efc-b05e68338dc3' using the [Get-AzADApplication](./get-azadapplication.md) cmdlet.</span></span> <span data-ttu-id="41d13-157">A parancsmag az eredményeket a parancsmagba becsökkentve létrehoz egy új `New-AzADServicePrincipal` AD-szolgáltatásnévrendszert az alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="41d13-157">The results are piped to the `New-AzADServicePrincipal` cmdlet to create a new AD service principal for that application.</span></span>

```powershell
Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

### <span data-ttu-id="41d13-158">7. példa: Új AD szolgáltatásnév létrehozása a DisplayName és a jelszó hitelesítő adataival</span><span class="sxs-lookup"><span data-stu-id="41d13-158">Example 7: Create a new AD service principal using DisplayName and password credential</span></span>

<span data-ttu-id="41d13-159">Az alábbi példa létrehoz egy új alkalmazást **ServicePrincipalName** néven és **a StrongPassworld!23 jelszavával.**</span><span class="sxs-lookup"><span data-stu-id="41d13-159">The following example creates a new application with the name **ServicePrincipalName** and a password of **StrongPassworld!23**.</span></span> <span data-ttu-id="41d13-160">Létrehozza a egyszerű szolgáltatást a létrehozott alkalmazás alapján.</span><span class="sxs-lookup"><span data-stu-id="41d13-160">It creates the service principal based on the created application.</span></span> <span data-ttu-id="41d13-161">A rendszer hozzáadja a kezdő dátumot és a záró dátumot a jelszó hitelesítő adataihoz.</span><span class="sxs-lookup"><span data-stu-id="41d13-161">The start date and end date are added to the password credential.</span></span>

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

### <span data-ttu-id="41d13-162">8. példa: Új AD szolgáltatásnév létrehozása a DisplayName és az egyszerű kulcs hitelesítő adataival</span><span class="sxs-lookup"><span data-stu-id="41d13-162">Example 8: Create a new AD service principal using DisplayName and plain key credential</span></span>

<span data-ttu-id="41d13-163">Az alábbi példa létrehoz egy új alkalmazást **ServicePrincipalName** névvel és egy **tanúsítványnévvel**$cert. Létrehozza az egyszerű szolgáltatásnév a létrehozott alkalmazás alapján.</span><span class="sxs-lookup"><span data-stu-id="41d13-163">The following example creates a new application with the name **ServicePrincipalName** and a certificate **$cert**. It creates the service principal based on the application created.</span></span> <span data-ttu-id="41d13-164">A rendszer hozzáadja a záró dátumot a kulcs hitelesítő adataihoz.</span><span class="sxs-lookup"><span data-stu-id="41d13-164">The end date is added to key credential.</span></span>

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

## <span data-ttu-id="41d13-165">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41d13-165">PARAMETERS</span></span>

### <span data-ttu-id="41d13-166">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="41d13-166">-ApplicationId</span></span>

<span data-ttu-id="41d13-167">A bérlői webhelyen egy egyszerű szolgáltatásnév egyedi alkalmazásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="41d13-167">The unique application ID for a service principal in a tenant.</span></span> <span data-ttu-id="41d13-168">A tulajdonság létrehozása után ezt a tulajdonságot nem lehet módosítani.</span><span class="sxs-lookup"><span data-stu-id="41d13-168">Once created this property cannot be changed.</span></span> <span data-ttu-id="41d13-169">Ha nincs megadva egy meglévő alkalmazás alkalmazásazonosítója, létrejön egy alkalmazás.</span><span class="sxs-lookup"><span data-stu-id="41d13-169">If an application ID for an existing application is not specified, an application is created.</span></span>

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

### <span data-ttu-id="41d13-170">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="41d13-170">-ApplicationObject</span></span>

<span data-ttu-id="41d13-171">Az az objektum, amely azt az alkalmazást képviseli, amelyhez a szolgáltatásnév létre van hozva.</span><span class="sxs-lookup"><span data-stu-id="41d13-171">The object representing the application for which the service principal is created.</span></span>

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

### <span data-ttu-id="41d13-172">-CertValue</span><span class="sxs-lookup"><span data-stu-id="41d13-172">-CertValue</span></span>

<span data-ttu-id="41d13-173">Az aszimmetrikus hitelesítőadat-típus értéke.</span><span class="sxs-lookup"><span data-stu-id="41d13-173">The value of the asymmetric credential type.</span></span> <span data-ttu-id="41d13-174">A kódolt Base64 tanúsítványt jelöli.</span><span class="sxs-lookup"><span data-stu-id="41d13-174">It represents the Base64 encoded certificate.</span></span>

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

### <span data-ttu-id="41d13-175">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41d13-175">-DefaultProfile</span></span>

<span data-ttu-id="41d13-176">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="41d13-176">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41d13-177">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="41d13-177">-DisplayName</span></span>

<span data-ttu-id="41d13-178">A szolgáltatásnév rövid neve.</span><span class="sxs-lookup"><span data-stu-id="41d13-178">The friendly name of the service principal.</span></span> <span data-ttu-id="41d13-179">Ha nincs megjelölve megjelenítendő név, ez az érték alapértelmezés szerint az **azure-powershell-MM-dd-y-HH-mm-mm-mm értékre** van állítva, ahol az utótag az alkalmazás létrehozásának ideje.</span><span class="sxs-lookup"><span data-stu-id="41d13-179">If a display name is not provided, this value will default to **azure-powershell-MM-dd-yyyy-HH-mm-ss** where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="41d13-180">-EndDate</span><span class="sxs-lookup"><span data-stu-id="41d13-180">-EndDate</span></span>

<span data-ttu-id="41d13-181">A hitelesítő adatok használatának tényleges záró dátuma.</span><span class="sxs-lookup"><span data-stu-id="41d13-181">The effective end date of the credential usage.</span></span> <span data-ttu-id="41d13-182">Az alapértelmezett záró dátum egy év a mai naptól.</span><span class="sxs-lookup"><span data-stu-id="41d13-182">The default end date value is one year from today.</span></span>
<span data-ttu-id="41d13-183">Aszimmetrikus típusú hitelesítő adatoknál ezt az X509-tanúsítvány érvényességének dátumán vagy azt megelőzően kell megadni.</span><span class="sxs-lookup"><span data-stu-id="41d13-183">For an asymmetric type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="41d13-184">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="41d13-184">-KeyCredential</span></span>

<span data-ttu-id="41d13-185">Az alkalmazáshoz társított kulcs hitelesítő adatok gyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="41d13-185">The collection of key credentials associated with the application.</span></span>

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

### <span data-ttu-id="41d13-186">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="41d13-186">-PasswordCredential</span></span>

<span data-ttu-id="41d13-187">Az alkalmazáshoz társított jelszó-hitelesítő adatok gyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="41d13-187">The collection of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="41d13-188">-Szerepkör</span><span class="sxs-lookup"><span data-stu-id="41d13-188">-Role</span></span>

<span data-ttu-id="41d13-189">Az egyszerű szolgáltatásnév szerepköre a hatókörben.</span><span class="sxs-lookup"><span data-stu-id="41d13-189">The role that the service principal has over the scope.</span></span> <span data-ttu-id="41d13-190">Ha nincs megjelölve érték, **a** szerepkör alapértelmezés szerint a **közreműködői szerepkört használja.**</span><span class="sxs-lookup"><span data-stu-id="41d13-190">If no value is provided, **Role** defaults to the **Contributor** role.</span></span>

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

### <span data-ttu-id="41d13-191">-Scope</span><span class="sxs-lookup"><span data-stu-id="41d13-191">-Scope</span></span>

<span data-ttu-id="41d13-192">Az a tartomány, amelyhez a egyszerű szolgáltatásnév rendelkezik engedélyekkel.</span><span class="sxs-lookup"><span data-stu-id="41d13-192">The scope that the service principal has permissions for.</span></span> <span data-ttu-id="41d13-193">Ha nincs megjelölve **érték,** a Hatókör alapértelmezés szerint az aktuális előfizetést használja.</span><span class="sxs-lookup"><span data-stu-id="41d13-193">If no value is provided, **Scope** defaults to the current subscription.</span></span>

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

### <span data-ttu-id="41d13-194">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="41d13-194">-SkipAssignment</span></span>

<span data-ttu-id="41d13-195">Ha be van állítva, hagyja ki az egyszerű szolgáltatásnév alapértelmezett szerepkör-hozzárendelésének létrehozását.</span><span class="sxs-lookup"><span data-stu-id="41d13-195">If set, skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="41d13-196">-StartDate</span><span class="sxs-lookup"><span data-stu-id="41d13-196">-StartDate</span></span>

<span data-ttu-id="41d13-197">A hitelesítő adatok használatának tényleges kezdő dátuma.</span><span class="sxs-lookup"><span data-stu-id="41d13-197">The effective start date of the credential usage.</span></span> <span data-ttu-id="41d13-198">Az alapértelmezett kezdő dátum a mai nap.</span><span class="sxs-lookup"><span data-stu-id="41d13-198">The default start date value is today.</span></span> <span data-ttu-id="41d13-199">Aszimmetrikus típusú hitelesítő adatoknál ezt az X509-tanúsítvány érvényességének dátumán vagy azt követően kell megadni.</span><span class="sxs-lookup"><span data-stu-id="41d13-199">For an asymmetric type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="41d13-200">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41d13-200">-Confirm</span></span>

<span data-ttu-id="41d13-201">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="41d13-201">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41d13-202">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41d13-202">-WhatIf</span></span>

<span data-ttu-id="41d13-203">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="41d13-203">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41d13-204">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="41d13-204">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41d13-205">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41d13-205">CommonParameters</span></span>
<span data-ttu-id="41d13-206">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41d13-206">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41d13-207">További információt a [about_CommonParameters.](/powershell/module/microsoft.powershell.core/about/about_commonparameters)</span><span class="sxs-lookup"><span data-stu-id="41d13-207">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>
## <span data-ttu-id="41d13-208">INPUTS</span><span class="sxs-lookup"><span data-stu-id="41d13-208">INPUTS</span></span>

### <span data-ttu-id="41d13-209">System.Guid</span><span class="sxs-lookup"><span data-stu-id="41d13-209">System.Guid</span></span>

### <span data-ttu-id="41d13-210">System.String</span><span class="sxs-lookup"><span data-stu-id="41d13-210">System.String</span></span>

### <span data-ttu-id="41d13-211">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="41d13-211">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="41d13-212">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span><span class="sxs-lookup"><span data-stu-id="41d13-212">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="41d13-213">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span><span class="sxs-lookup"><span data-stu-id="41d13-213">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="41d13-214">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="41d13-214">System.DateTime</span></span>

## <span data-ttu-id="41d13-215">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41d13-215">OUTPUTS</span></span>

### <span data-ttu-id="41d13-216">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="41d13-216">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="41d13-217">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="41d13-217">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="41d13-218">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="41d13-218">NOTES</span></span>

<span data-ttu-id="41d13-219">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, telepítés</span><span class="sxs-lookup"><span data-stu-id="41d13-219">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="41d13-220">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41d13-220">RELATED LINKS</span></span>

[<span data-ttu-id="41d13-221">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="41d13-221">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="41d13-222">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="41d13-222">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="41d13-223">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="41d13-223">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="41d13-224">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="41d13-224">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="41d13-225">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="41d13-225">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="41d13-226">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="41d13-226">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="41d13-227">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="41d13-227">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)