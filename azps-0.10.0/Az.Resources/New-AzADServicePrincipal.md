---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: 96ff12056167adaabcb828e2fedfe0c78d59e963
ms.sourcegitcommit: 375232b84336ef5e13052504deaa43f5bd4b7f65
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/05/2020
ms.locfileid: "94303971"
---
# <span data-ttu-id="bc402-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="bc402-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="bc402-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bc402-102">SYNOPSIS</span></span>
<span data-ttu-id="bc402-103">Új Azure Active Directory-szolgáltató létrehozása.</span><span class="sxs-lookup"><span data-stu-id="bc402-103">Creates a new azure active directory service principal.</span></span>

## <span data-ttu-id="bc402-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bc402-104">SYNTAX</span></span>

### <span data-ttu-id="bc402-105">SimpleParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bc402-105">SimpleParameterSet (Default)</span></span>
```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-Password <SecureString>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc402-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc402-106">ApplicationWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc402-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc402-107">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc402-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc402-108">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc402-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc402-109">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc402-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc402-110">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc402-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc402-111">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc402-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc402-112">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc402-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc402-113">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc402-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc402-114">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc402-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc402-115">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc402-116">ApplicationObjectWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc402-116">ApplicationObjectWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc402-117">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc402-117">ApplicationObjectWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -Password <SecureString>
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bc402-118">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc402-118">ApplicationObjectWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication>
 -PasswordCredential <PSADPasswordCredential[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bc402-119">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc402-119">ApplicationObjectWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc402-120">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc402-120">ApplicationObjectWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc402-121">Leírás</span><span class="sxs-lookup"><span data-stu-id="bc402-121">DESCRIPTION</span></span>
<span data-ttu-id="bc402-122">Új Azure Active Directory-szolgáltató létrehozása.</span><span class="sxs-lookup"><span data-stu-id="bc402-122">Creates a new azure active directory service principal.</span></span> <span data-ttu-id="bc402-123">Az alapértelmezett paraméterérték a paraméterek alapértelmezett értékeit használja, ha a felhasználó nem biztosít egyet nekik.</span><span class="sxs-lookup"><span data-stu-id="bc402-123">The default parameter set uses default values for parameters if the user does not provide one for them.</span></span> <span data-ttu-id="bc402-124">A használatban lévő alapértelmezett értékekről további információt az alábbi paraméterek című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="bc402-124">For more information on the default values used, please see the description for the given parameters below.</span></span>
<span data-ttu-id="bc402-125">Ennek a parancsmagnak az a feladata, hogy szerepkört rendeljen a szolgáltatóhoz a `Role` és `Scope` paraméterekkel; ha egyik paraméter sem áll rendelkezésre, akkor a szolgáltatáshoz nem kell szerepkört rendelni.</span><span class="sxs-lookup"><span data-stu-id="bc402-125">This cmdlet has the ability to assign a role to the service principal with the `Role` and `Scope` parameters; if neither of these parameters are provided, no role will be assigned to the service principal.</span></span> <span data-ttu-id="bc402-126">A és a paraméterek alapértelmezett értékei a `Role` `Scope` következők: "közreműködő" és a jelenlegi előfizetés ( _Megjegyzés_ : az alapértelmezett értékek csak akkor használhatók, ha a felhasználó a két paraméter egyikéhez adja meg a kívánt értéket, de nem a másikat).</span><span class="sxs-lookup"><span data-stu-id="bc402-126">The default values for the `Role` and `Scope` parameters are "Contributor" and the current subscription, respectively ( _note_ : the defaults are only used when the user provides a value for one of the two parameters, but not the other).</span></span>
<span data-ttu-id="bc402-127">A parancsmag emellett implicit módon létrehoz egy alkalmazást, és beállítja annak tulajdonságait (ha a ApplicationId nincs megadva).</span><span class="sxs-lookup"><span data-stu-id="bc402-127">The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span> <span data-ttu-id="bc402-128">Az alkalmazás specifikus paramétereinek frissítéséhez használja Set-AzADApplication parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="bc402-128">In order to update the application specific parameters please use Set-AzADApplication cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="bc402-129">Ha a **New-AzADServicePrincipal** parancs segítségével hoz létre egy egyszerű szolgáltatásnevet, a kimenet tartalmazza a védelemmel ellátott hitelesítő adatokat is.</span><span class="sxs-lookup"><span data-stu-id="bc402-129">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="bc402-130">Ügyeljen arra, hogy ne szerepeljenek ezek a hitelesítő adatok a kódban, vagy ellenőrizze a hitelesítő adatokat a forrás vezérlőben.</span><span class="sxs-lookup"><span data-stu-id="bc402-130">Be sure that you do not include these credentials in your code or check the credentials into your source control.</span></span> <span data-ttu-id="bc402-131">A [felügyelt identitások](/azure/active-directory/managed-identities-azure-resources/overview) használata helyett érdemes lehet használni a hitelesítő adatok használatát.</span><span class="sxs-lookup"><span data-stu-id="bc402-131">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="bc402-132">A **New-AzADServicePrincipal** alapértelmezés szerint a [munkatárs](/azure/role-based-access-control/built-in-roles#contributor) szerepkört rendeli hozzá az előfizetési tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="bc402-132">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="bc402-133">Ha csökkenteni szeretné a kiegyezéssel járó megbízó kockázatát, rendeljen hozzá egy specifikusabb szerepkört, és szűkítse a hatókört egy erőforrás vagy erőforrás csoportba.</span><span class="sxs-lookup"><span data-stu-id="bc402-133">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="bc402-134">További információért tekintse át [a szerepkör-hozzárendelés hozzáadásának lépéseit](/azure/role-based-access-control/role-assignments-steps) .</span><span class="sxs-lookup"><span data-stu-id="bc402-134">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="bc402-135">Példák</span><span class="sxs-lookup"><span data-stu-id="bc402-135">EXAMPLES</span></span>

### <span data-ttu-id="bc402-136">Példa 1 – Simple AD Service – egyszerű létrehozás</span><span class="sxs-lookup"><span data-stu-id="bc402-136">Example 1 - Simple AD service principal creation</span></span>

```
PS C:\> New-AzADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="bc402-137">A fenti parancs alapértelmezett értékekkel létrehoz egy AD-szolgáltatót a paraméterekhez.</span><span class="sxs-lookup"><span data-stu-id="bc402-137">The above command creates an AD service principal using default values for parameters not provided.</span></span> <span data-ttu-id="bc402-138">Mivel egy alkalmazás-azonosító nem volt megadva, létrejön egy alkalmazás a szolgáltatóhoz.</span><span class="sxs-lookup"><span data-stu-id="bc402-138">Since an application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="bc402-139">Mivel nincs megadva érték `Role` `Scope` , vagy a létrehozta a Service Principal szolgáltatáshoz nincs engedélye.</span><span class="sxs-lookup"><span data-stu-id="bc402-139">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="bc402-140">Példa 2 – az egyszerű AD-szolgáltatás egyszerű létrehozása egy megadott szerepkörrel és alapértelmezett hatókörrel</span><span class="sxs-lookup"><span data-stu-id="bc402-140">Example 2 - Simple AD service principal creation with a specified role and default scope</span></span>

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

