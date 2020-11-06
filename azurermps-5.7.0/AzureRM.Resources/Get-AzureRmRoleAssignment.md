---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 488229AF-FD6D-4E1B-B3DA-E57CA781D91E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleAssignment.md
ms.openlocfilehash: c6dd17917624d8b2b914ac94c8310358fac03b68
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501408"
---
# <span data-ttu-id="3bc90-101">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="3bc90-101">Get-AzureRmRoleAssignment</span></span>

## <span data-ttu-id="3bc90-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3bc90-102">SYNOPSIS</span></span>
<span data-ttu-id="3bc90-103">Az Azure RBAC szerepkör-hozzárendeléseinek listája a megadott hatókörben.</span><span class="sxs-lookup"><span data-stu-id="3bc90-103">Lists Azure RBAC role assignments at the specified scope.</span></span>
<span data-ttu-id="3bc90-104">Alapértelmezés szerint a kijelölt Azure-előfizetésben lévő összes szerepkör-hozzárendelést felsorolja.</span><span class="sxs-lookup"><span data-stu-id="3bc90-104">By default it lists all role assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="3bc90-105">A megfelelő paraméterekkel felsorolhatja a hozzárendeléseket egy adott felhasználóhoz, illetve felsorolhatja egy adott erőforráscsoport vagy erőforrás hozzárendeléseit.</span><span class="sxs-lookup"><span data-stu-id="3bc90-105">Use respective parameters to list assignments to a specific user, or to list assignments on a specific resource group or resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3bc90-106">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3bc90-106">SYNTAX</span></span>

