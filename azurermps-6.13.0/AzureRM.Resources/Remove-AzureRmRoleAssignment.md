---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8C1D738C-825D-4718-AD2A-9CFEAA7DBD3B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleAssignment.md
ms.openlocfilehash: 706ba111fb015c8865a33a9beec4fe3e722718ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493939"
---
# <span data-ttu-id="2d730-101">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="2d730-101">Remove-AzureRmRoleAssignment</span></span>

## <span data-ttu-id="2d730-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2d730-102">SYNOPSIS</span></span>
<span data-ttu-id="2d730-103">Eltávolítja a szerepkör-hozzárendelést a meghatározott megbízóhoz, aki egy bizonyos hatókörben meghatározott szerepkörhöz van rendelve.</span><span class="sxs-lookup"><span data-stu-id="2d730-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d730-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2d730-104">SYNTAX</span></span>

### <span data-ttu-id="2d730-105">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2d730-105">EmptyParameterSet (Default)</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d730-106">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d730-106">ResourceWithObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d730-107">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d730-107">ResourceGroupWithObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d730-108">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d730-108">ScopeWithObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d730-109">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d730-109">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d730-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d730-110">ResourceWithSignInNameParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d730-111">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d730-111">ResourceGroupWithSignInNameParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d730-112">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d730-112">ScopeWithSignInNameParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d730-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d730-113">ResourceWithSPNParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d730-114">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d730-114">ResourceGroupWithSPNParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 -RoleDefinitionName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d730-115">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d730-115">ScopeWithSPNParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ServicePrincipalName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d730-116">RoleAssignmentParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d730-116">RoleAssignmentParameterSet</span></span>
```
Remove-AzureRmRoleAssignment [-PassThru] [-InputObject] <PSRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d730-117">Leírás</span><span class="sxs-lookup"><span data-stu-id="2d730-117">DESCRIPTION</span></span>
<span data-ttu-id="2d730-118">A Remove-AzureRmRoleAssignment parancsmagot segítségével visszavonhatja a jogosultságokat egy adott hatókörhöz és adott szerepkörhöz.</span><span class="sxs-lookup"><span data-stu-id="2d730-118">Use the Remove-AzureRmRoleAssignment commandlet to revoke access to any principal at given scope and given role.</span></span>
<span data-ttu-id="2d730-119">A feladat objektumát, azaz a megbízót meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="2d730-119">The object of the assignment i.e. the principal MUST be specified.</span></span>
<span data-ttu-id="2d730-120">A megbízó lehet egy felhasználó (a SignInName vagy a ObjectId paraméterrel a felhasználó azonosítóját használhatja), a biztonsági csoportot (a ObjectId paramétert használva azonosíthat egy csoportot) vagy a szolgáltatót (a ServicePrincipalName vagy ObjectId paraméterekkel azonosíthat egy ServicePrincipal.</span><span class="sxs-lookup"><span data-stu-id="2d730-120">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ServicePrincipalName or ObjectId parameters to identify a ServicePrincipal.</span></span>
<span data-ttu-id="2d730-121">A megbízó által hozzárendelt szerepkört a RoleDefinitionName paraméterrel kell megadni.</span><span class="sxs-lookup"><span data-stu-id="2d730-121">The role that the principal is assigned to MUST be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="2d730-122">A hozzárendelés hatóköre megadható, és ha nincs megadva, az alapértelmezett érték az előfizetési tartományhoz, azaz megpróbálja törölni a feladatot a megadott megbízói és szerepkör-előfizetési hatókörben.</span><span class="sxs-lookup"><span data-stu-id="2d730-122">The scope of the assignment MAY be specified and if not specified, defaults to the subscription scope i.e. it will try to delete an assignment to the specified principal and role at the subscription scope.</span></span>
<span data-ttu-id="2d730-123">A hozzárendelés hatóköre az alábbi paraméterek valamelyikével határozható meg.</span><span class="sxs-lookup"><span data-stu-id="2d730-123">The scope of the assignment can be specified using one of the following parameters.</span></span>
<span data-ttu-id="2d730-124">egy.</span><span class="sxs-lookup"><span data-stu-id="2d730-124">a.</span></span>
<span data-ttu-id="2d730-125">Hatókör – ez a teljes mértékben minősített hatókör a/Subscriptions/b karakterrel kezdődően \<subscriptionId\> .</span><span class="sxs-lookup"><span data-stu-id="2d730-125">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="2d730-126">ResourceGroupName – bármely erőforráscsoport neve az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="2d730-126">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="2d730-127">c.</span><span class="sxs-lookup"><span data-stu-id="2d730-127">c.</span></span>
<span data-ttu-id="2d730-128">ResourceName, ResourceType, ResourceGroupName és (opcionálisan) ParentResource – az előfizetéshez tartozó adott erőforrás azonosítása.</span><span class="sxs-lookup"><span data-stu-id="2d730-128">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription.</span></span>

## <span data-ttu-id="2d730-129">Példák</span><span class="sxs-lookup"><span data-stu-id="2d730-129">EXAMPLES</span></span>

### <span data-ttu-id="2d730-130">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2d730-130">Example 1</span></span>
```
PS C:\> Remove-AzureRmRoleAssignment -ResourceGroupName rg1 -SignInName john.doe@contoso.com -RoleDefinitionName Reader
```

<span data-ttu-id="2d730-131">Annak a szerepkör-hozzárendelésnek a eltávolítása, amely a john.doe@contoso.com rg1 resourcegroup hatókörben az olvasó szerepkörhöz van rendelve.</span><span class="sxs-lookup"><span data-stu-id="2d730-131">Removes a role assignment for john.doe@contoso.com who is assigned to the Reader role at the rg1 resourcegroup scope.</span></span>

### <span data-ttu-id="2d730-132">2. példa</span><span class="sxs-lookup"><span data-stu-id="2d730-132">Example 2</span></span>
```
PS C:\> Remove-AzureRmRoleAssignment -ObjectId 36f81fc3-b00f-48cd-8218-3879f51ff39f -RoleDefinitionName Reader
```

<span data-ttu-id="2d730-133">Eltávolítja a szerepkör-hozzárendelést a ObjectId által azonosított és az olvasó szerepéhez rendelt csoport fő csoportjához.</span><span class="sxs-lookup"><span data-stu-id="2d730-133">Removes the role assignment to the group principal identified by the ObjectId and assigned to the Reader role.</span></span>
<span data-ttu-id="2d730-134">Alapértelmezés szerint az aktuális előfizetést a törlendő hozzárendelés megtalálásához használja.</span><span class="sxs-lookup"><span data-stu-id="2d730-134">Defaults to using the current subscription as the scope to find the assignment to be deleted.</span></span>

### <span data-ttu-id="2d730-135">3. példa</span><span class="sxs-lookup"><span data-stu-id="2d730-135">Example 3</span></span>
```
PS C:\> $roleassignment = Get-AzureRmRoleAssignment |Select-Object -First 1 -Wait
PS C:\> Remove-AzureRmRoleAssignment -InputObject $roleassignment
```

<span data-ttu-id="2d730-136">Eltávolítja az első szerepkör-hozzárendelési objektumot, amely a Get-AzureRmRoleAssignment parancsmagot lett beolvasva.</span><span class="sxs-lookup"><span data-stu-id="2d730-136">Removes the first role assignment object which is fetched from the Get-AzureRmRoleAssignment commandlet.</span></span>

## <span data-ttu-id="2d730-137">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2d730-137">PARAMETERS</span></span>

### <span data-ttu-id="2d730-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d730-138">-DefaultProfile</span></span>
<span data-ttu-id="2d730-139">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2d730-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d730-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d730-140">-InputObject</span></span>
<span data-ttu-id="2d730-141">Szerepkör-hozzárendelési objektum</span><span class="sxs-lookup"><span data-stu-id="2d730-141">Role Assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment
Parameter Sets: RoleAssignmentParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d730-142">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="2d730-142">-ObjectId</span></span>
<span data-ttu-id="2d730-143">Azure AD ObjectId a felhasználó, csoport vagy szolgáltatás megbízójának.</span><span class="sxs-lookup"><span data-stu-id="2d730-143">Azure AD ObjectId of the user, group or service principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d730-144">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="2d730-144">-ParentResource</span></span>
<span data-ttu-id="2d730-145">A fölérendelt erőforrás a hierarchiában (ResourceName paraméterrel megadott erőforrás), ha van ilyen.</span><span class="sxs-lookup"><span data-stu-id="2d730-145">The parent resource in the hierarchy(of the resource specified using ResourceName parameter), if any.</span></span>
<span data-ttu-id="2d730-146">A ResourceGroupName, a ResourceType és a ResourceName paraméterrel együtt kell használni, hogy hierarchikus hatókört hozzon létre az erőforrást azonosító relatív URI-azonosítók formájában.</span><span class="sxs-lookup"><span data-stu-id="2d730-146">Must be used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d730-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d730-147">-PassThru</span></span>
<span data-ttu-id="2d730-148">Ha meg van adva, a törölt szerepkör-hozzárendelést jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="2d730-148">If specified, displays the deleted role assignment</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d730-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d730-149">-ResourceGroupName</span></span>
<span data-ttu-id="2d730-150">Annak az erőforráscsoport-névnek a neve, amelyhez a szerepkör hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="2d730-150">The resource group name that the role is assigned to.</span></span>
<span data-ttu-id="2d730-151">Megpróbálja törölni a feladatot a megadott erőforráscsoport-hatókörben.</span><span class="sxs-lookup"><span data-stu-id="2d730-151">Attempts to delete an assignment at the specified resource group scope.</span></span>
<span data-ttu-id="2d730-152">Ha a ResourceName, az ResourceType és (opcionálisan) ParentResource-paraméterekkel együtt használja, a parancs hierarchikus hatókört hoz létre egy erőforrást azonosító relatív URI-azonosítók formájában.</span><span class="sxs-lookup"><span data-stu-id="2d730-152">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d730-153">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="2d730-153">-ResourceName</span></span>
<span data-ttu-id="2d730-154">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="2d730-154">The resource name.</span></span>
<span data-ttu-id="2d730-155">Például storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="2d730-155">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="2d730-156">A ResourceGroupName, ResourceType és (opcionálisan) ParentResource-paraméterekkel együtt kell használni, hogy hierarchikus hatókört hozzon létre egy relatív URI-azonosítóval, amely azonosítja az erőforrást, és törölje annak a hatókörnek a hozzárendelését.</span><span class="sxs-lookup"><span data-stu-id="2d730-156">Must be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters, to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that scope.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d730-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="2d730-157">-ResourceType</span></span>
<span data-ttu-id="2d730-158">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="2d730-158">The resource type.</span></span>
<span data-ttu-id="2d730-159">Például Microsoft. hálózat/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="2d730-159">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="2d730-160">A ResourceGroupName, ResourceName és (opcionálisan) ParentResource-paraméterekkel együtt kell használni ahhoz, hogy egy hierarchikus hatókört hozzon létre egy relatív URI-azonosítóval, amely azonosítja az erőforrást, és töröljön egy hozzárendelést az adott erőforrás-hatókörben.</span><span class="sxs-lookup"><span data-stu-id="2d730-160">Must be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that resource scope.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d730-161">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="2d730-161">-RoleDefinitionId</span></span>
<span data-ttu-id="2d730-162">Annak az RBAC-szerepkörnek az azonosítója, amelyhez a feladatot törölni kell.</span><span class="sxs-lookup"><span data-stu-id="2d730-162">Id of the RBAC role for which the assignment needs to be deleted.</span></span>

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

### <span data-ttu-id="2d730-163">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="2d730-163">-RoleDefinitionName</span></span>
<span data-ttu-id="2d730-164">Annak a RBAC szerepkörnek a neve, amelyhez a feladatot törölni kell (például olvasó, közreműködő, virtuális hálózati rendszergazda stb.).</span><span class="sxs-lookup"><span data-stu-id="2d730-164">Name of the RBAC role for which the assignment needs to be deleted i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d730-165">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="2d730-165">-Scope</span></span>
<span data-ttu-id="2d730-166">A törlendő szerepkör-hozzárendelés hatóköre.</span><span class="sxs-lookup"><span data-stu-id="2d730-166">The Scope of the role assignment to be deleted.</span></span>
<span data-ttu-id="2d730-167">A relatív URI formátuma.</span><span class="sxs-lookup"><span data-stu-id="2d730-167">In the format of relative URI.</span></span>
<span data-ttu-id="2d730-168">Például "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="2d730-168">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="2d730-169">Ha nem adja meg, akkor megkísérli törölni a szerepkört az előfizetési szinten.</span><span class="sxs-lookup"><span data-stu-id="2d730-169">If not specified, will attempt to delete the role at subscription level.</span></span>
<span data-ttu-id="2d730-170">Ha meg van adva, akkor a "/Subscriptions/{id}" szöveggel kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="2d730-170">If specified, it should start with "/subscriptions/{id}".</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d730-171">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="2d730-171">-ServicePrincipalName</span></span>
<span data-ttu-id="2d730-172">Az Azure AD-alkalmazás ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="2d730-172">The ServicePrincipalName of the Azure AD application</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d730-173">-SignInName</span><span class="sxs-lookup"><span data-stu-id="2d730-173">-SignInName</span></span>
<span data-ttu-id="2d730-174">Az e-mail-cím vagy a felhasználó egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="2d730-174">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ScopeWithSignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d730-175">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2d730-175">-Confirm</span></span>
<span data-ttu-id="2d730-176">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2d730-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d730-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d730-177">-WhatIf</span></span>
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

### <span data-ttu-id="2d730-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d730-178">CommonParameters</span></span>
<span data-ttu-id="2d730-179">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2d730-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d730-180">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d730-180">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d730-181">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d730-181">INPUTS</span></span>

### <span data-ttu-id="2d730-182">System. GUID</span><span class="sxs-lookup"><span data-stu-id="2d730-182">System.Guid</span></span>

### <span data-ttu-id="2d730-183">System. String</span><span class="sxs-lookup"><span data-stu-id="2d730-183">System.String</span></span>

### <span data-ttu-id="2d730-184">Microsoft. Azure. Command. Resources. modellek. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="2d730-184">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>
<span data-ttu-id="2d730-185">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2d730-185">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="2d730-186">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d730-186">OUTPUTS</span></span>

### <span data-ttu-id="2d730-187">Microsoft. Azure. Command. Resources. modellek. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="2d730-187">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="2d730-188">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2d730-188">NOTES</span></span>
<span data-ttu-id="2d730-189">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="2d730-189">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="2d730-190">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2d730-190">RELATED LINKS</span></span>

[<span data-ttu-id="2d730-191">Új – AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="2d730-191">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="2d730-192">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="2d730-192">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="2d730-193">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="2d730-193">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