<span data-ttu-id="bc402-141">A fenti parancs az alapértelmezett paraméterek nélkül hozza létre a AD Service principalt.</span><span class="sxs-lookup"><span data-stu-id="bc402-141">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="bc402-142">Mivel a program nem adta meg az alkalmazás azonosítóját, létrejön egy alkalmazás a szolgáltatóhoz.</span><span class="sxs-lookup"><span data-stu-id="bc402-142">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="bc402-143">A Service Principal a jelenlegi előfizetéshez tartozó "Reader" engedélyekkel lett létrehozva (mivel a paraméterhez nem tartozik érték `Scope` ).</span><span class="sxs-lookup"><span data-stu-id="bc402-143">The service principal was created with "Reader" permissions over the current subscription (since no value was provided for the `Scope` parameter).</span></span>

### <span data-ttu-id="bc402-144">Példa 3 – az egyszerű AD-szolgáltatás egyszerű létrehozása meghatározott hatókör és alapértelmezett szerepkörrel</span><span class="sxs-lookup"><span data-stu-id="bc402-144">Example 3 - Simple AD service principal creation with a specified scope and default role</span></span>

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

<span data-ttu-id="bc402-145">A fenti parancs az alapértelmezett paraméterek nélkül hozza létre a AD Service principalt.</span><span class="sxs-lookup"><span data-stu-id="bc402-145">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="bc402-146">Mivel a program nem adta meg az alkalmazás azonosítóját, létrejön egy alkalmazás a szolgáltatóhoz.</span><span class="sxs-lookup"><span data-stu-id="bc402-146">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="bc402-147">A Service Principal a "közreműködő" engedélyekkel lett létrehozva (mivel a `Role` paraméterhez nem tartozik érték) a megadott erőforráscsoport hatóköre fölött.</span><span class="sxs-lookup"><span data-stu-id="bc402-147">The service principal was created with "Contributor" permissions (since no value was provided for the `Role` parameter) over the provided resource group scope.</span></span>

