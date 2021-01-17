---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyDefinition.md
ms.openlocfilehash: 52de80f1ad3cf84a7aa309b5e97b7fa24e9419b8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466520"
---
# <span data-ttu-id="b93ae-101">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b93ae-101">Get-AzPolicyDefinition</span></span>

## <span data-ttu-id="b93ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b93ae-102">SYNOPSIS</span></span>
<span data-ttu-id="b93ae-103">Házirend-definíciókat kap.</span><span class="sxs-lookup"><span data-stu-id="b93ae-103">Gets policy definitions.</span></span>

## <span data-ttu-id="b93ae-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b93ae-104">SYNTAX</span></span>

### <span data-ttu-id="b93ae-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b93ae-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicyDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b93ae-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b93ae-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b93ae-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b93ae-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b93ae-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b93ae-108">IdParameterSet</span></span>
```
Get-AzPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b93ae-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="b93ae-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b93ae-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="b93ae-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b93ae-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b93ae-111">DESCRIPTION</span></span>
<span data-ttu-id="b93ae-112">A **Get-AzPolicyDefinition** parancsmag egy házirenddefiníciós gyűjteményt vagy egy név vagy azonosító által meghatározott házirenddefiníciót kap.</span><span class="sxs-lookup"><span data-stu-id="b93ae-112">The **Get-AzPolicyDefinition** cmdlet gets a collection of policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="b93ae-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b93ae-113">EXAMPLES</span></span>

### <span data-ttu-id="b93ae-114">1. példa: Az összes házirenddefiníció lekérte</span><span class="sxs-lookup"><span data-stu-id="b93ae-114">Example 1: Get all policy definitions</span></span>
```
PS C:\> Get-AzPolicyDefinition
```

<span data-ttu-id="b93ae-115">Ez a parancs az összes házirenddefiníciót beveszi.</span><span class="sxs-lookup"><span data-stu-id="b93ae-115">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="b93ae-116">2. példa: Házirenddefiníció lekérte az aktuális előfizetést név szerint</span><span class="sxs-lookup"><span data-stu-id="b93ae-116">Example 2: Get policy definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="b93ae-117">Ez a parancs a VMPolicyDefinition nevű házirend-definíciót az aktuális alapértelmezett előfizetésből kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b93ae-117">This command gets the policy definition named VMPolicyDefinition from the current default subscription.</span></span>

### <span data-ttu-id="b93ae-118">3. példa: Házirend-definíció lekérte a felügyeleti csoportból név szerint</span><span class="sxs-lookup"><span data-stu-id="b93ae-118">Example 3: Get policy definition from management group by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName 'Dept42'
```

<span data-ttu-id="b93ae-119">Ez a parancs a VMPolicyDefinition nevű házirend-definíciót a Dept42 nevű felügyeleti csoportból kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b93ae-119">This command gets the policy definition named VMPolicyDefinition from the management group named Dept42.</span></span>

### <span data-ttu-id="b93ae-120">4. példa: Az összes beépített házirenddefiníció lekérte az előfizetésből</span><span class="sxs-lookup"><span data-stu-id="b93ae-120">Example 4: Get all built-in policy definitions from subscription</span></span>
```
PS C:\> Get-AzPolicyDefinition -SubscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca' -Builtin
```

<span data-ttu-id="b93ae-121">Ez a parancs a 3bf44b72-c631-427a-b8c8-53e2595398ca azonosítójú előfizetés összes beépített házirenddefinícióját megkapja.</span><span class="sxs-lookup"><span data-stu-id="b93ae-121">This command gets all built-in policy definitions from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="b93ae-122">5. példa: Házirend-definíciók lekérte egy adott kategóriából</span><span class="sxs-lookup"><span data-stu-id="b93ae-122">Example 5: Get policy definitions from a given category</span></span>
```
PS C:\> Get-AzPolicyDefinition | where-object {$_.Properties.metadata.category -eq "Virtual Machine"}
```

<span data-ttu-id="b93ae-123">Ez a parancs az összes házirenddefiníciót a "Virtuális gép" kategóriában kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b93ae-123">This command gets all policy definitions in category "Virtual Machine".</span></span>

## <span data-ttu-id="b93ae-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b93ae-124">PARAMETERS</span></span>

### <span data-ttu-id="b93ae-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b93ae-125">-ApiVersion</span></span>
<span data-ttu-id="b93ae-126">Az erőforrás-szolgáltató API-jának használnia kell verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b93ae-126">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b93ae-127">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="b93ae-127">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="b93ae-128">-Builtin</span><span class="sxs-lookup"><span data-stu-id="b93ae-128">-Builtin</span></span>
<span data-ttu-id="b93ae-129">Az eredmények listáját csak a beépített házirend-definíciókra korlátozza.</span><span class="sxs-lookup"><span data-stu-id="b93ae-129">Limits list of results to only built-in policy definitions.</span></span>

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

### <span data-ttu-id="b93ae-130">-Custom</span><span class="sxs-lookup"><span data-stu-id="b93ae-130">-Custom</span></span>
<span data-ttu-id="b93ae-131">Az eredmények listáját csak egyéni házirend-definíciókra korlátozza.</span><span class="sxs-lookup"><span data-stu-id="b93ae-131">Limits list of results to only custom policy definitions.</span></span>

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

### <span data-ttu-id="b93ae-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b93ae-132">-DefaultProfile</span></span>
<span data-ttu-id="b93ae-133">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b93ae-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b93ae-134">-Id</span><span class="sxs-lookup"><span data-stu-id="b93ae-134">-Id</span></span>
<span data-ttu-id="b93ae-135">A parancsmag által begyűlített házirenddefiníció teljes erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b93ae-135">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b93ae-136">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="b93ae-136">-ManagementGroupName</span></span>
<span data-ttu-id="b93ae-137">A lekért házirend-definíció(k) felügyeleti csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="b93ae-137">The name of the management group of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="b93ae-138">-Name</span><span class="sxs-lookup"><span data-stu-id="b93ae-138">-Name</span></span>
<span data-ttu-id="b93ae-139">A parancsmag által begyabalyt házirenddefiníció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b93ae-139">Specifies the name of the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b93ae-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="b93ae-140">-Pre</span></span>
<span data-ttu-id="b93ae-141">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="b93ae-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b93ae-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b93ae-142">-SubscriptionId</span></span>
<span data-ttu-id="b93ae-143">A lekért házirenddefiníció(k) előfizetés-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b93ae-143">The subscription ID of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="b93ae-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b93ae-144">CommonParameters</span></span>
<span data-ttu-id="b93ae-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b93ae-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b93ae-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b93ae-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b93ae-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b93ae-147">INPUTS</span></span>

### <span data-ttu-id="b93ae-148">System.String</span><span class="sxs-lookup"><span data-stu-id="b93ae-148">System.String</span></span>

### <span data-ttu-id="b93ae-149">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b93ae-149">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="b93ae-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b93ae-150">OUTPUTS</span></span>

### <span data-ttu-id="b93ae-151">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="b93ae-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b93ae-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b93ae-152">NOTES</span></span>

## <span data-ttu-id="b93ae-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b93ae-153">RELATED LINKS</span></span>

[<span data-ttu-id="b93ae-154">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b93ae-154">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="b93ae-155">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b93ae-155">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="b93ae-156">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b93ae-156">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


