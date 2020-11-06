---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E460D108-2BF9-4F57-AF3D-13868DC73EA0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleAssignment.md
ms.openlocfilehash: 746dc2c7665cf41dc8d70bf7b16f667c6e22ef89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494364"
---
# <span data-ttu-id="7be08-101">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="7be08-101">New-AzureRmRoleAssignment</span></span>

## <span data-ttu-id="7be08-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7be08-102">SYNOPSIS</span></span>
<span data-ttu-id="7be08-103">A megadott RBAC szerepkör hozzárendelése a megadott hatókörhöz.</span><span class="sxs-lookup"><span data-stu-id="7be08-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7be08-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7be08-104">SYNTAX</span></span>

### <span data-ttu-id="7be08-105">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7be08-105">EmptyParameterSet (Default)</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -Scope <String> -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7be08-106">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7be08-106">ResourceGroupWithObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7be08-107">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7be08-107">ResourceWithObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7be08-108">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7be08-108">ScopeWithObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7be08-109">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7be08-109">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -Scope <String> -RoleDefinitionId <Guid> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7be08-110">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7be08-110">ResourceGroupWithSignInNameParameterSet</span></span>
```
New-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7be08-111">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7be08-111">ResourceWithSignInNameParameterSet</span></span>
```
New-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7be08-112">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7be08-112">ScopeWithSignInNameParameterSet</span></span>
```
New-AzureRmRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7be08-113">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="7be08-113">ResourceGroupWithSPNParameterSet</span></span>
```
New-AzureRmRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7be08-114">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="7be08-114">ResourceWithSPNParameterSet</span></span>
```
New-AzureRmRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7be08-115">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="7be08-115">ScopeWithSPNParameterSet</span></span>
```
New-AzureRmRoleAssignment -ApplicationId <String> [-Scope <String>] -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7be08-116">Leírás</span><span class="sxs-lookup"><span data-stu-id="7be08-116">DESCRIPTION</span></span>
<span data-ttu-id="7be08-117">A New-AzureRMRoleAssignment parancs segítségével adjon meg hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="7be08-117">Use the New-AzureRMRoleAssignment command to grant access.</span></span>
<span data-ttu-id="7be08-118">A hozzáférést úgy érheti el, hogy a megfelelő RBAC szerepkört rendeli hozzájuk a megfelelő hatókörben.</span><span class="sxs-lookup"><span data-stu-id="7be08-118">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="7be08-119">Ha hozzáférést szeretne adni a teljes előfizetéshez, társítson egy szerepkört az előfizetési tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="7be08-119">To grant access to the entire subscription, assign a role at the subscription scope.</span></span>
<span data-ttu-id="7be08-120">Ha egy előfizetésben egy adott erőforráscsoport számára szeretne hozzáférést adni, társítson egy szerepkört az erőforráscsoport hatóköréhez.</span><span class="sxs-lookup"><span data-stu-id="7be08-120">To grant access to a specific resource group within a subscription, assign a role at the resource group scope.</span></span>

<span data-ttu-id="7be08-121">A feladat tárgyát meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="7be08-121">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="7be08-122">A felhasználók megadásához használja a SignInName vagy az Azure AD ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="7be08-122">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="7be08-123">Ha meg szeretne adni egy biztonsági csoportot, használja az Azure AD ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="7be08-123">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="7be08-124">Az Azure AD-alkalmazások megadásához használja a ApplicationId vagy a ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="7be08-124">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>

<span data-ttu-id="7be08-125">A hozzárendelt szerepkört a RoleDefinitionName paraméterrel kell megadni.</span><span class="sxs-lookup"><span data-stu-id="7be08-125">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>

