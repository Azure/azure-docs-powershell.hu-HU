---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 488229AF-FD6D-4E1B-B3DA-E57CA781D91E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleAssignment.md
ms.openlocfilehash: 1b96617ce162f3b024cc8a5bd7df2d66c3820c38
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365887"
---
# <span data-ttu-id="5827c-101">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5827c-101">Get-AzRoleAssignment</span></span>

## <span data-ttu-id="5827c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5827c-102">SYNOPSIS</span></span>
<span data-ttu-id="5827c-103">A megadott hatókörű Azure RBAC-szerepkör-hozzárendelések listája.</span><span class="sxs-lookup"><span data-stu-id="5827c-103">Lists Azure RBAC role assignments at the specified scope.</span></span>
<span data-ttu-id="5827c-104">Alapértelmezés szerint a kijelölt Azure-előfizetés összes szerepkör-hozzárendelését felsorolja.</span><span class="sxs-lookup"><span data-stu-id="5827c-104">By default it lists all role assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="5827c-105">A megfelelő paramétereket használva listába sorolja egy adott felhasználó hozzárendelését, illetve egy adott erőforráscsoport vagy erőforrás hozzárendelését.</span><span class="sxs-lookup"><span data-stu-id="5827c-105">Use respective parameters to list assignments to a specific user, or to list assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="5827c-106">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5827c-106">SYNTAX</span></span>

