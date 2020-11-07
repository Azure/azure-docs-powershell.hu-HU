---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 488229AF-FD6D-4E1B-B3DA-E57CA781D91E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleAssignment.md
ms.openlocfilehash: 1fc81657b5e5be03daf191a1787ad342512d266e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669412"
---
# <span data-ttu-id="e35d2-101">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e35d2-101">Get-AzRoleAssignment</span></span>

## <span data-ttu-id="e35d2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e35d2-102">SYNOPSIS</span></span>
<span data-ttu-id="e35d2-103">Az Azure RBAC szerepkör-hozzárendeléseinek listája a megadott hatókörben.</span><span class="sxs-lookup"><span data-stu-id="e35d2-103">Lists Azure RBAC role assignments at the specified scope.</span></span>
<span data-ttu-id="e35d2-104">Alapértelmezés szerint a kijelölt Azure-előfizetésben lévő összes szerepkör-hozzárendelést felsorolja.</span><span class="sxs-lookup"><span data-stu-id="e35d2-104">By default it lists all role assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="e35d2-105">A megfelelő paraméterekkel felsorolhatja a hozzárendeléseket egy adott felhasználóhoz, illetve felsorolhatja egy adott erőforráscsoport vagy erőforrás hozzárendeléseit.</span><span class="sxs-lookup"><span data-stu-id="e35d2-105">Use respective parameters to list assignments to a specific user, or to list assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="e35d2-106">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e35d2-106">SYNTAX</span></span>

