---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: 8c7aa559ad6fde29c32f1958a4a0e2a6406ad42d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011761"
---
# <span data-ttu-id="9e900-101">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="9e900-101">Remove-AzPolicyAssignment</span></span>

## <span data-ttu-id="9e900-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9e900-102">SYNOPSIS</span></span>
<span data-ttu-id="9e900-103">Házirend-hozzárendelés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9e900-103">Removes a policy assignment.</span></span>

## <span data-ttu-id="9e900-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9e900-104">SYNTAX</span></span>

### <span data-ttu-id="9e900-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9e900-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyAssignment -Name <String> [-Scope <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e900-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e900-106">IdParameterSet</span></span>
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e900-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9e900-107">DESCRIPTION</span></span>
<span data-ttu-id="9e900-108">A **Remove-AzPolicyAssignment** parancsmag eltávolítja a megadott házirend-feladatot.</span><span class="sxs-lookup"><span data-stu-id="9e900-108">The **Remove-AzPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="9e900-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9e900-109">EXAMPLES</span></span>

### <span data-ttu-id="9e900-110">1. példa: házirend-hozzárendelés eltávolítása név és hatókör szerint</span><span class="sxs-lookup"><span data-stu-id="9e900-110">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="9e900-111">Az első parancs az Get-AzResourceGroup parancsmag segítségével a ResourceGroup11 nevű erőforráscsoportot kapja.</span><span class="sxs-lookup"><span data-stu-id="9e900-111">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="9e900-112">A parancs az objektumot a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9e900-112">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="9e900-113">A második parancs eltávolítja a PolicyAssignment07 nevű olyan házirend-hozzárendelést, amely egy erőforrás-csoport szintjén van társítva.</span><span class="sxs-lookup"><span data-stu-id="9e900-113">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="9e900-114">A $ResourceGroup **ResourceId** tulajdonság azonosítja az erőforráscsoport értékét.</span><span class="sxs-lookup"><span data-stu-id="9e900-114">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="9e900-115">2. példa: házirend-hozzárendelés eltávolítása AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="9e900-115">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="9e900-116">Az első parancs beolvassa a ResourceGroup11 nevű erőforráscsoportot, majd az objektumot a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9e900-116">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="9e900-117">A második parancs egy erőforráscsoport szintjén kapja meg a házirend-hozzárendelést, és a $PolicyAssignment változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9e900-117">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="9e900-118">A $ResourceGroup **ResourceId** tulajdonság azonosítja az erőforráscsoport értékét.</span><span class="sxs-lookup"><span data-stu-id="9e900-118">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="9e900-119">A végleges parancs eltávolítja azt a házirend-feladatot, amelyet az $PolicyAssignment **ResourceId** tulajdonsága azonosít.</span><span class="sxs-lookup"><span data-stu-id="9e900-119">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="9e900-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9e900-120">PARAMETERS</span></span>

### <span data-ttu-id="9e900-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9e900-121">-ApiVersion</span></span>
<span data-ttu-id="9e900-122">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e900-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="9e900-123">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="9e900-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="9e900-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e900-124">-DefaultProfile</span></span>
<span data-ttu-id="9e900-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9e900-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e900-126">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="9e900-126">-Id</span></span>
<span data-ttu-id="9e900-127">Annak a házirend-hozzárendelésnek a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="9e900-127">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9e900-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9e900-128">-Name</span></span>
<span data-ttu-id="9e900-129">A parancsmag által eltávolított házirend-hozzárendelés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e900-129">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9e900-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="9e900-130">-Pre</span></span>
<span data-ttu-id="9e900-131">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="9e900-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="9e900-132">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="9e900-132">-Scope</span></span>
<span data-ttu-id="9e900-133">Azt a hatókört adja meg, amelyen a házirendet alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="9e900-133">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="9e900-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9e900-134">-Confirm</span></span>
<span data-ttu-id="9e900-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9e900-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e900-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e900-136">-WhatIf</span></span>
<span data-ttu-id="9e900-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9e900-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e900-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9e900-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e900-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e900-139">CommonParameters</span></span>
<span data-ttu-id="9e900-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9e900-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e900-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9e900-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e900-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e900-142">INPUTS</span></span>

### <span data-ttu-id="9e900-143">System. String</span><span class="sxs-lookup"><span data-stu-id="9e900-143">System.String</span></span>

## <span data-ttu-id="9e900-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e900-144">OUTPUTS</span></span>

### <span data-ttu-id="9e900-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9e900-145">System.Boolean</span></span>

## <span data-ttu-id="9e900-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9e900-146">NOTES</span></span>

## <span data-ttu-id="9e900-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e900-147">RELATED LINKS</span></span>

[<span data-ttu-id="9e900-148">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="9e900-148">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="9e900-149">Új – AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="9e900-149">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="9e900-150">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="9e900-150">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


