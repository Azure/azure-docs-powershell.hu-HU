---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: cd8bc24a0cedac91ef18e19a80e1662fdcbac297
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300971"
---
# <span data-ttu-id="1f567-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="1f567-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="1f567-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1f567-102">SYNOPSIS</span></span>
<span data-ttu-id="1f567-103">Házirend-készlet definíciójának módosítása</span><span class="sxs-lookup"><span data-stu-id="1f567-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="1f567-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1f567-104">SYNTAX</span></span>

### <span data-ttu-id="1f567-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1f567-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f567-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f567-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f567-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f567-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f567-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f567-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f567-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f567-109">InputObjectParameterSet</span></span>
```
Set-AzPolicySetDefinition [-DisplayName <String>] [-Description <String>] [-PolicyDefinition <String>]
 [-Metadata <String>] [-Parameter <String>] -InputObject <PsPolicySetDefinition> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f567-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="1f567-110">DESCRIPTION</span></span>
<span data-ttu-id="1f567-111">A **set-AzPolicySetDefinition** parancsmag módosította a házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="1f567-111">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="1f567-112">Példák</span><span class="sxs-lookup"><span data-stu-id="1f567-112">EXAMPLES</span></span>

### <span data-ttu-id="1f567-113">Példa 1: a házirend-készlet definíciójának frissítése</span><span class="sxs-lookup"><span data-stu-id="1f567-113">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="1f567-114">Az első parancs a Get-AzPolicySetDefinition parancsmag használatával kapja meg a házirend-készlet definícióját.</span><span class="sxs-lookup"><span data-stu-id="1f567-114">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="1f567-115">A parancs az objektumot a $PolicySetDefinition változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1f567-115">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="1f567-116">A második parancs frissíti az $PolicySetDefinition **ResourceId** tulajdonsága által azonosított házirend-definíció leírását.</span><span class="sxs-lookup"><span data-stu-id="1f567-116">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

### <span data-ttu-id="1f567-117">2. példa: egy házirend-definíciós definíció metaadatait frissíti</span><span class="sxs-lookup"><span data-stu-id="1f567-117">Example 2: Update the metadata of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -Metadata '{"category":"Virtual Machine"}'


Name                  : VMPolicySetDefinition
ResourceId            : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policySetDefinitions/VMPolicySetDefinition
ResourceName          : VMPolicySetDefinition
ResourceType          : Microsoft.Authorization/policySetDefinitions
SubscriptionId        : 11111111-1111-1111-1111-111111111111
Properties            : @{displayName=VMPolicySetDefinition; policyType=Custom; metadata=; parameters=; policyDefinitions=System.Object[]}
PolicySetDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policySetDefinitions/VMPolicySetDefinition
```

<span data-ttu-id="1f567-118">Ez a parancs frissíti a VMPolicySetDefinition nevű, a "virtuális gép" kategóriát tartalmazó irányelvmodul-definíció metaadatait.</span><span class="sxs-lookup"><span data-stu-id="1f567-118">This command updates the metadata of a policy set definition named VMPolicySetDefinition to indicate its category is "Virtual Machine".</span></span>

