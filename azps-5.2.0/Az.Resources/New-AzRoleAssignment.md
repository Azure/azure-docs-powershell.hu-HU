---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E460D108-2BF9-4F57-AF3D-13868DC73EA0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleAssignment.md
ms.openlocfilehash: 2ec39bc66b3b027cb7b5ef9dda09734f8aaf457a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328534"
---
# <span data-ttu-id="0cd46-101">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="0cd46-101">New-AzRoleAssignment</span></span>

## <span data-ttu-id="0cd46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cd46-102">SYNOPSIS</span></span>
<span data-ttu-id="0cd46-103">Hozzárendeli a megadott rbac szerepkört a megadott egyszerű felhasználóhoz a megadott hatókörben.</span><span class="sxs-lookup"><span data-stu-id="0cd46-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="0cd46-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0cd46-104">SYNTAX</span></span>

### <span data-ttu-id="0cd46-105">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0cd46-105">EmptyParameterSet (Default)</span></span>
```
New-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cd46-106">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0cd46-106">ResourceGroupWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cd46-107">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0cd46-107">ResourceWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cd46-108">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0cd46-108">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -Scope <String> [-Description <String>] [-Condition <String>]
 [-ConditionVersion <String>] -RoleDefinitionId <Guid> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cd46-109">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0cd46-109">ResourceGroupWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cd46-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0cd46-110">ResourceWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cd46-111">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0cd46-111">ScopeWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cd46-112">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="0cd46-112">ResourceGroupWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cd46-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="0cd46-113">ResourceWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cd46-114">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="0cd46-114">ScopeWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> [-Scope <String>] -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cd46-115">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="0cd46-115">InputFileParameterSet</span></span>
```
New-AzRoleAssignment -InputFile <String> [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0cd46-116">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0cd46-116">DESCRIPTION</span></span>
<span data-ttu-id="0cd46-117">A hozzáférést New-AzRoleAssignment a New-AzRoleAssignment paranccsal.</span><span class="sxs-lookup"><span data-stu-id="0cd46-117">Use the New-AzRoleAssignment command to grant access.</span></span>
<span data-ttu-id="0cd46-118">Az Access úgy adható meg, hogy a megfelelő RBAC-szerepkört rendeli hozzájuk a megfelelő hatókörben.</span><span class="sxs-lookup"><span data-stu-id="0cd46-118">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="0cd46-119">Ha a teljes előfizetéshez szeretne hozzáférést rendelni, rendeljen hozzá egy szerepkört az előfizetés hatóköréhez.</span><span class="sxs-lookup"><span data-stu-id="0cd46-119">To grant access to the entire subscription, assign a role at the subscription scope.</span></span>
<span data-ttu-id="0cd46-120">Ha egy előfizetésen belül egy adott erőforráscsoporthoz szeretne hozzáférést rendelni, rendeljen hozzá egy szerepkört az erőforráscsoport hatóköréhez.</span><span class="sxs-lookup"><span data-stu-id="0cd46-120">To grant access to a specific resource group within a subscription, assign a role at the resource group scope.</span></span>
<span data-ttu-id="0cd46-121">A feladat tárgyát meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="0cd46-121">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="0cd46-122">Felhasználó megadásához használja a SignInName vagy az Azure AD ObjectId paramétereit.</span><span class="sxs-lookup"><span data-stu-id="0cd46-122">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="0cd46-123">Biztonsági csoport megadásához használja az Azure AD ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="0cd46-123">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="0cd46-124">Azure AD-alkalmazás megadásához használja az ApplicationId vagy az ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="0cd46-124">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="0cd46-125">A hozzárendelt szerepkört a RoleDefinitionName paraméterrel kell megadni.</span><span class="sxs-lookup"><span data-stu-id="0cd46-125">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="0cd46-126">A hozzáférés hatóköre meg lehet adni.</span><span class="sxs-lookup"><span data-stu-id="0cd46-126">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="0cd46-127">Alapértelmezés szerint a kijelölt előfizetést használja.</span><span class="sxs-lookup"><span data-stu-id="0cd46-127">It defaults to the selected subscription.</span></span> <span data-ttu-id="0cd46-128">A hozzárendelés hatóköre a következő paraméterkombinációk egyikével (a) lehet megadni.</span><span class="sxs-lookup"><span data-stu-id="0cd46-128">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="0cd46-129">Hatókör – Ez a teljes hatókör az /subscriptions/ b-ekkel \<subscriptionId\> kezdve.</span><span class="sxs-lookup"><span data-stu-id="0cd46-129">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="0cd46-130">ResourceGroupName – hozzáférés megadása a megadott erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="0cd46-130">ResourceGroupName - to grant access to the specified resource group.</span></span>
<span data-ttu-id="0cd46-131">c.</span><span class="sxs-lookup"><span data-stu-id="0cd46-131">c.</span></span>
<span data-ttu-id="0cd46-132">ResourceName, ResourceType, ResourceGroupName és (opcionális) ParentResource – adott erőforrás megadása egy erőforráscsoporton belül, amely hozzáférést biztosít az erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="0cd46-132">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - to specify a particular resource within a resource group to grant access to.</span></span>

## <span data-ttu-id="0cd46-133">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0cd46-133">EXAMPLES</span></span>

### <span data-ttu-id="0cd46-134">1. példa</span><span class="sxs-lookup"><span data-stu-id="0cd46-134">Example 1</span></span>
```
PS C:\> New-AzRoleAssignment -ResourceGroupName rg1 -SignInName allen.young@live.com -RoleDefinitionName Reader -AllowDelegation
```

<span data-ttu-id="0cd46-135">Hozzáférés megadása az olvasó szerepkörének egy felhasználóhoz egy erőforráscsoport hatókörében, delegálásra elérhető szerepkör-hozzárendeléssel</span><span class="sxs-lookup"><span data-stu-id="0cd46-135">Grant Reader role access to a user at a resource group scope with the Role Assignment being available for delegation</span></span>

### <span data-ttu-id="0cd46-136">2. példa</span><span class="sxs-lookup"><span data-stu-id="0cd46-136">Example 2</span></span>
```
PS C:\> Get-AzADGroup -SearchString "Christine Koch Team"

          DisplayName                    Type                           Id
          -----------                    ----                           --------
          Christine Koch Team                                           2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb

PS C:\> New-AzRoleAssignment -ObjectId 2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb -RoleDefinitionName Contributor  -ResourceGroupName rg1
```

<span data-ttu-id="0cd46-137">Hozzáférés megadása biztonsági csoportnak</span><span class="sxs-lookup"><span data-stu-id="0cd46-137">Grant access to a security group</span></span>

### <span data-ttu-id="0cd46-138">3. példa</span><span class="sxs-lookup"><span data-stu-id="0cd46-138">Example 3</span></span>
```
PS C:\> New-AzRoleAssignment -SignInName john.doe@contoso.com -RoleDefinitionName Owner -Scope "/subscriptions/86f81fc3-b00f-48cd-8218-3879f51ff362/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="0cd46-139">Hozzáférés megadása egy felhasználónak egy erőforrásnál (webhely)</span><span class="sxs-lookup"><span data-stu-id="0cd46-139">Grant access to a user at a resource (website)</span></span>

### <span data-ttu-id="0cd46-140">4. példa</span><span class="sxs-lookup"><span data-stu-id="0cd46-140">Example 4</span></span>
```
PS C:\> New-AzRoleAssignment -ObjectId 5ac84765-1c8c-4994-94b2-629461bd191b -RoleDefinitionName "Virtual Machine Contributor" -ResourceName Devices-Engineering-ProjectRND -ResourceType Microsoft.Network/virtualNetworks/subnets -ParentResource virtualNetworks/VNET-EASTUS-01 -ResourceGroupName Network
```

<span data-ttu-id="0cd46-141">Csoporthoz való hozzáférés megadása beágyazott erőforrásnál (alhálózaton)</span><span class="sxs-lookup"><span data-stu-id="0cd46-141">Grant access to a group at a nested resource (subnet)</span></span>

### <span data-ttu-id="0cd46-142">5. példa</span><span class="sxs-lookup"><span data-stu-id="0cd46-142">Example 5</span></span>
```
PS C:\> $servicePrincipal = New-AzADServicePrincipal -DisplayName "testServiceprincipal"
PS C:\> New-AzRoleAssignment -RoleDefinitionName "Reader" -ApplicationId $servicePrincipal.ApplicationId
```

<span data-ttu-id="0cd46-143">Egyszerű szolgáltatásnévhez való hozzáférés megadása az olvasóknak</span><span class="sxs-lookup"><span data-stu-id="0cd46-143">Grant reader access to a service principal</span></span>

## <span data-ttu-id="0cd46-144">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0cd46-144">PARAMETERS</span></span>

### <span data-ttu-id="0cd46-145">-AllowDelegation</span><span class="sxs-lookup"><span data-stu-id="0cd46-145">-AllowDelegation</span></span>
<span data-ttu-id="0cd46-146">A meghatalmazási jelölő szerepkör-hozzárendelés létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="0cd46-146">The delegation flag while creating a Role assignment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cd46-147">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="0cd46-147">-ApplicationId</span></span>
<span data-ttu-id="0cd46-148">A ServicePrincipal alkalmazásazonosítója</span><span class="sxs-lookup"><span data-stu-id="0cd46-148">The Application ID of the ServicePrincipal</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: SPN, ServicePrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cd46-149">-Feltétel</span><span class="sxs-lookup"><span data-stu-id="0cd46-149">-Condition</span></span>
<span data-ttu-id="0cd46-150">A Szerepkör-hozzárendelésre alkalmazandó feltétel.</span><span class="sxs-lookup"><span data-stu-id="0cd46-150">Condition to be applied to the RoleAssignment.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cd46-151">-ConditionVersion</span><span class="sxs-lookup"><span data-stu-id="0cd46-151">-ConditionVersion</span></span>
<span data-ttu-id="0cd46-152">A feltétel verziója.</span><span class="sxs-lookup"><span data-stu-id="0cd46-152">Version of the condition.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cd46-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cd46-153">-DefaultProfile</span></span>
<span data-ttu-id="0cd46-154">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0cd46-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0cd46-155">-Leírás</span><span class="sxs-lookup"><span data-stu-id="0cd46-155">-Description</span></span>
<span data-ttu-id="0cd46-156">A szerepkör-hozzárendelés rövid leírása.</span><span class="sxs-lookup"><span data-stu-id="0cd46-156">Brief description of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cd46-157">-InputFile</span><span class="sxs-lookup"><span data-stu-id="0cd46-157">-InputFile</span></span>
<span data-ttu-id="0cd46-158">Path to role assignment json</span><span class="sxs-lookup"><span data-stu-id="0cd46-158">Path to role assignment json</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cd46-159">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="0cd46-159">-ObjectId</span></span>
<span data-ttu-id="0cd46-160">A felhasználó, csoport vagy szolgáltatásnév Azure AD-objektumazonosítója.</span><span class="sxs-lookup"><span data-stu-id="0cd46-160">Azure AD Objectid of the user, group or service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cd46-161">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="0cd46-161">-ParentResource</span></span>
<span data-ttu-id="0cd46-162">A szülőerőforrás a hierarchiában (a ResourceName paraméterrel megadott erőforrásnál).</span><span class="sxs-lookup"><span data-stu-id="0cd46-162">The parent resource in the hierarchy(of the resource specified using ResourceName parameter).</span></span>
<span data-ttu-id="0cd46-163">Az erőforrást azonosító relatív URI azonosítók formájában hierarchikus hatókört csak a ResourceGroupName, az ResourceType és az ResourceName paraméterrel együtt kell használni.</span><span class="sxs-lookup"><span data-stu-id="0cd46-163">Should only be  used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="0cd46-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cd46-164">-ResourceGroupName</span></span>
<span data-ttu-id="0cd46-165">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0cd46-165">The resource group name.</span></span>
<span data-ttu-id="0cd46-166">Létrehoz egy hozzárendelést, amely a megadott erőforráscsoportban hatékony.</span><span class="sxs-lookup"><span data-stu-id="0cd46-166">Creates an assignment that is effective at the specified resource group.</span></span>
<span data-ttu-id="0cd46-167">Ha a ResourceName, a ResourceType és a ParentResource paraméterrel együtt használja, a parancs hierarchikus hatókört épít fel egy erőforrást azonosító relatív URI-val.</span><span class="sxs-lookup"><span data-stu-id="0cd46-167">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cd46-168">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0cd46-168">-ResourceName</span></span>
<span data-ttu-id="0cd46-169">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="0cd46-169">The resource name.</span></span>
<span data-ttu-id="0cd46-170">Például: storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="0cd46-170">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="0cd46-171">Csak az ResourceGroupName, az ResourceType és (opcionális) ParentResource paraméterekkel együtt használva építsen hierarchikus hatókört egy erőforrást azonosító relatív URI-ként.</span><span class="sxs-lookup"><span data-stu-id="0cd46-171">Should only be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a  relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="0cd46-172">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="0cd46-172">-ResourceType</span></span>
<span data-ttu-id="0cd46-173">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="0cd46-173">The resource type.</span></span>
<span data-ttu-id="0cd46-174">Például: Microsoft.Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="0cd46-174">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="0cd46-175">Csak a ResourceGroupName, az ResourceName és (opcionális)ParentResource paraméterekkel együtt használva építsen hierarchikus hatókört egy erőforrást azonosító relatív URI-ként.</span><span class="sxs-lookup"><span data-stu-id="0cd46-175">Should only be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in  the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="0cd46-176">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="0cd46-176">-RoleDefinitionId</span></span>
<span data-ttu-id="0cd46-177">Annak az RBAC-szerepkörnek az azonosítója, amely a taghoz van rendelve.</span><span class="sxs-lookup"><span data-stu-id="0cd46-177">Id of the RBAC role that needs to be assigned to the principal.</span></span>

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

### <span data-ttu-id="0cd46-178">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="0cd46-178">-RoleDefinitionName</span></span>
<span data-ttu-id="0cd46-179">Annak az RBAC-szerepkörnek a neve, amely a fő felhasználóhoz (olvasó, közreműködő, virtuális hálózati rendszergazda stb.) van hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="0cd46-179">Name of the RBAC role that needs to be assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cd46-180">-Scope</span><span class="sxs-lookup"><span data-stu-id="0cd46-180">-Scope</span></span>
<span data-ttu-id="0cd46-181">A szerepkör-hozzárendelés hatóköre.</span><span class="sxs-lookup"><span data-stu-id="0cd46-181">The Scope of the role assignment.</span></span>
<span data-ttu-id="0cd46-182">Relatív URI formátumban.</span><span class="sxs-lookup"><span data-stu-id="0cd46-182">In the format of relative URI.</span></span>
<span data-ttu-id="0cd46-183">Például: "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="0cd46-183">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="0cd46-184">Ha nincs megadva, előfizetési szinten hozza létre a szerepkör-hozzárendelést.</span><span class="sxs-lookup"><span data-stu-id="0cd46-184">If not specified, will create the role assignment at subscription level.</span></span>
<span data-ttu-id="0cd46-185">Ha meg van adva, akkor a következővel kell kezdődni: "/subscriptions/{id}".</span><span class="sxs-lookup"><span data-stu-id="0cd46-185">If specified, it should start with "/subscriptions/{id}".</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cd46-186">-SignInName</span><span class="sxs-lookup"><span data-stu-id="0cd46-186">-SignInName</span></span>
<span data-ttu-id="0cd46-187">A felhasználó e-mail-címe vagy egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="0cd46-187">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cd46-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cd46-188">CommonParameters</span></span>
<span data-ttu-id="0cd46-189">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cd46-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cd46-190">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0cd46-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cd46-191">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0cd46-191">INPUTS</span></span>

### <span data-ttu-id="0cd46-192">System.String</span><span class="sxs-lookup"><span data-stu-id="0cd46-192">System.String</span></span>

### <span data-ttu-id="0cd46-193">System.Guid</span><span class="sxs-lookup"><span data-stu-id="0cd46-193">System.Guid</span></span>

## <span data-ttu-id="0cd46-194">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0cd46-194">OUTPUTS</span></span>

### <span data-ttu-id="0cd46-195">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="0cd46-195">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="0cd46-196">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0cd46-196">NOTES</span></span>
<span data-ttu-id="0cd46-197">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, telepítés</span><span class="sxs-lookup"><span data-stu-id="0cd46-197">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="0cd46-198">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0cd46-198">RELATED LINKS</span></span>

[<span data-ttu-id="0cd46-199">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="0cd46-199">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="0cd46-200">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="0cd46-200">Remove-AzRoleAssignment</span></span>](./Remove-AzRoleAssignment.md)

[<span data-ttu-id="0cd46-201">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="0cd46-201">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)
