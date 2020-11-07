---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
ms.openlocfilehash: 689588e8b92b4b76c97f3972aa63c2f8cdc16535
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841918"
---
# <span data-ttu-id="99d31-101">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="99d31-101">Remove-AzScheduledQueryRule</span></span>

## <span data-ttu-id="99d31-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="99d31-102">SYNOPSIS</span></span>
<span data-ttu-id="99d31-103">Naplózási riasztási szabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="99d31-103">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="99d31-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="99d31-104">SYNTAX</span></span>

### <span data-ttu-id="99d31-105">ByRuleName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="99d31-105">ByRuleName (Default)</span></span>
```
Remove-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99d31-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="99d31-106">ByInputObject</span></span>
```
Remove-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99d31-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="99d31-107">ByResourceId</span></span>
```
Remove-AzScheduledQueryRule -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99d31-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="99d31-108">DESCRIPTION</span></span>
<span data-ttu-id="99d31-109">Naplózási riasztási szabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="99d31-109">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="99d31-110">Példák</span><span class="sxs-lookup"><span data-stu-id="99d31-110">EXAMPLES</span></span>

### <span data-ttu-id="99d31-111">Példa 1 – szabály nevének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="99d31-111">Example 1 - Remove by rule name</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1"
```

### <span data-ttu-id="99d31-112">2. példa – beviteli objektumból való eltávolítás</span><span class="sxs-lookup"><span data-stu-id="99d31-112">Example 2 - Remove by input object</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -InputObject $PSScheduledQueryRuleResource
```

### <span data-ttu-id="99d31-113">Példa 3 – erőforrás-azonosítóval való eltávolítás</span><span class="sxs-lookup"><span data-stu-id="99d31-113">Example 3 - Remove by resource Id</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledQueryRules/LogAlertRule1"
```

## <span data-ttu-id="99d31-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="99d31-114">PARAMETERS</span></span>

### <span data-ttu-id="99d31-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99d31-115">-DefaultProfile</span></span>
<span data-ttu-id="99d31-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="99d31-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99d31-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99d31-117">-InputObject</span></span>
<span data-ttu-id="99d31-118">Az ütemezett lekérdezési szabály erőforrás</span><span class="sxs-lookup"><span data-stu-id="99d31-118">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="99d31-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="99d31-119">-Name</span></span>
<span data-ttu-id="99d31-120">A riasztás neve</span><span class="sxs-lookup"><span data-stu-id="99d31-120">The alert name</span></span>

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

### <span data-ttu-id="99d31-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99d31-121">-PassThru</span></span>
<span data-ttu-id="99d31-122">A sikert vagy a hibát jelző értéket adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="99d31-122">Return a value indicating success or failure.</span></span>
<span data-ttu-id="99d31-123">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="99d31-123">This cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="99d31-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99d31-124">-ResourceGroupName</span></span>
<span data-ttu-id="99d31-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="99d31-125">The resource group name</span></span>

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

### <span data-ttu-id="99d31-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99d31-126">-ResourceId</span></span>
<span data-ttu-id="99d31-127">Az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="99d31-127">The resource Id</span></span>

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

### <span data-ttu-id="99d31-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="99d31-128">-Confirm</span></span>
<span data-ttu-id="99d31-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="99d31-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99d31-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99d31-130">-WhatIf</span></span>
<span data-ttu-id="99d31-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="99d31-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99d31-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="99d31-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99d31-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99d31-133">CommonParameters</span></span>
<span data-ttu-id="99d31-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="99d31-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99d31-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="99d31-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99d31-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="99d31-136">INPUTS</span></span>

### <span data-ttu-id="99d31-137">Microsoft. Azure. commands. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="99d31-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="99d31-138">System. String</span><span class="sxs-lookup"><span data-stu-id="99d31-138">System.String</span></span>

## <span data-ttu-id="99d31-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99d31-139">OUTPUTS</span></span>

### <span data-ttu-id="99d31-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="99d31-140">System.Boolean</span></span>

## <span data-ttu-id="99d31-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="99d31-141">NOTES</span></span>

## <span data-ttu-id="99d31-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99d31-142">RELATED LINKS</span></span>
