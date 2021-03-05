---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8C1D738C-825D-4718-AD2A-9CFEAA7DBD3B
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleAssignment.md
ms.openlocfilehash: d941e5cc3bf4a3f2363aa8369a7f5b0518ba2e07
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005798"
---
# <span data-ttu-id="16acc-101">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="16acc-101">Remove-AzRoleAssignment</span></span>

## <span data-ttu-id="16acc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16acc-102">SYNOPSIS</span></span>
<span data-ttu-id="16acc-103">Eltávolít egy szerepkör-hozzárendelést a megadott egyszerű felhasználóhoz, aki egy adott szerepkörhöz van hozzárendelve egy adott hatókörben.</span><span class="sxs-lookup"><span data-stu-id="16acc-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

## <span data-ttu-id="16acc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="16acc-104">SYNTAX</span></span>

### <span data-ttu-id="16acc-105">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="16acc-105">EmptyParameterSet (Default)</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16acc-106">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="16acc-106">ResourceWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16acc-107">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="16acc-107">ResourceGroupWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16acc-108">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="16acc-108">ScopeWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16acc-109">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="16acc-109">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16acc-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="16acc-110">ResourceWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16acc-111">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="16acc-111">ResourceGroupWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16acc-112">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="16acc-112">ScopeWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16acc-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="16acc-113">ResourceWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16acc-114">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="16acc-114">ResourceGroupWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16acc-115">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="16acc-115">ScopeWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16acc-116">RoleAssignmentParameterSet</span><span class="sxs-lookup"><span data-stu-id="16acc-116">RoleAssignmentParameterSet</span></span>
```
Remove-AzRoleAssignment [-PassThru] [-InputObject] <PSRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16acc-117">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="16acc-117">DESCRIPTION</span></span>
<span data-ttu-id="16acc-118">A Remove-AzRoleAssignment parancsmag használatával visszavonhatja a hozzáférést egy adott hatókörű és szerepkörű egyszerű felhasználóhoz.</span><span class="sxs-lookup"><span data-stu-id="16acc-118">Use the Remove-AzRoleAssignment commandlet to revoke access to any principal at given scope and given role.</span></span>
<span data-ttu-id="16acc-119">A feladat objektuma, vagyis a főnévnek meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="16acc-119">The object of the assignment i.e. the principal MUST be specified.</span></span>
<span data-ttu-id="16acc-120">A rendszernév lehet felhasználó (a SignInName vagy az ObjectId paramétert használva azonosíthat egy felhasználót), biztonsági csoport (csoport azonosításához használja az ObjectId paramétert) vagy egyszerű szolgáltatásnév (a ServicePrincipalName vagy az ObjectId paramétert használva azonosítsa a ServicePrincipal paramétert).</span><span class="sxs-lookup"><span data-stu-id="16acc-120">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ServicePrincipalName or ObjectId parameters to identify a ServicePrincipal.</span></span>
<span data-ttu-id="16acc-121">A SzerepkörDefinitionName paraméterrel meg kell adni azt a szerepkört, amelyhez a főnév hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="16acc-121">The role that the principal is assigned to MUST be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="16acc-122">Előfordulhat, hogy a hozzárendelés hatóköre meg van adva, és ha nincs megadva, akkor az előfizetés hatóköre lesz alapértelmezett, vagyis megpróbálja törölni a megadott fő és szerepkörhöz tartozó hozzárendelést az előfizetés hatókörében.</span><span class="sxs-lookup"><span data-stu-id="16acc-122">The scope of the assignment MAY be specified and if not specified, defaults to the subscription scope i.e. it will try to delete an assignment to the specified principal and role at the subscription scope.</span></span>
<span data-ttu-id="16acc-123">A hozzárendelés hatóköre az alábbi paraméterek egyikével is megadva lehet.</span><span class="sxs-lookup"><span data-stu-id="16acc-123">The scope of the assignment can be specified using one of the following parameters.</span></span>
<span data-ttu-id="16acc-124">a.</span><span class="sxs-lookup"><span data-stu-id="16acc-124">a.</span></span>
<span data-ttu-id="16acc-125">Hatókör – Ez a teljes hatókör az /subscriptions/ b-ekkel \<subscriptionId\> kezdve.</span><span class="sxs-lookup"><span data-stu-id="16acc-125">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="16acc-126">ResourceGroupName – Az előfizetés alatt bármelyik erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="16acc-126">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="16acc-127">c.</span><span class="sxs-lookup"><span data-stu-id="16acc-127">c.</span></span>
<span data-ttu-id="16acc-128">ResourceName, ResourceType, ResourceGroupName és (nem kötelező) ParentResource – Az előfizetés alatt egy adott erőforrást azonosít.</span><span class="sxs-lookup"><span data-stu-id="16acc-128">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription.</span></span>

## <span data-ttu-id="16acc-129">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="16acc-129">EXAMPLES</span></span>

### <span data-ttu-id="16acc-130">1. példa</span><span class="sxs-lookup"><span data-stu-id="16acc-130">Example 1</span></span>
```
PS C:\> Remove-AzRoleAssignment -ResourceGroupName rg1 -SignInName john.doe@contoso.com -RoleDefinitionName Reader
```

<span data-ttu-id="16acc-131">Eltávolít egy szerepkör-hozzárendelést az rg1 erőforráscsoport hatókörében az Olvasó john.doe@contoso.com szerepkörhöz hozzárendelt felhasználókhoz.</span><span class="sxs-lookup"><span data-stu-id="16acc-131">Removes a role assignment for john.doe@contoso.com who is assigned to the Reader role at the rg1 resourcegroup scope.</span></span>

### <span data-ttu-id="16acc-132">2. példa</span><span class="sxs-lookup"><span data-stu-id="16acc-132">Example 2</span></span>
```
PS C:\> Remove-AzRoleAssignment -ObjectId 36f81fc3-b00f-48cd-8218-3879f51ff39f -RoleDefinitionName Reader
```

<span data-ttu-id="16acc-133">Eltávolítja a szerepkör-hozzárendelést az ObjectId által azonosított csoporttaghoz, és hozzárendeli az Olvasó szerepkörhöz.</span><span class="sxs-lookup"><span data-stu-id="16acc-133">Removes the role assignment to the group principal identified by the ObjectId and assigned to the Reader role.</span></span>
<span data-ttu-id="16acc-134">Alapértelmezés szerint az aktuális előfizetést használja hatókörként a törölni szükséges feladat megkereséhez.</span><span class="sxs-lookup"><span data-stu-id="16acc-134">Defaults to using the current subscription as the scope to find the assignment to be deleted.</span></span>

### <span data-ttu-id="16acc-135">3. példa</span><span class="sxs-lookup"><span data-stu-id="16acc-135">Example 3</span></span>
```
PS C:\> $roleassignment = Get-AzRoleAssignment |Select-Object -First 1 -Wait
PS C:\> Remove-AzRoleAssignment -InputObject $roleassignment
```

<span data-ttu-id="16acc-136">Eltávolítja az első szerepkör-hozzárendelési objektumot, amely lekért a Get-AzRoleAssignment parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="16acc-136">Removes the first role assignment object which is fetched from the Get-AzRoleAssignment commandlet.</span></span>

## <span data-ttu-id="16acc-137">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16acc-137">PARAMETERS</span></span>

### <span data-ttu-id="16acc-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16acc-138">-DefaultProfile</span></span>
<span data-ttu-id="16acc-139">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="16acc-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16acc-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16acc-140">-InputObject</span></span>
<span data-ttu-id="16acc-141">Szerepkör-hozzárendelés objektum.</span><span class="sxs-lookup"><span data-stu-id="16acc-141">Role Assignment object.</span></span>

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

### <span data-ttu-id="16acc-142">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="16acc-142">-ObjectId</span></span>
<span data-ttu-id="16acc-143">A felhasználó, csoport vagy szolgáltatásnév Azure AD-objektumazonosítója.</span><span class="sxs-lookup"><span data-stu-id="16acc-143">Azure AD ObjectId of the user, group or service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16acc-144">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="16acc-144">-ParentResource</span></span>
<span data-ttu-id="16acc-145">A szülőerőforrás a hierarchiában (a ResourceName paraméterrel megadott erőforrásnál), ha van ilyen.</span><span class="sxs-lookup"><span data-stu-id="16acc-145">The parent resource in the hierarchy(of the resource specified using ResourceName parameter), if any.</span></span>
<span data-ttu-id="16acc-146">A ResourceGroupName, az ResourceType és az ResourceName paraméterrel együtt kell használni egy hierarchikus hatókör felépítéséhez egy relatív URI formájában, amely azonosítja az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="16acc-146">Must be used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource.</span></span>

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

### <span data-ttu-id="16acc-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16acc-147">-PassThru</span></span>
<span data-ttu-id="16acc-148">Ha meg van adva, a törölt szerepkör-hozzárendelés megjelenítése</span><span class="sxs-lookup"><span data-stu-id="16acc-148">If specified, displays the deleted role assignment</span></span>

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

### <span data-ttu-id="16acc-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16acc-149">-ResourceGroupName</span></span>
<span data-ttu-id="16acc-150">Az erőforráscsoport neve, amelyhez a szerepkör hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="16acc-150">The resource group name that the role is assigned to.</span></span>
<span data-ttu-id="16acc-151">Megkísérel törölni egy hozzárendelést a megadott erőforráscsoport-hatókörben.</span><span class="sxs-lookup"><span data-stu-id="16acc-151">Attempts to delete an assignment at the specified resource group scope.</span></span>
<span data-ttu-id="16acc-152">Ha a ResourceName, a ResourceType és a ParentResource paraméterrel együtt használja, a parancs hierarchikus hatókört épít fel egy erőforrást azonosító relatív URI-val.</span><span class="sxs-lookup"><span data-stu-id="16acc-152">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="16acc-153">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="16acc-153">-ResourceName</span></span>
<span data-ttu-id="16acc-154">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="16acc-154">The resource name.</span></span>
<span data-ttu-id="16acc-155">Például: storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="16acc-155">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="16acc-156">A ResourceGroupName, az ResourceType és (opcionálisan)ParentResource paraméterekkel együtt kell használni egy hierarchikus hatókör felépítéséhez egy relatív URI-ként, amely azonosítja az erőforrást, és törli az adott hatókörű hozzárendelést.</span><span class="sxs-lookup"><span data-stu-id="16acc-156">Must be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters, to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that scope.</span></span>

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

### <span data-ttu-id="16acc-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="16acc-157">-ResourceType</span></span>
<span data-ttu-id="16acc-158">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="16acc-158">The resource type.</span></span>
<span data-ttu-id="16acc-159">Például: Microsoft.Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="16acc-159">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="16acc-160">A ResourceGroupName, az ResourceName és a ParentResource paraméterekkel együtt kell használni egy hierarchikus hatókör felépítéséhez egy relatív URI-ként, amely azonosítja az erőforrást, és törli az adott erőforrás-hatókörben lévő hozzárendelést.</span><span class="sxs-lookup"><span data-stu-id="16acc-160">Must be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that resource scope.</span></span>

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

### <span data-ttu-id="16acc-161">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="16acc-161">-RoleDefinitionId</span></span>
<span data-ttu-id="16acc-162">Annak az RBAC-szerepkörnek az azonosítója, amelynek a hozzárendelését törölni kell.</span><span class="sxs-lookup"><span data-stu-id="16acc-162">Id of the RBAC role for which the assignment needs to be deleted.</span></span>

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

### <span data-ttu-id="16acc-163">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="16acc-163">-RoleDefinitionName</span></span>
<span data-ttu-id="16acc-164">Annak az RBAC-szerepkörnek a neve, amelynek a hozzárendelését törölni kell, például olvasó, közreműködő, virtuális hálózat rendszergazdája stb.</span><span class="sxs-lookup"><span data-stu-id="16acc-164">Name of the RBAC role for which the assignment needs to be deleted i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

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

### <span data-ttu-id="16acc-165">-Scope</span><span class="sxs-lookup"><span data-stu-id="16acc-165">-Scope</span></span>
<span data-ttu-id="16acc-166">A törölt szerepkör-hozzárendelés hatóköre.</span><span class="sxs-lookup"><span data-stu-id="16acc-166">The Scope of the role assignment to be deleted.</span></span>
<span data-ttu-id="16acc-167">Relatív URI formátumban.</span><span class="sxs-lookup"><span data-stu-id="16acc-167">In the format of relative URI.</span></span>
<span data-ttu-id="16acc-168">Például: "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="16acc-168">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="16acc-169">Ha nincs megadva, előfizetési szinten kísérelje meg törölni a szerepkört.</span><span class="sxs-lookup"><span data-stu-id="16acc-169">If not specified, will attempt to delete the role at subscription level.</span></span>
<span data-ttu-id="16acc-170">Ha meg van adva, akkor a következővel kell kezdődni: "/subscriptions/{id}".</span><span class="sxs-lookup"><span data-stu-id="16acc-170">If specified, it should start with "/subscriptions/{id}".</span></span>

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

### <span data-ttu-id="16acc-171">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="16acc-171">-ServicePrincipalName</span></span>
<span data-ttu-id="16acc-172">Az Azure AD alkalmazás ServicePrincipalName tulajdonsága</span><span class="sxs-lookup"><span data-stu-id="16acc-172">The ServicePrincipalName of the Azure AD application</span></span>

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

### <span data-ttu-id="16acc-173">-SignInName</span><span class="sxs-lookup"><span data-stu-id="16acc-173">-SignInName</span></span>
<span data-ttu-id="16acc-174">A felhasználó e-mail-címe vagy egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="16acc-174">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="16acc-175">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16acc-175">-Confirm</span></span>
<span data-ttu-id="16acc-176">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="16acc-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16acc-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16acc-177">-WhatIf</span></span>
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

### <span data-ttu-id="16acc-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16acc-178">CommonParameters</span></span>
<span data-ttu-id="16acc-179">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16acc-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16acc-180">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16acc-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16acc-181">INPUTS</span><span class="sxs-lookup"><span data-stu-id="16acc-181">INPUTS</span></span>

### <span data-ttu-id="16acc-182">System.String</span><span class="sxs-lookup"><span data-stu-id="16acc-182">System.String</span></span>

### <span data-ttu-id="16acc-183">System.Guid</span><span class="sxs-lookup"><span data-stu-id="16acc-183">System.Guid</span></span>

### <span data-ttu-id="16acc-184">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="16acc-184">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="16acc-185">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="16acc-185">OUTPUTS</span></span>

### <span data-ttu-id="16acc-186">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="16acc-186">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="16acc-187">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="16acc-187">NOTES</span></span>
<span data-ttu-id="16acc-188">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, telepítés</span><span class="sxs-lookup"><span data-stu-id="16acc-188">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="16acc-189">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="16acc-189">RELATED LINKS</span></span>

[<span data-ttu-id="16acc-190">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="16acc-190">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="16acc-191">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="16acc-191">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="16acc-192">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="16acc-192">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

