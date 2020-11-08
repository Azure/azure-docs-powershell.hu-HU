---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
ms.openlocfilehash: ea7679b2e3214c55463f9f6fd4ccaf2b22d32841
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195611"
---
# <span data-ttu-id="924fb-101">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="924fb-101">Remove-AzScheduledQueryRule</span></span>

## <span data-ttu-id="924fb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="924fb-102">SYNOPSIS</span></span>
<span data-ttu-id="924fb-103">Naplózási riasztási szabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="924fb-103">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="924fb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="924fb-104">SYNTAX</span></span>

### <span data-ttu-id="924fb-105">ByRuleName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="924fb-105">ByRuleName (Default)</span></span>
```
Remove-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="924fb-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="924fb-106">ByInputObject</span></span>
```
Remove-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="924fb-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="924fb-107">ByResourceId</span></span>
```
Remove-AzScheduledQueryRule -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="924fb-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="924fb-108">DESCRIPTION</span></span>
<span data-ttu-id="924fb-109">Naplózási riasztási szabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="924fb-109">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="924fb-110">Példák</span><span class="sxs-lookup"><span data-stu-id="924fb-110">EXAMPLES</span></span>

### <span data-ttu-id="924fb-111">1. példa: szabály neve szerinti eltávolítás</span><span class="sxs-lookup"><span data-stu-id="924fb-111">Example 1: Remove by rule name</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1"
```

### <span data-ttu-id="924fb-112">2. példa: beviteli objektum szerinti eltávolítás</span><span class="sxs-lookup"><span data-stu-id="924fb-112">Example 2: Remove by input object</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -InputObject $PSScheduledQueryRuleResource
```

### <span data-ttu-id="924fb-113">3. példa: erőforrás-azonosító szerinti eltávolítás</span><span class="sxs-lookup"><span data-stu-id="924fb-113">Example 3: Remove by resource Id</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledQueryRules/LogAlertRule1"
```

## <span data-ttu-id="924fb-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="924fb-114">PARAMETERS</span></span>

### <span data-ttu-id="924fb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="924fb-115">-DefaultProfile</span></span>
<span data-ttu-id="924fb-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="924fb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="924fb-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="924fb-117">-InputObject</span></span>
<span data-ttu-id="924fb-118">Az ütemezett lekérdezési szabály erőforrás</span><span class="sxs-lookup"><span data-stu-id="924fb-118">The Scheduled Query Rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="924fb-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="924fb-119">-Name</span></span>
<span data-ttu-id="924fb-120">A riasztás neve</span><span class="sxs-lookup"><span data-stu-id="924fb-120">The alert name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="924fb-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="924fb-121">-PassThru</span></span>
<span data-ttu-id="924fb-122">A sikert vagy a hibát jelző értéket adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="924fb-122">Return a value indicating success or failure.</span></span>
<span data-ttu-id="924fb-123">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="924fb-123">This cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="924fb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="924fb-124">-ResourceGroupName</span></span>
<span data-ttu-id="924fb-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="924fb-125">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="924fb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="924fb-126">-ResourceId</span></span>
<span data-ttu-id="924fb-127">Az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="924fb-127">The resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="924fb-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="924fb-128">-Confirm</span></span>
<span data-ttu-id="924fb-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="924fb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="924fb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="924fb-130">-WhatIf</span></span>
<span data-ttu-id="924fb-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="924fb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="924fb-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="924fb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="924fb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="924fb-133">CommonParameters</span></span>
<span data-ttu-id="924fb-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="924fb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="924fb-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="924fb-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="924fb-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="924fb-136">INPUTS</span></span>

### <span data-ttu-id="924fb-137">Microsoft. Azure. commands. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="924fb-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="924fb-138">System. String</span><span class="sxs-lookup"><span data-stu-id="924fb-138">System.String</span></span>

## <span data-ttu-id="924fb-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="924fb-139">OUTPUTS</span></span>

### <span data-ttu-id="924fb-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="924fb-140">System.Boolean</span></span>

## <span data-ttu-id="924fb-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="924fb-141">NOTES</span></span>

## <span data-ttu-id="924fb-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="924fb-142">RELATED LINKS</span></span>
