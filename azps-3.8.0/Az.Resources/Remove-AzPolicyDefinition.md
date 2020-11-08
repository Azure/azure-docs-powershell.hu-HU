---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: bd374f19a282ccafc3201a2965c33d4e8a3007ab
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011760"
---
# <span data-ttu-id="22989-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="22989-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="22989-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="22989-102">SYNOPSIS</span></span>
<span data-ttu-id="22989-103">Házirend-definíció eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="22989-103">Removes a policy definition.</span></span>

## <span data-ttu-id="22989-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="22989-104">SYNTAX</span></span>

### <span data-ttu-id="22989-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="22989-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22989-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="22989-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22989-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22989-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22989-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22989-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22989-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="22989-109">DESCRIPTION</span></span>
<span data-ttu-id="22989-110">A **Remove-AzPolicyDefinition** parancsmag eltávolítja a házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="22989-110">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="22989-111">Példák</span><span class="sxs-lookup"><span data-stu-id="22989-111">EXAMPLES</span></span>

### <span data-ttu-id="22989-112">1. példa: a házirend-definíció eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="22989-112">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="22989-113">Ez a parancs eltávolítja a megadott házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="22989-113">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="22989-114">2. példa: a házirend-definíció eltávolítása erőforrás-AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="22989-114">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="22989-115">Az első parancs az Get-AzPolicyDefinition parancsmag használatával megkapja a VMPolicyDefinition nevű házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="22989-115">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="22989-116">A parancs a $PolicyDefinition változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="22989-116">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="22989-117">A második parancs eltávolítja az $PolicyDefinition **ResourceId** tulajdonsága által azonosított házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="22989-117">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="22989-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="22989-118">PARAMETERS</span></span>

### <span data-ttu-id="22989-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="22989-119">-ApiVersion</span></span>
<span data-ttu-id="22989-120">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="22989-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="22989-121">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="22989-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="22989-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22989-122">-DefaultProfile</span></span>
<span data-ttu-id="22989-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="22989-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22989-124">-Force</span><span class="sxs-lookup"><span data-stu-id="22989-124">-Force</span></span>
<span data-ttu-id="22989-125">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="22989-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="22989-126">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="22989-126">-Id</span></span>
<span data-ttu-id="22989-127">Annak a házirend-definíciónak a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amely a parancsmag eltávolítását okozta.</span><span class="sxs-lookup"><span data-stu-id="22989-127">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="22989-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="22989-128">-ManagementGroupName</span></span>
<span data-ttu-id="22989-129">A törlendő házirend-definíciós kezelés csoport neve.</span><span class="sxs-lookup"><span data-stu-id="22989-129">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="22989-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="22989-130">-Name</span></span>
<span data-ttu-id="22989-131">Annak a házirend-definíciónak a nevét adja meg, amely a parancsmag eltávolítását okozta.</span><span class="sxs-lookup"><span data-stu-id="22989-131">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="22989-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="22989-132">-Pre</span></span>
<span data-ttu-id="22989-133">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="22989-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="22989-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="22989-134">-SubscriptionId</span></span>
<span data-ttu-id="22989-135">A törlendő házirend-definíció előfizetési azonosítója.</span><span class="sxs-lookup"><span data-stu-id="22989-135">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="22989-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="22989-136">-Confirm</span></span>
<span data-ttu-id="22989-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="22989-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22989-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22989-138">-WhatIf</span></span>
<span data-ttu-id="22989-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="22989-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22989-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="22989-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22989-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22989-141">CommonParameters</span></span>
<span data-ttu-id="22989-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="22989-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22989-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="22989-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22989-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="22989-144">INPUTS</span></span>

### <span data-ttu-id="22989-145">System. String</span><span class="sxs-lookup"><span data-stu-id="22989-145">System.String</span></span>

### <span data-ttu-id="22989-146">System. null ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="22989-146">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="22989-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22989-147">OUTPUTS</span></span>

### <span data-ttu-id="22989-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="22989-148">System.Boolean</span></span>

## <span data-ttu-id="22989-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="22989-149">NOTES</span></span>

## <span data-ttu-id="22989-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22989-150">RELATED LINKS</span></span>

[<span data-ttu-id="22989-151">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="22989-151">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="22989-152">Új – AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="22989-152">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="22989-153">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="22989-153">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


