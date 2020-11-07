---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
ms.openlocfilehash: 68c4f94ea4fee91c03ab0c65cbcba0f025c3c43b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672142"
---
# <span data-ttu-id="ff5b6-101">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ff5b6-101">Remove-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="ff5b6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ff5b6-102">SYNOPSIS</span></span>
<span data-ttu-id="ff5b6-103">Házirend-definíció eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="ff5b6-103">Removes a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff5b6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ff5b6-104">SYNTAX</span></span>

### <span data-ttu-id="ff5b6-105">RemoveByPolicyDefinitionName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ff5b6-105">RemoveByPolicyDefinitionName (Default)</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff5b6-106">RemoveByPolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="ff5b6-106">RemoveByPolicyDefinitionId</span></span>
```
Remove-AzureRmPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff5b6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ff5b6-107">DESCRIPTION</span></span>
<span data-ttu-id="ff5b6-108">A **Remove-AzureRmPolicyDefinition** parancsmag eltávolítja a házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="ff5b6-108">The **Remove-AzureRmPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="ff5b6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ff5b6-109">EXAMPLES</span></span>

### <span data-ttu-id="ff5b6-110">1. példa: a házirend-definíció eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="ff5b6-110">Example 1: Remove the policy definition by name</span></span>
```
PS C:\>Remove-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="ff5b6-111">Ez a parancs eltávolítja a megadott házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="ff5b6-111">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="ff5b6-112">2. példa: a házirend-definíció eltávolítása erőforrás-AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="ff5b6-112">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition" 
PS C:\> Remove-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="ff5b6-113">Az első parancs az Get-AzureRmPolicyDefinition parancsmag használatával megkapja a VMPolicyDefinition nevű házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="ff5b6-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="ff5b6-114">A parancs a $PolicyDefinition változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ff5b6-114">The command stores it in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="ff5b6-115">A második parancs eltávolítja az $PolicyDefinition **ResourceId** tulajdonsága által azonosított házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="ff5b6-115">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="ff5b6-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ff5b6-116">PARAMETERS</span></span>

### <span data-ttu-id="ff5b6-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ff5b6-117">-ApiVersion</span></span>
<span data-ttu-id="ff5b6-118">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff5b6-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="ff5b6-119">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="ff5b6-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="ff5b6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff5b6-120">-DefaultProfile</span></span>
<span data-ttu-id="ff5b6-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ff5b6-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff5b6-122">-Force</span><span class="sxs-lookup"><span data-stu-id="ff5b6-122">-Force</span></span>
<span data-ttu-id="ff5b6-123">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="ff5b6-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ff5b6-124">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="ff5b6-124">-Id</span></span>
<span data-ttu-id="ff5b6-125">Annak a házirend-definíciónak a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amely a parancsmag eltávolítását okozta.</span><span class="sxs-lookup"><span data-stu-id="ff5b6-125">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyDefinitionId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff5b6-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ff5b6-126">-InformationAction</span></span>
<span data-ttu-id="ff5b6-127">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="ff5b6-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ff5b6-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ff5b6-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ff5b6-129">Folytassa</span><span class="sxs-lookup"><span data-stu-id="ff5b6-129">Continue</span></span>
- <span data-ttu-id="ff5b6-130">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="ff5b6-130">Ignore</span></span>
- <span data-ttu-id="ff5b6-131">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="ff5b6-131">Inquire</span></span>
- <span data-ttu-id="ff5b6-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ff5b6-132">SilentlyContinue</span></span>
- <span data-ttu-id="ff5b6-133">állj</span><span class="sxs-lookup"><span data-stu-id="ff5b6-133">Stop</span></span>
- <span data-ttu-id="ff5b6-134">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="ff5b6-134">Suspend</span></span>

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

### <span data-ttu-id="ff5b6-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ff5b6-135">-InformationVariable</span></span>
<span data-ttu-id="ff5b6-136">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="ff5b6-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ff5b6-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ff5b6-137">-Name</span></span>
<span data-ttu-id="ff5b6-138">Annak a házirend-definíciónak a nevét adja meg, amely a parancsmag eltávolítását okozta.</span><span class="sxs-lookup"><span data-stu-id="ff5b6-138">Specifies the name of the policy definition that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyDefinitionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff5b6-139">-Pre</span><span class="sxs-lookup"><span data-stu-id="ff5b6-139">-Pre</span></span>
<span data-ttu-id="ff5b6-140">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="ff5b6-140">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ff5b6-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ff5b6-141">-Confirm</span></span>
<span data-ttu-id="ff5b6-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ff5b6-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff5b6-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff5b6-143">-WhatIf</span></span>
<span data-ttu-id="ff5b6-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ff5b6-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff5b6-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ff5b6-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff5b6-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff5b6-146">CommonParameters</span></span>
<span data-ttu-id="ff5b6-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ff5b6-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff5b6-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff5b6-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff5b6-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff5b6-149">INPUTS</span></span>

### <span data-ttu-id="ff5b6-150">Nincs</span><span class="sxs-lookup"><span data-stu-id="ff5b6-150">None</span></span>
<span data-ttu-id="ff5b6-151">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="ff5b6-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ff5b6-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff5b6-152">OUTPUTS</span></span>

### <span data-ttu-id="ff5b6-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ff5b6-153">System.Boolean</span></span>

## <span data-ttu-id="ff5b6-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ff5b6-154">NOTES</span></span>

## <span data-ttu-id="ff5b6-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ff5b6-155">RELATED LINKS</span></span>

[<span data-ttu-id="ff5b6-156">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ff5b6-156">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="ff5b6-157">Új – AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ff5b6-157">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="ff5b6-158">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ff5b6-158">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