<span data-ttu-id="7be08-126">Az Access által megadott hatókört meg lehet adni.</span><span class="sxs-lookup"><span data-stu-id="7be08-126">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="7be08-127">Az alapértelmezett érték a kijelölt előfizetéshez tartozik.</span><span class="sxs-lookup"><span data-stu-id="7be08-127">It defaults to the selected subscription.</span></span> <span data-ttu-id="7be08-128">A hozzárendelés hatóköre az a következő paraméter-kombinációk egyikével határozható meg.</span><span class="sxs-lookup"><span data-stu-id="7be08-128">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="7be08-129">Hatókör – ez a teljes mértékben minősített hatókör a/Subscriptions/b karakterrel kezdődően \<subscriptionId\> .</span><span class="sxs-lookup"><span data-stu-id="7be08-129">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="7be08-130">ResourceGroupName – hozzáférést biztosít a megadott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="7be08-130">ResourceGroupName - to grant access to the specified resource group.</span></span>
<span data-ttu-id="7be08-131">c.</span><span class="sxs-lookup"><span data-stu-id="7be08-131">c.</span></span>
<span data-ttu-id="7be08-132">ResourceName, ResourceType, ResourceGroupName és (opcionálisan) ParentResource – a hozzáférés engedélyezéséhez egy erőforráscsoport egy adott erőforrását adja meg.</span><span class="sxs-lookup"><span data-stu-id="7be08-132">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - to specify a particular resource within a resource group to grant access to.</span></span>

## <span data-ttu-id="7be08-133">Példák</span><span class="sxs-lookup"><span data-stu-id="7be08-133">EXAMPLES</span></span>

### <span data-ttu-id="7be08-134">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7be08-134">Example 1</span></span>
```
PS C:\> New-AzureRmRoleAssignment -ResourceGroupName rg1 -SignInName allen.young@live.com -RoleDefinitionName Reader -AllowDelegation
```

<span data-ttu-id="7be08-135">Hozzáférés megadása a felhasználóhoz egy erőforráscsoport-hatókörben, ahol a szerepkör-hozzárendelés elérhető a delegáláshoz</span><span class="sxs-lookup"><span data-stu-id="7be08-135">Grant Reader role access to a user at a resource group scope with the Role Assignment being available for delegation</span></span>

### <span data-ttu-id="7be08-136">2. példa</span><span class="sxs-lookup"><span data-stu-id="7be08-136">Example 2</span></span>
```
PS C:\> Get-AzureRMADGroup -SearchString "Christine Koch Team"

          DisplayName                    Type                           ObjectId
          -----------                    ----                           --------
          Christine Koch Team                                           2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb

PS C:\> New-AzureRmRoleAssignment -ObjectId 2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb -RoleDefinitionName Contributor  -ResourceGroupName rg1
```

<span data-ttu-id="7be08-137">Hozzáférés megadása egy biztonsági csoporthoz</span><span class="sxs-lookup"><span data-stu-id="7be08-137">Grant access to a security group</span></span>

