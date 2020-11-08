---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyDefinition.md
ms.openlocfilehash: 52de80f1ad3cf84a7aa309b5e97b7fa24e9419b8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012621"
---
# <span data-ttu-id="9ca17-101">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9ca17-101">Get-AzPolicyDefinition</span></span>

## <span data-ttu-id="9ca17-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9ca17-102">SYNOPSIS</span></span>
<span data-ttu-id="9ca17-103">Házirend-definíciókat kap.</span><span class="sxs-lookup"><span data-stu-id="9ca17-103">Gets policy definitions.</span></span>

## <span data-ttu-id="9ca17-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9ca17-104">SYNTAX</span></span>

### <span data-ttu-id="9ca17-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9ca17-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicyDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ca17-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ca17-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ca17-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ca17-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ca17-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ca17-108">IdParameterSet</span></span>
```
Get-AzPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ca17-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ca17-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ca17-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ca17-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ca17-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="9ca17-111">DESCRIPTION</span></span>
<span data-ttu-id="9ca17-112">A **Get-AzPolicyDefinition** parancsmag egy név vagy azonosító szerint azonosított házirend-definíciók vagy konkrét házirend-definíció gyűjteményét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9ca17-112">The **Get-AzPolicyDefinition** cmdlet gets a collection of policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="9ca17-113">Példák</span><span class="sxs-lookup"><span data-stu-id="9ca17-113">EXAMPLES</span></span>

### <span data-ttu-id="9ca17-114">Példa 1: az összes házirend-definíció beolvasása</span><span class="sxs-lookup"><span data-stu-id="9ca17-114">Example 1: Get all policy definitions</span></span>
```
PS C:\> Get-AzPolicyDefinition
```

<span data-ttu-id="9ca17-115">Ez a parancs az összes házirend-definíciót megkapja.</span><span class="sxs-lookup"><span data-stu-id="9ca17-115">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="9ca17-116">2. példa: házirend-definíció beolvasása az aktuális előfizetésből név szerint</span><span class="sxs-lookup"><span data-stu-id="9ca17-116">Example 2: Get policy definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="9ca17-117">Ez a parancs az aktuális alapértelmezett előfizetésből a VMPolicyDefinition nevű házirend-definíciót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9ca17-117">This command gets the policy definition named VMPolicyDefinition from the current default subscription.</span></span>

### <span data-ttu-id="9ca17-118">3. példa: házirend-definíció beolvasása a kezelés csoportból név szerint</span><span class="sxs-lookup"><span data-stu-id="9ca17-118">Example 3: Get policy definition from management group by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName 'Dept42'
```

<span data-ttu-id="9ca17-119">Ez a parancs a VMPolicyDefinition nevű házirend-definíciót a Dept42 nevű felügyeleti csoporttól kapja.</span><span class="sxs-lookup"><span data-stu-id="9ca17-119">This command gets the policy definition named VMPolicyDefinition from the management group named Dept42.</span></span>

### <span data-ttu-id="9ca17-120">Példa 4: a beépített házirend-definíciók beszerzése az előfizetésből</span><span class="sxs-lookup"><span data-stu-id="9ca17-120">Example 4: Get all built-in policy definitions from subscription</span></span>
```
PS C:\> Get-AzPolicyDefinition -SubscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca' -Builtin
```

<span data-ttu-id="9ca17-121">Ez a parancs a beépített házirend-definíciókat az előfizetés 3bf44b72-c631-427a-b8c8-53e2595398ca.</span><span class="sxs-lookup"><span data-stu-id="9ca17-121">This command gets all built-in policy definitions from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="9ca17-122">Példa 5: házirend-definíciók beolvasása egy adott kategóriából</span><span class="sxs-lookup"><span data-stu-id="9ca17-122">Example 5: Get policy definitions from a given category</span></span>
```
PS C:\> Get-AzPolicyDefinition | where-object {$_.Properties.metadata.category -eq "Virtual Machine"}
```

<span data-ttu-id="9ca17-123">Ez a parancs a "virtuális gép" kategóriába tartozó összes házirend-definíciót megkapja.</span><span class="sxs-lookup"><span data-stu-id="9ca17-123">This command gets all policy definitions in category "Virtual Machine".</span></span>

## <span data-ttu-id="9ca17-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9ca17-124">PARAMETERS</span></span>

### <span data-ttu-id="9ca17-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9ca17-125">-ApiVersion</span></span>
<span data-ttu-id="9ca17-126">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9ca17-126">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="9ca17-127">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="9ca17-127">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="9ca17-128">-Beépített</span><span class="sxs-lookup"><span data-stu-id="9ca17-128">-Builtin</span></span>
<span data-ttu-id="9ca17-129">Az eredmények listáját csak a beépített házirend-definíciókkal korlátozhatja.</span><span class="sxs-lookup"><span data-stu-id="9ca17-129">Limits list of results to only built-in policy definitions.</span></span>

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

### <span data-ttu-id="9ca17-130">-Custom</span><span class="sxs-lookup"><span data-stu-id="9ca17-130">-Custom</span></span>
<span data-ttu-id="9ca17-131">Az eredmények listáját csak az egyéni házirend-definíciók szerint korlátozhatja.</span><span class="sxs-lookup"><span data-stu-id="9ca17-131">Limits list of results to only custom policy definitions.</span></span>

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

### <span data-ttu-id="9ca17-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ca17-132">-DefaultProfile</span></span>
<span data-ttu-id="9ca17-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9ca17-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ca17-134">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="9ca17-134">-Id</span></span>
<span data-ttu-id="9ca17-135">Annak a házirend-definíciónak a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="9ca17-135">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9ca17-136">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="9ca17-136">-ManagementGroupName</span></span>
<span data-ttu-id="9ca17-137">A beolvasott házirend-definíció (ok) kezelési csoportjának a neve.</span><span class="sxs-lookup"><span data-stu-id="9ca17-137">The name of the management group of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="9ca17-138">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9ca17-138">-Name</span></span>
<span data-ttu-id="9ca17-139">Annak a házirend-definíciónak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="9ca17-139">Specifies the name of the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9ca17-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="9ca17-140">-Pre</span></span>
<span data-ttu-id="9ca17-141">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="9ca17-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="9ca17-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9ca17-142">-SubscriptionId</span></span>
<span data-ttu-id="9ca17-143">A házirend-definíció (ok) előfizetési azonosítója a beszerzéshez.</span><span class="sxs-lookup"><span data-stu-id="9ca17-143">The subscription ID of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="9ca17-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ca17-144">CommonParameters</span></span>
<span data-ttu-id="9ca17-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9ca17-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ca17-146">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9ca17-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ca17-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ca17-147">INPUTS</span></span>

### <span data-ttu-id="9ca17-148">System. String</span><span class="sxs-lookup"><span data-stu-id="9ca17-148">System.String</span></span>

### <span data-ttu-id="9ca17-149">System. null ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9ca17-149">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9ca17-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ca17-150">OUTPUTS</span></span>

### <span data-ttu-id="9ca17-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="9ca17-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9ca17-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9ca17-152">NOTES</span></span>

## <span data-ttu-id="9ca17-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9ca17-153">RELATED LINKS</span></span>

[<span data-ttu-id="9ca17-154">Új – AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9ca17-154">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="9ca17-155">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9ca17-155">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="9ca17-156">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9ca17-156">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


