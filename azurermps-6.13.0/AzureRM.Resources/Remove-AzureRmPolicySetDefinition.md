---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 9fcae03dba32aff18d2863c557c5827cf3e9d95e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493942"
---
# <span data-ttu-id="b402b-101">Remove-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="b402b-101">Remove-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="b402b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b402b-102">SYNOPSIS</span></span>
<span data-ttu-id="b402b-103">Házirend-készlet definíciójának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b402b-103">Removes a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b402b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b402b-104">SYNTAX</span></span>

### <span data-ttu-id="b402b-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b402b-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b402b-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b402b-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzureRmPolicySetDefinition [-Name <String>] [-Force] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b402b-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b402b-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzureRmPolicySetDefinition [-Name <String>] [-Force] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b402b-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b402b-108">IdParameterSet</span></span>
```
Remove-AzureRmPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b402b-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="b402b-109">DESCRIPTION</span></span>
<span data-ttu-id="b402b-110">A **Remove-AzureRmPolicySetDefinition** parancsmag eltávolítja a házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="b402b-110">The **Remove-AzureRmPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="b402b-111">Példák</span><span class="sxs-lookup"><span data-stu-id="b402b-111">EXAMPLES</span></span>

### <span data-ttu-id="b402b-112">Példa 1: a házirend-készlet definíciójának eltávolítása erőforrás-AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="b402b-112">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Remove-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="b402b-113">Az első parancs a Get-AzureRmPolicySetDefinition parancsmag használatával kapja meg a házirend-készlet definícióját.</span><span class="sxs-lookup"><span data-stu-id="b402b-113">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="b402b-114">A parancs a $PolicySetDefinition változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b402b-114">The command stores it in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="b402b-115">A második parancs eltávolítja az $PolicySetDefinition **ResourceId** tulajdonsága által azonosított házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="b402b-115">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="b402b-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b402b-116">PARAMETERS</span></span>

### <span data-ttu-id="b402b-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b402b-117">-ApiVersion</span></span>
<span data-ttu-id="b402b-118">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b402b-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b402b-119">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="b402b-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="b402b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b402b-120">-DefaultProfile</span></span>
<span data-ttu-id="b402b-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b402b-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b402b-122">-Force</span><span class="sxs-lookup"><span data-stu-id="b402b-122">-Force</span></span>
<span data-ttu-id="b402b-123">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b402b-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b402b-124">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="b402b-124">-Id</span></span>
<span data-ttu-id="b402b-125">A teljes mértékben minősített házirend-definíciós azonosító, az előfizetést is beleszámítva.</span><span class="sxs-lookup"><span data-stu-id="b402b-125">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="b402b-126">például/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="b402b-126">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="b402b-127">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="b402b-127">-ManagementGroupName</span></span>
<span data-ttu-id="b402b-128">A törölni kívánt Policy set Definition (felügyeleti csoport) neve.</span><span class="sxs-lookup"><span data-stu-id="b402b-128">The name of the management group of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="b402b-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b402b-129">-Name</span></span>
<span data-ttu-id="b402b-130">A Policy set definition név.</span><span class="sxs-lookup"><span data-stu-id="b402b-130">The policy set definition name.</span></span>

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

### <span data-ttu-id="b402b-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="b402b-131">-Pre</span></span>
<span data-ttu-id="b402b-132">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="b402b-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b402b-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b402b-133">-SubscriptionId</span></span>
<span data-ttu-id="b402b-134">A törléshez a házirend-készlet definíciójának előfizetési azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b402b-134">The subscription ID of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="b402b-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b402b-135">-Confirm</span></span>
<span data-ttu-id="b402b-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b402b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b402b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b402b-137">-WhatIf</span></span>
<span data-ttu-id="b402b-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b402b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b402b-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b402b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b402b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b402b-140">CommonParameters</span></span>
<span data-ttu-id="b402b-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b402b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b402b-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b402b-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b402b-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b402b-143">INPUTS</span></span>

### <span data-ttu-id="b402b-144">System. String</span><span class="sxs-lookup"><span data-stu-id="b402b-144">System.String</span></span>

### <span data-ttu-id="b402b-145">System. null ' 1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b402b-145">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="b402b-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b402b-146">OUTPUTS</span></span>

### <span data-ttu-id="b402b-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b402b-147">System.Boolean</span></span>

## <span data-ttu-id="b402b-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b402b-148">NOTES</span></span>

## <span data-ttu-id="b402b-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b402b-149">RELATED LINKS</span></span>