### <span data-ttu-id="7be08-138">3. példa</span><span class="sxs-lookup"><span data-stu-id="7be08-138">Example 3</span></span>
```
PS C:\> New-AzureRmRoleAssignment -SignInName john.doe@contoso.com -RoleDefinitionName Owner -Scope "/subscriptions/86f81fc3-b00f-48cd-8218-3879f51ff362/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="7be08-139">Hozzáférés megadása egy erőforrás felhasználójának (webhely)</span><span class="sxs-lookup"><span data-stu-id="7be08-139">Grant access to a user at a resource (website)</span></span>

### <span data-ttu-id="7be08-140">4. példa</span><span class="sxs-lookup"><span data-stu-id="7be08-140">Example 4</span></span>
```
PS C:\> New-AzureRMRoleAssignment -ObjectId 5ac84765-1c8c-4994-94b2-629461bd191b -RoleDefinitionName "Virtual Machine Contributor" -ResourceName Devices-Engineering-ProjectRND -ResourceType Microsoft.Network/virtualNetworks/subnets -ParentResource virtualNetworks/VNET-EASTUS-01 -ResourceGroupName Network
```

<span data-ttu-id="7be08-141">Hozzáférés biztosítása csoporthoz egy beágyazott erőforrásnál (alhálózat)</span><span class="sxs-lookup"><span data-stu-id="7be08-141">Grant access to a group at a nested resource (subnet)</span></span>

### <span data-ttu-id="7be08-142">Példa 5</span><span class="sxs-lookup"><span data-stu-id="7be08-142">Example 5</span></span>
```
PS C:\> $servicePrincipal = New-AzureRmADServicePrincipal -DisplayName "testServiceprincipal"
PS C:\> New-AzureRmRoleAssignment -RoleDefinitionName "Reader" -ApplicationId $servicePrincipal.ApplicationId
```

<span data-ttu-id="7be08-143">Képernyőolvasó-hozzáférés biztosítása egy egyszerű szolgáltatóhoz</span><span class="sxs-lookup"><span data-stu-id="7be08-143">Grant reader access to a service principal</span></span>

## <span data-ttu-id="7be08-144">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7be08-144">PARAMETERS</span></span>

### <span data-ttu-id="7be08-145">-AllowDelegation</span><span class="sxs-lookup"><span data-stu-id="7be08-145">-AllowDelegation</span></span>
<span data-ttu-id="7be08-146">A meghatalmazási jelölő a szerepkör-hozzárendelés létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="7be08-146">The delegation flag while creating a Role assignment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be08-147">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7be08-147">-ApplicationId</span></span>
<span data-ttu-id="7be08-148">A ServicePrincipal alkalmazás azonosítója</span><span class="sxs-lookup"><span data-stu-id="7be08-148">The Application ID of the ServicePrincipal</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: SPN, ServicePrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7be08-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7be08-149">-DefaultProfile</span></span>
<span data-ttu-id="7be08-150">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7be08-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7be08-151">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7be08-151">-ObjectId</span></span>
<span data-ttu-id="7be08-152">Azure AD ObjectId a felhasználó, csoport vagy szolgáltatás megbízójának.</span><span class="sxs-lookup"><span data-stu-id="7be08-152">Azure AD Objectid of the user, group or service principal.</span></span>

```yaml
Type: Guid
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7be08-153">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="7be08-153">-ParentResource</span></span>
<span data-ttu-id="7be08-154">A fölérendelt erőforrás a hierarchiában (az ResourceName paraméterrel megadott erőforrás).</span><span class="sxs-lookup"><span data-stu-id="7be08-154">The parent resource in the hierarchy(of the resource specified using ResourceName parameter).</span></span>
<span data-ttu-id="7be08-155">Csak a ResourceGroupName, az ResourceType és a ResourceName paraméterrel együtt kell használni az erőforrást azonosító relatív URI-azonosítók formájában.</span><span class="sxs-lookup"><span data-stu-id="7be08-155">Should only be  used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

```yaml
Type: String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7be08-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7be08-156">-ResourceGroupName</span></span>
<span data-ttu-id="7be08-157">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="7be08-157">The resource group name.</span></span>
<span data-ttu-id="7be08-158">A megadott erőforráscsoport számára hatékony feladatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="7be08-158">Creates an assignment that is effective at the specified resource group.</span></span>
<span data-ttu-id="7be08-159">Ha a ResourceName, az ResourceType és (opcionálisan) ParentResource-paraméterekkel együtt használja, a parancs hierarchikus hatókört hoz létre egy erőforrást azonosító relatív URI-azonosítók formájában.</span><span class="sxs-lookup"><span data-stu-id="7be08-159">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7be08-160">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="7be08-160">-ResourceName</span></span>
<span data-ttu-id="7be08-161">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="7be08-161">The resource name.</span></span>
<span data-ttu-id="7be08-162">Például storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="7be08-162">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="7be08-163">Csak a ResourceGroupName, az ResourceType és (opcionálisan) ParentResource-paraméterekkel együtt kell használni, hogy egy erőforrást azonosító relatív URI formájában hozzon létre hierarchikus hatókört.</span><span class="sxs-lookup"><span data-stu-id="7be08-163">Should only be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a  relative URI that identifies a resource.</span></span>

```yaml
Type: String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7be08-164">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="7be08-164">-ResourceType</span></span>
<span data-ttu-id="7be08-165">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="7be08-165">The resource type.</span></span>
<span data-ttu-id="7be08-166">Például Microsoft. hálózat/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="7be08-166">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="7be08-167">Csak a ResourceGroupName, az ResourceName és (opcionálisan) ParentResource-paraméterekkel együtt kell használni, hogy egy erőforrást azonosító relatív URI formájában hozzon létre hierarchikus hatókört.</span><span class="sxs-lookup"><span data-stu-id="7be08-167">Should only be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in  the form of a relative URI that identifies a resource.</span></span>

