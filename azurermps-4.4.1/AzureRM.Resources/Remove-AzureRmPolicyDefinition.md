---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
ms.openlocfilehash: 46323b260330ca84ee1ac2426ee7b6e2ab474f21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679949"
---
# <span data-ttu-id="bcf72-101">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="bcf72-101">Remove-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="bcf72-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bcf72-102">SYNOPSIS</span></span>
<span data-ttu-id="bcf72-103">Házirend-definíció eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="bcf72-103">Removes a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcf72-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bcf72-104">SYNTAX</span></span>

### <span data-ttu-id="bcf72-105">A Policy definition Name paraméter beállítása.</span><span class="sxs-lookup"><span data-stu-id="bcf72-105">The policy definition name parameter set.</span></span> <span data-ttu-id="bcf72-106">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="bcf72-106">(Default)</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcf72-107">A házirend-definíciós azonosító paraméter beállítása.</span><span class="sxs-lookup"><span data-stu-id="bcf72-107">The policy definition Id parameter set.</span></span>
```
Remove-AzureRmPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcf72-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="bcf72-108">DESCRIPTION</span></span>
<span data-ttu-id="bcf72-109">A **Remove-AzureRmPolicyDefinition** parancsmag eltávolítja a házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="bcf72-109">The **Remove-AzureRmPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="bcf72-110">Példák</span><span class="sxs-lookup"><span data-stu-id="bcf72-110">EXAMPLES</span></span>

### <span data-ttu-id="bcf72-111">1. példa: a házirend-definíció eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="bcf72-111">Example 1: Remove the policy definition by name</span></span>
```
PS C:\>Remove-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="bcf72-112">Ez a parancs eltávolítja a megadott házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="bcf72-112">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="bcf72-113">2. példa: a házirend-definíció eltávolítása erőforrás-AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="bcf72-113">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition" 
PS C:\> Remove-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="bcf72-114">Az első parancs az Get-AzureRmPolicyDefinition parancsmag használatával megkapja a VMPolicyDefinition nevű házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="bcf72-114">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="bcf72-115">A parancs a $PolicyDefinition változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="bcf72-115">The command stores it in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="bcf72-116">A második parancs eltávolítja az $PolicyDefinition **ResourceId** tulajdonsága által azonosított házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="bcf72-116">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="bcf72-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bcf72-117">PARAMETERS</span></span>

### <span data-ttu-id="bcf72-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bcf72-118">-ApiVersion</span></span>
<span data-ttu-id="bcf72-119">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="bcf72-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="bcf72-120">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="bcf72-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="bcf72-121">-Force</span><span class="sxs-lookup"><span data-stu-id="bcf72-121">-Force</span></span>
<span data-ttu-id="bcf72-122">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="bcf72-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bcf72-123">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="bcf72-123">-Id</span></span>
<span data-ttu-id="bcf72-124">Annak a házirend-definíciónak a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amely a parancsmag eltávolítását okozta.</span><span class="sxs-lookup"><span data-stu-id="bcf72-124">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcf72-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="bcf72-125">-InformationAction</span></span>
<span data-ttu-id="bcf72-126">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="bcf72-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="bcf72-127">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="bcf72-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bcf72-128">Folytassa</span><span class="sxs-lookup"><span data-stu-id="bcf72-128">Continue</span></span>
- <span data-ttu-id="bcf72-129">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="bcf72-129">Ignore</span></span>
- <span data-ttu-id="bcf72-130">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="bcf72-130">Inquire</span></span>
- <span data-ttu-id="bcf72-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="bcf72-131">SilentlyContinue</span></span>
- <span data-ttu-id="bcf72-132">állj</span><span class="sxs-lookup"><span data-stu-id="bcf72-132">Stop</span></span>
- <span data-ttu-id="bcf72-133">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="bcf72-133">Suspend</span></span>

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

### <span data-ttu-id="bcf72-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="bcf72-134">-InformationVariable</span></span>
<span data-ttu-id="bcf72-135">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="bcf72-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="bcf72-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bcf72-136">-Name</span></span>
<span data-ttu-id="bcf72-137">Annak a házirend-definíciónak a nevét adja meg, amely a parancsmag eltávolítását okozta.</span><span class="sxs-lookup"><span data-stu-id="bcf72-137">Specifies the name of the policy definition that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcf72-138">-Pre</span><span class="sxs-lookup"><span data-stu-id="bcf72-138">-Pre</span></span>
<span data-ttu-id="bcf72-139">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="bcf72-139">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="bcf72-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bcf72-140">-Confirm</span></span>
<span data-ttu-id="bcf72-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bcf72-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcf72-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcf72-142">-WhatIf</span></span>
<span data-ttu-id="bcf72-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bcf72-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcf72-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bcf72-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcf72-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcf72-145">-DefaultProfile</span></span>
<span data-ttu-id="bcf72-146">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bcf72-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcf72-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcf72-147">CommonParameters</span></span>
<span data-ttu-id="bcf72-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bcf72-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcf72-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcf72-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcf72-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bcf72-150">INPUTS</span></span>

## <span data-ttu-id="bcf72-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bcf72-151">OUTPUTS</span></span>

### <span data-ttu-id="bcf72-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bcf72-152">System.Boolean</span></span>

## <span data-ttu-id="bcf72-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bcf72-153">NOTES</span></span>

## <span data-ttu-id="bcf72-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bcf72-154">RELATED LINKS</span></span>

[<span data-ttu-id="bcf72-155">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="bcf72-155">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="bcf72-156">Új – AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="bcf72-156">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="bcf72-157">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="bcf72-157">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


