---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 488229AF-FD6D-4E1B-B3DA-E57CA781D91E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleAssignment.md
ms.openlocfilehash: 5cbf4f46d102188ff1db3becf66d3edffe426fae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500747"
---
# <span data-ttu-id="3c31a-101">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="3c31a-101">Get-AzureRmRoleAssignment</span></span>

## <span data-ttu-id="3c31a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3c31a-102">SYNOPSIS</span></span>
<span data-ttu-id="3c31a-103">Az Azure RBAC szerepkör-hozzárendeléseinek listája a megadott hatókörben.</span><span class="sxs-lookup"><span data-stu-id="3c31a-103">Lists Azure RBAC role assignments at the specified scope.</span></span>
<span data-ttu-id="3c31a-104">Alapértelmezés szerint a kijelölt Azure-előfizetésben lévő összes szerepkör-hozzárendelést felsorolja.</span><span class="sxs-lookup"><span data-stu-id="3c31a-104">By default it lists all role assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="3c31a-105">A megfelelő paraméterekkel felsorolhatja a hozzárendeléseket egy adott felhasználóhoz, illetve felsorolhatja egy adott erőforráscsoport vagy erőforrás hozzárendeléseit.</span><span class="sxs-lookup"><span data-stu-id="3c31a-105">Use respective parameters to list assignments to a specific user, or to list assignments on a specific resource group or resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c31a-106">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3c31a-106">SYNTAX</span></span>

