---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 488229AF-FD6D-4E1B-B3DA-E57CA781D91E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermroleassignment
schema: 2.0.0
ms.openlocfilehash: d2a0822febe38f5ac4e6ac435be180b81e799e14
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848382"
---
# <span data-ttu-id="94974-101">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="94974-101">Get-AzureRmRoleAssignment</span></span>

## <span data-ttu-id="94974-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="94974-102">SYNOPSIS</span></span>
<span data-ttu-id="94974-103">Az Azure RBAC szerepkör-hozzárendeléseinek listája a megadott hatókörben.</span><span class="sxs-lookup"><span data-stu-id="94974-103">Lists Azure RBAC role assignments at the specified scope.</span></span>
<span data-ttu-id="94974-104">Alapértelmezés szerint a kijelölt Azure-előfizetésben lévő összes szerepkör-hozzárendelést felsorolja.</span><span class="sxs-lookup"><span data-stu-id="94974-104">By default it lists all role assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="94974-105">A megfelelő paraméterekkel felsorolhatja a hozzárendeléseket egy adott felhasználóhoz, illetve felsorolhatja egy adott erőforráscsoport vagy erőforrás hozzárendeléseit.</span><span class="sxs-lookup"><span data-stu-id="94974-105">Use respective parameters to list assignments to a specific user, or to list assignments on a specific resource group or resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94974-106">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="94974-106">SYNTAX</span></span>