### <span data-ttu-id="1f567-119">3. példa: a set Policy set definition groups frissítése</span><span class="sxs-lookup"><span data-stu-id="1f567-119">Example 3: Update the groups of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition '[{ "name": "group1", "displayName": "Virtual Machine Security" }, { "name": "group2" }]'
```

<span data-ttu-id="1f567-120">Ez a parancs frissíti a VMPolicySetDefinition nevű irányelvmodul-definíciós csoportokat.</span><span class="sxs-lookup"><span data-stu-id="1f567-120">This command updates the groups of a policy set definition named VMPolicySetDefinition.</span></span>

### <span data-ttu-id="1f567-121">Példa 4: a házirendprofil-definíciók csoportjának frissítése kivonatoló táblázat használatával</span><span class="sxs-lookup"><span data-stu-id="1f567-121">Example 4: Update the groups of a policy set definition using a hash table</span></span>
```
$groupsJson = ConvertTo-Json @{ name = "group1", displayName = "Virtual Machine Security" }, @{ name = "group2" }
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition $groupsJson
```

<span data-ttu-id="1f567-122">Ez a parancs frissíti a csoportok létrehozásához a VMPolicySetDefinition nevű házirend-definíciós definíciót.</span><span class="sxs-lookup"><span data-stu-id="1f567-122">This command updates the groups of a policy set definition named VMPolicySetDefinition using a hash table to construct the groups.</span></span>

## <span data-ttu-id="1f567-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1f567-123">PARAMETERS</span></span>

### <span data-ttu-id="1f567-124">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1f567-124">-ApiVersion</span></span>
<span data-ttu-id="1f567-125">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f567-125">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="1f567-126">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="1f567-126">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f567-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f567-127">-DefaultProfile</span></span>
<span data-ttu-id="1f567-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1f567-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f567-129">-Leírás</span><span class="sxs-lookup"><span data-stu-id="1f567-129">-Description</span></span>
<span data-ttu-id="1f567-130">A házirend-készlet definíciójának leírása.</span><span class="sxs-lookup"><span data-stu-id="1f567-130">The description for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f567-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1f567-131">-DisplayName</span></span>
<span data-ttu-id="1f567-132">A házirend-készlet definíciójának megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="1f567-132">The display name for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f567-133">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="1f567-133">-GroupDefinition</span></span>
<span data-ttu-id="1f567-134">A frissített házirendprofil definíciójának házirend-definíciós csoportjai.</span><span class="sxs-lookup"><span data-stu-id="1f567-134">The policy definition groups of the updated policy set definition.</span></span> <span data-ttu-id="1f567-135">Ez lehet a csoportokat tartalmazó fájl elérési útja, vagy a csoportok JSON-karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="1f567-135">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f567-136">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="1f567-136">-Id</span></span>
<span data-ttu-id="1f567-137">A teljes mértékben minősített házirend-definíciós azonosító, az előfizetéssel együtt.</span><span class="sxs-lookup"><span data-stu-id="1f567-137">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="1f567-138">például/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="1f567-138">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f567-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f567-139">-InputObject</span></span>
<span data-ttu-id="1f567-140">A set definition objektum, amely egy másik parancsmagból származó kimenetet frissít.</span><span class="sxs-lookup"><span data-stu-id="1f567-140">The policy set definition object to update that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f567-141">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="1f567-141">-ManagementGroupName</span></span>
<span data-ttu-id="1f567-142">A frissítéshez a Policy set definition Definition (felügyeleti csoport) neve.</span><span class="sxs-lookup"><span data-stu-id="1f567-142">The name of the management group of the policy set definition to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f567-143">-Metadata</span><span class="sxs-lookup"><span data-stu-id="1f567-143">-Metadata</span></span>
<span data-ttu-id="1f567-144">A frissített házirend-készlet definíciójának metaadatai.</span><span class="sxs-lookup"><span data-stu-id="1f567-144">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="1f567-145">Ez lehet a metaadatokat tartalmazó fájlnév vagy a metaadatok használata JSON-karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="1f567-145">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f567-146">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1f567-146">-Name</span></span>
<span data-ttu-id="1f567-147">A Policy set definition név.</span><span class="sxs-lookup"><span data-stu-id="1f567-147">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f567-148">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="1f567-148">-Parameter</span></span>
<span data-ttu-id="1f567-149">A frissített házirend-definíció paramétereinek deklarációja.</span><span class="sxs-lookup"><span data-stu-id="1f567-149">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="1f567-150">Ez lehet a Parameters deklarációt vagy a Parameters deklarációt tartalmazó fájlnév vagy URI elérési útja JSON-karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="1f567-150">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f567-151">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1f567-151">-PolicyDefinition</span></span>
<span data-ttu-id="1f567-152">A házirend-definíciók.</span><span class="sxs-lookup"><span data-stu-id="1f567-152">The policy definitions.</span></span> <span data-ttu-id="1f567-153">Ez lehet egy elérési út a házirend-definíciókat tartalmazó fájlnévhez vagy a házirend-definíciók JSON-karakterláncként való eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="1f567-153">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f567-154">-Pre</span><span class="sxs-lookup"><span data-stu-id="1f567-154">-Pre</span></span>
<span data-ttu-id="1f567-155">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="1f567-155">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1f567-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1f567-156">-SubscriptionId</span></span>
<span data-ttu-id="1f567-157">A házirend-készlet definíciójának előfizetés azonosítója a frissítéshez.</span><span class="sxs-lookup"><span data-stu-id="1f567-157">The subscription ID of the policy set definition to update.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f567-158">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1f567-158">-Confirm</span></span>
<span data-ttu-id="1f567-159">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1f567-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f567-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f567-160">-WhatIf</span></span>
<span data-ttu-id="1f567-161">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1f567-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f567-162">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1f567-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f567-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f567-163">CommonParameters</span></span>
<span data-ttu-id="1f567-164">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1f567-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f567-165">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1f567-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f567-166">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f567-166">INPUTS</span></span>

### <span data-ttu-id="1f567-167">System. String</span><span class="sxs-lookup"><span data-stu-id="1f567-167">System.String</span></span>

### <span data-ttu-id="1f567-168">System. null ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1f567-168">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="1f567-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f567-169">OUTPUTS</span></span>

### <span data-ttu-id="1f567-170">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="1f567-170">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1f567-171">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1f567-171">NOTES</span></span>

## <span data-ttu-id="1f567-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f567-172">RELATED LINKS</span></span>