### <span data-ttu-id="bc402-148">Példa 4 – az egyszerű AD-szolgáltatás fő létrehozása meghatározott hatókörrel és szerepkörrel</span><span class="sxs-lookup"><span data-stu-id="bc402-148">Example 4 - Simple AD service principal creation with a specified scope and role</span></span>

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

<span data-ttu-id="bc402-149">A fenti parancs az alapértelmezett paraméterek nélkül hozza létre a AD Service principalt.</span><span class="sxs-lookup"><span data-stu-id="bc402-149">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="bc402-150">Mivel a program nem adta meg az alkalmazás azonosítóját, létrejön egy alkalmazás a szolgáltatóhoz.</span><span class="sxs-lookup"><span data-stu-id="bc402-150">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="bc402-151">A szolgáltató a megadott erőforráscsoport-hatókörre vonatkozóan "olvasó" engedélyekkel jött létre.</span><span class="sxs-lookup"><span data-stu-id="bc402-151">The service principal was created with "Reader" permissions over the provided resource group scope.</span></span>

### <span data-ttu-id="bc402-152">Példa 5 – új AD-szolgáltató létrehozása az alkalmazás-azonosítóval szerepkör-hozzárendeléssel</span><span class="sxs-lookup"><span data-stu-id="bc402-152">Example 5 - Create a new AD service principal using application id with role assignment</span></span>

