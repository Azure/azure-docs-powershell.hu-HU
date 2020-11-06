---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E460D108-2BF9-4F57-AF3D-13868DC73EA0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleAssignment.md
ms.openlocfilehash: 130f2ff4c65f282ca03f775500400479d16cc79c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493954"
---
# <span data-ttu-id="47b4b-101">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="47b4b-101">New-AzureRmRoleAssignment</span></span>

## <span data-ttu-id="47b4b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="47b4b-102">SYNOPSIS</span></span>
<span data-ttu-id="47b4b-103">A megadott RBAC szerepkör hozzárendelése a megadott hatókörhöz.</span><span class="sxs-lookup"><span data-stu-id="47b4b-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47b4b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="47b4b-104">SYNTAX</span></span>

### <span data-ttu-id="47b4b-105">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="47b4b-105">EmptyParameterSet (Default)</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -Scope <String> -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47b4b-106">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47b4b-106">ResourceGroupWithObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47b4b-107">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47b4b-107">ResourceWithObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47b4b-108">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47b4b-108">ScopeWithObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47b4b-109">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47b4b-109">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -Scope <String> -RoleDefinitionId <Guid> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47b4b-110">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="47b4b-110">ResourceGroupWithSignInNameParameterSet</span></span>
```
New-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47b4b-111">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="47b4b-111">ResourceWithSignInNameParameterSet</span></span>
```
New-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47b4b-112">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="47b4b-112">ScopeWithSignInNameParameterSet</span></span>
```
New-AzureRmRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47b4b-113">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="47b4b-113">ResourceGroupWithSPNParameterSet</span></span>
```
New-AzureRmRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47b4b-114">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="47b4b-114">ResourceWithSPNParameterSet</span></span>
```
New-AzureRmRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47b4b-115">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="47b4b-115">ScopeWithSPNParameterSet</span></span>
```
New-AzureRmRoleAssignment -ApplicationId <String> [-Scope <String>] -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47b4b-116">Leírás</span><span class="sxs-lookup"><span data-stu-id="47b4b-116">DESCRIPTION</span></span>
<span data-ttu-id="47b4b-117">A New-AzureRMRoleAssignment parancs segítségével adjon meg hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="47b4b-117">Use the New-AzureRMRoleAssignment command to grant access.</span></span>
<span data-ttu-id="47b4b-118">A hozzáférést úgy érheti el, hogy a megfelelő RBAC szerepkört rendeli hozzájuk a megfelelő hatókörben.</span><span class="sxs-lookup"><span data-stu-id="47b4b-118">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="47b4b-119">Ha hozzáférést szeretne adni a teljes előfizetéshez, társítson egy szerepkört az előfizetési tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="47b4b-119">To grant access to the entire subscription, assign a role at the subscription scope.</span></span>
<span data-ttu-id="47b4b-120">Ha egy előfizetésben egy adott erőforráscsoport számára szeretne hozzáférést adni, társítson egy szerepkört az erőforráscsoport hatóköréhez.</span><span class="sxs-lookup"><span data-stu-id="47b4b-120">To grant access to a specific resource group within a subscription, assign a role at the resource group scope.</span></span>
<span data-ttu-id="47b4b-121">A feladat tárgyát meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="47b4b-121">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="47b4b-122">A felhasználók megadásához használja a SignInName vagy az Azure AD ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="47b4b-122">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="47b4b-123">Ha meg szeretne adni egy biztonsági csoportot, használja az Azure AD ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="47b4b-123">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="47b4b-124">Az Azure AD-alkalmazások megadásához használja a ApplicationId vagy a ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="47b4b-124">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="47b4b-125">A hozzárendelt szerepkört a RoleDefinitionName paraméterrel kell megadni.</span><span class="sxs-lookup"><span data-stu-id="47b4b-125">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="47b4b-126">Az Access által megadott hatókört meg lehet adni.</span><span class="sxs-lookup"><span data-stu-id="47b4b-126">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="47b4b-127">Az alapértelmezett érték a kijelölt előfizetéshez tartozik.</span><span class="sxs-lookup"><span data-stu-id="47b4b-127">It defaults to the selected subscription.</span></span> <span data-ttu-id="47b4b-128">A hozzárendelés hatóköre az a következő paraméter-kombinációk egyikével határozható meg.</span><span class="sxs-lookup"><span data-stu-id="47b4b-128">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="47b4b-129">Hatókör – ez a teljes mértékben minősített hatókör a/Subscriptions/b karakterrel kezdődően \<subscriptionId\> .</span><span class="sxs-lookup"><span data-stu-id="47b4b-129">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="47b4b-130">ResourceGroupName – hozzáférést biztosít a megadott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="47b4b-130">ResourceGroupName - to grant access to the specified resource group.</span></span>
<span data-ttu-id="47b4b-131">c.</span><span class="sxs-lookup"><span data-stu-id="47b4b-131">c.</span></span>
<span data-ttu-id="47b4b-132">ResourceName, ResourceType, ResourceGroupName és (opcionálisan) ParentResource – a hozzáférés engedélyezéséhez egy erőforráscsoport egy adott erőforrását adja meg.</span><span class="sxs-lookup"><span data-stu-id="47b4b-132">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - to specify a particular resource within a resource group to grant access to.</span></span>

