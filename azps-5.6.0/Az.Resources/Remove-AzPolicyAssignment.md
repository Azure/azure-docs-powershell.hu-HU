---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: 83c6cc2ba8103b95aed6d6d365c700e656ac16a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005813"
---
# <span data-ttu-id="0d7ad-101">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="0d7ad-101">Remove-AzPolicyAssignment</span></span>

## <span data-ttu-id="0d7ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d7ad-102">SYNOPSIS</span></span>
<span data-ttu-id="0d7ad-103">Eltávolít egy házirend-hozzárendelést.</span><span class="sxs-lookup"><span data-stu-id="0d7ad-103">Removes a policy assignment.</span></span>

## <span data-ttu-id="0d7ad-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0d7ad-104">SYNTAX</span></span>

### <span data-ttu-id="0d7ad-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0d7ad-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyAssignment -Name <String> [-Scope <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d7ad-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d7ad-106">IdParameterSet</span></span>
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d7ad-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d7ad-107">InputObjectParameterSet</span></span>
```
Remove-AzPolicyAssignment -InputObject <PsPolicyAssignment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d7ad-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0d7ad-108">DESCRIPTION</span></span>
<span data-ttu-id="0d7ad-109">A **Remove-AzPolicyAssignment** parancsmag eltávolítja a megadott házirend-hozzárendelést.</span><span class="sxs-lookup"><span data-stu-id="0d7ad-109">The **Remove-AzPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="0d7ad-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0d7ad-110">EXAMPLES</span></span>

### <span data-ttu-id="0d7ad-111">1. példa: Házirend-hozzárendelés eltávolítása név és hatókör szerint</span><span class="sxs-lookup"><span data-stu-id="0d7ad-111">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Confirm
```

<span data-ttu-id="0d7ad-112">Az első parancs egy ResourceGroup11 nevű erőforráscsoportot kap a Get-AzResourceGroup parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="0d7ad-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="0d7ad-113">A parancs az objektumot a $ResourceGroup tárolja.</span><span class="sxs-lookup"><span data-stu-id="0d7ad-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="0d7ad-114">A második parancs eltávolítja a PolicyAssignment07 nevű házirend-hozzárendelést, amely erőforráscsoport szintjén lett hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="0d7ad-114">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="0d7ad-115">A **$ResourceGroup ResourceId** tulajdonsága azonosítja az erőforráscsoportot.</span><span class="sxs-lookup"><span data-stu-id="0d7ad-115">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="0d7ad-116">2. példa: Házirend-hozzárendelés eltávolítása azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="0d7ad-116">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Confirm
```

<span data-ttu-id="0d7ad-117">Az első parancs egy ResourceGroup11 nevű erőforráscsoportot kap, majd az objektumot a $ResourceGroup tárolja.</span><span class="sxs-lookup"><span data-stu-id="0d7ad-117">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="0d7ad-118">A második parancs erőforráscsoportszinten kapja meg a házirend-hozzárendelést, majd azt a $PolicyAssignment tárolja.</span><span class="sxs-lookup"><span data-stu-id="0d7ad-118">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="0d7ad-119">A **$ResourceGroup ResourceId** tulajdonsága azonosítja az erőforráscsoportot.</span><span class="sxs-lookup"><span data-stu-id="0d7ad-119">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="0d7ad-120">Az utolsó parancs eltávolítja azt a házirend-hozzárendelést, amit a $PolicyAssignment **resourceid** tulajdonsága azonosít.</span><span class="sxs-lookup"><span data-stu-id="0d7ad-120">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="0d7ad-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d7ad-121">PARAMETERS</span></span>

### <span data-ttu-id="0d7ad-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0d7ad-122">-ApiVersion</span></span>
<span data-ttu-id="0d7ad-123">Az erőforrás-szolgáltató API-jának használnia kell verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d7ad-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="0d7ad-124">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="0d7ad-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="0d7ad-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d7ad-125">-DefaultProfile</span></span>
<span data-ttu-id="0d7ad-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0d7ad-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d7ad-127">-Id</span><span class="sxs-lookup"><span data-stu-id="0d7ad-127">-Id</span></span>
<span data-ttu-id="0d7ad-128">A parancsmag által eltávolított házirend-hozzárendelés teljes erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d7ad-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0d7ad-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d7ad-129">-InputObject</span></span>
<span data-ttu-id="0d7ad-130">Az a házirend-hozzárendelési objektum, amely egy másik parancsmagból távolítja el a kimenetet.</span><span class="sxs-lookup"><span data-stu-id="0d7ad-130">The policy assignment object to remove that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyAssignment
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d7ad-131">-Name</span><span class="sxs-lookup"><span data-stu-id="0d7ad-131">-Name</span></span>
<span data-ttu-id="0d7ad-132">A parancsmag által eltávolított házirend-hozzárendelés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d7ad-132">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d7ad-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="0d7ad-133">-Pre</span></span>
<span data-ttu-id="0d7ad-134">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="0d7ad-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0d7ad-135">-Scope</span><span class="sxs-lookup"><span data-stu-id="0d7ad-135">-Scope</span></span>
<span data-ttu-id="0d7ad-136">A házirend hatókörét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="0d7ad-136">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d7ad-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d7ad-137">-Confirm</span></span>
<span data-ttu-id="0d7ad-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0d7ad-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d7ad-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d7ad-139">-WhatIf</span></span>
<span data-ttu-id="0d7ad-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0d7ad-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d7ad-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0d7ad-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d7ad-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d7ad-142">CommonParameters</span></span>
<span data-ttu-id="0d7ad-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d7ad-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d7ad-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d7ad-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d7ad-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0d7ad-145">INPUTS</span></span>

### <span data-ttu-id="0d7ad-146">System.String</span><span class="sxs-lookup"><span data-stu-id="0d7ad-146">System.String</span></span>

## <span data-ttu-id="0d7ad-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d7ad-147">OUTPUTS</span></span>

### <span data-ttu-id="0d7ad-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0d7ad-148">System.Boolean</span></span>

## <span data-ttu-id="0d7ad-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0d7ad-149">NOTES</span></span>

## <span data-ttu-id="0d7ad-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0d7ad-150">RELATED LINKS</span></span>

[<span data-ttu-id="0d7ad-151">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="0d7ad-151">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="0d7ad-152">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="0d7ad-152">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="0d7ad-153">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="0d7ad-153">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


