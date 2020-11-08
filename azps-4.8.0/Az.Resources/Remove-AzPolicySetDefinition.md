---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
ms.openlocfilehash: 551e30077fe1ce836f98c18d3c00976adc779f64
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180947"
---
# <span data-ttu-id="ef8ca-101">Remove-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="ef8ca-101">Remove-AzPolicySetDefinition</span></span>

## <span data-ttu-id="ef8ca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ef8ca-102">SYNOPSIS</span></span>
<span data-ttu-id="ef8ca-103">Házirend-készlet definíciójának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ef8ca-103">Removes a policy set definition.</span></span>

## <span data-ttu-id="ef8ca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ef8ca-104">SYNTAX</span></span>

### <span data-ttu-id="ef8ca-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ef8ca-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef8ca-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef8ca-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef8ca-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef8ca-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef8ca-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef8ca-108">IdParameterSet</span></span>
```
Remove-AzPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef8ca-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef8ca-109">InputObjectParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Force] -InputObject <PsPolicySetDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef8ca-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="ef8ca-110">DESCRIPTION</span></span>
<span data-ttu-id="ef8ca-111">A **Remove-AzPolicySetDefinition** parancsmag eltávolítja a házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="ef8ca-111">The **Remove-AzPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="ef8ca-112">Példák</span><span class="sxs-lookup"><span data-stu-id="ef8ca-112">EXAMPLES</span></span>

### <span data-ttu-id="ef8ca-113">Példa 1: a házirend-készlet definíciójának eltávolítása erőforrás-AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="ef8ca-113">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Remove-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="ef8ca-114">Az első parancs a Get-AzPolicySetDefinition parancsmag használatával kapja meg a házirend-készlet definícióját.</span><span class="sxs-lookup"><span data-stu-id="ef8ca-114">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="ef8ca-115">A parancs a $PolicySetDefinition változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ef8ca-115">The command stores it in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="ef8ca-116">A második parancs eltávolítja az $PolicySetDefinition **ResourceId** tulajdonsága által azonosított házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="ef8ca-116">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="ef8ca-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ef8ca-117">PARAMETERS</span></span>

### <span data-ttu-id="ef8ca-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ef8ca-118">-ApiVersion</span></span>
<span data-ttu-id="ef8ca-119">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef8ca-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="ef8ca-120">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="ef8ca-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="ef8ca-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef8ca-121">-DefaultProfile</span></span>
<span data-ttu-id="ef8ca-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ef8ca-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef8ca-123">-Force</span><span class="sxs-lookup"><span data-stu-id="ef8ca-123">-Force</span></span>
<span data-ttu-id="ef8ca-124">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ef8ca-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ef8ca-125">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="ef8ca-125">-Id</span></span>
<span data-ttu-id="ef8ca-126">A teljes mértékben minősített házirend-definíciós azonosító, az előfizetést is beleszámítva.</span><span class="sxs-lookup"><span data-stu-id="ef8ca-126">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="ef8ca-127">például/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="ef8ca-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="ef8ca-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef8ca-128">-InputObject</span></span>
<span data-ttu-id="ef8ca-129">A set definition objektum a másik parancsmagból származó kimenet eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="ef8ca-129">The policy set definition object to remove that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="ef8ca-130">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="ef8ca-130">-ManagementGroupName</span></span>
<span data-ttu-id="ef8ca-131">A törölni kívánt Policy set Definition (felügyeleti csoport) neve.</span><span class="sxs-lookup"><span data-stu-id="ef8ca-131">The name of the management group of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="ef8ca-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ef8ca-132">-Name</span></span>
<span data-ttu-id="ef8ca-133">A Policy set definition név.</span><span class="sxs-lookup"><span data-stu-id="ef8ca-133">The policy set definition name.</span></span>

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

### <span data-ttu-id="ef8ca-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="ef8ca-134">-Pre</span></span>
<span data-ttu-id="ef8ca-135">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="ef8ca-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ef8ca-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ef8ca-136">-SubscriptionId</span></span>
<span data-ttu-id="ef8ca-137">A törléshez a házirend-készlet definíciójának előfizetési azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ef8ca-137">The subscription ID of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="ef8ca-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ef8ca-138">-Confirm</span></span>
<span data-ttu-id="ef8ca-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ef8ca-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef8ca-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef8ca-140">-WhatIf</span></span>
<span data-ttu-id="ef8ca-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ef8ca-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef8ca-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ef8ca-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef8ca-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef8ca-143">CommonParameters</span></span>
<span data-ttu-id="ef8ca-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ef8ca-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef8ca-145">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ef8ca-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef8ca-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef8ca-146">INPUTS</span></span>

### <span data-ttu-id="ef8ca-147">System. String</span><span class="sxs-lookup"><span data-stu-id="ef8ca-147">System.String</span></span>

### <span data-ttu-id="ef8ca-148">System. null ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ef8ca-148">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ef8ca-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef8ca-149">OUTPUTS</span></span>

### <span data-ttu-id="ef8ca-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ef8ca-150">System.Boolean</span></span>

## <span data-ttu-id="ef8ca-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ef8ca-151">NOTES</span></span>

## <span data-ttu-id="ef8ca-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef8ca-152">RELATED LINKS</span></span>
