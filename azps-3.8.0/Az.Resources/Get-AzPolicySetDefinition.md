---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
ms.openlocfilehash: 4ec965e63a779a5b0ebb606819e5e9f7f20b035e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012619"
---
# <span data-ttu-id="d18a7-101">Get-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="d18a7-101">Get-AzPolicySetDefinition</span></span>

## <span data-ttu-id="d18a7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d18a7-102">SYNOPSIS</span></span>
<span data-ttu-id="d18a7-103">Kapja meg a házirend-definíciókat.</span><span class="sxs-lookup"><span data-stu-id="d18a7-103">Gets policy set definitions.</span></span>

## <span data-ttu-id="d18a7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d18a7-104">SYNTAX</span></span>

### <span data-ttu-id="d18a7-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d18a7-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d18a7-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d18a7-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d18a7-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d18a7-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d18a7-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d18a7-108">IdParameterSet</span></span>
```
Get-AzPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d18a7-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="d18a7-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d18a7-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="d18a7-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d18a7-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="d18a7-111">DESCRIPTION</span></span>
<span data-ttu-id="d18a7-112">A **Get-AzPolicySetDefinition** parancsmag a házirend-definíciók, illetve egy név vagy azonosító szerint azonosított speciális házirend-definíció gyűjteményét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d18a7-112">The **Get-AzPolicySetDefinition** cmdlet gets a collection of policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="d18a7-113">Példák</span><span class="sxs-lookup"><span data-stu-id="d18a7-113">EXAMPLES</span></span>

### <span data-ttu-id="d18a7-114">Példa 1: az összes házirend-készlet definíciójának beolvasása</span><span class="sxs-lookup"><span data-stu-id="d18a7-114">Example 1: Get all policy set definitions</span></span>
```
PS C:\> Get-AzPolicySetDefinition
```

<span data-ttu-id="d18a7-115">Ez a parancs beilleszti az összes házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="d18a7-115">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="d18a7-116">2. példa: a házirend-készlet definíciójának beszerzése a jelenlegi előfizetésből név szerint</span><span class="sxs-lookup"><span data-stu-id="d18a7-116">Example 2: Get policy set definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition'
```

<span data-ttu-id="d18a7-117">Ez a parancs az aktuális alapértelmezett előfizetésből a VMPolicySetDefinition nevű házirend-definíciót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d18a7-117">This command gets the policy set definition named VMPolicySetDefinition from the current default subscription.</span></span>

### <span data-ttu-id="d18a7-118">3. példa: házirend-definíció beszerzése az előfizetésből név szerint</span><span class="sxs-lookup"><span data-stu-id="d18a7-118">Example 3: Get policy set definition from subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -subscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca'
```

<span data-ttu-id="d18a7-119">Ez a parancs a VMPolicySetDefinition nevű házirend-definíciót kapja meg az 3bf44b72-c631-427a-b8c8-53e2595398ca AZONOSÍTÓJÚ előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="d18a7-119">This command gets the policy definition named VMPolicySetDefinition from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="d18a7-120">Példa 4: az összes egyéni házirend-készlet definíciójának beolvasása a kezelés csoportból</span><span class="sxs-lookup"><span data-stu-id="d18a7-120">Example 4: Get all custom policy set definitions from management group</span></span>
```
PS C:\> Get-AzPolicySetDefinition -ManagementGroupName 'Dept42' -Custom
```

<span data-ttu-id="d18a7-121">Ez a parancs beilleszti az összes egyéni házirend-definíciót a Dept42 nevű felügyeleti csoportból.</span><span class="sxs-lookup"><span data-stu-id="d18a7-121">This command gets all custom policy set definitions from the management group named Dept42.</span></span>

### <span data-ttu-id="d18a7-122">Példa 5: a házirend beállítása meghatározott kategóriából</span><span class="sxs-lookup"><span data-stu-id="d18a7-122">Example 5: Get policy set definitions from a given category</span></span>
```
PS C:\> Get-AzPolicySetDefinition | where-object {$_.Properties.metadata.category -eq "Virtual Machine"}
```

<span data-ttu-id="d18a7-123">Ez a parancs a "virtuális gép" kategóriába tartozik minden házirend-készlet definíciója.</span><span class="sxs-lookup"><span data-stu-id="d18a7-123">This command gets all policy set definitions in category "Virtual Machine".</span></span>

## <span data-ttu-id="d18a7-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d18a7-124">PARAMETERS</span></span>

### <span data-ttu-id="d18a7-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d18a7-125">-ApiVersion</span></span>
<span data-ttu-id="d18a7-126">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d18a7-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="d18a7-127">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="d18a7-127">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="d18a7-128">-Beépített</span><span class="sxs-lookup"><span data-stu-id="d18a7-128">-Builtin</span></span>
<span data-ttu-id="d18a7-129">Az eredmények listáját csak a beépített házirend-definíciók listájában korlátozhatja.</span><span class="sxs-lookup"><span data-stu-id="d18a7-129">Limits list of results to only built-in policy set definitions.</span></span>

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

### <span data-ttu-id="d18a7-130">-Custom</span><span class="sxs-lookup"><span data-stu-id="d18a7-130">-Custom</span></span>
<span data-ttu-id="d18a7-131">Az eredmények listáját csak az egyéni házirend-készlet definíciói szerint korlátozhatja.</span><span class="sxs-lookup"><span data-stu-id="d18a7-131">Limits list of results to only custom policy set definitions.</span></span>

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

### <span data-ttu-id="d18a7-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d18a7-132">-DefaultProfile</span></span>
<span data-ttu-id="d18a7-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d18a7-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d18a7-134">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="d18a7-134">-Id</span></span>
<span data-ttu-id="d18a7-135">A teljes mértékben minősített házirend-definíciós azonosító, az előfizetést is beleszámítva.</span><span class="sxs-lookup"><span data-stu-id="d18a7-135">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="d18a7-136">például/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="d18a7-136">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="d18a7-137">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="d18a7-137">-ManagementGroupName</span></span>
<span data-ttu-id="d18a7-138">A beolvasott házirend-definíció (ok) felügyeleti csoportjának a neve.</span><span class="sxs-lookup"><span data-stu-id="d18a7-138">The name of the management group of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="d18a7-139">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d18a7-139">-Name</span></span>
<span data-ttu-id="d18a7-140">A Policy set definition név.</span><span class="sxs-lookup"><span data-stu-id="d18a7-140">The policy set definition name.</span></span>

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

### <span data-ttu-id="d18a7-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="d18a7-141">-Pre</span></span>
<span data-ttu-id="d18a7-142">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="d18a7-142">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d18a7-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d18a7-143">-SubscriptionId</span></span>
<span data-ttu-id="d18a7-144">A házirend-készlet definíciójának (ek) előfizetési azonosítója a beszerzéshez.</span><span class="sxs-lookup"><span data-stu-id="d18a7-144">The subscription ID of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="d18a7-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d18a7-145">CommonParameters</span></span>
<span data-ttu-id="d18a7-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d18a7-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d18a7-147">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d18a7-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d18a7-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d18a7-148">INPUTS</span></span>

### <span data-ttu-id="d18a7-149">System. String</span><span class="sxs-lookup"><span data-stu-id="d18a7-149">System.String</span></span>

### <span data-ttu-id="d18a7-150">System. null ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d18a7-150">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d18a7-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d18a7-151">OUTPUTS</span></span>

### <span data-ttu-id="d18a7-152">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="d18a7-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d18a7-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d18a7-153">NOTES</span></span>

## <span data-ttu-id="d18a7-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d18a7-154">RELATED LINKS</span></span>