## <span data-ttu-id="47b4b-133">Példák</span><span class="sxs-lookup"><span data-stu-id="47b4b-133">EXAMPLES</span></span>

### <span data-ttu-id="47b4b-134">Példa 1</span><span class="sxs-lookup"><span data-stu-id="47b4b-134">Example 1</span></span>
```
PS C:\> New-AzureRmRoleAssignment -ResourceGroupName rg1 -SignInName allen.young@live.com -RoleDefinitionName Reader -AllowDelegation
```

<span data-ttu-id="47b4b-135">Hozzáférés megadása a felhasználóhoz egy erőforráscsoport-hatókörben, ahol a szerepkör-hozzárendelés elérhető a delegáláshoz</span><span class="sxs-lookup"><span data-stu-id="47b4b-135">Grant Reader role access to a user at a resource group scope with the Role Assignment being available for delegation</span></span>

### <span data-ttu-id="47b4b-136">2. példa</span><span class="sxs-lookup"><span data-stu-id="47b4b-136">Example 2</span></span>
```
PS C:\> Get-AzureRMADGroup -SearchString "Christine Koch Team"

          DisplayName                    Type                           Id
          -----------                    ----                           --------
          Christine Koch Team                                           2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb

PS C:\> New-AzureRmRoleAssignment -ObjectId 2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb -RoleDefinitionName Contributor  -ResourceGroupName rg1
```

<span data-ttu-id="47b4b-137">Hozzáférés megadása egy biztonsági csoporthoz</span><span class="sxs-lookup"><span data-stu-id="47b4b-137">Grant access to a security group</span></span>

