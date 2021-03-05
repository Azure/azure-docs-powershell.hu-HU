---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: fab07b94c565a37d2884c5074de9f23692878df4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011734"
---
# <span data-ttu-id="cd6e4-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="cd6e4-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="cd6e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd6e4-102">SYNOPSIS</span></span>
<span data-ttu-id="cd6e4-103">Házirendkészlet-definíciót módosít</span><span class="sxs-lookup"><span data-stu-id="cd6e4-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="cd6e4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cd6e4-104">SYNTAX</span></span>

### <span data-ttu-id="cd6e4-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cd6e4-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd6e4-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd6e4-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd6e4-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd6e4-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd6e4-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd6e4-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd6e4-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd6e4-109">InputObjectParameterSet</span></span>
```
Set-AzPolicySetDefinition [-DisplayName <String>] [-Description <String>] [-PolicyDefinition <String>]
 [-Metadata <String>] [-Parameter <String>] -InputObject <PsPolicySetDefinition> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cd6e4-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cd6e4-110">DESCRIPTION</span></span>
<span data-ttu-id="cd6e4-111">A **Set-AzPolicySetDefinition parancsmag** módosítja a házirenddefiníciót.</span><span class="sxs-lookup"><span data-stu-id="cd6e4-111">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="cd6e4-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cd6e4-112">EXAMPLES</span></span>

### <span data-ttu-id="cd6e4-113">1. példa: Házirendkészlet-definíció leírásának frissítése</span><span class="sxs-lookup"><span data-stu-id="cd6e4-113">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="cd6e4-114">Az első parancs egy házirendkészlet-definíciót kap a Get-AzPolicySetDefinition parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="cd6e4-114">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="cd6e4-115">A parancs az objektumot a $PolicySetDefinition tárolja.</span><span class="sxs-lookup"><span data-stu-id="cd6e4-115">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="cd6e4-116">A második parancs frissíti a házirendkészlet-definíció leírását, amelyet a rendszer **ResourceId** tulajdonsága $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="cd6e4-116">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

### <span data-ttu-id="cd6e4-117">2. példa: Házirendkészlet-definíció metaadatainak frissítése</span><span class="sxs-lookup"><span data-stu-id="cd6e4-117">Example 2: Update the metadata of a policy set definition</span></span>
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

<span data-ttu-id="cd6e4-118">Ez a parancs frissíti a VMPolicySetDefinition nevű házirendkészlet-definíció metaadatait, jelezve, hogy a kategória "Virtuális gép".</span><span class="sxs-lookup"><span data-stu-id="cd6e4-118">This command updates the metadata of a policy set definition named VMPolicySetDefinition to indicate its category is "Virtual Machine".</span></span>

### <span data-ttu-id="cd6e4-119">3. példa: Házirendkészlet-definíció csoportjainak frissítése</span><span class="sxs-lookup"><span data-stu-id="cd6e4-119">Example 3: Update the groups of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition '[{ "name": "group1", "displayName": "Virtual Machine Security" }, { "name": "group2" }]'
```

<span data-ttu-id="cd6e4-120">Ez a parancs frissíti a VMPolicySetDefinition nevű házirendkészlet-definíció csoportjait.</span><span class="sxs-lookup"><span data-stu-id="cd6e4-120">This command updates the groups of a policy set definition named VMPolicySetDefinition.</span></span>

### <span data-ttu-id="cd6e4-121">4. példa: Házirendkészlet-definíció csoportjainak frissítése kivonattáblával</span><span class="sxs-lookup"><span data-stu-id="cd6e4-121">Example 4: Update the groups of a policy set definition using a hash table</span></span>
```
$groupsJson = ConvertTo-Json @{ name = "group1", displayName = "Virtual Machine Security" }, @{ name = "group2" }
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition $groupsJson
```

<span data-ttu-id="cd6e4-122">Ez a parancs a VMPolicySetDefinition nevű házirendkészlet-definíció csoportjait egy kivonattáblával frissíti a csoportok felépítéséhez.</span><span class="sxs-lookup"><span data-stu-id="cd6e4-122">This command updates the groups of a policy set definition named VMPolicySetDefinition using a hash table to construct the groups.</span></span>

## <span data-ttu-id="cd6e4-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd6e4-123">PARAMETERS</span></span>

### <span data-ttu-id="cd6e4-124">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="cd6e4-124">-ApiVersion</span></span>
<span data-ttu-id="cd6e4-125">Ha be van állítva, az erőforrás-szolgáltató API-t használja.</span><span class="sxs-lookup"><span data-stu-id="cd6e4-125">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="cd6e4-126">Ha nincs megadva, az API-verziót a rendszer automatikusan a legújabb elérhetőként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="cd6e4-126">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="cd6e4-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd6e4-127">-DefaultProfile</span></span>
<span data-ttu-id="cd6e4-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cd6e4-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd6e4-129">-Leírás</span><span class="sxs-lookup"><span data-stu-id="cd6e4-129">-Description</span></span>
<span data-ttu-id="cd6e4-130">A házirendkészlet-definíció leírása.</span><span class="sxs-lookup"><span data-stu-id="cd6e4-130">The description for policy set definition.</span></span>

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

