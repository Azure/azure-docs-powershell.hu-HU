---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: 00ec24c13a5c51db7da63cd1d94c01f251a7e289
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300533"
---
# <span data-ttu-id="88361-101">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="88361-101">Remove-AzPolicyAssignment</span></span>

## <span data-ttu-id="88361-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="88361-102">SYNOPSIS</span></span>
<span data-ttu-id="88361-103">Házirend-hozzárendelés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="88361-103">Removes a policy assignment.</span></span>

## <span data-ttu-id="88361-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="88361-104">SYNTAX</span></span>

### <span data-ttu-id="88361-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="88361-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyAssignment -Name <String> [-Scope <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88361-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="88361-106">IdParameterSet</span></span>
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88361-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88361-107">InputObjectParameterSet</span></span>
```
Remove-AzPolicyAssignment -InputObject <PsPolicyAssignment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88361-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="88361-108">DESCRIPTION</span></span>
<span data-ttu-id="88361-109">A **Remove-AzPolicyAssignment** parancsmag eltávolítja a megadott házirend-feladatot.</span><span class="sxs-lookup"><span data-stu-id="88361-109">The **Remove-AzPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="88361-110">Példák</span><span class="sxs-lookup"><span data-stu-id="88361-110">EXAMPLES</span></span>

### <span data-ttu-id="88361-111">1. példa: házirend-hozzárendelés eltávolítása név és hatókör szerint</span><span class="sxs-lookup"><span data-stu-id="88361-111">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Confirm
```

<span data-ttu-id="88361-112">Az első parancs az Get-AzResourceGroup parancsmag segítségével a ResourceGroup11 nevű erőforráscsoportot kapja.</span><span class="sxs-lookup"><span data-stu-id="88361-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="88361-113">A parancs az objektumot a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="88361-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="88361-114">A második parancs eltávolítja a PolicyAssignment07 nevű olyan házirend-hozzárendelést, amely egy erőforrás-csoport szintjén van társítva.</span><span class="sxs-lookup"><span data-stu-id="88361-114">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="88361-115">A $ResourceGroup **ResourceId** tulajdonság azonosítja az erőforráscsoport értékét.</span><span class="sxs-lookup"><span data-stu-id="88361-115">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="88361-116">2. példa: házirend-hozzárendelés eltávolítása AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="88361-116">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Confirm
```

<span data-ttu-id="88361-117">Az első parancs beolvassa a ResourceGroup11 nevű erőforráscsoportot, majd az objektumot a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="88361-117">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="88361-118">A második parancs egy erőforráscsoport szintjén kapja meg a házirend-hozzárendelést, és a $PolicyAssignment változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="88361-118">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="88361-119">A $ResourceGroup **ResourceId** tulajdonság azonosítja az erőforráscsoport értékét.</span><span class="sxs-lookup"><span data-stu-id="88361-119">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="88361-120">A végleges parancs eltávolítja azt a házirend-feladatot, amelyet az $PolicyAssignment **ResourceId** tulajdonsága azonosít.</span><span class="sxs-lookup"><span data-stu-id="88361-120">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="88361-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="88361-121">PARAMETERS</span></span>

### <span data-ttu-id="88361-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="88361-122">-ApiVersion</span></span>
<span data-ttu-id="88361-123">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="88361-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="88361-124">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="88361-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="88361-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88361-125">-DefaultProfile</span></span>
<span data-ttu-id="88361-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="88361-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88361-127">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="88361-127">-Id</span></span>
<span data-ttu-id="88361-128">Annak a házirend-hozzárendelésnek a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="88361-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="88361-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88361-129">-InputObject</span></span>
<span data-ttu-id="88361-130">Az a házirend-hozzárendelési objektum, amely egy másik parancsmagból származó kimenetet távolítja el.</span><span class="sxs-lookup"><span data-stu-id="88361-130">The policy assignment object to remove that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="88361-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="88361-131">-Name</span></span>
<span data-ttu-id="88361-132">A parancsmag által eltávolított házirend-hozzárendelés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="88361-132">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="88361-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="88361-133">-Pre</span></span>
<span data-ttu-id="88361-134">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="88361-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="88361-135">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="88361-135">-Scope</span></span>
<span data-ttu-id="88361-136">Azt a hatókört adja meg, amelyen a házirendet alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="88361-136">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="88361-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="88361-137">-Confirm</span></span>
<span data-ttu-id="88361-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="88361-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88361-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88361-139">-WhatIf</span></span>
<span data-ttu-id="88361-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="88361-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88361-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="88361-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88361-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88361-142">CommonParameters</span></span>
<span data-ttu-id="88361-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="88361-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88361-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="88361-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88361-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="88361-145">INPUTS</span></span>

### <span data-ttu-id="88361-146">System. String</span><span class="sxs-lookup"><span data-stu-id="88361-146">System.String</span></span>

## <span data-ttu-id="88361-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="88361-147">OUTPUTS</span></span>

### <span data-ttu-id="88361-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="88361-148">System.Boolean</span></span>

## <span data-ttu-id="88361-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="88361-149">NOTES</span></span>

## <span data-ttu-id="88361-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="88361-150">RELATED LINKS</span></span>

[<span data-ttu-id="88361-151">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="88361-151">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="88361-152">Új – AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="88361-152">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="88361-153">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="88361-153">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


