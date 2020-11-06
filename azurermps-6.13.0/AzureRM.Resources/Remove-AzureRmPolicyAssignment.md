---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
ms.openlocfilehash: 63b88096200c5db55f9c40a4ba839ffbf25c681d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495672"
---
# <span data-ttu-id="9aa02-101">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="9aa02-101">Remove-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="9aa02-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9aa02-102">SYNOPSIS</span></span>
<span data-ttu-id="9aa02-103">Házirend-hozzárendelés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9aa02-103">Removes a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9aa02-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9aa02-104">SYNTAX</span></span>

### <span data-ttu-id="9aa02-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9aa02-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmPolicyAssignment -Name <String> -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9aa02-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9aa02-106">IdParameterSet</span></span>
```
Remove-AzureRmPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9aa02-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9aa02-107">DESCRIPTION</span></span>
<span data-ttu-id="9aa02-108">A **Remove-AzureRmPolicyAssignment** parancsmag eltávolítja a megadott házirend-feladatot.</span><span class="sxs-lookup"><span data-stu-id="9aa02-108">The **Remove-AzureRmPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="9aa02-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9aa02-109">EXAMPLES</span></span>

### <span data-ttu-id="9aa02-110">1. példa: házirend-hozzárendelés eltávolítása név és hatókör szerint</span><span class="sxs-lookup"><span data-stu-id="9aa02-110">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzureRmPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="9aa02-111">Az első parancs az Get-AzureRMResourceGroup parancsmag segítségével a ResourceGroup11 nevű erőforráscsoportot kapja.</span><span class="sxs-lookup"><span data-stu-id="9aa02-111">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="9aa02-112">A parancs az objektumot a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9aa02-112">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="9aa02-113">A második parancs eltávolítja a PolicyAssignment07 nevű olyan házirend-hozzárendelést, amely egy erőforrás-csoport szintjén van társítva.</span><span class="sxs-lookup"><span data-stu-id="9aa02-113">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="9aa02-114">A $ResourceGroup **ResourceId** tulajdonság azonosítja az erőforráscsoport értékét.</span><span class="sxs-lookup"><span data-stu-id="9aa02-114">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="9aa02-115">2. példa: házirend-hozzárendelés eltávolítása AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="9aa02-115">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="9aa02-116">Az első parancs beolvassa a ResourceGroup11 nevű erőforráscsoportot, majd az objektumot a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9aa02-116">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="9aa02-117">A második parancs egy erőforráscsoport szintjén kapja meg a házirend-hozzárendelést, és a $PolicyAssignment változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9aa02-117">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="9aa02-118">A $ResourceGroup **ResourceId** tulajdonság azonosítja az erőforráscsoport értékét.</span><span class="sxs-lookup"><span data-stu-id="9aa02-118">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="9aa02-119">A végleges parancs eltávolítja azt a házirend-feladatot, amelyet az $PolicyAssignment **ResourceId** tulajdonsága azonosít.</span><span class="sxs-lookup"><span data-stu-id="9aa02-119">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="9aa02-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9aa02-120">PARAMETERS</span></span>

### <span data-ttu-id="9aa02-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9aa02-121">-ApiVersion</span></span>
<span data-ttu-id="9aa02-122">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9aa02-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="9aa02-123">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="9aa02-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="9aa02-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aa02-124">-DefaultProfile</span></span>
<span data-ttu-id="9aa02-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9aa02-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aa02-126">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="9aa02-126">-Id</span></span>
<span data-ttu-id="9aa02-127">Annak a házirend-hozzárendelésnek a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="9aa02-127">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9aa02-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9aa02-128">-InformationAction</span></span>
<span data-ttu-id="9aa02-129">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="9aa02-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="9aa02-130">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="9aa02-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9aa02-131">Folytassa</span><span class="sxs-lookup"><span data-stu-id="9aa02-131">Continue</span></span>
- <span data-ttu-id="9aa02-132">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="9aa02-132">Ignore</span></span>
- <span data-ttu-id="9aa02-133">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="9aa02-133">Inquire</span></span>
- <span data-ttu-id="9aa02-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9aa02-134">SilentlyContinue</span></span>
- <span data-ttu-id="9aa02-135">állj</span><span class="sxs-lookup"><span data-stu-id="9aa02-135">Stop</span></span>
- <span data-ttu-id="9aa02-136">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="9aa02-136">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aa02-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9aa02-137">-InformationVariable</span></span>
<span data-ttu-id="9aa02-138">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="9aa02-138">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aa02-139">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9aa02-139">-Name</span></span>
<span data-ttu-id="9aa02-140">A parancsmag által eltávolított házirend-hozzárendelés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9aa02-140">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9aa02-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="9aa02-141">-Pre</span></span>
<span data-ttu-id="9aa02-142">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="9aa02-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="9aa02-143">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="9aa02-143">-Scope</span></span>
<span data-ttu-id="9aa02-144">Azt a hatókört adja meg, amelyen a házirendet alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="9aa02-144">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="9aa02-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9aa02-145">-Confirm</span></span>
<span data-ttu-id="9aa02-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9aa02-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9aa02-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9aa02-147">-WhatIf</span></span>
<span data-ttu-id="9aa02-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9aa02-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9aa02-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9aa02-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9aa02-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aa02-150">CommonParameters</span></span>
<span data-ttu-id="9aa02-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9aa02-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aa02-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9aa02-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aa02-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9aa02-153">INPUTS</span></span>

## <span data-ttu-id="9aa02-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9aa02-154">OUTPUTS</span></span>

## <span data-ttu-id="9aa02-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9aa02-155">NOTES</span></span>

## <span data-ttu-id="9aa02-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9aa02-156">RELATED LINKS</span></span>

[<span data-ttu-id="9aa02-157">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="9aa02-157">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="9aa02-158">Új – AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="9aa02-158">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="9aa02-159">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="9aa02-159">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


