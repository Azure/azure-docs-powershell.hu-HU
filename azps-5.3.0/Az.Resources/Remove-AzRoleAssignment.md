---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8C1D738C-825D-4718-AD2A-9CFEAA7DBD3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleAssignment.md
ms.openlocfilehash: fc954dcf2ce3b9a1c066b3986bbc0bbea302ea2d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375772"
---
# <span data-ttu-id="f86a2-101">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f86a2-101">Remove-AzRoleAssignment</span></span>

## <span data-ttu-id="f86a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f86a2-102">SYNOPSIS</span></span>
<span data-ttu-id="f86a2-103">Eltávolít egy szerepkör-hozzárendelést a megadott egyszerű felhasználóhoz, aki egy adott szerepkörhöz van hozzárendelve egy adott hatókörben.</span><span class="sxs-lookup"><span data-stu-id="f86a2-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

## <span data-ttu-id="f86a2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f86a2-104">SYNTAX</span></span>

### <span data-ttu-id="f86a2-105">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f86a2-105">EmptyParameterSet (Default)</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f86a2-106">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f86a2-106">ResourceWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f86a2-107">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f86a2-107">ResourceGroupWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f86a2-108">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f86a2-108">ScopeWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f86a2-109">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f86a2-109">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f86a2-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f86a2-110">ResourceWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f86a2-111">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f86a2-111">ResourceGroupWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f86a2-112">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f86a2-112">ScopeWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f86a2-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="f86a2-113">ResourceWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f86a2-114">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="f86a2-114">ResourceGroupWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f86a2-115">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="f86a2-115">ScopeWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f86a2-116">RoleAssignmentParameterSet</span><span class="sxs-lookup"><span data-stu-id="f86a2-116">RoleAssignmentParameterSet</span></span>
```
Remove-AzRoleAssignment [-PassThru] [-InputObject] <PSRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f86a2-117">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f86a2-117">DESCRIPTION</span></span>
<span data-ttu-id="f86a2-118">A Remove-AzRoleAssignment parancsmagot használva visszavonhatja a hozzáférést egy adott hatókörű és szerepkörű egyszerű felhasználóhoz.</span><span class="sxs-lookup"><span data-stu-id="f86a2-118">Use the Remove-AzRoleAssignment commandlet to revoke access to any principal at given scope and given role.</span></span>
<span data-ttu-id="f86a2-119">A feladat objektuma, vagyis a tőketnévnek meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="f86a2-119">The object of the assignment i.e. the principal MUST be specified.</span></span>
<span data-ttu-id="f86a2-120">A rendszernév lehet felhasználó (a SignInName vagy az ObjectId paramétert használva azonosíthat egy felhasználót), biztonsági csoport (csoport azonosításához használja az ObjectId paramétert) vagy egyszerű szolgáltatásnév (a ServicePrincipalName vagy az ObjectId paramétert használva azonosítsa a ServicePrincipal paramétert).</span><span class="sxs-lookup"><span data-stu-id="f86a2-120">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ServicePrincipalName or ObjectId parameters to identify a ServicePrincipal.</span></span>
<span data-ttu-id="f86a2-121">A szerepkört, amelyhez a főnevet hozzárendelték, a RoleDefinitionName paraméterrel kell megadni.</span><span class="sxs-lookup"><span data-stu-id="f86a2-121">The role that the principal is assigned to MUST be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="f86a2-122">Előfordulhat, hogy a hozzárendelés hatóköre meg van adva, és ha nincs megadva, akkor az előfizetés hatóköre lesz alapértelmezett, vagyis megpróbálja törölni a megadott fő és szerepkörhöz tartozó hozzárendelést az előfizetés hatókörében.</span><span class="sxs-lookup"><span data-stu-id="f86a2-122">The scope of the assignment MAY be specified and if not specified, defaults to the subscription scope i.e. it will try to delete an assignment to the specified principal and role at the subscription scope.</span></span>
<span data-ttu-id="f86a2-123">A hozzárendelés hatóköre az alábbi paraméterek egyikével is megadva lehet.</span><span class="sxs-lookup"><span data-stu-id="f86a2-123">The scope of the assignment can be specified using one of the following parameters.</span></span>
<span data-ttu-id="f86a2-124">a.</span><span class="sxs-lookup"><span data-stu-id="f86a2-124">a.</span></span>
<span data-ttu-id="f86a2-125">Hatókör – Ez a teljes hatókör az /subscriptions/ b-ekkel \<subscriptionId\> kezdve.</span><span class="sxs-lookup"><span data-stu-id="f86a2-125">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="f86a2-126">ResourceGroupName – Az előfizetés alatt bármelyik erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f86a2-126">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="f86a2-127">c.</span><span class="sxs-lookup"><span data-stu-id="f86a2-127">c.</span></span>
<span data-ttu-id="f86a2-128">ResourceName, ResourceType, ResourceGroupName és (opcionális) ParentResource – Az előfizetés alatt egy adott erőforrást azonosít.</span><span class="sxs-lookup"><span data-stu-id="f86a2-128">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription.</span></span>

## <span data-ttu-id="f86a2-129">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f86a2-129">EXAMPLES</span></span>

### <span data-ttu-id="f86a2-130">1. példa</span><span class="sxs-lookup"><span data-stu-id="f86a2-130">Example 1</span></span>
```
PS C:\> Remove-AzRoleAssignment -ResourceGroupName rg1 -SignInName john.doe@contoso.com -RoleDefinitionName Reader
```

<span data-ttu-id="f86a2-131">Eltávolít egy szerepkör-hozzárendelést az rg1 erőforráscsoport hatókörében az Olvasó john.doe@contoso.com szerepkörhöz hozzárendelt felhasználókhoz.</span><span class="sxs-lookup"><span data-stu-id="f86a2-131">Removes a role assignment for john.doe@contoso.com who is assigned to the Reader role at the rg1 resourcegroup scope.</span></span>

### <span data-ttu-id="f86a2-132">2. példa</span><span class="sxs-lookup"><span data-stu-id="f86a2-132">Example 2</span></span>
```
PS C:\> Remove-AzRoleAssignment -ObjectId 36f81fc3-b00f-48cd-8218-3879f51ff39f -RoleDefinitionName Reader
```

<span data-ttu-id="f86a2-133">Eltávolítja az ObjectId által azonosított és az Olvasó szerepkörhöz hozzárendelt csoporttag szerepkör-hozzárendelését.</span><span class="sxs-lookup"><span data-stu-id="f86a2-133">Removes the role assignment to the group principal identified by the ObjectId and assigned to the Reader role.</span></span>
<span data-ttu-id="f86a2-134">Alapértelmezés szerint az aktuális előfizetést használja hatókörként a törölni szükséges feladat megkereséhez.</span><span class="sxs-lookup"><span data-stu-id="f86a2-134">Defaults to using the current subscription as the scope to find the assignment to be deleted.</span></span>

### <span data-ttu-id="f86a2-135">3. példa</span><span class="sxs-lookup"><span data-stu-id="f86a2-135">Example 3</span></span>
```
PS C:\> $roleassignment = Get-AzRoleAssignment |Select-Object -First 1 -Wait
PS C:\> Remove-AzRoleAssignment -InputObject $roleassignment
```

<span data-ttu-id="f86a2-136">Eltávolítja az első szerepkör-hozzárendelési objektumot, amely lekért a Get-AzRoleAssignment parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="f86a2-136">Removes the first role assignment object which is fetched from the Get-AzRoleAssignment commandlet.</span></span>

## <span data-ttu-id="f86a2-137">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f86a2-137">PARAMETERS</span></span>

### <span data-ttu-id="f86a2-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f86a2-138">-DefaultProfile</span></span>
<span data-ttu-id="f86a2-139">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f86a2-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f86a2-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f86a2-140">-InputObject</span></span>
<span data-ttu-id="f86a2-141">Szerepkör-hozzárendelés objektum.</span><span class="sxs-lookup"><span data-stu-id="f86a2-141">Role Assignment object.</span></span>

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

### <span data-ttu-id="f86a2-142">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f86a2-142">-ObjectId</span></span>
<span data-ttu-id="f86a2-143">A felhasználó, csoport vagy szolgáltatásnév Azure AD-objektumazonosítója.</span><span class="sxs-lookup"><span data-stu-id="f86a2-143">Azure AD ObjectId of the user, group or service principal.</span></span>

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

### <span data-ttu-id="f86a2-144">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="f86a2-144">-ParentResource</span></span>
<span data-ttu-id="f86a2-145">A szülőerőforrás a hierarchiában (a ResourceName paraméterrel megadott erőforrásnál), ha van ilyen.</span><span class="sxs-lookup"><span data-stu-id="f86a2-145">The parent resource in the hierarchy(of the resource specified using ResourceName parameter), if any.</span></span>
<span data-ttu-id="f86a2-146">A ResourceGroupName, az ResourceType és az ResourceName paraméterrel együtt kell használni egy hierarchikus hatókör felépítéséhez egy relatív URI formájában, amely azonosítja az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="f86a2-146">Must be used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource.</span></span>

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

### <span data-ttu-id="f86a2-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f86a2-147">-PassThru</span></span>
<span data-ttu-id="f86a2-148">Ha meg van adva, a törölt szerepkör-hozzárendelés megjelenítése</span><span class="sxs-lookup"><span data-stu-id="f86a2-148">If specified, displays the deleted role assignment</span></span>

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

### <span data-ttu-id="f86a2-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f86a2-149">-ResourceGroupName</span></span>
<span data-ttu-id="f86a2-150">Az erőforráscsoport neve, amelyhez a szerepkör hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="f86a2-150">The resource group name that the role is assigned to.</span></span>
<span data-ttu-id="f86a2-151">Megkísérel törölni egy hozzárendelést a megadott erőforráscsoport-hatókörben.</span><span class="sxs-lookup"><span data-stu-id="f86a2-151">Attempts to delete an assignment at the specified resource group scope.</span></span>
<span data-ttu-id="f86a2-152">Ha a ResourceName, a ResourceType és a ParentResource paraméterrel együtt használja, a parancs hierarchikus hatókört épít fel egy erőforrást azonosító relatív URI-val.</span><span class="sxs-lookup"><span data-stu-id="f86a2-152">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="f86a2-153">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f86a2-153">-ResourceName</span></span>
<span data-ttu-id="f86a2-154">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f86a2-154">The resource name.</span></span>
<span data-ttu-id="f86a2-155">Például: storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="f86a2-155">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="f86a2-156">A ResourceGroupName, az ResourceType és (opcionális) ParentResource paraméterekkel együtt kell használni egy hierarchikus hatókör felépítéséhez egy relatív URI-ként, amely azonosítja az erőforrást, és törli az adott hatókörben lévő hozzárendelést.</span><span class="sxs-lookup"><span data-stu-id="f86a2-156">Must be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters, to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that scope.</span></span>

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

### <span data-ttu-id="f86a2-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="f86a2-157">-ResourceType</span></span>
<span data-ttu-id="f86a2-158">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="f86a2-158">The resource type.</span></span>
<span data-ttu-id="f86a2-159">Például: Microsoft.Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="f86a2-159">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="f86a2-160">A ResourceGroupName, az ResourceName és a ParentResource paraméterekkel együtt kell használni egy hierarchikus hatókör felépítéséhez egy relatív URI-ként, amely azonosítja az erőforrást, és törli az adott erőforrás-hatókörben lévő hozzárendelést.</span><span class="sxs-lookup"><span data-stu-id="f86a2-160">Must be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that resource scope.</span></span>

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

### <span data-ttu-id="f86a2-161">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="f86a2-161">-RoleDefinitionId</span></span>
<span data-ttu-id="f86a2-162">Annak az RBAC-szerepkörnek az azonosítója, amelynek a hozzárendelését törölni kell.</span><span class="sxs-lookup"><span data-stu-id="f86a2-162">Id of the RBAC role for which the assignment needs to be deleted.</span></span>

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

### <span data-ttu-id="f86a2-163">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="f86a2-163">-RoleDefinitionName</span></span>
<span data-ttu-id="f86a2-164">Annak az RBAC-szerepkörnek a neve, amelynek a hozzárendelését törölni kell, például olvasó, közreműködő, virtuális hálózat rendszergazdája stb.</span><span class="sxs-lookup"><span data-stu-id="f86a2-164">Name of the RBAC role for which the assignment needs to be deleted i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

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

### <span data-ttu-id="f86a2-165">-Scope</span><span class="sxs-lookup"><span data-stu-id="f86a2-165">-Scope</span></span>
<span data-ttu-id="f86a2-166">A törölt szerepkör-hozzárendelés hatóköre.</span><span class="sxs-lookup"><span data-stu-id="f86a2-166">The Scope of the role assignment to be deleted.</span></span>
<span data-ttu-id="f86a2-167">Relatív URI formátumban.</span><span class="sxs-lookup"><span data-stu-id="f86a2-167">In the format of relative URI.</span></span>
<span data-ttu-id="f86a2-168">Például: "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="f86a2-168">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="f86a2-169">Ha nincs megadva, előfizetési szinten megpróbálja törölni a szerepkört.</span><span class="sxs-lookup"><span data-stu-id="f86a2-169">If not specified, will attempt to delete the role at subscription level.</span></span>
<span data-ttu-id="f86a2-170">Ha meg van adva, akkor a következővel kell kezdődni: "/subscriptions/{id}".</span><span class="sxs-lookup"><span data-stu-id="f86a2-170">If specified, it should start with "/subscriptions/{id}".</span></span>

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

### <span data-ttu-id="f86a2-171">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="f86a2-171">-ServicePrincipalName</span></span>
<span data-ttu-id="f86a2-172">Az Azure AD alkalmazás ServicePrincipalName tulajdonsága</span><span class="sxs-lookup"><span data-stu-id="f86a2-172">The ServicePrincipalName of the Azure AD application</span></span>

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

### <span data-ttu-id="f86a2-173">-SignInName</span><span class="sxs-lookup"><span data-stu-id="f86a2-173">-SignInName</span></span>
<span data-ttu-id="f86a2-174">A felhasználó e-mail-címe vagy egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="f86a2-174">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="f86a2-175">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f86a2-175">-Confirm</span></span>
<span data-ttu-id="f86a2-176">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f86a2-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f86a2-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f86a2-177">-WhatIf</span></span>
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

### <span data-ttu-id="f86a2-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f86a2-178">CommonParameters</span></span>
<span data-ttu-id="f86a2-179">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f86a2-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f86a2-180">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f86a2-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f86a2-181">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f86a2-181">INPUTS</span></span>

### <span data-ttu-id="f86a2-182">System.String</span><span class="sxs-lookup"><span data-stu-id="f86a2-182">System.String</span></span>

### <span data-ttu-id="f86a2-183">System.Guid</span><span class="sxs-lookup"><span data-stu-id="f86a2-183">System.Guid</span></span>

### <span data-ttu-id="f86a2-184">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f86a2-184">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="f86a2-185">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f86a2-185">OUTPUTS</span></span>

### <span data-ttu-id="f86a2-186">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f86a2-186">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="f86a2-187">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f86a2-187">NOTES</span></span>
<span data-ttu-id="f86a2-188">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, telepítés</span><span class="sxs-lookup"><span data-stu-id="f86a2-188">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="f86a2-189">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f86a2-189">RELATED LINKS</span></span>

[<span data-ttu-id="f86a2-190">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f86a2-190">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="f86a2-191">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f86a2-191">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="f86a2-192">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f86a2-192">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

