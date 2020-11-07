---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadserviceprincipal
schema: 2.0.0
ms.openlocfilehash: 9d0fb4f188b3753e22258a27cf8632d85fe866dc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850289"
---
# <span data-ttu-id="ee2f7-101">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ee2f7-101">New-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="ee2f7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ee2f7-102">SYNOPSIS</span></span>
<span data-ttu-id="ee2f7-103">Új Azure Active Directory-szolgáltató létrehozása.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-103">Creates a new azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee2f7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ee2f7-104">SYNTAX</span></span>

### <span data-ttu-id="ee2f7-105">SimpleParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ee2f7-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-Password <SecureString>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee2f7-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee2f7-106">ApplicationWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee2f7-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee2f7-107">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee2f7-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee2f7-108">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee2f7-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee2f7-109">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee2f7-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee2f7-110">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee2f7-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee2f7-111">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee2f7-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee2f7-112">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee2f7-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee2f7-113">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee2f7-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee2f7-114">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee2f7-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee2f7-115">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee2f7-116">ApplicationObjectWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee2f7-116">ApplicationObjectWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee2f7-117">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee2f7-117">ApplicationObjectWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> -Password <SecureString>
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee2f7-118">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee2f7-118">ApplicationObjectWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication>
 -PasswordCredential <PSADPasswordCredential[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee2f7-119">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee2f7-119">ApplicationObjectWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee2f7-120">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee2f7-120">ApplicationObjectWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee2f7-121">Leírás</span><span class="sxs-lookup"><span data-stu-id="ee2f7-121">DESCRIPTION</span></span>
<span data-ttu-id="ee2f7-122">Új Azure Active Directory-szolgáltató létrehozása.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-122">Creates a new azure active directory service principal.</span></span> <span data-ttu-id="ee2f7-123">Az alapértelmezett paraméterérték a paraméterek alapértelmezett értékeit használja, ha a felhasználó nem biztosít egyet nekik.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-123">The default parameter set uses default values for parameters if the user does not provide one for them.</span></span> <span data-ttu-id="ee2f7-124">A használatban lévő alapértelmezett értékekről további információt az alábbi paraméterek című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-124">For more information on the default values used, please see the description for the given parameters below.</span></span>
<span data-ttu-id="ee2f7-125">Ennek a parancsmagnak az a feladata, hogy szerepkört rendeljen a szolgáltatóhoz a `Role` és `Scope` paraméterekkel; ha egyik paraméter sem áll rendelkezésre, akkor a szolgáltatáshoz nem kell szerepkört rendelni.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-125">This cmdlet has the ability to assign a role to the service principal with the `Role` and `Scope` parameters; if neither of these parameters are provided, no role will be assigned to the service principal.</span></span> <span data-ttu-id="ee2f7-126">A és a paraméterek alapértelmezett értékei a `Role` `Scope` következők: "közreműködő" és a jelenlegi előfizetés ( _Megjegyzés_ : az alapértelmezett értékek csak akkor használhatók, ha a felhasználó a két paraméter egyikéhez adja meg a kívánt értéket, de nem a másikat).</span><span class="sxs-lookup"><span data-stu-id="ee2f7-126">The default values for the `Role` and `Scope` parameters are "Contributor" and the current subscription, respectively ( _note_ : the defaults are only used when the user provides a value for one of the two parameters, but not the other).</span></span>
<span data-ttu-id="ee2f7-127">A parancsmag emellett implicit módon létrehoz egy alkalmazást, és beállítja annak tulajdonságait (ha a ApplicationId nincs megadva).</span><span class="sxs-lookup"><span data-stu-id="ee2f7-127">The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span> <span data-ttu-id="ee2f7-128">Az alkalmazás specifikus paramétereinek frissítéséhez használja Set-AzureRmADApplication parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-128">In order to update the application specific parameters please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="ee2f7-129">Példák</span><span class="sxs-lookup"><span data-stu-id="ee2f7-129">EXAMPLES</span></span>

### <span data-ttu-id="ee2f7-130">Példa 1 – Simple AD Service – egyszerű létrehozás</span><span class="sxs-lookup"><span data-stu-id="ee2f7-130">Example 1 - Simple AD service principal creation</span></span>

```
PS C:\> New-AzureRmADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="ee2f7-131">A fenti parancs alapértelmezett értékekkel létrehoz egy AD-szolgáltatót a paraméterekhez.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-131">The above command creates an AD service principal using default values for parameters not provided.</span></span> <span data-ttu-id="ee2f7-132">Mivel egy alkalmazás-azonosító nem volt megadva, létrejön egy alkalmazás a szolgáltatóhoz.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-132">Since an application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="ee2f7-133">Mivel nincs megadva érték `Role` `Scope` , vagy a létrehozta a Service Principal szolgáltatáshoz nincs engedélye.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-133">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="ee2f7-134">Példa 2 – az egyszerű AD-szolgáltatás egyszerű létrehozása egy megadott szerepkörrel és alapértelmezett hatókörrel</span><span class="sxs-lookup"><span data-stu-id="ee2f7-134">Example 2 - Simple AD service principal creation with a specified role and default scope</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -Role Reader

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz' to the new service principal.
```

<span data-ttu-id="ee2f7-135">A fenti parancs az alapértelmezett paraméterek nélkül hozza létre a AD Service principalt.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-135">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="ee2f7-136">Mivel a program nem adta meg az alkalmazás azonosítóját, létrejön egy alkalmazás a szolgáltatóhoz.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-136">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="ee2f7-137">A Service Principal a jelenlegi előfizetéshez tartozó "Reader" engedélyekkel lett létrehozva (mivel a paraméterhez nem tartozik érték `Scope` ).</span><span class="sxs-lookup"><span data-stu-id="ee2f7-137">The service principal was created with "Reader" permissions over the current subscription (since no value was provided for the `Scope` parameter).</span></span>

### <span data-ttu-id="ee2f7-138">Példa 3 – az egyszerű AD-szolgáltatás egyszerű létrehozása meghatározott hatókör és alapértelmezett szerepkörrel</span><span class="sxs-lookup"><span data-stu-id="ee2f7-138">Example 3 - Simple AD service principal creation with a specified scope and default role</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="ee2f7-139">A fenti parancs az alapértelmezett paraméterek nélkül hozza létre a AD Service principalt.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-139">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="ee2f7-140">Mivel a program nem adta meg az alkalmazás azonosítóját, létrejön egy alkalmazás a szolgáltatóhoz.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-140">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="ee2f7-141">A Service Principal a "közreműködő" engedélyekkel lett létrehozva (mivel a `Role` paraméterhez nem tartozik érték) a megadott erőforráscsoport hatóköre fölött.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-141">The service principal was created with "Contributor" permissions (since no value was provided for the `Role` parameter) over the provided resource group scope.</span></span>

### <span data-ttu-id="ee2f7-142">Példa 4 – az egyszerű AD-szolgáltatás fő létrehozása meghatározott hatókörrel és szerepkörrel</span><span class="sxs-lookup"><span data-stu-id="ee2f7-142">Example 4 - Simple AD service principal creation with a specified scope and role</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -Role Reader -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="ee2f7-143">A fenti parancs az alapértelmezett paraméterek nélkül hozza létre a AD Service principalt.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-143">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="ee2f7-144">Mivel a program nem adta meg az alkalmazás azonosítóját, létrejön egy alkalmazás a szolgáltatóhoz.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-144">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="ee2f7-145">A szolgáltató a megadott erőforráscsoport-hatókörre vonatkozóan "olvasó" engedélyekkel jött létre.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-145">The service principal was created with "Reader" permissions over the provided resource group scope.</span></span>

### <span data-ttu-id="ee2f7-146">Példa 5 – új AD-szolgáltató létrehozása az alkalmazás-azonosítóval szerepkör-hozzárendeléssel</span><span class="sxs-lookup"><span data-stu-id="ee2f7-146">Example 5 - Create a new AD service principal using application id with role assignment</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="ee2f7-147">Új AD-szolgáltatót hoz létre a "34a28ad2-DEC4-4a41-bc3b-d22ddf90000e" azonosítójú alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-147">Creates a new AD service principal for the application with application id '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span></span> <span data-ttu-id="ee2f7-148">Mivel nincs megadva érték `Role` `Scope` , vagy a létrehozta a Service Principal szolgáltatáshoz nincs engedélye.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-148">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="ee2f7-149">6 példa – új AD-szolgáltató létrehozása csővezetékek használatával</span><span class="sxs-lookup"><span data-stu-id="ee2f7-149">Example 6 - Create a new AD service principal using piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzureRmADServicePrincipal
```

<span data-ttu-id="ee2f7-150">Beilleszti az alkalmazást a "3ede3c26-b443-4e0b-9efc-b05e68338dc3" azonosítójú objektumazonosítót, valamint a New-AzureRmADServicePrincipal parancsmagot tartalmazó csöveket, amelyekkel új AD-szolgáltatót hozhat létre az adott alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-150">Gets the application with object id '3ede3c26-b443-4e0b-9efc-b05e68338dc3' and pipes that to the New-AzureRmADServicePrincipal cmdlet to create a new AD service principal for that application.</span></span>

## <span data-ttu-id="ee2f7-151">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ee2f7-151">PARAMETERS</span></span>

### <span data-ttu-id="ee2f7-152">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ee2f7-152">-ApplicationId</span></span>
<span data-ttu-id="ee2f7-153">Egy szolgáltató egyedi alkalmazásspecifikus azonosítója bérlői fiókban.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-153">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="ee2f7-154">Miután létrehozta ezt a tulajdonságot, nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-154">Once created this property cannot be changed.</span></span>
<span data-ttu-id="ee2f7-155">Ha egy alkalmazás-azonosító nincs megadva, a program létrehoz egy azonosítót.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-155">If an application id is not specified, one will be generated.</span></span>

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

### <span data-ttu-id="ee2f7-156">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="ee2f7-156">-ApplicationObject</span></span>
<span data-ttu-id="ee2f7-157">Annak az alkalmazásnak az objektuma, amelybe a szolgáltatásnevet létrehozta.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-157">The object representing the application for which the service principal is created.</span></span>

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

### <span data-ttu-id="ee2f7-158">-CertValue</span><span class="sxs-lookup"><span data-stu-id="ee2f7-158">-CertValue</span></span>
<span data-ttu-id="ee2f7-159">Az "aszimmetrikus" hitelesítőadat-típus értéke.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-159">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="ee2f7-160">A 64 kódolt tanúsítványát jelöli.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-160">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="ee2f7-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee2f7-161">-DefaultProfile</span></span>
<span data-ttu-id="ee2f7-162">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ee2f7-162">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee2f7-163">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ee2f7-163">-DisplayName</span></span>
<span data-ttu-id="ee2f7-164">A szolgáltatás megbízójának rövid neve.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-164">The friendly name of the service principal.</span></span> <span data-ttu-id="ee2f7-165">Ha a megjelenítendő név nem szerepel a listában, akkor ez az érték alapértelmezés szerint "Azure-PowerShell-HH-NN-ÉÉÉÉ-HH-HH-HH", ahol az utótag az alkalmazás létrehozásának időpontja.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-165">If a display name is not provided, this value will default to 'azure-powershell-MM-dd-yyyy-HH-mm-ss', where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="ee2f7-166">-EndDate</span><span class="sxs-lookup"><span data-stu-id="ee2f7-166">-EndDate</span></span>
<span data-ttu-id="ee2f7-167">A hitelesítő adatok használatának tényleges befejezési dátuma.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-167">The effective end date of the credential usage.</span></span>
<span data-ttu-id="ee2f7-168">Az alapértelmezett befejezési dátum értéke egy év a mai naptól számítva.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-168">The default end date value is one year from today.</span></span> <span data-ttu-id="ee2f7-169">Ha "aszimmetrikus" típusú hitelesítő adatokra van szükség, ezt a X509 tanúsítvány érvényességi dátumának be vagy ki kell állítania.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-169">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="ee2f7-170">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="ee2f7-170">-KeyCredential</span></span>
<span data-ttu-id="ee2f7-171">Az alkalmazáshoz társított legfontosabb hitelesítő adatok gyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-171">The collection of key credentials associated with the application.</span></span>

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

### <span data-ttu-id="ee2f7-172">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="ee2f7-172">-Password</span></span>
<span data-ttu-id="ee2f7-173">A szolgáltatásnevet társítani kívánt jelszó.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-173">The password to be associated with the service principal.</span></span> <span data-ttu-id="ee2f7-174">Ha nem ad meg jelszót, a program véletlenszerű globális azonosítót hoz létre, és a jelszót használja.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-174">If a password is not provided, a random GUID will be generated and used as the password.</span></span>

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

### <span data-ttu-id="ee2f7-175">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="ee2f7-175">-PasswordCredential</span></span>
<span data-ttu-id="ee2f7-176">Az alkalmazáshoz társított jelszó-hitelesítő adatok gyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-176">The collection of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="ee2f7-177">-Role (szerepkör)</span><span class="sxs-lookup"><span data-stu-id="ee2f7-177">-Role</span></span>
<span data-ttu-id="ee2f7-178">Annak a szerepkörnek a szerepe, amelyet a szolgáltató a hatókör felett tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-178">The role that the service principal has over the scope.</span></span> <span data-ttu-id="ee2f7-179">Ha meg `Scope` van határozva egy érték, de nincs megadva érték `Role` , akkor `Role` az alapértelmezett érték a "munkatárs" szerepkört adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-179">If a value for `Scope` is provided, but no value is provided for `Role`, then `Role` will default to the 'Contributor' role.</span></span>

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

### <span data-ttu-id="ee2f7-180">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="ee2f7-180">-Scope</span></span>
<span data-ttu-id="ee2f7-181">Az a hatókör, amelyre a szolgáltatónak van engedélye.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-181">The scope that the service principal has permissions on.</span></span> <span data-ttu-id="ee2f7-182">Ha meg `Role` van határozva egy érték, de nincs megadva érték `Scope` , akkor `Scope` az alapértelmezés szerint az aktuális előfizetést adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-182">If a value for `Role` is provided, but no value is provided for `Scope`, then `Scope` will default to the current subscription.</span></span>

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

### <span data-ttu-id="ee2f7-183">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="ee2f7-183">-SkipAssignment</span></span>
<span data-ttu-id="ee2f7-184">Ha be van állítva, akkor a program kihagyja az alapértelmezett szerepkör-hozzárendelés létrehozását a szolgáltatónál.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-184">If set, will skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="ee2f7-185">-StartDate</span><span class="sxs-lookup"><span data-stu-id="ee2f7-185">-StartDate</span></span>
<span data-ttu-id="ee2f7-186">A hitelesítő adatok használatának tényleges kezdési dátuma.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-186">The effective start date of the credential usage.</span></span>
<span data-ttu-id="ee2f7-187">A kezdő dátum alapértelmezett értéke ma.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-187">The default start date value is today.</span></span> <span data-ttu-id="ee2f7-188">Ha "aszimmetrikus" típusú hitelesítő adatokra van szükség, ezt a X509-tanúsítvány érvényességi dátumának be vagy mögé kell állítani.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-188">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="ee2f7-189">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ee2f7-189">-Confirm</span></span>
<span data-ttu-id="ee2f7-190">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-190">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee2f7-191">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee2f7-191">-WhatIf</span></span>
<span data-ttu-id="ee2f7-192">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-192">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee2f7-193">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ee2f7-193">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee2f7-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee2f7-194">CommonParameters</span></span>
<span data-ttu-id="ee2f7-195">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ee2f7-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee2f7-196">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee2f7-196">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee2f7-197">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee2f7-197">INPUTS</span></span>

### <span data-ttu-id="ee2f7-198">System. GUID</span><span class="sxs-lookup"><span data-stu-id="ee2f7-198">System.Guid</span></span>

### <span data-ttu-id="ee2f7-199">System. String</span><span class="sxs-lookup"><span data-stu-id="ee2f7-199">System.String</span></span>

### <span data-ttu-id="ee2f7-200">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="ee2f7-200">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="ee2f7-201">Paraméterek: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ee2f7-201">Parameters: ApplicationObject (ByValue)</span></span>

### <span data-ttu-id="ee2f7-202">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="ee2f7-202">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="ee2f7-203">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="ee2f7-203">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="ee2f7-204">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="ee2f7-204">System.Security.SecureString</span></span>

### <span data-ttu-id="ee2f7-205">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="ee2f7-205">System.DateTime</span></span>

## <span data-ttu-id="ee2f7-206">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee2f7-206">OUTPUTS</span></span>

### <span data-ttu-id="ee2f7-207">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ee2f7-207">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="ee2f7-208">Microsoft. Azure. Command. Resources. modellek. Authorization. PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="ee2f7-208">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="ee2f7-209">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ee2f7-209">NOTES</span></span>
<span data-ttu-id="ee2f7-210">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="ee2f7-210">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="ee2f7-211">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee2f7-211">RELATED LINKS</span></span>

[<span data-ttu-id="ee2f7-212">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ee2f7-212">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="ee2f7-213">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ee2f7-213">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="ee2f7-214">Új – AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="ee2f7-214">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="ee2f7-215">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="ee2f7-215">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="ee2f7-216">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="ee2f7-216">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="ee2f7-217">Új – AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="ee2f7-217">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="ee2f7-218">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="ee2f7-218">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

