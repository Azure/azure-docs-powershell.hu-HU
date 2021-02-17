---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
ms.openlocfilehash: 4ec965e63a779a5b0ebb606819e5e9f7f20b035e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160011"
---
# <span data-ttu-id="97f26-101">Get-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="97f26-101">Get-AzPolicySetDefinition</span></span>

## <span data-ttu-id="97f26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97f26-102">SYNOPSIS</span></span>
<span data-ttu-id="97f26-103">Házirend-definíciókat kap.</span><span class="sxs-lookup"><span data-stu-id="97f26-103">Gets policy set definitions.</span></span>

## <span data-ttu-id="97f26-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="97f26-104">SYNTAX</span></span>

### <span data-ttu-id="97f26-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="97f26-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97f26-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="97f26-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97f26-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="97f26-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97f26-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="97f26-108">IdParameterSet</span></span>
```
Get-AzPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="97f26-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="97f26-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97f26-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="97f26-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97f26-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="97f26-111">DESCRIPTION</span></span>
<span data-ttu-id="97f26-112">A **Get-AzPolicySetDefinition parancsmag** a házirend-definíciók gyűjteményét vagy egy név vagy azonosító által meghatározott házirendkészlet-definíciót kap.</span><span class="sxs-lookup"><span data-stu-id="97f26-112">The **Get-AzPolicySetDefinition** cmdlet gets a collection of policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="97f26-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="97f26-113">EXAMPLES</span></span>

### <span data-ttu-id="97f26-114">1. példa: Az összes házirendkészlet-definíció lekérte</span><span class="sxs-lookup"><span data-stu-id="97f26-114">Example 1: Get all policy set definitions</span></span>
```
PS C:\> Get-AzPolicySetDefinition
```

<span data-ttu-id="97f26-115">Ez a parancs az összes házirendkészlet-definíciót beveszi.</span><span class="sxs-lookup"><span data-stu-id="97f26-115">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="97f26-116">2. példa: Házirendkészlet-definíció lekérte az aktuális előfizetésből név szerint</span><span class="sxs-lookup"><span data-stu-id="97f26-116">Example 2: Get policy set definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition'
```

<span data-ttu-id="97f26-117">Ez a parancs a VMPolicySetDefinition nevű házirendkészlet-definíciót az aktuális alapértelmezett előfizetésből kapja meg.</span><span class="sxs-lookup"><span data-stu-id="97f26-117">This command gets the policy set definition named VMPolicySetDefinition from the current default subscription.</span></span>