```
PS C:\> New-AzADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="bc402-153">Új AD-szolgáltatót hoz létre a "34a28ad2-DEC4-4a41-bc3b-d22ddf90000e" azonosítójú alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="bc402-153">Creates a new AD service principal for the application with application id '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span></span> <span data-ttu-id="bc402-154">Mivel nincs megadva érték `Role` `Scope` , vagy a létrehozta a Service Principal szolgáltatáshoz nincs engedélye.</span><span class="sxs-lookup"><span data-stu-id="bc402-154">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="bc402-155">6 példa – új AD-szolgáltató létrehozása csővezetékek használatával</span><span class="sxs-lookup"><span data-stu-id="bc402-155">Example 6 - Create a new AD service principal using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

<span data-ttu-id="bc402-156">Beilleszti az alkalmazást a "3ede3c26-b443-4e0b-9efc-b05e68338dc3" azonosítójú objektumazonosítót, valamint a New-AzADServicePrincipal parancsmagot tartalmazó csöveket, amelyekkel új AD-szolgáltatót hozhat létre az adott alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="bc402-156">Gets the application with object id '3ede3c26-b443-4e0b-9efc-b05e68338dc3' and pipes that to the New-AzADServicePrincipal cmdlet to create a new AD service principal for that application.</span></span>

## <span data-ttu-id="bc402-157">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bc402-157">PARAMETERS</span></span>

### <span data-ttu-id="bc402-158">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="bc402-158">-ApplicationId</span></span>
<span data-ttu-id="bc402-159">Egy szolgáltató egyedi alkalmazásspecifikus azonosítója bérlői fiókban.</span><span class="sxs-lookup"><span data-stu-id="bc402-159">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="bc402-160">Miután létrehozta ezt a tulajdonságot, nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="bc402-160">Once created this property cannot be changed.</span></span>
<span data-ttu-id="bc402-161">Ha egy alkalmazás-azonosító nincs megadva, a program létrehoz egy azonosítót.</span><span class="sxs-lookup"><span data-stu-id="bc402-161">If an application id is not specified, one will be generated.</span></span>

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

### <span data-ttu-id="bc402-162">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="bc402-162">-ApplicationObject</span></span>
<span data-ttu-id="bc402-163">Annak az alkalmazásnak az objektuma, amelybe a szolgáltatásnevet létrehozta.</span><span class="sxs-lookup"><span data-stu-id="bc402-163">The object representing the application for which the service principal is created.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithoutCredentialParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc402-164">-CertValue</span><span class="sxs-lookup"><span data-stu-id="bc402-164">-CertValue</span></span>
<span data-ttu-id="bc402-165">Az "aszimmetrikus" hitelesítőadat-típus értéke.</span><span class="sxs-lookup"><span data-stu-id="bc402-165">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="bc402-166">A 64 kódolt tanúsítványát jelöli.</span><span class="sxs-lookup"><span data-stu-id="bc402-166">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="bc402-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc402-167">-DefaultProfile</span></span>
<span data-ttu-id="bc402-168">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bc402-168">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc402-169">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="bc402-169">-DisplayName</span></span>
<span data-ttu-id="bc402-170">A szolgáltatás megbízójának rövid neve.</span><span class="sxs-lookup"><span data-stu-id="bc402-170">The friendly name of the service principal.</span></span> <span data-ttu-id="bc402-171">Ha a megjelenítendő név nem szerepel a listában, akkor ez az érték alapértelmezés szerint "Azure-PowerShell-HH-NN-ÉÉÉÉ-HH-HH-HH", ahol az utótag az alkalmazás létrehozásának időpontja.</span><span class="sxs-lookup"><span data-stu-id="bc402-171">If a display name is not provided, this value will default to 'azure-powershell-MM-dd-yyyy-HH-mm-ss', where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="bc402-172">-EndDate</span><span class="sxs-lookup"><span data-stu-id="bc402-172">-EndDate</span></span>
<span data-ttu-id="bc402-173">A hitelesítő adatok használatának tényleges befejezési dátuma.</span><span class="sxs-lookup"><span data-stu-id="bc402-173">The effective end date of the credential usage.</span></span>
<span data-ttu-id="bc402-174">Az alapértelmezett befejezési dátum értéke egy év a mai naptól számítva.</span><span class="sxs-lookup"><span data-stu-id="bc402-174">The default end date value is one year from today.</span></span> <span data-ttu-id="bc402-175">Ha "aszimmetrikus" típusú hitelesítő adatokra van szükség, ezt a X509 tanúsítvány érvényességi dátumának be vagy ki kell állítania.</span><span class="sxs-lookup"><span data-stu-id="bc402-175">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="bc402-176">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="bc402-176">-KeyCredential</span></span>
<span data-ttu-id="bc402-177">Az alkalmazáshoz társított legfontosabb hitelesítő adatok gyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="bc402-177">The collection of key credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationObjectWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc402-178">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="bc402-178">-Password</span></span>
<span data-ttu-id="bc402-179">A szolgáltatásnevet társítani kívánt jelszó.</span><span class="sxs-lookup"><span data-stu-id="bc402-179">The password to be associated with the service principal.</span></span> <span data-ttu-id="bc402-180">Ha nem ad meg jelszót, a program véletlenszerű globális azonosítót hoz létre, és a jelszót használja.</span><span class="sxs-lookup"><span data-stu-id="bc402-180">If a password is not provided, a random GUID will be generated and used as the password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet, DisplayNameWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationObjectWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc402-181">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="bc402-181">-PasswordCredential</span></span>
<span data-ttu-id="bc402-182">Az alkalmazáshoz társított jelszó-hitelesítő adatok gyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="bc402-182">The collection of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationObjectWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc402-183">-Role (szerepkör)</span><span class="sxs-lookup"><span data-stu-id="bc402-183">-Role</span></span>
<span data-ttu-id="bc402-184">Annak a szerepkörnek a szerepe, amelyet a szolgáltató a hatókör felett tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="bc402-184">The role that the service principal has over the scope.</span></span> <span data-ttu-id="bc402-185">Ha meg `Scope` van határozva egy érték, de nincs megadva érték `Role` , akkor `Role` az alapértelmezett érték a "munkatárs" szerepkört adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc402-185">If a value for `Scope` is provided, but no value is provided for `Role`, then `Role` will default to the 'Contributor' role.</span></span>

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

### <span data-ttu-id="bc402-186">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="bc402-186">-Scope</span></span>
<span data-ttu-id="bc402-187">Az a hatókör, amelyre a szolgáltatónak van engedélye.</span><span class="sxs-lookup"><span data-stu-id="bc402-187">The scope that the service principal has permissions on.</span></span> <span data-ttu-id="bc402-188">Ha meg `Role` van határozva egy érték, de nincs megadva érték `Scope` , akkor `Scope` az alapértelmezés szerint az aktuális előfizetést adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc402-188">If a value for `Role` is provided, but no value is provided for `Scope`, then `Scope` will default to the current subscription.</span></span>

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

### <span data-ttu-id="bc402-189">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="bc402-189">-SkipAssignment</span></span>
<span data-ttu-id="bc402-190">Ha be van állítva, akkor a program kihagyja az alapértelmezett szerepkör-hozzárendelés létrehozását a szolgáltatónál.</span><span class="sxs-lookup"><span data-stu-id="bc402-190">If set, will skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="bc402-191">-StartDate</span><span class="sxs-lookup"><span data-stu-id="bc402-191">-StartDate</span></span>
<span data-ttu-id="bc402-192">A hitelesítő adatok használatának tényleges kezdési dátuma.</span><span class="sxs-lookup"><span data-stu-id="bc402-192">The effective start date of the credential usage.</span></span>
<span data-ttu-id="bc402-193">A kezdő dátum alapértelmezett értéke ma.</span><span class="sxs-lookup"><span data-stu-id="bc402-193">The default start date value is today.</span></span> <span data-ttu-id="bc402-194">Ha "aszimmetrikus" típusú hitelesítő adatokra van szükség, ezt a X509-tanúsítvány érvényességi dátumának be vagy mögé kell állítani.</span><span class="sxs-lookup"><span data-stu-id="bc402-194">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="bc402-195">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bc402-195">-Confirm</span></span>
<span data-ttu-id="bc402-196">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bc402-196">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc402-197">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc402-197">-WhatIf</span></span>
<span data-ttu-id="bc402-198">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bc402-198">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc402-199">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bc402-199">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc402-200">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc402-200">CommonParameters</span></span>
<span data-ttu-id="bc402-201">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bc402-201">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc402-202">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc402-202">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc402-203">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc402-203">INPUTS</span></span>

### <span data-ttu-id="bc402-204">System. GUID</span><span class="sxs-lookup"><span data-stu-id="bc402-204">System.Guid</span></span>

### <span data-ttu-id="bc402-205">System. String</span><span class="sxs-lookup"><span data-stu-id="bc402-205">System.String</span></span>

### <span data-ttu-id="bc402-206">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="bc402-206">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="bc402-207">Paraméterek: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bc402-207">Parameters: ApplicationObject (ByValue)</span></span>

### <span data-ttu-id="bc402-208">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="bc402-208">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="bc402-209">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="bc402-209">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="bc402-210">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="bc402-210">System.Security.SecureString</span></span>

### <span data-ttu-id="bc402-211">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="bc402-211">System.DateTime</span></span>

## <span data-ttu-id="bc402-212">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc402-212">OUTPUTS</span></span>

### <span data-ttu-id="bc402-213">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="bc402-213">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="bc402-214">Microsoft. Azure. Command. Resources. modellek. Authorization. PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="bc402-214">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="bc402-215">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bc402-215">NOTES</span></span>
<span data-ttu-id="bc402-216">Kulcsszavak: Azure, az, kar, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="bc402-216">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="bc402-217">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bc402-217">RELATED LINKS</span></span>

[<span data-ttu-id="bc402-218">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="bc402-218">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="bc402-219">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="bc402-219">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="bc402-220">Új – AzADApplication</span><span class="sxs-lookup"><span data-stu-id="bc402-220">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="bc402-221">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="bc402-221">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="bc402-222">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="bc402-222">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="bc402-223">Új – AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="bc402-223">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="bc402-224">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="bc402-224">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