```yaml
Type: String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7be08-168">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="7be08-168">-RoleDefinitionId</span></span>
<span data-ttu-id="7be08-169">Annak a RBAC-szerepkörnek az azonosítója, amelyet hozzá kell rendelni a megbízóhoz.</span><span class="sxs-lookup"><span data-stu-id="7be08-169">Id of the RBAC role that needs to be assigned to the principal.</span></span>

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

### <span data-ttu-id="7be08-170">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="7be08-170">-RoleDefinitionName</span></span>
<span data-ttu-id="7be08-171">Annak a RBAC szerepkörnek a neve, amelyet ki kell osztani a megbízóhoz (például olvasó, közreműködő, virtuális hálózati rendszergazda stb.).</span><span class="sxs-lookup"><span data-stu-id="7be08-171">Name of the RBAC role that needs to be assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7be08-172">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="7be08-172">-Scope</span></span>
<span data-ttu-id="7be08-173">A szerepkör-hozzárendelés hatóköre.</span><span class="sxs-lookup"><span data-stu-id="7be08-173">The Scope of the role assignment.</span></span>
<span data-ttu-id="7be08-174">A relatív URI formátuma.</span><span class="sxs-lookup"><span data-stu-id="7be08-174">In the format of relative URI.</span></span>
<span data-ttu-id="7be08-175">Például "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="7be08-175">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="7be08-176">Ha nem adja meg, hozza létre a szerepkör-hozzárendelést az előfizetési szinten.</span><span class="sxs-lookup"><span data-stu-id="7be08-176">If not specified, will create the role assignment at subscription level.</span></span>
<span data-ttu-id="7be08-177">Ha meg van adva, akkor a "/Subscriptions/{id}" szöveggel kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="7be08-177">If specified, it should start with "/subscriptions/{id}".</span></span>

```yaml
Type: String
Parameter Sets: EmptyParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ScopeWithObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7be08-178">-SignInName</span><span class="sxs-lookup"><span data-stu-id="7be08-178">-SignInName</span></span>
<span data-ttu-id="7be08-179">Az e-mail-cím vagy a felhasználó egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="7be08-179">The email address or the user principal name of the user.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7be08-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7be08-180">CommonParameters</span></span>
<span data-ttu-id="7be08-181">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7be08-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7be08-182">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7be08-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7be08-183">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7be08-183">INPUTS</span></span>

### <span data-ttu-id="7be08-184">Nincs</span><span class="sxs-lookup"><span data-stu-id="7be08-184">None</span></span>
<span data-ttu-id="7be08-185">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="7be08-185">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7be08-186">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7be08-186">OUTPUTS</span></span>

### <span data-ttu-id="7be08-187">Microsoft. Azure. Command. Resources. modellek. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="7be08-187">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="7be08-188">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7be08-188">NOTES</span></span>
<span data-ttu-id="7be08-189">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="7be08-189">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="7be08-190">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7be08-190">RELATED LINKS</span></span>

[<span data-ttu-id="7be08-191">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="7be08-191">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="7be08-192">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="7be08-192">Remove-AzureRmRoleAssignment</span></span>](./Remove-AzureRmRoleAssignment.md)

[<span data-ttu-id="7be08-193">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7be08-193">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)
