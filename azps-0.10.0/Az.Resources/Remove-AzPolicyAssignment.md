---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: 8fbf6c16dce1f8d96dcc9546c801e389493e7bcd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843254"
---
# <span data-ttu-id="ab0ec-101">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ab0ec-101">Remove-AzPolicyAssignment</span></span>

## <span data-ttu-id="ab0ec-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ab0ec-102">SYNOPSIS</span></span>
<span data-ttu-id="ab0ec-103">Házirend-hozzárendelés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ab0ec-103">Removes a policy assignment.</span></span>

## <span data-ttu-id="ab0ec-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ab0ec-104">SYNTAX</span></span>

### <span data-ttu-id="ab0ec-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ab0ec-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyAssignment -Name <String> -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab0ec-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab0ec-106">IdParameterSet</span></span>
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab0ec-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ab0ec-107">DESCRIPTION</span></span>
<span data-ttu-id="ab0ec-108">A **Remove-AzPolicyAssignment** parancsmag eltávolítja a megadott házirend-feladatot.</span><span class="sxs-lookup"><span data-stu-id="ab0ec-108">The **Remove-AzPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="ab0ec-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ab0ec-109">EXAMPLES</span></span>

### <span data-ttu-id="ab0ec-110">1. példa: házirend-hozzárendelés eltávolítása név és hatókör szerint</span><span class="sxs-lookup"><span data-stu-id="ab0ec-110">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="ab0ec-111">Az első parancs az Get-AzResourceGroup parancsmag segítségével a ResourceGroup11 nevű erőforráscsoportot kapja.</span><span class="sxs-lookup"><span data-stu-id="ab0ec-111">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="ab0ec-112">A parancs az objektumot a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ab0ec-112">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="ab0ec-113">A második parancs eltávolítja a PolicyAssignment07 nevű olyan házirend-hozzárendelést, amely egy erőforrás-csoport szintjén van társítva.</span><span class="sxs-lookup"><span data-stu-id="ab0ec-113">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="ab0ec-114">A $ResourceGroup **ResourceId** tulajdonság azonosítja az erőforráscsoport értékét.</span><span class="sxs-lookup"><span data-stu-id="ab0ec-114">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="ab0ec-115">2. példa: házirend-hozzárendelés eltávolítása AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="ab0ec-115">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="ab0ec-116">Az első parancs beolvassa a ResourceGroup11 nevű erőforráscsoportot, majd az objektumot a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ab0ec-116">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="ab0ec-117">A második parancs egy erőforráscsoport szintjén kapja meg a házirend-hozzárendelést, és a $PolicyAssignment változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ab0ec-117">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="ab0ec-118">A $ResourceGroup **ResourceId** tulajdonság azonosítja az erőforráscsoport értékét.</span><span class="sxs-lookup"><span data-stu-id="ab0ec-118">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="ab0ec-119">A végleges parancs eltávolítja azt a házirend-feladatot, amelyet az $PolicyAssignment **ResourceId** tulajdonsága azonosít.</span><span class="sxs-lookup"><span data-stu-id="ab0ec-119">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="ab0ec-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ab0ec-120">PARAMETERS</span></span>

### <span data-ttu-id="ab0ec-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ab0ec-121">-ApiVersion</span></span>
<span data-ttu-id="ab0ec-122">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab0ec-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="ab0ec-123">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="ab0ec-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="ab0ec-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab0ec-124">-DefaultProfile</span></span>
<span data-ttu-id="ab0ec-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ab0ec-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab0ec-126">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="ab0ec-126">-Id</span></span>
<span data-ttu-id="ab0ec-127">Annak a házirend-hozzárendelésnek a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="ab0ec-127">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ab0ec-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ab0ec-128">-InformationAction</span></span>
<span data-ttu-id="ab0ec-129">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="ab0ec-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="ab0ec-130">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ab0ec-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ab0ec-131">Folytassa</span><span class="sxs-lookup"><span data-stu-id="ab0ec-131">Continue</span></span>
- <span data-ttu-id="ab0ec-132">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="ab0ec-132">Ignore</span></span>
- <span data-ttu-id="ab0ec-133">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="ab0ec-133">Inquire</span></span>
- <span data-ttu-id="ab0ec-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ab0ec-134">SilentlyContinue</span></span>
- <span data-ttu-id="ab0ec-135">állj</span><span class="sxs-lookup"><span data-stu-id="ab0ec-135">Stop</span></span>
- <span data-ttu-id="ab0ec-136">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="ab0ec-136">Suspend</span></span>

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

### <span data-ttu-id="ab0ec-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ab0ec-137">-InformationVariable</span></span>
<span data-ttu-id="ab0ec-138">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="ab0ec-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ab0ec-139">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ab0ec-139">-Name</span></span>
<span data-ttu-id="ab0ec-140">A parancsmag által eltávolított házirend-hozzárendelés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab0ec-140">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ab0ec-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="ab0ec-141">-Pre</span></span>
<span data-ttu-id="ab0ec-142">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="ab0ec-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ab0ec-143">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="ab0ec-143">-Scope</span></span>
<span data-ttu-id="ab0ec-144">Azt a hatókört adja meg, amelyen a házirendet alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="ab0ec-144">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="ab0ec-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ab0ec-145">-Confirm</span></span>
<span data-ttu-id="ab0ec-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ab0ec-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab0ec-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab0ec-147">-WhatIf</span></span>
<span data-ttu-id="ab0ec-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ab0ec-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab0ec-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ab0ec-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab0ec-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab0ec-150">CommonParameters</span></span>
<span data-ttu-id="ab0ec-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ab0ec-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab0ec-152">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab0ec-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab0ec-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab0ec-153">INPUTS</span></span>

## <span data-ttu-id="ab0ec-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab0ec-154">OUTPUTS</span></span>

## <span data-ttu-id="ab0ec-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ab0ec-155">NOTES</span></span>

## <span data-ttu-id="ab0ec-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab0ec-156">RELATED LINKS</span></span>

[<span data-ttu-id="ab0ec-157">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ab0ec-157">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="ab0ec-158">Új – AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ab0ec-158">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="ab0ec-159">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ab0ec-159">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


