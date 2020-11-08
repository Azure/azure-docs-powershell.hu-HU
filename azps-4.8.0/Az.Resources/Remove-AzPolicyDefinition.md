---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: c7d292a983090d8be22e159fbca6e423778b21f6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180948"
---
# <span data-ttu-id="7a84c-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7a84c-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="7a84c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7a84c-102">SYNOPSIS</span></span>
<span data-ttu-id="7a84c-103">Házirend-definíció eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="7a84c-103">Removes a policy definition.</span></span>

## <span data-ttu-id="7a84c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7a84c-104">SYNTAX</span></span>

### <span data-ttu-id="7a84c-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7a84c-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a84c-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a84c-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a84c-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a84c-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a84c-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a84c-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a84c-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a84c-109">InputObjectParameterSet</span></span>
```
Remove-AzPolicyDefinition [-Force] -InputObject <PsPolicyDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a84c-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="7a84c-110">DESCRIPTION</span></span>
<span data-ttu-id="7a84c-111">A **Remove-AzPolicyDefinition** parancsmag eltávolítja a házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="7a84c-111">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="7a84c-112">Példák</span><span class="sxs-lookup"><span data-stu-id="7a84c-112">EXAMPLES</span></span>

### <span data-ttu-id="7a84c-113">1. példa: a házirend-definíció eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="7a84c-113">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="7a84c-114">Ez a parancs eltávolítja a megadott házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="7a84c-114">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="7a84c-115">2. példa: a házirend-definíció eltávolítása erőforrás-AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="7a84c-115">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="7a84c-116">Az első parancs az Get-AzPolicyDefinition parancsmag használatával megkapja a VMPolicyDefinition nevű házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="7a84c-116">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="7a84c-117">A parancs a $PolicyDefinition változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7a84c-117">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="7a84c-118">A második parancs eltávolítja az $PolicyDefinition **ResourceId** tulajdonsága által azonosított házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="7a84c-118">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="7a84c-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7a84c-119">PARAMETERS</span></span>

### <span data-ttu-id="7a84c-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7a84c-120">-ApiVersion</span></span>
<span data-ttu-id="7a84c-121">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7a84c-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="7a84c-122">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="7a84c-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="7a84c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a84c-123">-DefaultProfile</span></span>
<span data-ttu-id="7a84c-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7a84c-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a84c-125">-Force</span><span class="sxs-lookup"><span data-stu-id="7a84c-125">-Force</span></span>
<span data-ttu-id="7a84c-126">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="7a84c-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7a84c-127">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="7a84c-127">-Id</span></span>
<span data-ttu-id="7a84c-128">Annak a házirend-definíciónak a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amely a parancsmag eltávolítását okozta.</span><span class="sxs-lookup"><span data-stu-id="7a84c-128">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7a84c-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a84c-129">-InputObject</span></span>
<span data-ttu-id="7a84c-130">A házirend-definíciós objektum, amely egy másik parancsmagból származó kimenetet távolítja el.</span><span class="sxs-lookup"><span data-stu-id="7a84c-130">The policy definition object to remove that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a84c-131">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="7a84c-131">-ManagementGroupName</span></span>
<span data-ttu-id="7a84c-132">A törlendő házirend-definíciós kezelés csoport neve.</span><span class="sxs-lookup"><span data-stu-id="7a84c-132">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="7a84c-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7a84c-133">-Name</span></span>
<span data-ttu-id="7a84c-134">Annak a házirend-definíciónak a nevét adja meg, amely a parancsmag eltávolítását okozta.</span><span class="sxs-lookup"><span data-stu-id="7a84c-134">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7a84c-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="7a84c-135">-Pre</span></span>
<span data-ttu-id="7a84c-136">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="7a84c-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="7a84c-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7a84c-137">-SubscriptionId</span></span>
<span data-ttu-id="7a84c-138">A törlendő házirend-definíció előfizetési azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7a84c-138">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="7a84c-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7a84c-139">-Confirm</span></span>
<span data-ttu-id="7a84c-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7a84c-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a84c-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a84c-141">-WhatIf</span></span>
<span data-ttu-id="7a84c-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7a84c-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a84c-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7a84c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a84c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a84c-144">CommonParameters</span></span>
<span data-ttu-id="7a84c-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7a84c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a84c-146">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7a84c-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a84c-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a84c-147">INPUTS</span></span>

### <span data-ttu-id="7a84c-148">System. String</span><span class="sxs-lookup"><span data-stu-id="7a84c-148">System.String</span></span>

### <span data-ttu-id="7a84c-149">System. null ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7a84c-149">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="7a84c-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a84c-150">OUTPUTS</span></span>

### <span data-ttu-id="7a84c-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7a84c-151">System.Boolean</span></span>

## <span data-ttu-id="7a84c-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7a84c-152">NOTES</span></span>

## <span data-ttu-id="7a84c-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7a84c-153">RELATED LINKS</span></span>

[<span data-ttu-id="7a84c-154">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7a84c-154">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="7a84c-155">Új – AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7a84c-155">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="7a84c-156">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7a84c-156">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


