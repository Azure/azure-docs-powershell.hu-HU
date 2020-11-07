---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicysetdefinition
schema: 2.0.0
ms.openlocfilehash: 1096dc42ce02f3255c3c144852fc13029aebd113
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850541"
---
# <span data-ttu-id="86358-101">Remove-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="86358-101">Remove-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="86358-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="86358-102">SYNOPSIS</span></span>
<span data-ttu-id="86358-103">Házirend-készlet definíciójának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="86358-103">Removes a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86358-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="86358-104">SYNTAX</span></span>

### <span data-ttu-id="86358-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="86358-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86358-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="86358-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzureRmPolicySetDefinition [-Name <String>] [-Force] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="86358-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="86358-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzureRmPolicySetDefinition [-Name <String>] [-Force] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86358-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="86358-108">IdParameterSet</span></span>
```
Remove-AzureRmPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86358-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="86358-109">DESCRIPTION</span></span>
<span data-ttu-id="86358-110">A **Remove-AzureRmPolicySetDefinition** parancsmag eltávolítja a házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="86358-110">The **Remove-AzureRmPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="86358-111">Példák</span><span class="sxs-lookup"><span data-stu-id="86358-111">EXAMPLES</span></span>

### <span data-ttu-id="86358-112">Példa 1: a házirend-készlet definíciójának eltávolítása erőforrás-AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="86358-112">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Remove-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="86358-113">Az első parancs a Get-AzureRmPolicySetDefinition parancsmag használatával kapja meg a házirend-készlet definícióját.</span><span class="sxs-lookup"><span data-stu-id="86358-113">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="86358-114">A parancs a $PolicySetDefinition változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="86358-114">The command stores it in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="86358-115">A második parancs eltávolítja az $PolicySetDefinition **ResourceId** tulajdonsága által azonosított házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="86358-115">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="86358-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="86358-116">PARAMETERS</span></span>

### <span data-ttu-id="86358-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="86358-117">-ApiVersion</span></span>
<span data-ttu-id="86358-118">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="86358-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="86358-119">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="86358-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="86358-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86358-120">-DefaultProfile</span></span>
<span data-ttu-id="86358-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="86358-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86358-122">-Force</span><span class="sxs-lookup"><span data-stu-id="86358-122">-Force</span></span>
<span data-ttu-id="86358-123">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="86358-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="86358-124">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="86358-124">-Id</span></span>
<span data-ttu-id="86358-125">A teljes mértékben minősített házirend-definíciós azonosító, az előfizetést is beleszámítva.</span><span class="sxs-lookup"><span data-stu-id="86358-125">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="86358-126">például/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="86358-126">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="86358-127">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="86358-127">-ManagementGroupName</span></span>
<span data-ttu-id="86358-128">A törölni kívánt Policy set Definition (felügyeleti csoport) neve.</span><span class="sxs-lookup"><span data-stu-id="86358-128">The name of the management group of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="86358-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="86358-129">-Name</span></span>
<span data-ttu-id="86358-130">A Policy set definition név.</span><span class="sxs-lookup"><span data-stu-id="86358-130">The policy set definition name.</span></span>

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

### <span data-ttu-id="86358-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="86358-131">-Pre</span></span>
<span data-ttu-id="86358-132">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="86358-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="86358-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="86358-133">-SubscriptionId</span></span>
<span data-ttu-id="86358-134">A törléshez a házirend-készlet definíciójának előfizetési azonosítója.</span><span class="sxs-lookup"><span data-stu-id="86358-134">The subscription ID of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="86358-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="86358-135">-Confirm</span></span>
<span data-ttu-id="86358-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="86358-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86358-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86358-137">-WhatIf</span></span>
<span data-ttu-id="86358-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="86358-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86358-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="86358-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86358-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86358-140">CommonParameters</span></span>
<span data-ttu-id="86358-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="86358-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86358-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86358-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86358-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="86358-143">INPUTS</span></span>

### <span data-ttu-id="86358-144">System. String</span><span class="sxs-lookup"><span data-stu-id="86358-144">System.String</span></span>

### <span data-ttu-id="86358-145">System. null ' 1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="86358-145">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="86358-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86358-146">OUTPUTS</span></span>

### <span data-ttu-id="86358-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="86358-147">System.Boolean</span></span>

## <span data-ttu-id="86358-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="86358-148">NOTES</span></span>

## <span data-ttu-id="86358-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86358-149">RELATED LINKS</span></span>