### <span data-ttu-id="97f26-118">3. példa: Házirendkészlet-definíció lekérte az előfizetésből név szerint</span><span class="sxs-lookup"><span data-stu-id="97f26-118">Example 3: Get policy set definition from subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -subscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca'
```

<span data-ttu-id="97f26-119">Ez a parancs a VMPolicySetDefinition nevű házirend-definíciót a 3bf44b72-c631-427a-b8c8-53e2595398ca azonosítójú előfizetésből kapja meg.</span><span class="sxs-lookup"><span data-stu-id="97f26-119">This command gets the policy definition named VMPolicySetDefinition from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="97f26-120">4. példa: Az összes egyéni házirendkészlet-definíció lekérte a felügyeleti csoporttól</span><span class="sxs-lookup"><span data-stu-id="97f26-120">Example 4: Get all custom policy set definitions from management group</span></span>
```
PS C:\> Get-AzPolicySetDefinition -ManagementGroupName 'Dept42' -Custom
```

<span data-ttu-id="97f26-121">Ez a parancs a Dept42 nevű felügyeleti csoport összes egyéni házirendkészlet-definícióját beveszi.</span><span class="sxs-lookup"><span data-stu-id="97f26-121">This command gets all custom policy set definitions from the management group named Dept42.</span></span>

### <span data-ttu-id="97f26-122">5. példa: Házirendkészlet-definíciók lekérte egy adott kategóriából</span><span class="sxs-lookup"><span data-stu-id="97f26-122">Example 5: Get policy set definitions from a given category</span></span>
```
PS C:\> Get-AzPolicySetDefinition | where-object {$_.Properties.metadata.category -eq "Virtual Machine"}
```

<span data-ttu-id="97f26-123">Ez a parancs az összes házirendkészlet-definíciót a "Virtuális gép" kategóriában kapja meg.</span><span class="sxs-lookup"><span data-stu-id="97f26-123">This command gets all policy set definitions in category "Virtual Machine".</span></span>

## <span data-ttu-id="97f26-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97f26-124">PARAMETERS</span></span>

### <span data-ttu-id="97f26-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="97f26-125">-ApiVersion</span></span>
<span data-ttu-id="97f26-126">Ha be van állítva, az erőforrás-szolgáltató API-t használja.</span><span class="sxs-lookup"><span data-stu-id="97f26-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="97f26-127">Ha nincs megadva, az API-verziót a rendszer automatikusan a legújabb elérhetőként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="97f26-127">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="97f26-128">-Builtin</span><span class="sxs-lookup"><span data-stu-id="97f26-128">-Builtin</span></span>
<span data-ttu-id="97f26-129">Az eredmények listáját csak a beépített házirendkészlet-definíciókra korlátozza.</span><span class="sxs-lookup"><span data-stu-id="97f26-129">Limits list of results to only built-in policy set definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BuiltinFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97f26-130">-Custom</span><span class="sxs-lookup"><span data-stu-id="97f26-130">-Custom</span></span>
<span data-ttu-id="97f26-131">Az eredmények listáját csak egyéni házirendkészlet-definíciókra korlátozza.</span><span class="sxs-lookup"><span data-stu-id="97f26-131">Limits list of results to only custom policy set definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CustomFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97f26-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97f26-132">-DefaultProfile</span></span>
<span data-ttu-id="97f26-133">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="97f26-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97f26-134">-Id</span><span class="sxs-lookup"><span data-stu-id="97f26-134">-Id</span></span>
<span data-ttu-id="97f26-135">A házirendkészlet teljes definícióazonosítója, az előfizetéssel együtt.</span><span class="sxs-lookup"><span data-stu-id="97f26-135">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="97f26-136">pl. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="97f26-136">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="97f26-137">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="97f26-137">-ManagementGroupName</span></span>
<span data-ttu-id="97f26-138">A lekért házirendkészlet-definíció(k) felügyeleti csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="97f26-138">The name of the management group of the policy set definition(s) to get.</span></span>

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

```yaml
Type: System.String
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97f26-139">-Name</span><span class="sxs-lookup"><span data-stu-id="97f26-139">-Name</span></span>
<span data-ttu-id="97f26-140">A házirendkészlet definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="97f26-140">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97f26-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="97f26-141">-Pre</span></span>
<span data-ttu-id="97f26-142">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="97f26-142">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="97f26-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="97f26-143">-SubscriptionId</span></span>
<span data-ttu-id="97f26-144">A lekért házirendkészlet-definíció(k) előfizetés-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="97f26-144">The subscription ID of the policy set definition(s) to get.</span></span>

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

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97f26-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97f26-145">CommonParameters</span></span>
<span data-ttu-id="97f26-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97f26-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97f26-147">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97f26-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97f26-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="97f26-148">INPUTS</span></span>

### <span data-ttu-id="97f26-149">System.String</span><span class="sxs-lookup"><span data-stu-id="97f26-149">System.String</span></span>

### <span data-ttu-id="97f26-150">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="97f26-150">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="97f26-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97f26-151">OUTPUTS</span></span>

### <span data-ttu-id="97f26-152">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="97f26-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="97f26-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="97f26-153">NOTES</span></span>

## <span data-ttu-id="97f26-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97f26-154">RELATED LINKS</span></span>
