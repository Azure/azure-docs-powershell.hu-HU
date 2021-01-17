---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
ms.openlocfilehash: 5a896bedd7e0dd6e220fb4b8dae2cc2e87ae0fcb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480049"
---
# <span data-ttu-id="f0a0d-101">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f0a0d-101">New-AzScheduledQueryRule</span></span>

## <span data-ttu-id="f0a0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0a0d-102">SYNOPSIS</span></span>
<span data-ttu-id="f0a0d-103">Naplóriasztás szabály (ütemezett lekérdezési szabálytípus) létrehozása</span><span class="sxs-lookup"><span data-stu-id="f0a0d-103">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="f0a0d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f0a0d-104">SYNTAX</span></span>

```
New-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> -Schedule <PSScheduledQueryRuleSchedule>
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -Enabled <Boolean> -ResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0a0d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f0a0d-105">DESCRIPTION</span></span>
<span data-ttu-id="f0a0d-106">Naplóriasztás szabályának létrehozása (ütemezett lekérdezési szabálytípus)</span><span class="sxs-lookup"><span data-stu-id="f0a0d-106">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="f0a0d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f0a0d-107">EXAMPLES</span></span>

### <span data-ttu-id="f0a0d-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="f0a0d-108">Example 1</span></span>
```powershell
PS C:\> New-AzScheduledQueryRule -Location "West Europe" -Action $alertingAction -Enabled $true -Description "log alert foo" -Schedule $schedule -Source $source -Name "LogAlertRule1"
```

## <span data-ttu-id="f0a0d-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0a0d-109">PARAMETERS</span></span>

### <span data-ttu-id="f0a0d-110">-Művelet</span><span class="sxs-lookup"><span data-stu-id="f0a0d-110">-Action</span></span>
<span data-ttu-id="f0a0d-111">Az ütemezett lekérdezési szabály riasztási művelete</span><span class="sxs-lookup"><span data-stu-id="f0a0d-111">The scheduled query rule Alerting Action</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0a0d-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0a0d-112">-AsJob</span></span>
<span data-ttu-id="f0a0d-113">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f0a0d-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f0a0d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0a0d-114">-DefaultProfile</span></span>
<span data-ttu-id="f0a0d-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f0a0d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0a0d-116">-Leírás</span><span class="sxs-lookup"><span data-stu-id="f0a0d-116">-Description</span></span>
<span data-ttu-id="f0a0d-117">A riasztás leírása</span><span class="sxs-lookup"><span data-stu-id="f0a0d-117">The description for this alert</span></span>

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

### <span data-ttu-id="f0a0d-118">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="f0a0d-118">-Enabled</span></span>
<span data-ttu-id="f0a0d-119">Az Azure riasztási állapota – érvényes értékek – $true, $false</span><span class="sxs-lookup"><span data-stu-id="f0a0d-119">The azure alert state - valid values - $true, $false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0a0d-120">-Location</span><span class="sxs-lookup"><span data-stu-id="f0a0d-120">-Location</span></span>
<span data-ttu-id="f0a0d-121">A riasztás helye</span><span class="sxs-lookup"><span data-stu-id="f0a0d-121">The location for this alert</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0a0d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f0a0d-122">-Name</span></span>
<span data-ttu-id="f0a0d-123">A riasztás neve</span><span class="sxs-lookup"><span data-stu-id="f0a0d-123">The alert name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0a0d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0a0d-124">-ResourceGroupName</span></span>
<span data-ttu-id="f0a0d-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="f0a0d-125">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0a0d-126">-Schedule</span><span class="sxs-lookup"><span data-stu-id="f0a0d-126">-Schedule</span></span>
<span data-ttu-id="f0a0d-127">Az ütemezett lekérdezési szabály ütemezése</span><span class="sxs-lookup"><span data-stu-id="f0a0d-127">The scheduled query rule schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0a0d-128">-Source</span><span class="sxs-lookup"><span data-stu-id="f0a0d-128">-Source</span></span>
<span data-ttu-id="f0a0d-129">Az ütemezett lekérdezési szabályforrás</span><span class="sxs-lookup"><span data-stu-id="f0a0d-129">The scheduled query rule source</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0a0d-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="f0a0d-130">-Tag</span></span>
<span data-ttu-id="f0a0d-131">Erőforráscímkék</span><span class="sxs-lookup"><span data-stu-id="f0a0d-131">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0a0d-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0a0d-132">-Confirm</span></span>
<span data-ttu-id="f0a0d-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f0a0d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0a0d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0a0d-134">-WhatIf</span></span>
<span data-ttu-id="f0a0d-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f0a0d-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f0a0d-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f0a0d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0a0d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0a0d-137">CommonParameters</span></span>
<span data-ttu-id="f0a0d-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0a0d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0a0d-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0a0d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0a0d-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f0a0d-140">INPUTS</span></span>

### <span data-ttu-id="f0a0d-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f0a0d-141">System.String</span></span>

## <span data-ttu-id="f0a0d-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0a0d-142">OUTPUTS</span></span>

### <span data-ttu-id="f0a0d-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="f0a0d-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="f0a0d-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f0a0d-144">NOTES</span></span>

## <span data-ttu-id="f0a0d-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f0a0d-145">RELATED LINKS</span></span>