### <span data-ttu-id="e35d2-107">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e35d2-107">EmptyParameterSet (Default)</span></span>
```
Get-AzRoleAssignment [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e35d2-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e35d2-108">ObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e35d2-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e35d2-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e35d2-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e35d2-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e35d2-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e35d2-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e35d2-112">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e35d2-112">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment [-ObjectId <String>] -RoleDefinitionId <Guid> [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e35d2-113">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e35d2-113">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e35d2-114">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e35d2-114">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e35d2-115">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e35d2-115">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e35d2-116">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e35d2-116">SignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e35d2-117">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="e35d2-117">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e35d2-118">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="e35d2-118">ResourceWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e35d2-119">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="e35d2-119">ScopeWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e35d2-120">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="e35d2-120">SPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e35d2-121">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="e35d2-121">ResourceGroupParameterSet</span></span>
```
Get-AzRoleAssignment -ResourceGroupName <String> [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e35d2-122">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="e35d2-122">ResourceParameterSet</span></span>
```
Get-AzRoleAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e35d2-123">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="e35d2-123">ScopeParameterSet</span></span>
```
Get-AzRoleAssignment [-RoleDefinitionName <String>] -Scope <String> [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e35d2-124">Leírás</span><span class="sxs-lookup"><span data-stu-id="e35d2-124">DESCRIPTION</span></span>
<span data-ttu-id="e35d2-125">A Get-AzRoleAssignment parancs segítségével listázhatja az összes olyan szerepkör-hozzárendelést, amely egy hatókörre érvényes.</span><span class="sxs-lookup"><span data-stu-id="e35d2-125">Use the Get-AzRoleAssignment command to list all role assignments that are effective on a scope.</span></span>
<span data-ttu-id="e35d2-126">Paraméterek nélkül a parancs az előfizetésben szereplő összes szerepkör-hozzárendelést visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="e35d2-126">Without any parameters, this command returns all the role assignments made under the subscription.</span></span>
<span data-ttu-id="e35d2-127">Ezt a listát a megbízó, a szerep és a hatókör szűrési paramétereinek használatával lehet szűrni.</span><span class="sxs-lookup"><span data-stu-id="e35d2-127">This list can  be filtered using filtering parameters for principal, role and scope.</span></span>
<span data-ttu-id="e35d2-128">A feladat tárgyát meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="e35d2-128">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="e35d2-129">A felhasználók megadásához használja a SignInName vagy az Azure AD ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="e35d2-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="e35d2-130">Ha meg szeretne adni egy biztonsági csoportot, használja az Azure AD ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="e35d2-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="e35d2-131">Az Azure AD-alkalmazások megadásához használja a ServicePrincipalName vagy a ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="e35d2-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="e35d2-132">A hozzárendelt szerepkört a RoleDefinitionName paraméterrel kell megadni.</span><span class="sxs-lookup"><span data-stu-id="e35d2-132">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="e35d2-133">Az Access által megadott hatókört meg lehet adni.</span><span class="sxs-lookup"><span data-stu-id="e35d2-133">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="e35d2-134">Az alapértelmezett érték a kijelölt előfizetéshez tartozik.</span><span class="sxs-lookup"><span data-stu-id="e35d2-134">It defaults to the selected subscription.</span></span> <span data-ttu-id="e35d2-135">A hozzárendelés hatóköre az a következő paraméter-kombinációk egyikével határozható meg.</span><span class="sxs-lookup"><span data-stu-id="e35d2-135">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="e35d2-136">Hatókör – ez a teljes mértékben minősített hatókör a/Subscriptions/subscriptionId kezdődően \< \> .</span><span class="sxs-lookup"><span data-stu-id="e35d2-136">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="e35d2-137">Ez a funkció azokat a feladatokat fogja szűrni, amelyek az adott hatókörben, azaz a hatókörben és a fenti hatókörben érvényesek.</span><span class="sxs-lookup"><span data-stu-id="e35d2-137">This will filter assignments that are effective at that particular scope i.e. all assignments at that scope and above.</span></span>
<span data-ttu-id="e35d2-138">b.</span><span class="sxs-lookup"><span data-stu-id="e35d2-138">b.</span></span>
<span data-ttu-id="e35d2-139">ResourceGroupName – bármely erőforráscsoport neve az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="e35d2-139">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="e35d2-140">Ez a funkció a c meghatározott erőforrás-csoportban érvényes hozzárendeléseket fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="e35d2-140">This will filter assignments effective at the specified resource group c.</span></span>
<span data-ttu-id="e35d2-141">ResourceName, ResourceType, ResourceGroupName és (opcionálisan) ParentResource – az előfizetésben egy adott erőforrást azonosít, és az adott erőforrás-tartományra érvényes hozzárendeléseket fogja szűrni.</span><span class="sxs-lookup"><span data-stu-id="e35d2-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter assignments effective at that resource scope.</span></span>
<span data-ttu-id="e35d2-142">Ha meg szeretné állapítani, hogy egy adott felhasználó Hogyan férhet hozzá az előfizetéshez, használja a ExpandPrincipalGroups kapcsolót.</span><span class="sxs-lookup"><span data-stu-id="e35d2-142">To determine what access a particular user has in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="e35d2-143">Ez felsorolja a felhasználóhoz rendelt összes szerepkört, valamint azokat a csoportokat, amelyeknek a felhasználó a tagja.</span><span class="sxs-lookup"><span data-stu-id="e35d2-143">This will list all roles assigned to the user, and to the groups that the user is member of.</span></span>
<span data-ttu-id="e35d2-144">Az IncludeClassicAdministrators kapcsolóval az előfizetési rendszergazdák és a közös adminisztrátorok is megjeleníthetők.</span><span class="sxs-lookup"><span data-stu-id="e35d2-144">Use the IncludeClassicAdministrators switch to also display the subscription admins and co-admins.</span></span>

## <span data-ttu-id="e35d2-145">Példák</span><span class="sxs-lookup"><span data-stu-id="e35d2-145">EXAMPLES</span></span>

### <span data-ttu-id="e35d2-146">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e35d2-146">Example 1</span></span>
```
PS C:\> Get-AzRoleAssignment
```

<span data-ttu-id="e35d2-147">Az előfizetésben szereplő összes szerepkör-hozzárendelés listázása</span><span class="sxs-lookup"><span data-stu-id="e35d2-147">List all role assignments in the subscription</span></span>

### <span data-ttu-id="e35d2-148">2. példa</span><span class="sxs-lookup"><span data-stu-id="e35d2-148">Example 2</span></span>
```
PS C:\> Get-AzRoleAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com
```

<span data-ttu-id="e35d2-149">A felhasználó minden szerepkör-hozzárendelését john.doe@contoso.com , illetve a tagokat a testRG-vagy a fentieken keresztül kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e35d2-149">Gets all role assignments made to user john.doe@contoso.com, and the groups of which he is member, at the testRG scope or above.</span></span>

### <span data-ttu-id="e35d2-150">3. példa</span><span class="sxs-lookup"><span data-stu-id="e35d2-150">Example 3</span></span>
```
PS C:\> Get-AzRoleAssignment -ServicePrincipalName "http://testapp1.com"
```

<span data-ttu-id="e35d2-151">A megadott szolgáltatási megbízó minden szerepkör-hozzárendelésének beolvasása</span><span class="sxs-lookup"><span data-stu-id="e35d2-151">Gets all role assignments of the specified service principal</span></span>

### <span data-ttu-id="e35d2-152">4. példa</span><span class="sxs-lookup"><span data-stu-id="e35d2-152">Example 4</span></span>
```
PS C:\> Get-AzRoleAssignment -Scope "/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="e35d2-153">Szerepkör-hozzárendeléseket kap a "hely1" webhely hatókörében.</span><span class="sxs-lookup"><span data-stu-id="e35d2-153">Gets role assignments at the 'site1' website scope.</span></span>

## <span data-ttu-id="e35d2-154">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e35d2-154">PARAMETERS</span></span>

### <span data-ttu-id="e35d2-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e35d2-155">-DefaultProfile</span></span>
<span data-ttu-id="e35d2-156">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e35d2-156">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e35d2-157">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="e35d2-157">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="e35d2-158">Ha meg van adva, azokat a szerepköröket adja eredményül, amelyek közvetlenül a felhasználóhoz lettek rendelve (tranzitívan).</span><span class="sxs-lookup"><span data-stu-id="e35d2-158">If specified, returns roles directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="e35d2-159">Csak a felhasználói résztvevők számára támogatott.</span><span class="sxs-lookup"><span data-stu-id="e35d2-159">Supported only for a user principal.</span></span>

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

### <span data-ttu-id="e35d2-160">-IncludeClassicAdministrators</span><span class="sxs-lookup"><span data-stu-id="e35d2-160">-IncludeClassicAdministrators</span></span>
<span data-ttu-id="e35d2-161">Ha meg van adva, az előfizetés klasszikus rendszergazdáknak (rendszergazdáknak, szolgáltatás-rendszergazdáknak stb.) szerepkör-hozzárendeléseit is megjeleníti.</span><span class="sxs-lookup"><span data-stu-id="e35d2-161">If specified, also lists subscription classic administrators (co-admins, service admins, etc.) role assignments.</span></span>

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

### <span data-ttu-id="e35d2-162">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e35d2-162">-ObjectId</span></span>
<span data-ttu-id="e35d2-163">Az Azure AD ObjectId a felhasználó, a csoport vagy a szolgáltatás megbízójának</span><span class="sxs-lookup"><span data-stu-id="e35d2-163">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="e35d2-164">A megadott tőkeösszeg összes hozzárendelésének szűrése.</span><span class="sxs-lookup"><span data-stu-id="e35d2-164">Filters all assignments that are made to the specified principal.</span></span>

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

### <span data-ttu-id="e35d2-165">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="e35d2-165">-ParentResource</span></span>
<span data-ttu-id="e35d2-166">A szülő erőforrás az erőforrás hierarchiájában a ResourceName paraméterrel megadva.</span><span class="sxs-lookup"><span data-stu-id="e35d2-166">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="e35d2-167">A ResourceGroupName, az ResourceType és a ResourceName paraméterekkel együtt kell használni.</span><span class="sxs-lookup"><span data-stu-id="e35d2-167">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

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

### <span data-ttu-id="e35d2-168">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e35d2-168">-ResourceGroupName</span></span>
<span data-ttu-id="e35d2-169">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e35d2-169">The resource group name.</span></span>
<span data-ttu-id="e35d2-170">Felsorolja azokat a szerepkör-hozzárendeléseket, amelyek a megadott erőforráscsoport hatékonyságát jelentik.</span><span class="sxs-lookup"><span data-stu-id="e35d2-170">Lists role assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="e35d2-171">Ha a ResourceName, az ResourceType és a ParentResource paraméterekkel együtt használja, a parancs felsorolja az erőforrás csoport erőforrásain érvényes hozzárendeléseket.</span><span class="sxs-lookup"><span data-stu-id="e35d2-171">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists assignments effective at resources within the resource group.</span></span>

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

### <span data-ttu-id="e35d2-172">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e35d2-172">-ResourceName</span></span>
<span data-ttu-id="e35d2-173">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e35d2-173">The resource name.</span></span>
<span data-ttu-id="e35d2-174">Például storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="e35d2-174">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="e35d2-175">A ResourceGroupName, ResourceType és (opcionálisan) ParentResource paraméterekkel együtt kell használni.</span><span class="sxs-lookup"><span data-stu-id="e35d2-175">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="e35d2-176">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="e35d2-176">-ResourceType</span></span>
<span data-ttu-id="e35d2-177">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="e35d2-177">The resource type.</span></span>
<span data-ttu-id="e35d2-178">Például Microsoft. hálózat/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="e35d2-178">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="e35d2-179">A ResourceGroupName, ResourceName és (opcionálisan) ParentResource paraméterekkel együtt kell használni.</span><span class="sxs-lookup"><span data-stu-id="e35d2-179">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="e35d2-180">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="e35d2-180">-RoleDefinitionId</span></span>
<span data-ttu-id="e35d2-181">A megbízóhoz rendelt szerepkör azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e35d2-181">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="e35d2-182">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="e35d2-182">-RoleDefinitionName</span></span>
<span data-ttu-id="e35d2-183">A megbízóhoz (például olvasóhoz, Közreműködőhöz, virtuális hálózati adminisztrátorhoz stb.) rendelt szerepkör</span><span class="sxs-lookup"><span data-stu-id="e35d2-183">Role that is assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

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

### <span data-ttu-id="e35d2-184">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="e35d2-184">-Scope</span></span>
<span data-ttu-id="e35d2-185">A szerepkör-hozzárendelés hatóköre.</span><span class="sxs-lookup"><span data-stu-id="e35d2-185">The Scope of the role assignment.</span></span>
<span data-ttu-id="e35d2-186">A relatív URI formátuma.</span><span class="sxs-lookup"><span data-stu-id="e35d2-186">In the format of relative URI.</span></span>
<span data-ttu-id="e35d2-187">Például/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="e35d2-187">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="e35d2-188">A "/Subscriptions/{id}" szöveggel kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="e35d2-188">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="e35d2-189">A parancs az összes olyan feladatot szűri, amely az adott hatókörben érvényes.</span><span class="sxs-lookup"><span data-stu-id="e35d2-189">The command filters all assignments that are effective at that scope.</span></span>

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

### <span data-ttu-id="e35d2-190">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="e35d2-190">-ServicePrincipalName</span></span>
<span data-ttu-id="e35d2-191">A ServicePrincipalName.</span><span class="sxs-lookup"><span data-stu-id="e35d2-191">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="e35d2-192">A megadott Azure AD-alkalmazás összes hozzárendelésének szűrése.</span><span class="sxs-lookup"><span data-stu-id="e35d2-192">Filters all assignments that are made to the specified Azure AD application.</span></span>

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

### <span data-ttu-id="e35d2-193">-SignInName</span><span class="sxs-lookup"><span data-stu-id="e35d2-193">-SignInName</span></span>
<span data-ttu-id="e35d2-194">Az e-mail-cím vagy a felhasználó egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="e35d2-194">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="e35d2-195">A megadott felhasználó összes hozzárendelésének szűrése.</span><span class="sxs-lookup"><span data-stu-id="e35d2-195">Filters all assignments that are made to the specified user.</span></span>

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

### <span data-ttu-id="e35d2-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e35d2-196">CommonParameters</span></span>
<span data-ttu-id="e35d2-197">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e35d2-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e35d2-198">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e35d2-198">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e35d2-199">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e35d2-199">INPUTS</span></span>

### <span data-ttu-id="e35d2-200">System. String</span><span class="sxs-lookup"><span data-stu-id="e35d2-200">System.String</span></span>

### <span data-ttu-id="e35d2-201">System. GUID</span><span class="sxs-lookup"><span data-stu-id="e35d2-201">System.Guid</span></span>

## <span data-ttu-id="e35d2-202">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e35d2-202">OUTPUTS</span></span>

### <span data-ttu-id="e35d2-203">Microsoft. Azure. Command. Resources. modellek. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e35d2-203">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="e35d2-204">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e35d2-204">NOTES</span></span>
<span data-ttu-id="e35d2-205">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="e35d2-205">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="e35d2-206">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e35d2-206">RELATED LINKS</span></span>

[<span data-ttu-id="e35d2-207">Új – AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e35d2-207">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="e35d2-208">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e35d2-208">Remove-AzRoleAssignment</span></span>](./Remove-AzRoleAssignment.md)

[<span data-ttu-id="e35d2-209">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e35d2-209">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

