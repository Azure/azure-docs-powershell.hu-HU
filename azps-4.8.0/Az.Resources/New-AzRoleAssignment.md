---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E460D108-2BF9-4F57-AF3D-13868DC73EA0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleAssignment.md
ms.openlocfilehash: 2ec39bc66b3b027cb7b5ef9dda09734f8aaf457a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180966"
---
# <span data-ttu-id="6ffd0-101">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="6ffd0-101">New-AzRoleAssignment</span></span>

## <span data-ttu-id="6ffd0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6ffd0-102">SYNOPSIS</span></span>
<span data-ttu-id="6ffd0-103">A megadott RBAC szerepkör hozzárendelése a megadott hatókörhöz.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="6ffd0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6ffd0-104">SYNTAX</span></span>

### <span data-ttu-id="6ffd0-105">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6ffd0-105">EmptyParameterSet (Default)</span></span>
```
New-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ffd0-106">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ffd0-106">ResourceGroupWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ffd0-107">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ffd0-107">ResourceWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ffd0-108">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ffd0-108">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -Scope <String> [-Description <String>] [-Condition <String>]
 [-ConditionVersion <String>] -RoleDefinitionId <Guid> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ffd0-109">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ffd0-109">ResourceGroupWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ffd0-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ffd0-110">ResourceWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ffd0-111">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ffd0-111">ScopeWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ffd0-112">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ffd0-112">ResourceGroupWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ffd0-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ffd0-113">ResourceWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ffd0-114">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ffd0-114">ScopeWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> [-Scope <String>] -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ffd0-115">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ffd0-115">InputFileParameterSet</span></span>
```
New-AzRoleAssignment -InputFile <String> [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6ffd0-116">Leírás</span><span class="sxs-lookup"><span data-stu-id="6ffd0-116">DESCRIPTION</span></span>
<span data-ttu-id="6ffd0-117">A New-AzRoleAssignment parancs segítségével adjon meg hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-117">Use the New-AzRoleAssignment command to grant access.</span></span>
<span data-ttu-id="6ffd0-118">A hozzáférést úgy érheti el, hogy a megfelelő RBAC szerepkört rendeli hozzájuk a megfelelő hatókörben.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-118">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="6ffd0-119">Ha hozzáférést szeretne adni a teljes előfizetéshez, társítson egy szerepkört az előfizetési tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-119">To grant access to the entire subscription, assign a role at the subscription scope.</span></span>
<span data-ttu-id="6ffd0-120">Ha egy előfizetésben egy adott erőforráscsoport számára szeretne hozzáférést adni, társítson egy szerepkört az erőforráscsoport hatóköréhez.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-120">To grant access to a specific resource group within a subscription, assign a role at the resource group scope.</span></span>
<span data-ttu-id="6ffd0-121">A feladat tárgyát meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-121">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="6ffd0-122">A felhasználók megadásához használja a SignInName vagy az Azure AD ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-122">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="6ffd0-123">Ha meg szeretne adni egy biztonsági csoportot, használja az Azure AD ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-123">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="6ffd0-124">Az Azure AD-alkalmazások megadásához használja a ApplicationId vagy a ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-124">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="6ffd0-125">A hozzárendelt szerepkört a RoleDefinitionName paraméterrel kell megadni.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-125">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="6ffd0-126">Az Access által megadott hatókört meg lehet adni.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-126">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="6ffd0-127">Az alapértelmezett érték a kijelölt előfizetéshez tartozik.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-127">It defaults to the selected subscription.</span></span> <span data-ttu-id="6ffd0-128">A hozzárendelés hatóköre az a következő paraméter-kombinációk egyikével határozható meg.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-128">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="6ffd0-129">Hatókör – ez a teljes mértékben minősített hatókör a/Subscriptions/b karakterrel kezdődően \<subscriptionId\> .</span><span class="sxs-lookup"><span data-stu-id="6ffd0-129">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="6ffd0-130">ResourceGroupName – hozzáférést biztosít a megadott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-130">ResourceGroupName - to grant access to the specified resource group.</span></span>
<span data-ttu-id="6ffd0-131">c.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-131">c.</span></span>
<span data-ttu-id="6ffd0-132">ResourceName, ResourceType, ResourceGroupName és (opcionálisan) ParentResource – a hozzáférés engedélyezéséhez egy erőforráscsoport egy adott erőforrását adja meg.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-132">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - to specify a particular resource within a resource group to grant access to.</span></span>

## <span data-ttu-id="6ffd0-133">Példák</span><span class="sxs-lookup"><span data-stu-id="6ffd0-133">EXAMPLES</span></span>

### <span data-ttu-id="6ffd0-134">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6ffd0-134">Example 1</span></span>
```
PS C:\> New-AzRoleAssignment -ResourceGroupName rg1 -SignInName allen.young@live.com -RoleDefinitionName Reader -AllowDelegation
```

<span data-ttu-id="6ffd0-135">Hozzáférés megadása a felhasználóhoz egy erőforráscsoport-hatókörben, ahol a szerepkör-hozzárendelés elérhető a delegáláshoz</span><span class="sxs-lookup"><span data-stu-id="6ffd0-135">Grant Reader role access to a user at a resource group scope with the Role Assignment being available for delegation</span></span>

### <span data-ttu-id="6ffd0-136">2. példa</span><span class="sxs-lookup"><span data-stu-id="6ffd0-136">Example 2</span></span>
```
PS C:\> Get-AzADGroup -SearchString "Christine Koch Team"

          DisplayName                    Type                           Id
          -----------                    ----                           --------
          Christine Koch Team                                           2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb

PS C:\> New-AzRoleAssignment -ObjectId 2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb -RoleDefinitionName Contributor  -ResourceGroupName rg1
```

<span data-ttu-id="6ffd0-137">Hozzáférés megadása egy biztonsági csoporthoz</span><span class="sxs-lookup"><span data-stu-id="6ffd0-137">Grant access to a security group</span></span>

### <span data-ttu-id="6ffd0-138">3. példa</span><span class="sxs-lookup"><span data-stu-id="6ffd0-138">Example 3</span></span>
```
PS C:\> New-AzRoleAssignment -SignInName john.doe@contoso.com -RoleDefinitionName Owner -Scope "/subscriptions/86f81fc3-b00f-48cd-8218-3879f51ff362/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="6ffd0-139">Hozzáférés megadása egy erőforrás felhasználójának (webhely)</span><span class="sxs-lookup"><span data-stu-id="6ffd0-139">Grant access to a user at a resource (website)</span></span>

### <span data-ttu-id="6ffd0-140">4. példa</span><span class="sxs-lookup"><span data-stu-id="6ffd0-140">Example 4</span></span>
```
PS C:\> New-AzRoleAssignment -ObjectId 5ac84765-1c8c-4994-94b2-629461bd191b -RoleDefinitionName "Virtual Machine Contributor" -ResourceName Devices-Engineering-ProjectRND -ResourceType Microsoft.Network/virtualNetworks/subnets -ParentResource virtualNetworks/VNET-EASTUS-01 -ResourceGroupName Network
```

<span data-ttu-id="6ffd0-141">Hozzáférés biztosítása csoporthoz egy beágyazott erőforrásnál (alhálózat)</span><span class="sxs-lookup"><span data-stu-id="6ffd0-141">Grant access to a group at a nested resource (subnet)</span></span>

### <span data-ttu-id="6ffd0-142">Példa 5</span><span class="sxs-lookup"><span data-stu-id="6ffd0-142">Example 5</span></span>
```
PS C:\> $servicePrincipal = New-AzADServicePrincipal -DisplayName "testServiceprincipal"
PS C:\> New-AzRoleAssignment -RoleDefinitionName "Reader" -ApplicationId $servicePrincipal.ApplicationId
```

<span data-ttu-id="6ffd0-143">Képernyőolvasó-hozzáférés biztosítása egy egyszerű szolgáltatóhoz</span><span class="sxs-lookup"><span data-stu-id="6ffd0-143">Grant reader access to a service principal</span></span>

## <span data-ttu-id="6ffd0-144">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6ffd0-144">PARAMETERS</span></span>

### <span data-ttu-id="6ffd0-145">-AllowDelegation</span><span class="sxs-lookup"><span data-stu-id="6ffd0-145">-AllowDelegation</span></span>
<span data-ttu-id="6ffd0-146">A meghatalmazási jelölő a szerepkör-hozzárendelés létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="6ffd0-146">The delegation flag while creating a Role assignment.</span></span>

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

### <span data-ttu-id="6ffd0-147">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="6ffd0-147">-ApplicationId</span></span>
<span data-ttu-id="6ffd0-148">A ServicePrincipal alkalmazás azonosítója</span><span class="sxs-lookup"><span data-stu-id="6ffd0-148">The Application ID of the ServicePrincipal</span></span>

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

### <span data-ttu-id="6ffd0-149">-Feltétel</span><span class="sxs-lookup"><span data-stu-id="6ffd0-149">-Condition</span></span>
<span data-ttu-id="6ffd0-150">A RoleAssignment alkalmazandó feltétel.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-150">Condition to be applied to the RoleAssignment.</span></span>

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

### <span data-ttu-id="6ffd0-151">-ConditionVersion</span><span class="sxs-lookup"><span data-stu-id="6ffd0-151">-ConditionVersion</span></span>
<span data-ttu-id="6ffd0-152">A feltétel verziója.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-152">Version of the condition.</span></span>

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

### <span data-ttu-id="6ffd0-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ffd0-153">-DefaultProfile</span></span>
<span data-ttu-id="6ffd0-154">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6ffd0-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ffd0-155">-Leírás</span><span class="sxs-lookup"><span data-stu-id="6ffd0-155">-Description</span></span>
<span data-ttu-id="6ffd0-156">A szerepkör-hozzárendelés rövid leírása.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-156">Brief description of the role assignment.</span></span>

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

### <span data-ttu-id="6ffd0-157">-InputFile</span><span class="sxs-lookup"><span data-stu-id="6ffd0-157">-InputFile</span></span>
<span data-ttu-id="6ffd0-158">Elérési út a szerepkör-hozzárendeléshez JSON</span><span class="sxs-lookup"><span data-stu-id="6ffd0-158">Path to role assignment json</span></span>

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

### <span data-ttu-id="6ffd0-159">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="6ffd0-159">-ObjectId</span></span>
<span data-ttu-id="6ffd0-160">Azure AD ObjectId a felhasználó, csoport vagy szolgáltatás megbízójának.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-160">Azure AD Objectid of the user, group or service principal.</span></span>

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

### <span data-ttu-id="6ffd0-161">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="6ffd0-161">-ParentResource</span></span>
<span data-ttu-id="6ffd0-162">A fölérendelt erőforrás a hierarchiában (az ResourceName paraméterrel megadott erőforrás).</span><span class="sxs-lookup"><span data-stu-id="6ffd0-162">The parent resource in the hierarchy(of the resource specified using ResourceName parameter).</span></span>
<span data-ttu-id="6ffd0-163">Csak a ResourceGroupName, az ResourceType és a ResourceName paraméterrel együtt kell használni az erőforrást azonosító relatív URI-azonosítók formájában.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-163">Should only be  used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="6ffd0-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ffd0-164">-ResourceGroupName</span></span>
<span data-ttu-id="6ffd0-165">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-165">The resource group name.</span></span>
<span data-ttu-id="6ffd0-166">A megadott erőforráscsoport számára hatékony feladatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-166">Creates an assignment that is effective at the specified resource group.</span></span>
<span data-ttu-id="6ffd0-167">Ha a ResourceName, az ResourceType és (opcionálisan) ParentResource-paraméterekkel együtt használja, a parancs hierarchikus hatókört hoz létre egy erőforrást azonosító relatív URI-azonosítók formájában.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-167">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="6ffd0-168">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="6ffd0-168">-ResourceName</span></span>
<span data-ttu-id="6ffd0-169">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-169">The resource name.</span></span>
<span data-ttu-id="6ffd0-170">Például storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-170">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="6ffd0-171">Csak a ResourceGroupName, az ResourceType és (opcionálisan) ParentResource-paraméterekkel együtt kell használni, hogy egy erőforrást azonosító relatív URI formájában hozzon létre hierarchikus hatókört.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-171">Should only be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a  relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="6ffd0-172">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="6ffd0-172">-ResourceType</span></span>
<span data-ttu-id="6ffd0-173">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-173">The resource type.</span></span>
<span data-ttu-id="6ffd0-174">Például Microsoft. hálózat/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-174">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="6ffd0-175">Csak a ResourceGroupName, az ResourceName és (opcionálisan) ParentResource-paraméterekkel együtt kell használni, hogy egy erőforrást azonosító relatív URI formájában hozzon létre hierarchikus hatókört.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-175">Should only be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in  the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="6ffd0-176">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="6ffd0-176">-RoleDefinitionId</span></span>
<span data-ttu-id="6ffd0-177">Annak a RBAC-szerepkörnek az azonosítója, amelyet hozzá kell rendelni a megbízóhoz.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-177">Id of the RBAC role that needs to be assigned to the principal.</span></span>

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

### <span data-ttu-id="6ffd0-178">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="6ffd0-178">-RoleDefinitionName</span></span>
<span data-ttu-id="6ffd0-179">Annak a RBAC szerepkörnek a neve, amelyet ki kell osztani a megbízóhoz (például olvasó, közreműködő, virtuális hálózati rendszergazda stb.).</span><span class="sxs-lookup"><span data-stu-id="6ffd0-179">Name of the RBAC role that needs to be assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

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

### <span data-ttu-id="6ffd0-180">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="6ffd0-180">-Scope</span></span>
<span data-ttu-id="6ffd0-181">A szerepkör-hozzárendelés hatóköre.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-181">The Scope of the role assignment.</span></span>
<span data-ttu-id="6ffd0-182">A relatív URI formátuma.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-182">In the format of relative URI.</span></span>
<span data-ttu-id="6ffd0-183">Például "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="6ffd0-183">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="6ffd0-184">Ha nem adja meg, hozza létre a szerepkör-hozzárendelést az előfizetési szinten.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-184">If not specified, will create the role assignment at subscription level.</span></span>
<span data-ttu-id="6ffd0-185">Ha meg van adva, akkor a "/Subscriptions/{id}" szöveggel kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-185">If specified, it should start with "/subscriptions/{id}".</span></span>

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

### <span data-ttu-id="6ffd0-186">-SignInName</span><span class="sxs-lookup"><span data-stu-id="6ffd0-186">-SignInName</span></span>
<span data-ttu-id="6ffd0-187">Az e-mail-cím vagy a felhasználó egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-187">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="6ffd0-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ffd0-188">CommonParameters</span></span>
<span data-ttu-id="6ffd0-189">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6ffd0-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ffd0-190">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6ffd0-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ffd0-191">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ffd0-191">INPUTS</span></span>

### <span data-ttu-id="6ffd0-192">System. String</span><span class="sxs-lookup"><span data-stu-id="6ffd0-192">System.String</span></span>

### <span data-ttu-id="6ffd0-193">System. GUID</span><span class="sxs-lookup"><span data-stu-id="6ffd0-193">System.Guid</span></span>

## <span data-ttu-id="6ffd0-194">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ffd0-194">OUTPUTS</span></span>

### <span data-ttu-id="6ffd0-195">Microsoft. Azure. Command. Resources. modellek. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="6ffd0-195">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="6ffd0-196">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6ffd0-196">NOTES</span></span>
<span data-ttu-id="6ffd0-197">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="6ffd0-197">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="6ffd0-198">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6ffd0-198">RELATED LINKS</span></span>

[<span data-ttu-id="6ffd0-199">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="6ffd0-199">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="6ffd0-200">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="6ffd0-200">Remove-AzRoleAssignment</span></span>](./Remove-AzRoleAssignment.md)

[<span data-ttu-id="6ffd0-201">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="6ffd0-201">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)
