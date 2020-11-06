---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
ms.openlocfilehash: d78cf9d28c453626c26656b9f9280f5c52695434
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495258"
---
# <span data-ttu-id="e6d80-101">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e6d80-101">Remove-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="e6d80-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e6d80-102">SYNOPSIS</span></span>
<span data-ttu-id="e6d80-103">Házirend-hozzárendelés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e6d80-103">Removes a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6d80-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e6d80-104">SYNTAX</span></span>

### <span data-ttu-id="e6d80-105">RemoveByPolicyAssignmentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e6d80-105">RemoveByPolicyAssignmentName (Default)</span></span>
```
Remove-AzureRmPolicyAssignment -Name <String> -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6d80-106">RemoveByPolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="e6d80-106">RemoveByPolicyAssignmentId</span></span>
```
Remove-AzureRmPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6d80-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e6d80-107">DESCRIPTION</span></span>
<span data-ttu-id="e6d80-108">A **Remove-AzureRmPolicyAssignment** parancsmag eltávolítja a megadott házirend-feladatot.</span><span class="sxs-lookup"><span data-stu-id="e6d80-108">The **Remove-AzureRmPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="e6d80-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e6d80-109">EXAMPLES</span></span>

### <span data-ttu-id="e6d80-110">1. példa: házirend-hozzárendelés eltávolítása név és hatókör szerint</span><span class="sxs-lookup"><span data-stu-id="e6d80-110">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Remove-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="e6d80-111">Az első parancs az Get-AzureRMResourceGroup parancsmag segítségével a ResourceGroup11 nevű erőforráscsoportot kapja.</span><span class="sxs-lookup"><span data-stu-id="e6d80-111">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="e6d80-112">A parancs az objektumot a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e6d80-112">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="e6d80-113">A második parancs eltávolítja a PolicyAssignment07 nevű olyan házirend-hozzárendelést, amely egy erőforrás-csoport szintjén van társítva.</span><span class="sxs-lookup"><span data-stu-id="e6d80-113">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="e6d80-114">A $ResourceGroup **ResourceId** tulajdonság azonosítja az erőforráscsoport értékét.</span><span class="sxs-lookup"><span data-stu-id="e6d80-114">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="e6d80-115">2. példa: házirend-hozzárendelés eltávolítása AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="e6d80-115">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11" 
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="e6d80-116">Az első parancs beolvassa a ResourceGroup11 nevű erőforráscsoportot, majd az objektumot a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e6d80-116">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="e6d80-117">A második parancs egy erőforráscsoport szintjén kapja meg a házirend-hozzárendelést, és a $PolicyAssignment változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e6d80-117">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="e6d80-118">A $ResourceGroup **ResourceId** tulajdonság azonosítja az erőforráscsoport értékét.</span><span class="sxs-lookup"><span data-stu-id="e6d80-118">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

<span data-ttu-id="e6d80-119">A végleges parancs eltávolítja azt a házirend-feladatot, amelyet az $PolicyAssignment **ResourceId** tulajdonsága azonosít.</span><span class="sxs-lookup"><span data-stu-id="e6d80-119">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="e6d80-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e6d80-120">PARAMETERS</span></span>

### <span data-ttu-id="e6d80-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e6d80-121">-ApiVersion</span></span>
<span data-ttu-id="e6d80-122">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e6d80-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="e6d80-123">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="e6d80-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6d80-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6d80-124">-DefaultProfile</span></span>
<span data-ttu-id="e6d80-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e6d80-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6d80-126">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="e6d80-126">-Id</span></span>
<span data-ttu-id="e6d80-127">Annak a házirend-hozzárendelésnek a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="e6d80-127">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyAssignmentId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6d80-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e6d80-128">-InformationAction</span></span>
<span data-ttu-id="e6d80-129">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="e6d80-129">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e6d80-130">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e6d80-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e6d80-131">Folytassa</span><span class="sxs-lookup"><span data-stu-id="e6d80-131">Continue</span></span>
- <span data-ttu-id="e6d80-132">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="e6d80-132">Ignore</span></span>
- <span data-ttu-id="e6d80-133">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="e6d80-133">Inquire</span></span>
- <span data-ttu-id="e6d80-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e6d80-134">SilentlyContinue</span></span>
- <span data-ttu-id="e6d80-135">állj</span><span class="sxs-lookup"><span data-stu-id="e6d80-135">Stop</span></span>
- <span data-ttu-id="e6d80-136">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="e6d80-136">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6d80-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e6d80-137">-InformationVariable</span></span>
<span data-ttu-id="e6d80-138">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="e6d80-138">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6d80-139">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e6d80-139">-Name</span></span>
<span data-ttu-id="e6d80-140">A parancsmag által eltávolított házirend-hozzárendelés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e6d80-140">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6d80-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="e6d80-141">-Pre</span></span>
<span data-ttu-id="e6d80-142">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="e6d80-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6d80-143">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="e6d80-143">-Scope</span></span>
<span data-ttu-id="e6d80-144">Azt a hatókört adja meg, amelyen a házirendet alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="e6d80-144">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6d80-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e6d80-145">-Confirm</span></span>
<span data-ttu-id="e6d80-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e6d80-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6d80-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6d80-147">-WhatIf</span></span>
<span data-ttu-id="e6d80-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e6d80-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6d80-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e6d80-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6d80-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6d80-150">CommonParameters</span></span>
<span data-ttu-id="e6d80-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e6d80-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6d80-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6d80-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6d80-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6d80-153">INPUTS</span></span>

### <span data-ttu-id="e6d80-154">Nincs</span><span class="sxs-lookup"><span data-stu-id="e6d80-154">None</span></span>
<span data-ttu-id="e6d80-155">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="e6d80-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e6d80-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6d80-156">OUTPUTS</span></span>

### <span data-ttu-id="e6d80-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e6d80-157">System.Boolean</span></span>

## <span data-ttu-id="e6d80-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e6d80-158">NOTES</span></span>

## <span data-ttu-id="e6d80-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6d80-159">RELATED LINKS</span></span>

[<span data-ttu-id="e6d80-160">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e6d80-160">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="e6d80-161">Új – AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e6d80-161">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="e6d80-162">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e6d80-162">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


