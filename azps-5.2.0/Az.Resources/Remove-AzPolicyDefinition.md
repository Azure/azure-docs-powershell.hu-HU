---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: c7d292a983090d8be22e159fbca6e423778b21f6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355518"
---
# <span data-ttu-id="bd405-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="bd405-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="bd405-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd405-102">SYNOPSIS</span></span>
<span data-ttu-id="bd405-103">Eltávolít egy házirenddefiníciót.</span><span class="sxs-lookup"><span data-stu-id="bd405-103">Removes a policy definition.</span></span>

## <span data-ttu-id="bd405-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bd405-104">SYNTAX</span></span>

### <span data-ttu-id="bd405-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bd405-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd405-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd405-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd405-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd405-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd405-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd405-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd405-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd405-109">InputObjectParameterSet</span></span>
```
Remove-AzPolicyDefinition [-Force] -InputObject <PsPolicyDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd405-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bd405-110">DESCRIPTION</span></span>
<span data-ttu-id="bd405-111">A **Remove-AzPolicyDefinition** parancsmag eltávolítja a házirend-definíciókat.</span><span class="sxs-lookup"><span data-stu-id="bd405-111">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="bd405-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bd405-112">EXAMPLES</span></span>

### <span data-ttu-id="bd405-113">1. példa: A házirenddefiníció eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="bd405-113">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="bd405-114">Ez a parancs eltávolítja a megadott házirenddefiníciót.</span><span class="sxs-lookup"><span data-stu-id="bd405-114">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="bd405-115">2. példa: Házirenddefiníció eltávolítása erőforrás-azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="bd405-115">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="bd405-116">Az első parancs egy VMPolicyDefinition nevű házirenddefiníciót kap a Get-AzPolicyDefinition parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="bd405-116">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="bd405-117">A parancs a $PolicyDefinition tárolja.</span><span class="sxs-lookup"><span data-stu-id="bd405-117">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="bd405-118">A második parancs eltávolítja a  házirend-definíciót, amelyet a $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="bd405-118">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="bd405-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd405-119">PARAMETERS</span></span>

### <span data-ttu-id="bd405-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bd405-120">-ApiVersion</span></span>
<span data-ttu-id="bd405-121">Az erőforrás-szolgáltató API-jának használnia kell verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bd405-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="bd405-122">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="bd405-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="bd405-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd405-123">-DefaultProfile</span></span>
<span data-ttu-id="bd405-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bd405-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd405-125">-Force</span><span class="sxs-lookup"><span data-stu-id="bd405-125">-Force</span></span>
<span data-ttu-id="bd405-126">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="bd405-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bd405-127">-Id</span><span class="sxs-lookup"><span data-stu-id="bd405-127">-Id</span></span>
<span data-ttu-id="bd405-128">A parancsmag által eltávolított házirenddefiníció teljes erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bd405-128">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bd405-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd405-129">-InputObject</span></span>
<span data-ttu-id="bd405-130">A másik parancsmagból származó kimenetet eltávolító házirenddefiníciós objektum.</span><span class="sxs-lookup"><span data-stu-id="bd405-130">The policy definition object to remove that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="bd405-131">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="bd405-131">-ManagementGroupName</span></span>
<span data-ttu-id="bd405-132">A törölni kívánt házirenddefiníció felügyeleti csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="bd405-132">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="bd405-133">-Name</span><span class="sxs-lookup"><span data-stu-id="bd405-133">-Name</span></span>
<span data-ttu-id="bd405-134">A parancsmag által eltávolított házirenddefiníció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bd405-134">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bd405-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="bd405-135">-Pre</span></span>
<span data-ttu-id="bd405-136">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="bd405-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="bd405-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bd405-137">-SubscriptionId</span></span>
<span data-ttu-id="bd405-138">A törölni kívánt házirend-definíció előfizetésazonosítója.</span><span class="sxs-lookup"><span data-stu-id="bd405-138">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="bd405-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd405-139">-Confirm</span></span>
<span data-ttu-id="bd405-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bd405-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd405-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd405-141">-WhatIf</span></span>
<span data-ttu-id="bd405-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bd405-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd405-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bd405-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd405-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd405-144">CommonParameters</span></span>
<span data-ttu-id="bd405-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd405-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd405-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd405-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd405-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd405-147">INPUTS</span></span>

### <span data-ttu-id="bd405-148">System.String</span><span class="sxs-lookup"><span data-stu-id="bd405-148">System.String</span></span>

### <span data-ttu-id="bd405-149">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bd405-149">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="bd405-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd405-150">OUTPUTS</span></span>

### <span data-ttu-id="bd405-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bd405-151">System.Boolean</span></span>

## <span data-ttu-id="bd405-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bd405-152">NOTES</span></span>

## <span data-ttu-id="bd405-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd405-153">RELATED LINKS</span></span>

[<span data-ttu-id="bd405-154">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="bd405-154">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="bd405-155">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="bd405-155">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="bd405-156">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="bd405-156">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


