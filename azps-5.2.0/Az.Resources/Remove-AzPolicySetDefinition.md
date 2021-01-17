---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
ms.openlocfilehash: 551e30077fe1ce836f98c18d3c00976adc779f64
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345750"
---
# <span data-ttu-id="8ee4e-101">Remove-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="8ee4e-101">Remove-AzPolicySetDefinition</span></span>

## <span data-ttu-id="8ee4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ee4e-102">SYNOPSIS</span></span>
<span data-ttu-id="8ee4e-103">Eltávolít egy házirendkészlet-definíciót.</span><span class="sxs-lookup"><span data-stu-id="8ee4e-103">Removes a policy set definition.</span></span>

## <span data-ttu-id="8ee4e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8ee4e-104">SYNTAX</span></span>

### <span data-ttu-id="8ee4e-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8ee4e-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ee4e-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ee4e-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ee4e-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ee4e-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ee4e-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ee4e-108">IdParameterSet</span></span>
```
Remove-AzPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ee4e-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ee4e-109">InputObjectParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Force] -InputObject <PsPolicySetDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ee4e-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8ee4e-110">DESCRIPTION</span></span>
<span data-ttu-id="8ee4e-111">A **Remove-AzPolicySetDefinition parancsmag** eltávolítja a házirenddefiníciót.</span><span class="sxs-lookup"><span data-stu-id="8ee4e-111">The **Remove-AzPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="8ee4e-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8ee4e-112">EXAMPLES</span></span>

### <span data-ttu-id="8ee4e-113">1. példa: Házirendkészlet-definíció eltávolítása erőforrásazonosító szerint</span><span class="sxs-lookup"><span data-stu-id="8ee4e-113">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Remove-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="8ee4e-114">Az első parancs egy házirendkészlet-definíciót kap a Get-AzPolicySetDefinition parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="8ee4e-114">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="8ee4e-115">A parancs a $PolicySetDefinition tárolja.</span><span class="sxs-lookup"><span data-stu-id="8ee4e-115">The command stores it in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="8ee4e-116">A második parancs eltávolítja a házirendkészlet-definíciót, amelyet a szabály **ResourceId** tulajdonsága $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="8ee4e-116">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="8ee4e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ee4e-117">PARAMETERS</span></span>

### <span data-ttu-id="8ee4e-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8ee4e-118">-ApiVersion</span></span>
<span data-ttu-id="8ee4e-119">Ha be van állítva, az erőforrás-szolgáltató API-t használja.</span><span class="sxs-lookup"><span data-stu-id="8ee4e-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="8ee4e-120">Ha nincs megadva, az API-verziót a rendszer automatikusan a legújabb elérhetőként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="8ee4e-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="8ee4e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ee4e-121">-DefaultProfile</span></span>
<span data-ttu-id="8ee4e-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8ee4e-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ee4e-123">-Force</span><span class="sxs-lookup"><span data-stu-id="8ee4e-123">-Force</span></span>
<span data-ttu-id="8ee4e-124">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8ee4e-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8ee4e-125">-Id</span><span class="sxs-lookup"><span data-stu-id="8ee4e-125">-Id</span></span>
<span data-ttu-id="8ee4e-126">A házirendkészlet teljes definícióazonosítója, az előfizetéssel együtt.</span><span class="sxs-lookup"><span data-stu-id="8ee4e-126">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="8ee4e-127">pl. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="8ee4e-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="8ee4e-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ee4e-128">-InputObject</span></span>
<span data-ttu-id="8ee4e-129">A házirend-beállításdefiníciós objektum eltávolítja a kimenetet egy másik parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="8ee4e-129">The policy set definition object to remove that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ee4e-130">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="8ee4e-130">-ManagementGroupName</span></span>
<span data-ttu-id="8ee4e-131">A törölni kívánt házirendkészlet-definíció felügyeleti csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="8ee4e-131">The name of the management group of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="8ee4e-132">-Name</span><span class="sxs-lookup"><span data-stu-id="8ee4e-132">-Name</span></span>
<span data-ttu-id="8ee4e-133">A házirendkészlet definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="8ee4e-133">The policy set definition name.</span></span>

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

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ee4e-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="8ee4e-134">-Pre</span></span>
<span data-ttu-id="8ee4e-135">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="8ee4e-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="8ee4e-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8ee4e-136">-SubscriptionId</span></span>
<span data-ttu-id="8ee4e-137">A törölni kívánt házirendkészlet-definíció előfizetésazonosítója.</span><span class="sxs-lookup"><span data-stu-id="8ee4e-137">The subscription ID of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="8ee4e-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ee4e-138">-Confirm</span></span>
<span data-ttu-id="8ee4e-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8ee4e-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ee4e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ee4e-140">-WhatIf</span></span>
<span data-ttu-id="8ee4e-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8ee4e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ee4e-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8ee4e-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ee4e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ee4e-143">CommonParameters</span></span>
<span data-ttu-id="8ee4e-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ee4e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ee4e-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ee4e-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ee4e-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8ee4e-146">INPUTS</span></span>

### <span data-ttu-id="8ee4e-147">System.String</span><span class="sxs-lookup"><span data-stu-id="8ee4e-147">System.String</span></span>

### <span data-ttu-id="8ee4e-148">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8ee4e-148">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8ee4e-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ee4e-149">OUTPUTS</span></span>

### <span data-ttu-id="8ee4e-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8ee4e-150">System.Boolean</span></span>

## <span data-ttu-id="8ee4e-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8ee4e-151">NOTES</span></span>

## <span data-ttu-id="8ee4e-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8ee4e-152">RELATED LINKS</span></span>