### <span data-ttu-id="5827c-107">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5827c-107">EmptyParameterSet (Default)</span></span>
```
Get-AzRoleAssignment [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5827c-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5827c-108">ObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5827c-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5827c-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5827c-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5827c-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5827c-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5827c-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5827c-112">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5827c-112">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment [-ObjectId <String>] -RoleDefinitionId <Guid> [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5827c-113">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5827c-113">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5827c-114">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5827c-114">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5827c-115">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5827c-115">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5827c-116">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5827c-116">SignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5827c-117">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="5827c-117">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5827c-118">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="5827c-118">ResourceWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5827c-119">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="5827c-119">ScopeWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5827c-120">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="5827c-120">SPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5827c-121">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="5827c-121">ResourceGroupParameterSet</span></span>
```
Get-AzRoleAssignment -ResourceGroupName <String> [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5827c-122">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="5827c-122">ResourceParameterSet</span></span>
```
Get-AzRoleAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5827c-123">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="5827c-123">ScopeParameterSet</span></span>
```
Get-AzRoleAssignment [-RoleDefinitionName <String>] -Scope <String> [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5827c-124">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5827c-124">DESCRIPTION</span></span>
<span data-ttu-id="5827c-125">A Get-AzRoleAssignment paranccsal felsorolja az összes olyan szerepkör-hozzárendelést, amely hatókör szerint hatékony.</span><span class="sxs-lookup"><span data-stu-id="5827c-125">Use the Get-AzRoleAssignment command to list all role assignments that are effective on a scope.</span></span>
<span data-ttu-id="5827c-126">Paraméterek nélkül ez a parancs az előfizetésben megadott összes szerepkör-hozzárendelést visszaadja.</span><span class="sxs-lookup"><span data-stu-id="5827c-126">Without any parameters, this command returns all the role assignments made under the subscription.</span></span>
<span data-ttu-id="5827c-127">Ez a lista szűrhető a főnév, a szerepkör és a hatókör szűrési paramétereivel.</span><span class="sxs-lookup"><span data-stu-id="5827c-127">This list can  be filtered using filtering parameters for principal, role and scope.</span></span>
<span data-ttu-id="5827c-128">A feladat tárgyát meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="5827c-128">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="5827c-129">Felhasználó megadásához használja a SignInName vagy az Azure AD ObjectId paramétereit.</span><span class="sxs-lookup"><span data-stu-id="5827c-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="5827c-130">Biztonsági csoport megadásához használja az Azure AD ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="5827c-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="5827c-131">Azure AD-alkalmazás megadásához használja a ServicePrincipalName vagy az ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="5827c-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="5827c-132">A hozzárendelt szerepkört a RoleDefinitionName paraméterrel kell megadni.</span><span class="sxs-lookup"><span data-stu-id="5827c-132">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="5827c-133">A hozzáférés hatóköre meg lehet adni.</span><span class="sxs-lookup"><span data-stu-id="5827c-133">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="5827c-134">Alapértelmezés szerint a kijelölt előfizetést használja.</span><span class="sxs-lookup"><span data-stu-id="5827c-134">It defaults to the selected subscription.</span></span> <span data-ttu-id="5827c-135">A hozzárendelés hatóköre a következő paraméterkombinációk egyikével (a) lehet megadni.</span><span class="sxs-lookup"><span data-stu-id="5827c-135">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="5827c-136">Hatókör – Ez a teljesen minősített hatókör az /subscriptions/ tartománytól \<subscriptionId\> kezdve.</span><span class="sxs-lookup"><span data-stu-id="5827c-136">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="5827c-137">Ezzel szűri az adott hatókörben, azaz az adott hatókörben és a fenti hatókörben minden hozzárendelést.</span><span class="sxs-lookup"><span data-stu-id="5827c-137">This will filter assignments that are effective at that particular scope i.e. all assignments at that scope and above.</span></span>
<span data-ttu-id="5827c-138">b.</span><span class="sxs-lookup"><span data-stu-id="5827c-138">b.</span></span>
<span data-ttu-id="5827c-139">ResourceGroupName – Az előfizetés alatt bármelyik erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5827c-139">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="5827c-140">Ezzel szűri a hozzárendeléseket, amelyek a megadott erőforráscsoportban (c) lesznek használatban.</span><span class="sxs-lookup"><span data-stu-id="5827c-140">This will filter assignments effective at the specified resource group c.</span></span>
<span data-ttu-id="5827c-141">ResourceName, ResourceType, ResourceGroupName és (nem kötelező) ParentResource – Azonosítja az előfizetés egy adott erőforrását, és szűri a hozzárendeléseket az adott erőforrás-hatókör szerint.</span><span class="sxs-lookup"><span data-stu-id="5827c-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter assignments effective at that resource scope.</span></span>
<span data-ttu-id="5827c-142">Ha meg szeretné állapítani, hogy egy adott felhasználó milyen hozzáféréssel rendelkezik az előfizetéshez, használja az ExpandPrincipalGroups kapcsolót.</span><span class="sxs-lookup"><span data-stu-id="5827c-142">To determine what access a particular user has in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="5827c-143">Ez felsorolja a felhasználóhoz és azon csoportokhoz rendelt összes szerepkört, amelyekhez a felhasználó tagja.</span><span class="sxs-lookup"><span data-stu-id="5827c-143">This will list all roles assigned to the user, and to the groups that the user is member of.</span></span>
<span data-ttu-id="5827c-144">Használja az IncludeClassicAdministrators kapcsolót az előfizetés-rendszergazdák és a társadminisztrátorok megjelenítéséhez is.</span><span class="sxs-lookup"><span data-stu-id="5827c-144">Use the IncludeClassicAdministrators switch to also display the subscription admins and co-admins.</span></span>

## <span data-ttu-id="5827c-145">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5827c-145">EXAMPLES</span></span>

### <span data-ttu-id="5827c-146">1. példa</span><span class="sxs-lookup"><span data-stu-id="5827c-146">Example 1</span></span>
```
PS C:\> Get-AzRoleAssignment
```

<span data-ttu-id="5827c-147">Az előfizetés összes szerepkör-hozzárendelésének felsorolása</span><span class="sxs-lookup"><span data-stu-id="5827c-147">List all role assignments in the subscription</span></span>

### <span data-ttu-id="5827c-148">2. példa</span><span class="sxs-lookup"><span data-stu-id="5827c-148">Example 2</span></span>
```
PS C:\> Get-AzRoleAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com
```

<span data-ttu-id="5827c-149">Az összes szerepkör-hozzárendelést megkapja, amelyet a felhasználónak – és amelynek tagja – a testRG hatókörében vagy john.doe@contoso.com felett.</span><span class="sxs-lookup"><span data-stu-id="5827c-149">Gets all role assignments made to user john.doe@contoso.com, and the groups of which he is member, at the testRG scope or above.</span></span>

### <span data-ttu-id="5827c-150">3. példa</span><span class="sxs-lookup"><span data-stu-id="5827c-150">Example 3</span></span>
```
PS C:\> Get-AzRoleAssignment -ServicePrincipalName "http://testapp1.com"
```

<span data-ttu-id="5827c-151">A megadott egyszerű szolgáltatásnév összes szerepkör-hozzárendelését lekérte</span><span class="sxs-lookup"><span data-stu-id="5827c-151">Gets all role assignments of the specified service principal</span></span>

### <span data-ttu-id="5827c-152">4. példa</span><span class="sxs-lookup"><span data-stu-id="5827c-152">Example 4</span></span>
```
PS C:\> Get-AzRoleAssignment -Scope "/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="5827c-153">Szerepkör-hozzárendeléseket kap a "webhely1" webhely hatókörében.</span><span class="sxs-lookup"><span data-stu-id="5827c-153">Gets role assignments at the 'site1' website scope.</span></span>

## <span data-ttu-id="5827c-154">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5827c-154">PARAMETERS</span></span>

### <span data-ttu-id="5827c-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5827c-155">-DefaultProfile</span></span>
<span data-ttu-id="5827c-156">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5827c-156">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5827c-157">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="5827c-157">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="5827c-158">Ha meg van adva, visszaadja a felhasználóhoz közvetlenül hozzárendelt szerepköröket, valamint azokat a csoportokat, amelyekhez a felhasználó tag (átvitel közben).</span><span class="sxs-lookup"><span data-stu-id="5827c-158">If specified, returns roles directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="5827c-159">Csak egyszerű felhasználó esetén támogatott.</span><span class="sxs-lookup"><span data-stu-id="5827c-159">Supported only for a user principal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ObjectIdParameterSet, SignInNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5827c-160">-IncludeClassicAdministrators</span><span class="sxs-lookup"><span data-stu-id="5827c-160">-IncludeClassicAdministrators</span></span>
<span data-ttu-id="5827c-161">Ha meg van adva, akkor az előfizetés klasszikus rendszergazdái (társadminisztránsok, szolgáltatás-rendszergazdák stb.) szerepkör-hozzárendelései is megjelennek.</span><span class="sxs-lookup"><span data-stu-id="5827c-161">If specified, also lists subscription classic administrators (co-admins, service admins, etc.) role assignments.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EmptyParameterSet, ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet, ScopeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5827c-162">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="5827c-162">-ObjectId</span></span>
<span data-ttu-id="5827c-163">A felhasználó, csoport vagy szolgáltatásnév Azure AD-objektumazonosítója.</span><span class="sxs-lookup"><span data-stu-id="5827c-163">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="5827c-164">A megadott egyszerű feladathoz adott összes hozzárendelést szűri.</span><span class="sxs-lookup"><span data-stu-id="5827c-164">Filters all assignments that are made to the specified principal.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5827c-165">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="5827c-165">-ParentResource</span></span>
<span data-ttu-id="5827c-166">A szülőerőforrás a ResourceName paraméterrel megadott erőforrás hierarchiában.</span><span class="sxs-lookup"><span data-stu-id="5827c-166">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="5827c-167">A ResourceGroupName, az ResourceType és az ResourceName paraméterekkel együtt kell használni.</span><span class="sxs-lookup"><span data-stu-id="5827c-167">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5827c-168">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5827c-168">-ResourceGroupName</span></span>
<span data-ttu-id="5827c-169">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5827c-169">The resource group name.</span></span>
<span data-ttu-id="5827c-170">A megadott erőforráscsoportban hatályos szerepkör-hozzárendelések listája.</span><span class="sxs-lookup"><span data-stu-id="5827c-170">Lists role assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="5827c-171">Az Erőforrásnév, Az Erőforrás típusa és a ParentResource paraméterekkel együtt használva a parancs felsorolja a hozzárendeléseket, amelyek az erőforráscsoportban lévő erőforrásoknál hatékonyak.</span><span class="sxs-lookup"><span data-stu-id="5827c-171">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists assignments effective at resources within the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5827c-172">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="5827c-172">-ResourceName</span></span>
<span data-ttu-id="5827c-173">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="5827c-173">The resource name.</span></span>
<span data-ttu-id="5827c-174">Például: storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="5827c-174">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="5827c-175">Az ResourceGroupName, az ResourceType és (opcionális) ParentResource paraméterekkel együtt kell használni.</span><span class="sxs-lookup"><span data-stu-id="5827c-175">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5827c-176">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="5827c-176">-ResourceType</span></span>
<span data-ttu-id="5827c-177">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="5827c-177">The resource type.</span></span>
<span data-ttu-id="5827c-178">Például: Microsoft.Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="5827c-178">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="5827c-179">A ResourceGroupName, az ResourceName és a ParentResource paraméterekkel együtt kell használni.</span><span class="sxs-lookup"><span data-stu-id="5827c-179">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5827c-180">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="5827c-180">-RoleDefinitionId</span></span>
<span data-ttu-id="5827c-181">A főnévhez hozzárendelt szerepkör azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5827c-181">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5827c-182">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="5827c-182">-RoleDefinitionName</span></span>
<span data-ttu-id="5827c-183">A fő felhasználóhoz (olvasó, közreműködő, virtuális hálózati rendszergazda stb.) hozzárendelt szerepkör.</span><span class="sxs-lookup"><span data-stu-id="5827c-183">Role that is assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet, ScopeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5827c-184">-Scope</span><span class="sxs-lookup"><span data-stu-id="5827c-184">-Scope</span></span>
<span data-ttu-id="5827c-185">A szerepkör-hozzárendelés hatóköre.</span><span class="sxs-lookup"><span data-stu-id="5827c-185">The Scope of the role assignment.</span></span>
<span data-ttu-id="5827c-186">Relatív URI formátumban.</span><span class="sxs-lookup"><span data-stu-id="5827c-186">In the format of relative URI.</span></span>
<span data-ttu-id="5827c-187">Például: /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="5827c-187">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="5827c-188">A műveletnek a következővel kell kezdődnie: "/subscriptions/{id}".</span><span class="sxs-lookup"><span data-stu-id="5827c-188">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="5827c-189">A parancs az összes olyan hozzárendelést szűri, amely ebben a hatókörben hatékony.</span><span class="sxs-lookup"><span data-stu-id="5827c-189">The command filters all assignments that are effective at that scope.</span></span>

```yaml
Type: System.String
Parameter Sets: ScopeWithObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet, ScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5827c-190">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="5827c-190">-ServicePrincipalName</span></span>
<span data-ttu-id="5827c-191">A szolgáltatásnév ServicePrincipalName tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="5827c-191">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="5827c-192">A megadott Azure AD-alkalmazáshoz készült összes hozzárendelést szűri.</span><span class="sxs-lookup"><span data-stu-id="5827c-192">Filters all assignments that are made to the specified Azure AD application.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5827c-193">-SignInName</span><span class="sxs-lookup"><span data-stu-id="5827c-193">-SignInName</span></span>
<span data-ttu-id="5827c-194">A felhasználó e-mail-címe vagy egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="5827c-194">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="5827c-195">A megadott felhasználóhoz adott összes hozzárendelést szűri.</span><span class="sxs-lookup"><span data-stu-id="5827c-195">Filters all assignments that are made to the specified user.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5827c-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5827c-196">CommonParameters</span></span>
<span data-ttu-id="5827c-197">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5827c-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5827c-198">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5827c-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5827c-199">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5827c-199">INPUTS</span></span>

### <span data-ttu-id="5827c-200">System.String</span><span class="sxs-lookup"><span data-stu-id="5827c-200">System.String</span></span>

### <span data-ttu-id="5827c-201">System.Guid</span><span class="sxs-lookup"><span data-stu-id="5827c-201">System.Guid</span></span>

## <span data-ttu-id="5827c-202">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5827c-202">OUTPUTS</span></span>

### <span data-ttu-id="5827c-203">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5827c-203">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="5827c-204">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5827c-204">NOTES</span></span>
<span data-ttu-id="5827c-205">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, telepítés</span><span class="sxs-lookup"><span data-stu-id="5827c-205">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="5827c-206">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5827c-206">RELATED LINKS</span></span>

[<span data-ttu-id="5827c-207">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5827c-207">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="5827c-208">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5827c-208">Remove-AzRoleAssignment</span></span>](./Remove-AzRoleAssignment.md)

[<span data-ttu-id="5827c-209">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="5827c-209">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

