---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: e25a41c80c7bc277073f9b00331087203590cd22
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838893"
---
# <span data-ttu-id="18c72-101">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="18c72-101">Remove-AzPolicyAssignment</span></span>

## <span data-ttu-id="18c72-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="18c72-102">SYNOPSIS</span></span>
<span data-ttu-id="18c72-103">Házirend-hozzárendelés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="18c72-103">Removes a policy assignment.</span></span>

## <span data-ttu-id="18c72-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="18c72-104">SYNTAX</span></span>

### <span data-ttu-id="18c72-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="18c72-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyAssignment -Name <String> -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18c72-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="18c72-106">IdParameterSet</span></span>
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18c72-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="18c72-107">DESCRIPTION</span></span>
<span data-ttu-id="18c72-108">A **Remove-AzPolicyAssignment** parancsmag eltávolítja a megadott házirend-feladatot.</span><span class="sxs-lookup"><span data-stu-id="18c72-108">The **Remove-AzPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="18c72-109">Példák</span><span class="sxs-lookup"><span data-stu-id="18c72-109">EXAMPLES</span></span>

### <span data-ttu-id="18c72-110">1. példa: házirend-hozzárendelés eltávolítása név és hatókör szerint</span><span class="sxs-lookup"><span data-stu-id="18c72-110">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="18c72-111">Az első parancs az Get-AzResourceGroup parancsmag segítségével a ResourceGroup11 nevű erőforráscsoportot kapja.</span><span class="sxs-lookup"><span data-stu-id="18c72-111">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="18c72-112">A parancs az objektumot a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="18c72-112">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="18c72-113">A második parancs eltávolítja a PolicyAssignment07 nevű olyan házirend-hozzárendelést, amely egy erőforrás-csoport szintjén van társítva.</span><span class="sxs-lookup"><span data-stu-id="18c72-113">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="18c72-114">A $ResourceGroup **ResourceId** tulajdonság azonosítja az erőforráscsoport értékét.</span><span class="sxs-lookup"><span data-stu-id="18c72-114">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="18c72-115">2. példa: házirend-hozzárendelés eltávolítása AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="18c72-115">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="18c72-116">Az első parancs beolvassa a ResourceGroup11 nevű erőforráscsoportot, majd az objektumot a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="18c72-116">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="18c72-117">A második parancs egy erőforráscsoport szintjén kapja meg a házirend-hozzárendelést, és a $PolicyAssignment változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="18c72-117">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="18c72-118">A $ResourceGroup **ResourceId** tulajdonság azonosítja az erőforráscsoport értékét.</span><span class="sxs-lookup"><span data-stu-id="18c72-118">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="18c72-119">A végleges parancs eltávolítja azt a házirend-feladatot, amelyet az $PolicyAssignment **ResourceId** tulajdonsága azonosít.</span><span class="sxs-lookup"><span data-stu-id="18c72-119">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="18c72-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="18c72-120">PARAMETERS</span></span>

### <span data-ttu-id="18c72-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="18c72-121">-ApiVersion</span></span>
<span data-ttu-id="18c72-122">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="18c72-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="18c72-123">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="18c72-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="18c72-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18c72-124">-DefaultProfile</span></span>
<span data-ttu-id="18c72-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="18c72-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18c72-126">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="18c72-126">-Id</span></span>
<span data-ttu-id="18c72-127">Annak a házirend-hozzárendelésnek a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="18c72-127">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="18c72-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="18c72-128">-Name</span></span>
<span data-ttu-id="18c72-129">A parancsmag által eltávolított házirend-hozzárendelés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="18c72-129">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="18c72-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="18c72-130">-Pre</span></span>
<span data-ttu-id="18c72-131">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="18c72-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="18c72-132">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="18c72-132">-Scope</span></span>
<span data-ttu-id="18c72-133">Azt a hatókört adja meg, amelyen a házirendet alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="18c72-133">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="18c72-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="18c72-134">-Confirm</span></span>
<span data-ttu-id="18c72-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="18c72-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18c72-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18c72-136">-WhatIf</span></span>
<span data-ttu-id="18c72-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="18c72-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18c72-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="18c72-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18c72-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18c72-139">CommonParameters</span></span>
<span data-ttu-id="18c72-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="18c72-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18c72-141">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="18c72-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18c72-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="18c72-142">INPUTS</span></span>

### <span data-ttu-id="18c72-143">System. String</span><span class="sxs-lookup"><span data-stu-id="18c72-143">System.String</span></span>

## <span data-ttu-id="18c72-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18c72-144">OUTPUTS</span></span>

### <span data-ttu-id="18c72-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="18c72-145">System.Boolean</span></span>

## <span data-ttu-id="18c72-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="18c72-146">NOTES</span></span>

## <span data-ttu-id="18c72-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18c72-147">RELATED LINKS</span></span>

[<span data-ttu-id="18c72-148">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="18c72-148">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="18c72-149">Új – AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="18c72-149">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="18c72-150">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="18c72-150">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