### <span data-ttu-id="3bc90-107">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3bc90-107">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmRoleAssignment [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bc90-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bc90-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ObjectId <Guid> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bc90-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bc90-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bc90-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bc90-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bc90-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bc90-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ObjectId <Guid> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bc90-112">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bc90-112">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment [-ObjectId <Guid>] -RoleDefinitionId <Guid> [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bc90-113">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bc90-113">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bc90-114">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bc90-114">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bc90-115">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bc90-115">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzureRmRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bc90-116">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bc90-116">SignInNameParameterSet</span></span>
```
Get-AzureRmRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bc90-117">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bc90-117">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 [-RoleDefinitionName <String>] [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3bc90-118">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bc90-118">ResourceWithSPNParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bc90-119">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bc90-119">ScopeWithSPNParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bc90-120">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bc90-120">SPNParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bc90-121">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bc90-121">ResourceGroupParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bc90-122">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bc90-122">ResourceParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bc90-123">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bc90-123">ScopeParameterSet</span></span>
```
Get-AzureRmRoleAssignment [-RoleDefinitionName <String>] -Scope <String> [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3bc90-124">Leírás</span><span class="sxs-lookup"><span data-stu-id="3bc90-124">DESCRIPTION</span></span>
<span data-ttu-id="3bc90-125">A Get-AzureRMRoleAssignment parancs segítségével listázhatja az összes olyan szerepkör-hozzárendelést, amely egy hatókörre érvényes.</span><span class="sxs-lookup"><span data-stu-id="3bc90-125">Use the Get-AzureRMRoleAssignment command to list all role assignments that are effective on a scope.</span></span>

<span data-ttu-id="3bc90-126">Paraméterek nélkül a parancs az előfizetésben szereplő összes szerepkör-hozzárendelést visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="3bc90-126">Without any parameters, this command returns all the role assignments made under the subscription.</span></span>
<span data-ttu-id="3bc90-127">Ezt a listát a megbízó, a szerep és a hatókör szűrési paramétereinek használatával lehet szűrni.</span><span class="sxs-lookup"><span data-stu-id="3bc90-127">This list can  be filtered using filtering parameters for principal, role and scope.</span></span>

<span data-ttu-id="3bc90-128">A feladat tárgyát meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="3bc90-128">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="3bc90-129">A felhasználók megadásához használja a SignInName vagy az Azure AD ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="3bc90-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="3bc90-130">Ha meg szeretne adni egy biztonsági csoportot, használja az Azure AD ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="3bc90-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="3bc90-131">Az Azure AD-alkalmazások megadásához használja a ServicePrincipalName vagy a ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="3bc90-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>

<span data-ttu-id="3bc90-132">A hozzárendelt szerepkört a RoleDefinitionName paraméterrel kell megadni.</span><span class="sxs-lookup"><span data-stu-id="3bc90-132">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>

<span data-ttu-id="3bc90-133">Az Access által megadott hatókört meg lehet adni.</span><span class="sxs-lookup"><span data-stu-id="3bc90-133">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="3bc90-134">Az alapértelmezett érték a kijelölt előfizetéshez tartozik.</span><span class="sxs-lookup"><span data-stu-id="3bc90-134">It defaults to the selected subscription.</span></span> <span data-ttu-id="3bc90-135">A hozzárendelés hatóköre az a következő paraméter-kombinációk egyikével határozható meg.</span><span class="sxs-lookup"><span data-stu-id="3bc90-135">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="3bc90-136">Hatókör – ez a teljes mértékben minősített hatókör a/Subscriptions/kezdve \<subscriptionId\> .</span><span class="sxs-lookup"><span data-stu-id="3bc90-136">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="3bc90-137">Ez a funkció azokat a feladatokat fogja szűrni, amelyek az adott hatókörben, azaz a hatókörben és a fenti hatókörben érvényesek.</span><span class="sxs-lookup"><span data-stu-id="3bc90-137">This will filter assignments that are effective at that particular scope i.e. all assignments at that scope and above.</span></span>
<span data-ttu-id="3bc90-138">b.</span><span class="sxs-lookup"><span data-stu-id="3bc90-138">b.</span></span>
<span data-ttu-id="3bc90-139">ResourceGroupName – bármely erőforráscsoport neve az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="3bc90-139">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="3bc90-140">Ez a funkció a c meghatározott erőforrás-csoportban érvényes hozzárendeléseket fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="3bc90-140">This will filter assignments effective at the specified resource group c.</span></span>
<span data-ttu-id="3bc90-141">ResourceName, ResourceType, ResourceGroupName és (opcionálisan) ParentResource – az előfizetésben egy adott erőforrást azonosít, és az adott erőforrás-tartományra érvényes hozzárendeléseket fogja szűrni.</span><span class="sxs-lookup"><span data-stu-id="3bc90-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter assignments effective at that resource scope.</span></span>

<span data-ttu-id="3bc90-142">Ha meg szeretné állapítani, hogy egy adott felhasználó Hogyan férhet hozzá az előfizetéshez, használja a ExpandPrincipalGroups kapcsolót.</span><span class="sxs-lookup"><span data-stu-id="3bc90-142">To determine what access a particular user has in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="3bc90-143">Ez felsorolja a felhasználóhoz rendelt összes szerepkört, valamint azokat a csoportokat, amelyeknek a felhasználó a tagja.</span><span class="sxs-lookup"><span data-stu-id="3bc90-143">This will list all roles assigned to the user, and to the groups that the user is member of.</span></span>

<span data-ttu-id="3bc90-144">Az IncludeClassicAdministrators kapcsolóval az előfizetési rendszergazdák és a közös adminisztrátorok is megjeleníthetők.</span><span class="sxs-lookup"><span data-stu-id="3bc90-144">Use the IncludeClassicAdministrators switch to also display the subscription admins and co-admins.</span></span>

## <span data-ttu-id="3bc90-145">Példák</span><span class="sxs-lookup"><span data-stu-id="3bc90-145">EXAMPLES</span></span>

### <span data-ttu-id="3bc90-146">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3bc90-146">Example 1</span></span>
```
PS C:\> Get-AzureRmRoleAssignment
```

<span data-ttu-id="3bc90-147">Az előfizetésben szereplő összes szerepkör-hozzárendelés listázása</span><span class="sxs-lookup"><span data-stu-id="3bc90-147">List all role assignments in the subscription</span></span>

### <span data-ttu-id="3bc90-148">2. példa</span><span class="sxs-lookup"><span data-stu-id="3bc90-148">Example 2</span></span>
```
PS C:\> Get-AzureRmRoleAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com
```

<span data-ttu-id="3bc90-149">A felhasználó minden szerepkör-hozzárendelését john.doe@contoso.com , illetve a tagokat a testRG-vagy a fentieken keresztül kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3bc90-149">Gets all role assignments made to user john.doe@contoso.com, and the groups of which he is member, at the testRG scope or above.</span></span>

### <span data-ttu-id="3bc90-150">3. példa</span><span class="sxs-lookup"><span data-stu-id="3bc90-150">Example 3</span></span>
```
PS C:\> Get-AzureRmRoleAssignment -ServicePrincipalName "http://testapp1.com"
```

<span data-ttu-id="3bc90-151">A megadott szolgáltatási megbízó minden szerepkör-hozzárendelésének beolvasása</span><span class="sxs-lookup"><span data-stu-id="3bc90-151">Gets all role assignments of the specified service principal</span></span>

### <span data-ttu-id="3bc90-152">4. példa</span><span class="sxs-lookup"><span data-stu-id="3bc90-152">Example 4</span></span>
```
PS C:\> Get-AzureRmRoleAssignment -Scope "/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="3bc90-153">Szerepkör-hozzárendeléseket kap a "hely1" webhely hatókörében.</span><span class="sxs-lookup"><span data-stu-id="3bc90-153">Gets role assignments at the 'site1' website scope.</span></span>

## <span data-ttu-id="3bc90-154">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3bc90-154">PARAMETERS</span></span>

### <span data-ttu-id="3bc90-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bc90-155">-DefaultProfile</span></span>
<span data-ttu-id="3bc90-156">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3bc90-156">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc90-157">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="3bc90-157">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="3bc90-158">Ha meg van adva, azokat a szerepköröket adja eredményül, amelyek közvetlenül a felhasználóhoz lettek rendelve (tranzitívan).</span><span class="sxs-lookup"><span data-stu-id="3bc90-158">If specified, returns roles directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="3bc90-159">Csak a felhasználói résztvevők számára támogatott.</span><span class="sxs-lookup"><span data-stu-id="3bc90-159">Supported only for a user principal.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ObjectIdParameterSet, SignInNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc90-160">-IncludeClassicAdministrators</span><span class="sxs-lookup"><span data-stu-id="3bc90-160">-IncludeClassicAdministrators</span></span>
<span data-ttu-id="3bc90-161">Ha meg van adva, az előfizetés klasszikus rendszergazdáknak (rendszergazdáknak, szolgáltatás-rendszergazdáknak stb.) szerepkör-hozzárendeléseit is megjeleníti.</span><span class="sxs-lookup"><span data-stu-id="3bc90-161">If specified, also lists subscription classic administrators (co-admins, service admins, etc.) role assignments.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EmptyParameterSet, ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet, ScopeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc90-162">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="3bc90-162">-ObjectId</span></span>
<span data-ttu-id="3bc90-163">Az Azure AD ObjectId a felhasználó, a csoport vagy a szolgáltatás megbízójának</span><span class="sxs-lookup"><span data-stu-id="3bc90-163">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="3bc90-164">A megadott tőkeösszeg összes hozzárendelésének szűrése.</span><span class="sxs-lookup"><span data-stu-id="3bc90-164">Filters all assignments that are made to the specified principal.</span></span>

```yaml
Type: Guid
Parameter Sets: ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Guid
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc90-165">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="3bc90-165">-ParentResource</span></span>
<span data-ttu-id="3bc90-166">A szülő erőforrás az erőforrás hierarchiájában a ResourceName paraméterrel megadva.</span><span class="sxs-lookup"><span data-stu-id="3bc90-166">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="3bc90-167">A ResourceGroupName, az ResourceType és a ResourceName paraméterekkel együtt kell használni.</span><span class="sxs-lookup"><span data-stu-id="3bc90-167">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

```yaml
Type: String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc90-168">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bc90-168">-ResourceGroupName</span></span>
<span data-ttu-id="3bc90-169">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="3bc90-169">The resource group name.</span></span>
<span data-ttu-id="3bc90-170">Felsorolja azokat a szerepkör-hozzárendeléseket, amelyek a megadott erőforráscsoport hatékonyságát jelentik.</span><span class="sxs-lookup"><span data-stu-id="3bc90-170">Lists role assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="3bc90-171">Ha a ResourceName, az ResourceType és a ParentResource paraméterekkel együtt használja, a parancs felsorolja az erőforrás csoport erőforrásain érvényes hozzárendeléseket.</span><span class="sxs-lookup"><span data-stu-id="3bc90-171">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists assignments effective at resources within the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc90-172">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="3bc90-172">-ResourceName</span></span>
<span data-ttu-id="3bc90-173">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="3bc90-173">The resource name.</span></span>
<span data-ttu-id="3bc90-174">Például storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="3bc90-174">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="3bc90-175">A ResourceGroupName, ResourceType és (opcionálisan) ParentResource paraméterekkel együtt kell használni.</span><span class="sxs-lookup"><span data-stu-id="3bc90-175">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

```yaml
Type: String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc90-176">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="3bc90-176">-ResourceType</span></span>
<span data-ttu-id="3bc90-177">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="3bc90-177">The resource type.</span></span>
<span data-ttu-id="3bc90-178">Például Microsoft. hálózat/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="3bc90-178">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="3bc90-179">A ResourceGroupName, ResourceName és (opcionálisan) ParentResource paraméterekkel együtt kell használni.</span><span class="sxs-lookup"><span data-stu-id="3bc90-179">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

```yaml
Type: String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc90-180">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="3bc90-180">-RoleDefinitionId</span></span>
<span data-ttu-id="3bc90-181">A megbízóhoz rendelt szerepkör azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3bc90-181">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: Guid
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc90-182">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="3bc90-182">-RoleDefinitionName</span></span>
<span data-ttu-id="3bc90-183">A megbízóhoz (például olvasóhoz, Közreműködőhöz, virtuális hálózati adminisztrátorhoz stb.) rendelt szerepkör</span><span class="sxs-lookup"><span data-stu-id="3bc90-183">Role that is assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: String
Parameter Sets: EmptyParameterSet, ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet, ScopeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc90-184">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="3bc90-184">-Scope</span></span>
<span data-ttu-id="3bc90-185">A szerepkör-hozzárendelés hatóköre.</span><span class="sxs-lookup"><span data-stu-id="3bc90-185">The Scope of the role assignment.</span></span>
<span data-ttu-id="3bc90-186">A relatív URI formátuma.</span><span class="sxs-lookup"><span data-stu-id="3bc90-186">In the format of relative URI.</span></span>
<span data-ttu-id="3bc90-187">Például/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="3bc90-187">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="3bc90-188">A "/Subscriptions/{id}" szöveggel kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="3bc90-188">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="3bc90-189">A parancs az összes olyan feladatot szűri, amely az adott hatókörben érvényes.</span><span class="sxs-lookup"><span data-stu-id="3bc90-189">The command filters all assignments that are effective at that scope.</span></span>

```yaml
Type: String
Parameter Sets: ScopeWithObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet, ScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc90-190">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="3bc90-190">-ServicePrincipalName</span></span>
<span data-ttu-id="3bc90-191">A ServicePrincipalName.</span><span class="sxs-lookup"><span data-stu-id="3bc90-191">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="3bc90-192">A megadott Azure AD-alkalmazás összes hozzárendelésének szűrése.</span><span class="sxs-lookup"><span data-stu-id="3bc90-192">Filters all assignments that are made to the specified Azure AD application.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc90-193">-SignInName</span><span class="sxs-lookup"><span data-stu-id="3bc90-193">-SignInName</span></span>
<span data-ttu-id="3bc90-194">Az e-mail-cím vagy a felhasználó egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="3bc90-194">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="3bc90-195">A megadott felhasználó összes hozzárendelésének szűrése.</span><span class="sxs-lookup"><span data-stu-id="3bc90-195">Filters all assignments that are made to the specified user.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc90-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bc90-196">CommonParameters</span></span>
<span data-ttu-id="3bc90-197">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3bc90-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bc90-198">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bc90-198">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bc90-199">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3bc90-199">INPUTS</span></span>

### <span data-ttu-id="3bc90-200">Nincs</span><span class="sxs-lookup"><span data-stu-id="3bc90-200">None</span></span>
<span data-ttu-id="3bc90-201">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="3bc90-201">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3bc90-202">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3bc90-202">OUTPUTS</span></span>

### <span data-ttu-id="3bc90-203">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. Resources. PSRoleAssignment]</span><span class="sxs-lookup"><span data-stu-id="3bc90-203">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment]</span></span>

## <span data-ttu-id="3bc90-204">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3bc90-204">NOTES</span></span>
<span data-ttu-id="3bc90-205">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="3bc90-205">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="3bc90-206">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3bc90-206">RELATED LINKS</span></span>

[<span data-ttu-id="3bc90-207">Új – AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="3bc90-207">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="3bc90-208">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="3bc90-208">Remove-AzureRmRoleAssignment</span></span>](./Remove-AzureRmRoleAssignment.md)

[<span data-ttu-id="3bc90-209">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3bc90-209">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