### <span data-ttu-id="47b4b-138">3. példa</span><span class="sxs-lookup"><span data-stu-id="47b4b-138">Example 3</span></span>
```
PS C:\> New-AzureRmRoleAssignment -SignInName john.doe@contoso.com -RoleDefinitionName Owner -Scope "/subscriptions/86f81fc3-b00f-48cd-8218-3879f51ff362/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="47b4b-139">Hozzáférés megadása egy erőforrás felhasználójának (webhely)</span><span class="sxs-lookup"><span data-stu-id="47b4b-139">Grant access to a user at a resource (website)</span></span>

### <span data-ttu-id="47b4b-140">4. példa</span><span class="sxs-lookup"><span data-stu-id="47b4b-140">Example 4</span></span>
```
PS C:\> New-AzureRMRoleAssignment -ObjectId 5ac84765-1c8c-4994-94b2-629461bd191b -RoleDefinitionName "Virtual Machine Contributor" -ResourceName Devices-Engineering-ProjectRND -ResourceType Microsoft.Network/virtualNetworks/subnets -ParentResource virtualNetworks/VNET-EASTUS-01 -ResourceGroupName Network
```

<span data-ttu-id="47b4b-141">Hozzáférés biztosítása csoporthoz egy beágyazott erőforrásnál (alhálózat)</span><span class="sxs-lookup"><span data-stu-id="47b4b-141">Grant access to a group at a nested resource (subnet)</span></span>

### <span data-ttu-id="47b4b-142">Példa 5</span><span class="sxs-lookup"><span data-stu-id="47b4b-142">Example 5</span></span>
```
PS C:\> $servicePrincipal = New-AzureRmADServicePrincipal -DisplayName "testServiceprincipal"
PS C:\> New-AzureRmRoleAssignment -RoleDefinitionName "Reader" -ApplicationId $servicePrincipal.ApplicationId
```

<span data-ttu-id="47b4b-143">Képernyőolvasó-hozzáférés biztosítása egy egyszerű szolgáltatóhoz</span><span class="sxs-lookup"><span data-stu-id="47b4b-143">Grant reader access to a service principal</span></span>

## <span data-ttu-id="47b4b-144">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="47b4b-144">PARAMETERS</span></span>

### <span data-ttu-id="47b4b-145">-AllowDelegation</span><span class="sxs-lookup"><span data-stu-id="47b4b-145">-AllowDelegation</span></span>
<span data-ttu-id="47b4b-146">A meghatalmazási jelölő a szerepkör-hozzárendelés létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="47b4b-146">The delegation flag while creating a Role assignment.</span></span>

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

### <span data-ttu-id="47b4b-147">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="47b4b-147">-ApplicationId</span></span>
<span data-ttu-id="47b4b-148">A ServicePrincipal alkalmazás azonosítója</span><span class="sxs-lookup"><span data-stu-id="47b4b-148">The Application ID of the ServicePrincipal</span></span>

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

### <span data-ttu-id="47b4b-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47b4b-149">-DefaultProfile</span></span>
<span data-ttu-id="47b4b-150">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="47b4b-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47b4b-151">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="47b4b-151">-ObjectId</span></span>
<span data-ttu-id="47b4b-152">Azure AD ObjectId a felhasználó, csoport vagy szolgáltatás megbízójának.</span><span class="sxs-lookup"><span data-stu-id="47b4b-152">Azure AD Objectid of the user, group or service principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47b4b-153">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="47b4b-153">-ParentResource</span></span>
<span data-ttu-id="47b4b-154">A fölérendelt erőforrás a hierarchiában (az ResourceName paraméterrel megadott erőforrás).</span><span class="sxs-lookup"><span data-stu-id="47b4b-154">The parent resource in the hierarchy(of the resource specified using ResourceName parameter).</span></span>
<span data-ttu-id="47b4b-155">Csak a ResourceGroupName, az ResourceType és a ResourceName paraméterrel együtt kell használni az erőforrást azonosító relatív URI-azonosítók formájában.</span><span class="sxs-lookup"><span data-stu-id="47b4b-155">Should only be  used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="47b4b-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47b4b-156">-ResourceGroupName</span></span>
<span data-ttu-id="47b4b-157">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="47b4b-157">The resource group name.</span></span>
<span data-ttu-id="47b4b-158">A megadott erőforráscsoport számára hatékony feladatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="47b4b-158">Creates an assignment that is effective at the specified resource group.</span></span>
<span data-ttu-id="47b4b-159">Ha a ResourceName, az ResourceType és (opcionálisan) ParentResource-paraméterekkel együtt használja, a parancs hierarchikus hatókört hoz létre egy erőforrást azonosító relatív URI-azonosítók formájában.</span><span class="sxs-lookup"><span data-stu-id="47b4b-159">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="47b4b-160">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="47b4b-160">-ResourceName</span></span>
<span data-ttu-id="47b4b-161">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="47b4b-161">The resource name.</span></span>
<span data-ttu-id="47b4b-162">Például storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="47b4b-162">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="47b4b-163">Csak a ResourceGroupName, az ResourceType és (opcionálisan) ParentResource-paraméterekkel együtt kell használni, hogy egy erőforrást azonosító relatív URI formájában hozzon létre hierarchikus hatókört.</span><span class="sxs-lookup"><span data-stu-id="47b4b-163">Should only be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a  relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="47b4b-164">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="47b4b-164">-ResourceType</span></span>
<span data-ttu-id="47b4b-165">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="47b4b-165">The resource type.</span></span>
<span data-ttu-id="47b4b-166">Például Microsoft. hálózat/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="47b4b-166">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="47b4b-167">Csak a ResourceGroupName, az ResourceName és (opcionálisan) ParentResource-paraméterekkel együtt kell használni, hogy egy erőforrást azonosító relatív URI formájában hozzon létre hierarchikus hatókört.</span><span class="sxs-lookup"><span data-stu-id="47b4b-167">Should only be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in  the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="47b4b-168">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="47b4b-168">-RoleDefinitionId</span></span>
<span data-ttu-id="47b4b-169">Annak a RBAC-szerepkörnek az azonosítója, amelyet hozzá kell rendelni a megbízóhoz.</span><span class="sxs-lookup"><span data-stu-id="47b4b-169">Id of the RBAC role that needs to be assigned to the principal.</span></span>

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

### <span data-ttu-id="47b4b-170">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="47b4b-170">-RoleDefinitionName</span></span>
<span data-ttu-id="47b4b-171">Annak a RBAC szerepkörnek a neve, amelyet ki kell osztani a megbízóhoz (például olvasó, közreműködő, virtuális hálózati rendszergazda stb.).</span><span class="sxs-lookup"><span data-stu-id="47b4b-171">Name of the RBAC role that needs to be assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47b4b-172">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="47b4b-172">-Scope</span></span>
<span data-ttu-id="47b4b-173">A szerepkör-hozzárendelés hatóköre.</span><span class="sxs-lookup"><span data-stu-id="47b4b-173">The Scope of the role assignment.</span></span>
<span data-ttu-id="47b4b-174">A relatív URI formátuma.</span><span class="sxs-lookup"><span data-stu-id="47b4b-174">In the format of relative URI.</span></span>
<span data-ttu-id="47b4b-175">Például "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="47b4b-175">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="47b4b-176">Ha nem adja meg, hozza létre a szerepkör-hozzárendelést az előfizetési szinten.</span><span class="sxs-lookup"><span data-stu-id="47b4b-176">If not specified, will create the role assignment at subscription level.</span></span>
<span data-ttu-id="47b4b-177">Ha meg van adva, akkor a "/Subscriptions/{id}" szöveggel kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="47b4b-177">If specified, it should start with "/subscriptions/{id}".</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ScopeWithObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47b4b-178">-SignInName</span><span class="sxs-lookup"><span data-stu-id="47b4b-178">-SignInName</span></span>
<span data-ttu-id="47b4b-179">Az e-mail-cím vagy a felhasználó egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="47b4b-179">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="47b4b-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47b4b-180">CommonParameters</span></span>
<span data-ttu-id="47b4b-181">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="47b4b-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47b4b-182">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47b4b-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47b4b-183">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="47b4b-183">INPUTS</span></span>

### <span data-ttu-id="47b4b-184">System. GUID</span><span class="sxs-lookup"><span data-stu-id="47b4b-184">System.Guid</span></span>

### <span data-ttu-id="47b4b-185">System. String</span><span class="sxs-lookup"><span data-stu-id="47b4b-185">System.String</span></span>

## <span data-ttu-id="47b4b-186">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47b4b-186">OUTPUTS</span></span>

### <span data-ttu-id="47b4b-187">Microsoft. Azure. Command. Resources. modellek. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="47b4b-187">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="47b4b-188">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="47b4b-188">NOTES</span></span>
<span data-ttu-id="47b4b-189">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="47b4b-189">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="47b4b-190">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47b4b-190">RELATED LINKS</span></span>

[<span data-ttu-id="47b4b-191">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="47b4b-191">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="47b4b-192">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="47b4b-192">Remove-AzureRmRoleAssignment</span></span>](./Remove-AzureRmRoleAssignment.md)

[<span data-ttu-id="47b4b-193">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="47b4b-193">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)