### <span data-ttu-id="cd6e4-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="cd6e4-131">-DisplayName</span></span>
<span data-ttu-id="cd6e4-132">A házirendkészlet-definíció megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="cd6e4-132">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="cd6e4-133">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="cd6e4-133">-GroupDefinition</span></span>
<span data-ttu-id="cd6e4-134">A frissített házirendkészlet-definíció házirenddefiníciós csoportjai.</span><span class="sxs-lookup"><span data-stu-id="cd6e4-134">The policy definition groups of the updated policy set definition.</span></span> <span data-ttu-id="cd6e4-135">Ez lehet egy olyan fájl elérési útja, amely a csoportokat tartalmazza, vagy a csoportokat JSON-karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="cd6e4-135">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="cd6e4-136">-Id</span><span class="sxs-lookup"><span data-stu-id="cd6e4-136">-Id</span></span>
<span data-ttu-id="cd6e4-137">A teljesen minősített házirenddefiníciós azonosító, az előfizetéssel együtt.</span><span class="sxs-lookup"><span data-stu-id="cd6e4-137">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="cd6e4-138">pl. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="cd6e4-138">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="cd6e4-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd6e4-139">-InputObject</span></span>
<span data-ttu-id="cd6e4-140">A házirend-beállításdefiníciós objektum egy másik parancsmagból származó kimenet frissítésére.</span><span class="sxs-lookup"><span data-stu-id="cd6e4-140">The policy set definition object to update that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="cd6e4-141">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="cd6e4-141">-ManagementGroupName</span></span>
<span data-ttu-id="cd6e4-142">A frissítenie kell a házirendkészlet-definíció felügyeleti csoportjának nevét.</span><span class="sxs-lookup"><span data-stu-id="cd6e4-142">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="cd6e4-143">-Metadata</span><span class="sxs-lookup"><span data-stu-id="cd6e4-143">-Metadata</span></span>
<span data-ttu-id="cd6e4-144">A frissített házirendkészlet-definíció metaadatai.</span><span class="sxs-lookup"><span data-stu-id="cd6e4-144">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="cd6e4-145">Ez lehet egy olyan fájlnév elérési útja, amely tartalmazza a metaadatokat vagy a metaadatokat JSON-karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="cd6e4-145">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="cd6e4-146">-Name</span><span class="sxs-lookup"><span data-stu-id="cd6e4-146">-Name</span></span>
<span data-ttu-id="cd6e4-147">A házirendkészlet definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="cd6e4-147">The policy set definition name.</span></span>

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

### <span data-ttu-id="cd6e4-148">-Parameter</span><span class="sxs-lookup"><span data-stu-id="cd6e4-148">-Parameter</span></span>
<span data-ttu-id="cd6e4-149">A frissített házirendkészlet-definíció paramétereinek deklarációja.</span><span class="sxs-lookup"><span data-stu-id="cd6e4-149">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="cd6e4-150">Ez lehet egy olyan fájlnév vagy uri elérési útja, amely a paraméterdeklarációt tartalmazza, vagy a paraméterek deklarációja JSON-karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="cd6e4-150">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="cd6e4-151">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cd6e4-151">-PolicyDefinition</span></span>
<span data-ttu-id="cd6e4-152">A házirend-definíciók.</span><span class="sxs-lookup"><span data-stu-id="cd6e4-152">The policy definitions.</span></span> <span data-ttu-id="cd6e4-153">Ez lehet egy olyan fájlnév elérési útja, amely tartalmazza a házirenddefiníciókat, vagy a házirenddefiníciókat JSON-karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="cd6e4-153">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

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

### <span data-ttu-id="cd6e4-154">-Pre</span><span class="sxs-lookup"><span data-stu-id="cd6e4-154">-Pre</span></span>
<span data-ttu-id="cd6e4-155">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="cd6e4-155">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="cd6e4-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd6e4-156">-SubscriptionId</span></span>
<span data-ttu-id="cd6e4-157">A frissíteni szükséges házirendkészlet-definíció előfizetésazonosítója.</span><span class="sxs-lookup"><span data-stu-id="cd6e4-157">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="cd6e4-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd6e4-158">-Confirm</span></span>
<span data-ttu-id="cd6e4-159">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cd6e4-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd6e4-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd6e4-160">-WhatIf</span></span>
<span data-ttu-id="cd6e4-161">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cd6e4-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd6e4-162">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cd6e4-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd6e4-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd6e4-163">CommonParameters</span></span>
<span data-ttu-id="cd6e4-164">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd6e4-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd6e4-165">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd6e4-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd6e4-166">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cd6e4-166">INPUTS</span></span>

### <span data-ttu-id="cd6e4-167">System.String</span><span class="sxs-lookup"><span data-stu-id="cd6e4-167">System.String</span></span>

### <span data-ttu-id="cd6e4-168">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="cd6e4-168">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="cd6e4-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd6e4-169">OUTPUTS</span></span>

### <span data-ttu-id="cd6e4-170">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="cd6e4-170">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="cd6e4-171">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cd6e4-171">NOTES</span></span>

## <span data-ttu-id="cd6e4-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd6e4-172">RELATED LINKS</span></span>