### <span data-ttu-id="3c31a-107">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3c31a-107">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmRoleAssignment [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c31a-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c31a-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ObjectId <Guid> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c31a-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c31a-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c31a-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c31a-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c31a-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c31a-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ObjectId <Guid> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c31a-112">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c31a-112">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment [-ObjectId <Guid>] -RoleDefinitionId <Guid> [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c31a-113">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c31a-113">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c31a-114">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c31a-114">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c31a-115">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c31a-115">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzureRmRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c31a-116">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c31a-116">SignInNameParameterSet</span></span>
```
Get-AzureRmRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c31a-117">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c31a-117">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 [-RoleDefinitionName <String>] [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3c31a-118">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c31a-118">ResourceWithSPNParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c31a-119">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c31a-119">ScopeWithSPNParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c31a-120">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c31a-120">SPNParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c31a-121">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c31a-121">ResourceGroupParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c31a-122">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c31a-122">ResourceParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c31a-123">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c31a-123">ScopeParameterSet</span></span>
```
Get-AzureRmRoleAssignment [-RoleDefinitionName <String>] -Scope <String> [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c31a-124">Leírás</span><span class="sxs-lookup"><span data-stu-id="3c31a-124">DESCRIPTION</span></span>
<span data-ttu-id="3c31a-125">A Get-AzureRMRoleAssignment parancs segítségével listázhatja az összes olyan szerepkör-hozzárendelést, amely egy hatókörre érvényes.</span><span class="sxs-lookup"><span data-stu-id="3c31a-125">Use the Get-AzureRMRoleAssignment command to list all role assignments that are effective on a scope.</span></span>

<span data-ttu-id="3c31a-126">Paraméterek nélkül a parancs az előfizetésben szereplő összes szerepkör-hozzárendelést visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="3c31a-126">Without any parameters, this command returns all the role assignments made under the subscription.</span></span>
<span data-ttu-id="3c31a-127">Ezt a listát a megbízó, a szerep és a hatókör szűrési paramétereinek használatával lehet szűrni.</span><span class="sxs-lookup"><span data-stu-id="3c31a-127">This list can  be filtered using filtering parameters for principal, role and scope.</span></span>

<span data-ttu-id="3c31a-128">A feladat tárgyát meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="3c31a-128">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="3c31a-129">A felhasználók megadásához használja a SignInName vagy az Azure AD ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="3c31a-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="3c31a-130">Ha meg szeretne adni egy biztonsági csoportot, használja az Azure AD ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="3c31a-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="3c31a-131">Az Azure AD-alkalmazások megadásához használja a ServicePrincipalName vagy a ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="3c31a-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>

<span data-ttu-id="3c31a-132">A hozzárendelt szerepkört a RoleDefinitionName paraméterrel kell megadni.</span><span class="sxs-lookup"><span data-stu-id="3c31a-132">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>

<span data-ttu-id="3c31a-133">Az Access által megadott hatókört meg lehet adni.</span><span class="sxs-lookup"><span data-stu-id="3c31a-133">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="3c31a-134">Az alapértelmezett érték a kijelölt előfizetéshez tartozik.</span><span class="sxs-lookup"><span data-stu-id="3c31a-134">It defaults to the selected subscription.</span></span> <span data-ttu-id="3c31a-135">A hozzárendelés hatóköre az a következő paraméter-kombinációk egyikével határozható meg.</span><span class="sxs-lookup"><span data-stu-id="3c31a-135">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="3c31a-136">Hatókör – ez a teljes mértékben minősített hatókör a/Subscriptions/kezdve \<subscriptionId\> .</span><span class="sxs-lookup"><span data-stu-id="3c31a-136">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="3c31a-137">Ez a funkció azokat a feladatokat fogja szűrni, amelyek az adott hatókörben, azaz a hatókörben és a fenti hatókörben érvényesek.</span><span class="sxs-lookup"><span data-stu-id="3c31a-137">This will filter assignments that are effective at that particular scope i.e. all assignments at that scope and above.</span></span>
<span data-ttu-id="3c31a-138">b.</span><span class="sxs-lookup"><span data-stu-id="3c31a-138">b.</span></span>
<span data-ttu-id="3c31a-139">ResourceGroupName – bármely erőforráscsoport neve az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="3c31a-139">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="3c31a-140">Ez a funkció a c meghatározott erőforrás-csoportban érvényes hozzárendeléseket fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="3c31a-140">This will filter assignments effective at the specified resource group c.</span></span>
<span data-ttu-id="3c31a-141">ResourceName, ResourceType, ResourceGroupName és (opcionálisan) ParentResource – az előfizetésben egy adott erőforrást azonosít, és az adott erőforrás-tartományra érvényes hozzárendeléseket fogja szűrni.</span><span class="sxs-lookup"><span data-stu-id="3c31a-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter assignments effective at that resource scope.</span></span>

<span data-ttu-id="3c31a-142">Ha meg szeretné állapítani, hogy egy adott felhasználó Hogyan férhet hozzá az előfizetéshez, használja a ExpandPrincipalGroups kapcsolót.</span><span class="sxs-lookup"><span data-stu-id="3c31a-142">To determine what access a particular user has in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="3c31a-143">Ez felsorolja a felhasználóhoz rendelt összes szerepkört, valamint azokat a csoportokat, amelyeknek a felhasználó a tagja.</span><span class="sxs-lookup"><span data-stu-id="3c31a-143">This will list all roles assigned to the user, and to the groups that the user is member of.</span></span>

<span data-ttu-id="3c31a-144">Az IncludeClassicAdministrators kapcsolóval az előfizetési rendszergazdák és a közös adminisztrátorok is megjeleníthetők.</span><span class="sxs-lookup"><span data-stu-id="3c31a-144">Use the IncludeClassicAdministrators switch to also display the subscription admins and co-admins.</span></span>

## <span data-ttu-id="3c31a-145">Példák</span><span class="sxs-lookup"><span data-stu-id="3c31a-145">EXAMPLES</span></span>

### <span data-ttu-id="3c31a-146">--------------------------Példa 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3c31a-146">--------------------------  Example 1  --------------------------</span></span>
```
PS C:\> Get-AzureRmRoleAssignment
```

<span data-ttu-id="3c31a-147">Az előfizetésben szereplő összes szerepkör-hozzárendelés listázása</span><span class="sxs-lookup"><span data-stu-id="3c31a-147">List all role assignments in the subscription</span></span>

### <span data-ttu-id="3c31a-148">--------------------------Példa 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="3c31a-148">--------------------------  Example 2  --------------------------</span></span>
```
PS C:\> Get-AzureRmRoleAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com -ExpandPrincipalGroups
```

<span data-ttu-id="3c31a-149">A felhasználó minden szerepkör-hozzárendelését john.doe@contoso.com , illetve a tagokat a testRG-vagy a fentieken keresztül kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3c31a-149">Gets all role assignments made to user john.doe@contoso.com, and the groups of which he is member, at the testRG scope or above.</span></span>

### <span data-ttu-id="3c31a-150">Példa--------------------------3--------------------------</span><span class="sxs-lookup"><span data-stu-id="3c31a-150">--------------------------  Example 3  --------------------------</span></span>
```
PS C:\> Get-AzureRmRoleAssignment -ServicePrincipalName "http://testapp1.com"
```

<span data-ttu-id="3c31a-151">A megadott szolgáltatási megbízó minden szerepkör-hozzárendelésének beolvasása</span><span class="sxs-lookup"><span data-stu-id="3c31a-151">Gets all role assignments of the specified service principal</span></span>

### <span data-ttu-id="3c31a-152">--------------------------Példa 4--------------------------</span><span class="sxs-lookup"><span data-stu-id="3c31a-152">--------------------------  Example 4  --------------------------</span></span>
```
PS C:\> Get-AzureRmRoleAssignment -Scope "/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="3c31a-153">Szerepkör-hozzárendeléseket kap a "hely1" webhely hatókörében.</span><span class="sxs-lookup"><span data-stu-id="3c31a-153">Gets role assignments at the 'site1' website scope.</span></span>

## <span data-ttu-id="3c31a-154">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3c31a-154">PARAMETERS</span></span>

### <span data-ttu-id="3c31a-155">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="3c31a-155">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="3c31a-156">Ha meg van adva, azokat a szerepköröket adja eredményül, amelyek közvetlenül a felhasználóhoz lettek rendelve (tranzitívan).</span><span class="sxs-lookup"><span data-stu-id="3c31a-156">If specified, returns roles directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="3c31a-157">Csak a felhasználói résztvevők számára támogatott.</span><span class="sxs-lookup"><span data-stu-id="3c31a-157">Supported only for a user principal.</span></span>

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

### <span data-ttu-id="3c31a-158">-IncludeClassicAdministrators</span><span class="sxs-lookup"><span data-stu-id="3c31a-158">-IncludeClassicAdministrators</span></span>
<span data-ttu-id="3c31a-159">Ha meg van adva, az előfizetés klasszikus rendszergazdáknak (rendszergazdáknak, szolgáltatás-rendszergazdáknak stb.) szerepkör-hozzárendeléseit is megjeleníti.</span><span class="sxs-lookup"><span data-stu-id="3c31a-159">If specified, also lists subscription classic administrators (co-admins, service admins, etc.) role assignments.</span></span>

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

### <span data-ttu-id="3c31a-160">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="3c31a-160">-ObjectId</span></span>
<span data-ttu-id="3c31a-161">Az Azure AD ObjectId a felhasználó, a csoport vagy a szolgáltatás megbízójának</span><span class="sxs-lookup"><span data-stu-id="3c31a-161">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="3c31a-162">A megadott tőkeösszeg összes hozzárendelésének szűrése.</span><span class="sxs-lookup"><span data-stu-id="3c31a-162">Filters all assignments that are made to the specified principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c31a-163">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="3c31a-163">-ParentResource</span></span>
<span data-ttu-id="3c31a-164">A szülő erőforrás az erőforrás hierarchiájában a ResourceName paraméterrel megadva.</span><span class="sxs-lookup"><span data-stu-id="3c31a-164">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="3c31a-165">A ResourceGroupName, az ResourceType és a ResourceName paraméterekkel együtt kell használni.</span><span class="sxs-lookup"><span data-stu-id="3c31a-165">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

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

### <span data-ttu-id="3c31a-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c31a-166">-ResourceGroupName</span></span>
<span data-ttu-id="3c31a-167">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="3c31a-167">The resource group name.</span></span>
<span data-ttu-id="3c31a-168">Felsorolja azokat a szerepkör-hozzárendeléseket, amelyek a megadott erőforráscsoport hatékonyságát jelentik.</span><span class="sxs-lookup"><span data-stu-id="3c31a-168">Lists role assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="3c31a-169">Ha a ResourceName, az ResourceType és a ParentResource paraméterekkel együtt használja, a parancs felsorolja az erőforrás csoport erőforrásain érvényes hozzárendeléseket.</span><span class="sxs-lookup"><span data-stu-id="3c31a-169">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists assignments effective at resources within the resource group.</span></span>

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

### <span data-ttu-id="3c31a-170">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="3c31a-170">-ResourceName</span></span>
<span data-ttu-id="3c31a-171">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="3c31a-171">The resource name.</span></span>
<span data-ttu-id="3c31a-172">Például storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="3c31a-172">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="3c31a-173">A ResourceGroupName, ResourceType és (opcionálisan) ParentResource paraméterekkel együtt kell használni.</span><span class="sxs-lookup"><span data-stu-id="3c31a-173">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="3c31a-174">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="3c31a-174">-ResourceType</span></span>
<span data-ttu-id="3c31a-175">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="3c31a-175">The resource type.</span></span>
<span data-ttu-id="3c31a-176">Például Microsoft. hálózat/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="3c31a-176">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="3c31a-177">A ResourceGroupName, ResourceName és (opcionálisan) ParentResource paraméterekkel együtt kell használni.</span><span class="sxs-lookup"><span data-stu-id="3c31a-177">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="3c31a-178">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="3c31a-178">-RoleDefinitionId</span></span>
<span data-ttu-id="3c31a-179">A megbízóhoz rendelt szerepkör azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3c31a-179">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="3c31a-180">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="3c31a-180">-RoleDefinitionName</span></span>
<span data-ttu-id="3c31a-181">A megbízóhoz (például olvasóhoz, Közreműködőhöz, virtuális hálózati adminisztrátorhoz stb.) rendelt szerepkör</span><span class="sxs-lookup"><span data-stu-id="3c31a-181">Role that is assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

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

### <span data-ttu-id="3c31a-182">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="3c31a-182">-Scope</span></span>
<span data-ttu-id="3c31a-183">A szerepkör-hozzárendelés hatóköre.</span><span class="sxs-lookup"><span data-stu-id="3c31a-183">The Scope of the role assignment.</span></span>
<span data-ttu-id="3c31a-184">A relatív URI formátuma.</span><span class="sxs-lookup"><span data-stu-id="3c31a-184">In the format of relative URI.</span></span>
<span data-ttu-id="3c31a-185">Például/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="3c31a-185">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="3c31a-186">A "/Subscriptions/{id}" szöveggel kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="3c31a-186">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="3c31a-187">A parancs az összes olyan feladatot szűri, amely az adott hatókörben érvényes.</span><span class="sxs-lookup"><span data-stu-id="3c31a-187">The command filters all assignments that are effective at that scope.</span></span>

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

### <span data-ttu-id="3c31a-188">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="3c31a-188">-ServicePrincipalName</span></span>
<span data-ttu-id="3c31a-189">A ServicePrincipalName.</span><span class="sxs-lookup"><span data-stu-id="3c31a-189">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="3c31a-190">A megadott Azure AD-alkalmazás összes hozzárendelésének szűrése.</span><span class="sxs-lookup"><span data-stu-id="3c31a-190">Filters all assignments that are made to the specified Azure AD application.</span></span>

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

### <span data-ttu-id="3c31a-191">-SignInName</span><span class="sxs-lookup"><span data-stu-id="3c31a-191">-SignInName</span></span>
<span data-ttu-id="3c31a-192">Az e-mail-cím vagy a felhasználó egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="3c31a-192">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="3c31a-193">A megadott felhasználó összes hozzárendelésének szűrése.</span><span class="sxs-lookup"><span data-stu-id="3c31a-193">Filters all assignments that are made to the specified user.</span></span>

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

### <span data-ttu-id="3c31a-194">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c31a-194">-DefaultProfile</span></span>
<span data-ttu-id="3c31a-195">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3c31a-195">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c31a-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c31a-196">CommonParameters</span></span>
<span data-ttu-id="3c31a-197">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3c31a-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c31a-198">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c31a-198">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c31a-199">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c31a-199">INPUTS</span></span>

## <span data-ttu-id="3c31a-200">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c31a-200">OUTPUTS</span></span>

### <span data-ttu-id="3c31a-201">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. Resources. PSRoleAssignment]</span><span class="sxs-lookup"><span data-stu-id="3c31a-201">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment]</span></span>

## <span data-ttu-id="3c31a-202">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3c31a-202">NOTES</span></span>
<span data-ttu-id="3c31a-203">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="3c31a-203">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="3c31a-204">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c31a-204">RELATED LINKS</span></span>

[<span data-ttu-id="3c31a-205">Új – AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="3c31a-205">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="3c31a-206">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="3c31a-206">Remove-AzureRmRoleAssignment</span></span>](./Remove-AzureRmRoleAssignment.md)

[<span data-ttu-id="3c31a-207">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3c31a-207">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