### <span data-ttu-id="94974-107">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="94974-107">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmRoleAssignment [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94974-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94974-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ObjectId <Guid> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94974-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94974-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94974-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94974-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94974-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94974-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ObjectId <Guid> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94974-112">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94974-112">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment [-ObjectId <Guid>] -RoleDefinitionId <Guid> [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94974-113">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="94974-113">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94974-114">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="94974-114">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94974-115">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="94974-115">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzureRmRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94974-116">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="94974-116">SignInNameParameterSet</span></span>
```
Get-AzureRmRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94974-117">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="94974-117">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 [-RoleDefinitionName <String>] [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="94974-118">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="94974-118">ResourceWithSPNParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94974-119">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="94974-119">ScopeWithSPNParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94974-120">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="94974-120">SPNParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94974-121">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="94974-121">ResourceGroupParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94974-122">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="94974-122">ResourceParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94974-123">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="94974-123">ScopeParameterSet</span></span>
```
Get-AzureRmRoleAssignment [-RoleDefinitionName <String>] -Scope <String> [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94974-124">Leírás</span><span class="sxs-lookup"><span data-stu-id="94974-124">DESCRIPTION</span></span>
<span data-ttu-id="94974-125">A Get-AzureRMRoleAssignment parancs segítségével listázhatja az összes olyan szerepkör-hozzárendelést, amely egy hatókörre érvényes.</span><span class="sxs-lookup"><span data-stu-id="94974-125">Use the Get-AzureRMRoleAssignment command to list all role assignments that are effective on a scope.</span></span>
<span data-ttu-id="94974-126">Paraméterek nélkül a parancs az előfizetésben szereplő összes szerepkör-hozzárendelést visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="94974-126">Without any parameters, this command returns all the role assignments made under the subscription.</span></span>
<span data-ttu-id="94974-127">Ezt a listát a megbízó, a szerep és a hatókör szűrési paramétereinek használatával lehet szűrni.</span><span class="sxs-lookup"><span data-stu-id="94974-127">This list can  be filtered using filtering parameters for principal, role and scope.</span></span>
<span data-ttu-id="94974-128">A feladat tárgyát meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="94974-128">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="94974-129">A felhasználók megadásához használja a SignInName vagy az Azure AD ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="94974-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="94974-130">Ha meg szeretne adni egy biztonsági csoportot, használja az Azure AD ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="94974-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="94974-131">Az Azure AD-alkalmazások megadásához használja a ServicePrincipalName vagy a ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="94974-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="94974-132">A hozzárendelt szerepkört a RoleDefinitionName paraméterrel kell megadni.</span><span class="sxs-lookup"><span data-stu-id="94974-132">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="94974-133">Az Access által megadott hatókört meg lehet adni.</span><span class="sxs-lookup"><span data-stu-id="94974-133">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="94974-134">Az alapértelmezett érték a kijelölt előfizetéshez tartozik.</span><span class="sxs-lookup"><span data-stu-id="94974-134">It defaults to the selected subscription.</span></span> <span data-ttu-id="94974-135">A hozzárendelés hatóköre az a következő paraméter-kombinációk egyikével határozható meg.</span><span class="sxs-lookup"><span data-stu-id="94974-135">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="94974-136">Hatókör – ez a teljes mértékben minősített hatókör a/Subscriptions/kezdve \<subscriptionId\> .</span><span class="sxs-lookup"><span data-stu-id="94974-136">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="94974-137">Ez a funkció azokat a feladatokat fogja szűrni, amelyek az adott hatókörben, azaz a hatókörben és a fenti hatókörben érvényesek.</span><span class="sxs-lookup"><span data-stu-id="94974-137">This will filter assignments that are effective at that particular scope i.e. all assignments at that scope and above.</span></span>
<span data-ttu-id="94974-138">b.</span><span class="sxs-lookup"><span data-stu-id="94974-138">b.</span></span>
<span data-ttu-id="94974-139">ResourceGroupName – bármely erőforráscsoport neve az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="94974-139">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="94974-140">Ez a funkció a c meghatározott erőforrás-csoportban érvényes hozzárendeléseket fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="94974-140">This will filter assignments effective at the specified resource group c.</span></span>
<span data-ttu-id="94974-141">ResourceName, ResourceType, ResourceGroupName és (opcionálisan) ParentResource – az előfizetésben egy adott erőforrást azonosít, és az adott erőforrás-tartományra érvényes hozzárendeléseket fogja szűrni.</span><span class="sxs-lookup"><span data-stu-id="94974-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter assignments effective at that resource scope.</span></span>
<span data-ttu-id="94974-142">Ha meg szeretné állapítani, hogy egy adott felhasználó Hogyan férhet hozzá az előfizetéshez, használja a ExpandPrincipalGroups kapcsolót.</span><span class="sxs-lookup"><span data-stu-id="94974-142">To determine what access a particular user has in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="94974-143">Ez felsorolja a felhasználóhoz rendelt összes szerepkört, valamint azokat a csoportokat, amelyeknek a felhasználó a tagja.</span><span class="sxs-lookup"><span data-stu-id="94974-143">This will list all roles assigned to the user, and to the groups that the user is member of.</span></span>
<span data-ttu-id="94974-144">Az IncludeClassicAdministrators kapcsolóval az előfizetési rendszergazdák és a közös adminisztrátorok is megjeleníthetők.</span><span class="sxs-lookup"><span data-stu-id="94974-144">Use the IncludeClassicAdministrators switch to also display the subscription admins and co-admins.</span></span>

## <span data-ttu-id="94974-145">Példák</span><span class="sxs-lookup"><span data-stu-id="94974-145">EXAMPLES</span></span>

### <span data-ttu-id="94974-146">Példa 1</span><span class="sxs-lookup"><span data-stu-id="94974-146">Example 1</span></span>
```
PS C:\> Get-AzureRmRoleAssignment
```

<span data-ttu-id="94974-147">Az előfizetésben szereplő összes szerepkör-hozzárendelés listázása</span><span class="sxs-lookup"><span data-stu-id="94974-147">List all role assignments in the subscription</span></span>

### <span data-ttu-id="94974-148">2. példa</span><span class="sxs-lookup"><span data-stu-id="94974-148">Example 2</span></span>
```
PS C:\> Get-AzureRmRoleAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com
```

<span data-ttu-id="94974-149">A felhasználó minden szerepkör-hozzárendelését john.doe@contoso.com , illetve a tagokat a testRG-vagy a fentieken keresztül kapja meg.</span><span class="sxs-lookup"><span data-stu-id="94974-149">Gets all role assignments made to user john.doe@contoso.com, and the groups of which he is member, at the testRG scope or above.</span></span>

### <span data-ttu-id="94974-150">3. példa</span><span class="sxs-lookup"><span data-stu-id="94974-150">Example 3</span></span>
```
PS C:\> Get-AzureRmRoleAssignment -ServicePrincipalName "http://testapp1.com"
```

<span data-ttu-id="94974-151">A megadott szolgáltatási megbízó minden szerepkör-hozzárendelésének beolvasása</span><span class="sxs-lookup"><span data-stu-id="94974-151">Gets all role assignments of the specified service principal</span></span>

### <span data-ttu-id="94974-152">4. példa</span><span class="sxs-lookup"><span data-stu-id="94974-152">Example 4</span></span>
```
PS C:\> Get-AzureRmRoleAssignment -Scope "/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="94974-153">Szerepkör-hozzárendeléseket kap a "hely1" webhely hatókörében.</span><span class="sxs-lookup"><span data-stu-id="94974-153">Gets role assignments at the 'site1' website scope.</span></span>

## <span data-ttu-id="94974-154">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="94974-154">PARAMETERS</span></span>

### <span data-ttu-id="94974-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94974-155">-DefaultProfile</span></span>
<span data-ttu-id="94974-156">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="94974-156">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94974-157">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="94974-157">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="94974-158">Ha meg van adva, azokat a szerepköröket adja eredményül, amelyek közvetlenül a felhasználóhoz lettek rendelve (tranzitívan).</span><span class="sxs-lookup"><span data-stu-id="94974-158">If specified, returns roles directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="94974-159">Csak a felhasználói résztvevők számára támogatott.</span><span class="sxs-lookup"><span data-stu-id="94974-159">Supported only for a user principal.</span></span>

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

### <span data-ttu-id="94974-160">-IncludeClassicAdministrators</span><span class="sxs-lookup"><span data-stu-id="94974-160">-IncludeClassicAdministrators</span></span>
<span data-ttu-id="94974-161">Ha meg van adva, az előfizetés klasszikus rendszergazdáknak (rendszergazdáknak, szolgáltatás-rendszergazdáknak stb.) szerepkör-hozzárendeléseit is megjeleníti.</span><span class="sxs-lookup"><span data-stu-id="94974-161">If specified, also lists subscription classic administrators (co-admins, service admins, etc.) role assignments.</span></span>

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

### <span data-ttu-id="94974-162">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="94974-162">-ObjectId</span></span>
<span data-ttu-id="94974-163">Az Azure AD ObjectId a felhasználó, a csoport vagy a szolgáltatás megbízójának</span><span class="sxs-lookup"><span data-stu-id="94974-163">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="94974-164">A megadott tőkeösszeg összes hozzárendelésének szűrése.</span><span class="sxs-lookup"><span data-stu-id="94974-164">Filters all assignments that are made to the specified principal.</span></span>

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

### <span data-ttu-id="94974-165">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="94974-165">-ParentResource</span></span>
<span data-ttu-id="94974-166">A szülő erőforrás az erőforrás hierarchiájában a ResourceName paraméterrel megadva.</span><span class="sxs-lookup"><span data-stu-id="94974-166">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="94974-167">A ResourceGroupName, az ResourceType és a ResourceName paraméterekkel együtt kell használni.</span><span class="sxs-lookup"><span data-stu-id="94974-167">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

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

### <span data-ttu-id="94974-168">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94974-168">-ResourceGroupName</span></span>
<span data-ttu-id="94974-169">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="94974-169">The resource group name.</span></span>
<span data-ttu-id="94974-170">Felsorolja azokat a szerepkör-hozzárendeléseket, amelyek a megadott erőforráscsoport hatékonyságát jelentik.</span><span class="sxs-lookup"><span data-stu-id="94974-170">Lists role assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="94974-171">Ha a ResourceName, az ResourceType és a ParentResource paraméterekkel együtt használja, a parancs felsorolja az erőforrás csoport erőforrásain érvényes hozzárendeléseket.</span><span class="sxs-lookup"><span data-stu-id="94974-171">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists assignments effective at resources within the resource group.</span></span>

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

### <span data-ttu-id="94974-172">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="94974-172">-ResourceName</span></span>
<span data-ttu-id="94974-173">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="94974-173">The resource name.</span></span>
<span data-ttu-id="94974-174">Például storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="94974-174">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="94974-175">A ResourceGroupName, ResourceType és (opcionálisan) ParentResource paraméterekkel együtt kell használni.</span><span class="sxs-lookup"><span data-stu-id="94974-175">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="94974-176">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="94974-176">-ResourceType</span></span>
<span data-ttu-id="94974-177">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="94974-177">The resource type.</span></span>
<span data-ttu-id="94974-178">Például Microsoft. hálózat/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="94974-178">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="94974-179">A ResourceGroupName, ResourceName és (opcionálisan) ParentResource paraméterekkel együtt kell használni.</span><span class="sxs-lookup"><span data-stu-id="94974-179">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="94974-180">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="94974-180">-RoleDefinitionId</span></span>
<span data-ttu-id="94974-181">A megbízóhoz rendelt szerepkör azonosítója.</span><span class="sxs-lookup"><span data-stu-id="94974-181">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="94974-182">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="94974-182">-RoleDefinitionName</span></span>
<span data-ttu-id="94974-183">A megbízóhoz (például olvasóhoz, Közreműködőhöz, virtuális hálózati adminisztrátorhoz stb.) rendelt szerepkör</span><span class="sxs-lookup"><span data-stu-id="94974-183">Role that is assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

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

### <span data-ttu-id="94974-184">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="94974-184">-Scope</span></span>
<span data-ttu-id="94974-185">A szerepkör-hozzárendelés hatóköre.</span><span class="sxs-lookup"><span data-stu-id="94974-185">The Scope of the role assignment.</span></span>
<span data-ttu-id="94974-186">A relatív URI formátuma.</span><span class="sxs-lookup"><span data-stu-id="94974-186">In the format of relative URI.</span></span>
<span data-ttu-id="94974-187">Például/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="94974-187">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="94974-188">A "/Subscriptions/{id}" szöveggel kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="94974-188">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="94974-189">A parancs az összes olyan feladatot szűri, amely az adott hatókörben érvényes.</span><span class="sxs-lookup"><span data-stu-id="94974-189">The command filters all assignments that are effective at that scope.</span></span>

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

### <span data-ttu-id="94974-190">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="94974-190">-ServicePrincipalName</span></span>
<span data-ttu-id="94974-191">A ServicePrincipalName.</span><span class="sxs-lookup"><span data-stu-id="94974-191">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="94974-192">A megadott Azure AD-alkalmazás összes hozzárendelésének szűrése.</span><span class="sxs-lookup"><span data-stu-id="94974-192">Filters all assignments that are made to the specified Azure AD application.</span></span>

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

### <span data-ttu-id="94974-193">-SignInName</span><span class="sxs-lookup"><span data-stu-id="94974-193">-SignInName</span></span>
<span data-ttu-id="94974-194">Az e-mail-cím vagy a felhasználó egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="94974-194">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="94974-195">A megadott felhasználó összes hozzárendelésének szűrése.</span><span class="sxs-lookup"><span data-stu-id="94974-195">Filters all assignments that are made to the specified user.</span></span>

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

### <span data-ttu-id="94974-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94974-196">CommonParameters</span></span>
<span data-ttu-id="94974-197">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="94974-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94974-198">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94974-198">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94974-199">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="94974-199">INPUTS</span></span>

### <span data-ttu-id="94974-200">System. GUID</span><span class="sxs-lookup"><span data-stu-id="94974-200">System.Guid</span></span>

### <span data-ttu-id="94974-201">System. String</span><span class="sxs-lookup"><span data-stu-id="94974-201">System.String</span></span>

## <span data-ttu-id="94974-202">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94974-202">OUTPUTS</span></span>

### <span data-ttu-id="94974-203">Microsoft. Azure. Command. Resources. modellek. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="94974-203">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="94974-204">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="94974-204">NOTES</span></span>
<span data-ttu-id="94974-205">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="94974-205">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="94974-206">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94974-206">RELATED LINKS</span></span>

[<span data-ttu-id="94974-207">Új – AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="94974-207">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="94974-208">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="94974-208">Remove-AzureRmRoleAssignment</span></span>](./Remove-AzureRmRoleAssignment.md)

[<span data-ttu-id="94974-209">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="94974-209">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

