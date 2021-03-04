---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 488229AF-FD6D-4E1B-B3DA-E57CA781D91E
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleAssignment.md
ms.openlocfilehash: dd59b49ad4002d38cd9a49506cb1723b5ac1e426
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942225"
---
# <span data-ttu-id="dbcc4-101">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="dbcc4-101">Get-AzRoleAssignment</span></span>

## <span data-ttu-id="dbcc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbcc4-102">SYNOPSIS</span></span>
<span data-ttu-id="dbcc4-103">A megadott hatókörű Azure RBAC-szerepkör-hozzárendelések listája.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-103">Lists Azure RBAC role assignments at the specified scope.</span></span>
<span data-ttu-id="dbcc4-104">Alapértelmezés szerint a kijelölt Azure-előfizetés összes szerepkör-hozzárendelését felsorolja.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-104">By default it lists all role assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="dbcc4-105">A megfelelő paramétereket használva listába sorolja egy adott felhasználó hozzárendelését, illetve egy adott erőforráscsoport vagy erőforrás hozzárendelését.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-105">Use respective parameters to list assignments to a specific user, or to list assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="dbcc4-106">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dbcc4-106">SYNTAX</span></span>

### <span data-ttu-id="dbcc4-107">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dbcc4-107">EmptyParameterSet (Default)</span></span>
```
Get-AzRoleAssignment [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbcc4-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbcc4-108">ObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbcc4-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbcc4-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbcc4-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbcc4-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbcc4-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbcc4-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbcc4-112">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbcc4-112">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment [-ObjectId <String>] -RoleDefinitionId <Guid> [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbcc4-113">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbcc4-113">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbcc4-114">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbcc4-114">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbcc4-115">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbcc4-115">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbcc4-116">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbcc4-116">SignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbcc4-117">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbcc4-117">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbcc4-118">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbcc4-118">ResourceWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbcc4-119">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbcc4-119">ScopeWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbcc4-120">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbcc4-120">SPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbcc4-121">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbcc4-121">ResourceGroupParameterSet</span></span>
```
Get-AzRoleAssignment -ResourceGroupName <String> [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbcc4-122">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbcc4-122">ResourceParameterSet</span></span>
```
Get-AzRoleAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbcc4-123">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbcc4-123">ScopeParameterSet</span></span>
```
Get-AzRoleAssignment [-RoleDefinitionName <String>] -Scope <String> [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbcc4-124">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dbcc4-124">DESCRIPTION</span></span>
<span data-ttu-id="dbcc4-125">A Get-AzRoleAssignment paranccsal felsorolja az összes olyan szerepkör-hozzárendelést, amely hatókör szerint hatékony.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-125">Use the Get-AzRoleAssignment command to list all role assignments that are effective on a scope.</span></span>
<span data-ttu-id="dbcc4-126">Paraméterek nélkül ez a parancs az előfizetésben megadott összes szerepkör-hozzárendelést visszaadja.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-126">Without any parameters, this command returns all the role assignments made under the subscription.</span></span>
<span data-ttu-id="dbcc4-127">Ez a lista szűrhető a főnév, a szerepkör és a hatókör szűrési paramétereivel.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-127">This list can  be filtered using filtering parameters for principal, role and scope.</span></span>
<span data-ttu-id="dbcc4-128">A feladat tárgyát meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-128">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="dbcc4-129">Felhasználó megadásához használja a SignInName vagy az Azure AD ObjectId paramétereit.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="dbcc4-130">Biztonsági csoport megadásához használja az Azure AD ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="dbcc4-131">Azure AD-alkalmazás megadásához használja a ServicePrincipalName vagy az ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="dbcc4-132">A hozzárendelt szerepkört a RoleDefinitionName paraméterrel kell megadni.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-132">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="dbcc4-133">A hozzáférés hatóköre meg lehet adni.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-133">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="dbcc4-134">Alapértelmezés szerint a kijelölt előfizetést használja.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-134">It defaults to the selected subscription.</span></span> <span data-ttu-id="dbcc4-135">A hozzárendelés hatóköre a következő paraméterkombinációk egyikével (a) lehet megadni.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-135">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="dbcc4-136">Hatókör – Ez a teljesen minősített hatókör az /subscriptions/ tartománytól \<subscriptionId\> kezdve.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-136">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="dbcc4-137">Ezzel szűri az adott hatókörben, azaz az adott hatókörben és a fenti hatókörben minden hozzárendelést.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-137">This will filter assignments that are effective at that particular scope i.e. all assignments at that scope and above.</span></span>
<span data-ttu-id="dbcc4-138">b.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-138">b.</span></span>
<span data-ttu-id="dbcc4-139">ResourceGroupName – Az előfizetés alatt bármelyik erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-139">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="dbcc4-140">Ezzel szűri a hozzárendeléseket, amelyek a megadott erőforráscsoportban (c) lesznek használatban.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-140">This will filter assignments effective at the specified resource group c.</span></span>
<span data-ttu-id="dbcc4-141">ResourceName, ResourceType, ResourceGroupName és (nem kötelező) ParentResource – Azonosítja az előfizetés egy adott erőforrását, és szűri a hozzárendeléseket az adott erőforrás-hatókör szerint.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter assignments effective at that resource scope.</span></span>
<span data-ttu-id="dbcc4-142">Ha meg szeretné állapítani, hogy egy adott felhasználó milyen hozzáféréssel rendelkezik az előfizetéshez, használja az ExpandPrincipalGroups kapcsolót.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-142">To determine what access a particular user has in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="dbcc4-143">Ez felsorolja a felhasználóhoz és azon csoportokhoz rendelt összes szerepkört, amelyekhez a felhasználó tagja.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-143">This will list all roles assigned to the user, and to the groups that the user is member of.</span></span>
<span data-ttu-id="dbcc4-144">Használja az IncludeClassicAdministrators kapcsolót az előfizetés-rendszergazdák és a társadminisztrátorok megjelenítéséhez is.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-144">Use the IncludeClassicAdministrators switch to also display the subscription admins and co-admins.</span></span>

## <span data-ttu-id="dbcc4-145">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dbcc4-145">EXAMPLES</span></span>

### <span data-ttu-id="dbcc4-146">1. példa</span><span class="sxs-lookup"><span data-stu-id="dbcc4-146">Example 1</span></span>
```
PS C:\> Get-AzRoleAssignment
```

<span data-ttu-id="dbcc4-147">Az előfizetés összes szerepkör-hozzárendelésének felsorolása</span><span class="sxs-lookup"><span data-stu-id="dbcc4-147">List all role assignments in the subscription</span></span>

### <span data-ttu-id="dbcc4-148">2. példa</span><span class="sxs-lookup"><span data-stu-id="dbcc4-148">Example 2</span></span>
```
PS C:\> Get-AzRoleAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com
```

<span data-ttu-id="dbcc4-149">Az összes szerepkör-hozzárendelést megkapja, amelyet a felhasználónak – és amelynek tagja – a testRG hatókörében vagy john.doe@contoso.com felett.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-149">Gets all role assignments made to user john.doe@contoso.com, and the groups of which he is member, at the testRG scope or above.</span></span>

### <span data-ttu-id="dbcc4-150">3. példa</span><span class="sxs-lookup"><span data-stu-id="dbcc4-150">Example 3</span></span>
```
PS C:\> Get-AzRoleAssignment -ServicePrincipalName "http://testapp1.com"
```

<span data-ttu-id="dbcc4-151">A megadott egyszerű szolgáltatásnév összes szerepkör-hozzárendelését lekérte</span><span class="sxs-lookup"><span data-stu-id="dbcc4-151">Gets all role assignments of the specified service principal</span></span>

### <span data-ttu-id="dbcc4-152">4. példa</span><span class="sxs-lookup"><span data-stu-id="dbcc4-152">Example 4</span></span>
```
PS C:\> Get-AzRoleAssignment -Scope "/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="dbcc4-153">Szerepkör-hozzárendeléseket kap a "webhely1" webhely hatókörében.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-153">Gets role assignments at the 'site1' website scope.</span></span>

## <span data-ttu-id="dbcc4-154">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbcc4-154">PARAMETERS</span></span>

### <span data-ttu-id="dbcc4-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbcc4-155">-DefaultProfile</span></span>
<span data-ttu-id="dbcc4-156">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="dbcc4-156">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dbcc4-157">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="dbcc4-157">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="dbcc4-158">Ha meg van adva, a felhasználóhoz közvetlenül hozzárendelt szerepköröket, valamint azokat a csoportokat adja vissza, amelyekhez a felhasználó tag (átvitel közben).</span><span class="sxs-lookup"><span data-stu-id="dbcc4-158">If specified, returns roles directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="dbcc4-159">Csak egyszerű felhasználó esetén támogatott.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-159">Supported only for a user principal.</span></span>

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

### <span data-ttu-id="dbcc4-160">-IncludeClassicAdministrators</span><span class="sxs-lookup"><span data-stu-id="dbcc4-160">-IncludeClassicAdministrators</span></span>
<span data-ttu-id="dbcc4-161">Ha meg van adva, akkor az előfizetés klasszikus rendszergazdái (társadminisztránsok, szolgáltatás-rendszergazdák stb.) szerepkör-hozzárendelései is megjelennek.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-161">If specified, also lists subscription classic administrators (co-admins, service admins, etc.) role assignments.</span></span>

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

### <span data-ttu-id="dbcc4-162">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="dbcc4-162">-ObjectId</span></span>
<span data-ttu-id="dbcc4-163">A felhasználó, csoport vagy szolgáltatásnév Azure AD-objektumazonosítója.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-163">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="dbcc4-164">A megadott egyszerű feladathoz adott összes hozzárendelést szűri.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-164">Filters all assignments that are made to the specified principal.</span></span>

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

### <span data-ttu-id="dbcc4-165">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="dbcc4-165">-ParentResource</span></span>
<span data-ttu-id="dbcc4-166">A szülőerőforrás a ResourceName paraméterrel megadott erőforrás hierarchiában.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-166">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="dbcc4-167">A ResourceGroupName, az ResourceType és az ResourceName paraméterekkel együtt kell használni.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-167">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

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

### <span data-ttu-id="dbcc4-168">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbcc4-168">-ResourceGroupName</span></span>
<span data-ttu-id="dbcc4-169">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-169">The resource group name.</span></span>
<span data-ttu-id="dbcc4-170">A megadott erőforráscsoportban hatályos szerepkör-hozzárendelések listája.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-170">Lists role assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="dbcc4-171">Az Erőforrásnév, Az Erőforrás típusa és a ParentResource paraméterekkel együtt használva a parancs felsorolja a hozzárendeléseket, amelyek az erőforráscsoportban lévő erőforrásoknál hatékonyak.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-171">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists assignments effective at resources within the resource group.</span></span>

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

### <span data-ttu-id="dbcc4-172">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="dbcc4-172">-ResourceName</span></span>
<span data-ttu-id="dbcc4-173">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-173">The resource name.</span></span>
<span data-ttu-id="dbcc4-174">Például: storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-174">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="dbcc4-175">Az ResourceGroupName, az ResourceType és (opcionális) ParentResource paraméterekkel együtt kell használni.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-175">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="dbcc4-176">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="dbcc4-176">-ResourceType</span></span>
<span data-ttu-id="dbcc4-177">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-177">The resource type.</span></span>
<span data-ttu-id="dbcc4-178">Például: Microsoft.Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-178">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="dbcc4-179">A ResourceGroupName, az ResourceName és a ParentResource paraméterekkel együtt kell használni.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-179">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="dbcc4-180">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="dbcc4-180">-RoleDefinitionId</span></span>
<span data-ttu-id="dbcc4-181">A főnévhez hozzárendelt szerepkör azonosítója.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-181">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="dbcc4-182">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="dbcc4-182">-RoleDefinitionName</span></span>
<span data-ttu-id="dbcc4-183">A fő felhasználóhoz (olvasó, közreműködő, virtuális hálózati rendszergazda stb.) hozzárendelt szerepkör.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-183">Role that is assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

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

### <span data-ttu-id="dbcc4-184">-Scope</span><span class="sxs-lookup"><span data-stu-id="dbcc4-184">-Scope</span></span>
<span data-ttu-id="dbcc4-185">A szerepkör-hozzárendelés hatóköre.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-185">The Scope of the role assignment.</span></span>
<span data-ttu-id="dbcc4-186">Relatív URI formátumban.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-186">In the format of relative URI.</span></span>
<span data-ttu-id="dbcc4-187">Például: /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-187">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="dbcc4-188">A műveletnek a következővel kell kezdődnie: "/subscriptions/{id}".</span><span class="sxs-lookup"><span data-stu-id="dbcc4-188">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="dbcc4-189">A parancs az összes olyan hozzárendelést szűri, amely ebben a hatókörben hatékony.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-189">The command filters all assignments that are effective at that scope.</span></span>

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

### <span data-ttu-id="dbcc4-190">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="dbcc4-190">-ServicePrincipalName</span></span>
<span data-ttu-id="dbcc4-191">A szolgáltatásnév ServicePrincipalName tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-191">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="dbcc4-192">A megadott Azure AD-alkalmazáshoz készült összes hozzárendelést szűri.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-192">Filters all assignments that are made to the specified Azure AD application.</span></span>

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

### <span data-ttu-id="dbcc4-193">-SignInName</span><span class="sxs-lookup"><span data-stu-id="dbcc4-193">-SignInName</span></span>
<span data-ttu-id="dbcc4-194">A felhasználó e-mail-címe vagy egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-194">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="dbcc4-195">A megadott felhasználóhoz adott összes hozzárendelést szűri.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-195">Filters all assignments that are made to the specified user.</span></span>

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

### <span data-ttu-id="dbcc4-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbcc4-196">CommonParameters</span></span>
<span data-ttu-id="dbcc4-197">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbcc4-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbcc4-198">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dbcc4-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbcc4-199">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dbcc4-199">INPUTS</span></span>

### <span data-ttu-id="dbcc4-200">System.String</span><span class="sxs-lookup"><span data-stu-id="dbcc4-200">System.String</span></span>

### <span data-ttu-id="dbcc4-201">System.Guid</span><span class="sxs-lookup"><span data-stu-id="dbcc4-201">System.Guid</span></span>

## <span data-ttu-id="dbcc4-202">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dbcc4-202">OUTPUTS</span></span>

### <span data-ttu-id="dbcc4-203">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="dbcc4-203">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="dbcc4-204">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dbcc4-204">NOTES</span></span>
<span data-ttu-id="dbcc4-205">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, telepítés</span><span class="sxs-lookup"><span data-stu-id="dbcc4-205">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="dbcc4-206">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dbcc4-206">RELATED LINKS</span></span>

[<span data-ttu-id="dbcc4-207">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="dbcc4-207">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="dbcc4-208">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="dbcc4-208">Remove-AzRoleAssignment</span></span>](./Remove-AzRoleAssignment.md)

[<span data-ttu-id="dbcc4-209">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="dbcc4-209">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

