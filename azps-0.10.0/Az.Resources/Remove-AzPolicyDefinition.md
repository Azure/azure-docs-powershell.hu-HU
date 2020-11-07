---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: 8cd1ee1d8f32bd203e9fb2d8ac5d75c2d6b2938d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843245"
---
# <span data-ttu-id="a58a9-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a58a9-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="a58a9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a58a9-102">SYNOPSIS</span></span>
<span data-ttu-id="a58a9-103">Házirend-definíció eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="a58a9-103">Removes a policy definition.</span></span>

## <span data-ttu-id="a58a9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a58a9-104">SYNTAX</span></span>

### <span data-ttu-id="a58a9-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a58a9-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a58a9-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a58a9-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a58a9-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a58a9-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a58a9-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a58a9-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a58a9-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="a58a9-109">DESCRIPTION</span></span>
<span data-ttu-id="a58a9-110">A **Remove-AzPolicyDefinition** parancsmag eltávolítja a házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="a58a9-110">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="a58a9-111">Példák</span><span class="sxs-lookup"><span data-stu-id="a58a9-111">EXAMPLES</span></span>

### <span data-ttu-id="a58a9-112">1. példa: a házirend-definíció eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="a58a9-112">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="a58a9-113">Ez a parancs eltávolítja a megadott házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="a58a9-113">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="a58a9-114">2. példa: a házirend-definíció eltávolítása erőforrás-AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="a58a9-114">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="a58a9-115">Az első parancs az Get-AzPolicyDefinition parancsmag használatával megkapja a VMPolicyDefinition nevű házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="a58a9-115">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="a58a9-116">A parancs a $PolicyDefinition változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a58a9-116">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="a58a9-117">A második parancs eltávolítja az $PolicyDefinition **ResourceId** tulajdonsága által azonosított házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="a58a9-117">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="a58a9-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a58a9-118">PARAMETERS</span></span>

### <span data-ttu-id="a58a9-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a58a9-119">-ApiVersion</span></span>
<span data-ttu-id="a58a9-120">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a58a9-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a58a9-121">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="a58a9-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="a58a9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a58a9-122">-DefaultProfile</span></span>
<span data-ttu-id="a58a9-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a58a9-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a58a9-124">-Force</span><span class="sxs-lookup"><span data-stu-id="a58a9-124">-Force</span></span>
<span data-ttu-id="a58a9-125">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="a58a9-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a58a9-126">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="a58a9-126">-Id</span></span>
<span data-ttu-id="a58a9-127">Annak a házirend-definíciónak a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amely a parancsmag eltávolítását okozta.</span><span class="sxs-lookup"><span data-stu-id="a58a9-127">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a58a9-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a58a9-128">-InformationAction</span></span>
<span data-ttu-id="a58a9-129">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="a58a9-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="a58a9-130">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a58a9-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a58a9-131">Folytassa</span><span class="sxs-lookup"><span data-stu-id="a58a9-131">Continue</span></span>
- <span data-ttu-id="a58a9-132">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="a58a9-132">Ignore</span></span>
- <span data-ttu-id="a58a9-133">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="a58a9-133">Inquire</span></span>
- <span data-ttu-id="a58a9-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a58a9-134">SilentlyContinue</span></span>
- <span data-ttu-id="a58a9-135">állj</span><span class="sxs-lookup"><span data-stu-id="a58a9-135">Stop</span></span>
- <span data-ttu-id="a58a9-136">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="a58a9-136">Suspend</span></span>

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

### <span data-ttu-id="a58a9-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a58a9-137">-InformationVariable</span></span>
<span data-ttu-id="a58a9-138">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="a58a9-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a58a9-139">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="a58a9-139">-ManagementGroupName</span></span>
<span data-ttu-id="a58a9-140">A törlendő házirend-definíciós kezelés csoport neve.</span><span class="sxs-lookup"><span data-stu-id="a58a9-140">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="a58a9-141">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a58a9-141">-Name</span></span>
<span data-ttu-id="a58a9-142">Annak a házirend-definíciónak a nevét adja meg, amely a parancsmag eltávolítását okozta.</span><span class="sxs-lookup"><span data-stu-id="a58a9-142">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a58a9-143">-Pre</span><span class="sxs-lookup"><span data-stu-id="a58a9-143">-Pre</span></span>
<span data-ttu-id="a58a9-144">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="a58a9-144">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a58a9-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a58a9-145">-SubscriptionId</span></span>
<span data-ttu-id="a58a9-146">A törlendő házirend-definíció előfizetési azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a58a9-146">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="a58a9-147">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a58a9-147">-Confirm</span></span>
<span data-ttu-id="a58a9-148">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a58a9-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a58a9-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a58a9-149">-WhatIf</span></span>
<span data-ttu-id="a58a9-150">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a58a9-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a58a9-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a58a9-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a58a9-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a58a9-152">CommonParameters</span></span>
<span data-ttu-id="a58a9-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a58a9-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a58a9-154">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a58a9-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a58a9-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a58a9-155">INPUTS</span></span>

## <span data-ttu-id="a58a9-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a58a9-156">OUTPUTS</span></span>

## <span data-ttu-id="a58a9-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a58a9-157">NOTES</span></span>

## <span data-ttu-id="a58a9-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a58a9-158">RELATED LINKS</span></span>

[<span data-ttu-id="a58a9-159">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a58a9-159">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="a58a9-160">Új – AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a58a9-160">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="a58a9-161">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a58a9-161">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


