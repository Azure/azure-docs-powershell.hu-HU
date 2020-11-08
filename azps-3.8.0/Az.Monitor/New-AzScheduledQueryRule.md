---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
ms.openlocfilehash: 5a896bedd7e0dd6e220fb4b8dae2cc2e87ae0fcb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94002848"
---
# <span data-ttu-id="f4edc-101">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f4edc-101">New-AzScheduledQueryRule</span></span>

## <span data-ttu-id="f4edc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f4edc-102">SYNOPSIS</span></span>
<span data-ttu-id="f4edc-103">Naplózási riasztási szabály létrehozása (ütemezett lekérdezési szabály típusa)</span><span class="sxs-lookup"><span data-stu-id="f4edc-103">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="f4edc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f4edc-104">SYNTAX</span></span>

```
New-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> -Schedule <PSScheduledQueryRuleSchedule>
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -Enabled <Boolean> -ResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4edc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f4edc-105">DESCRIPTION</span></span>
<span data-ttu-id="f4edc-106">Naplózási riasztási szabály létrehozása (ütemezett lekérdezési szabály típusa)</span><span class="sxs-lookup"><span data-stu-id="f4edc-106">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="f4edc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f4edc-107">EXAMPLES</span></span>

### <span data-ttu-id="f4edc-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f4edc-108">Example 1</span></span>
```powershell
PS C:\> New-AzScheduledQueryRule -Location "West Europe" -Action $alertingAction -Enabled $true -Description "log alert foo" -Schedule $schedule -Source $source -Name "LogAlertRule1"
```

## <span data-ttu-id="f4edc-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f4edc-109">PARAMETERS</span></span>

### <span data-ttu-id="f4edc-110">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="f4edc-110">-Action</span></span>
<span data-ttu-id="f4edc-111">Az ütemezett lekérdezési szabály értesítési hatása</span><span class="sxs-lookup"><span data-stu-id="f4edc-111">The scheduled query rule Alerting Action</span></span>

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

### <span data-ttu-id="f4edc-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4edc-112">-AsJob</span></span>
<span data-ttu-id="f4edc-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f4edc-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f4edc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4edc-114">-DefaultProfile</span></span>
<span data-ttu-id="f4edc-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4edc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4edc-116">-Leírás</span><span class="sxs-lookup"><span data-stu-id="f4edc-116">-Description</span></span>
<span data-ttu-id="f4edc-117">Az értesítés leírása</span><span class="sxs-lookup"><span data-stu-id="f4edc-117">The description for this alert</span></span>

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

### <span data-ttu-id="f4edc-118">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="f4edc-118">-Enabled</span></span>
<span data-ttu-id="f4edc-119">Az Azure riasztási állapota – érvényes értékek – $true, $false</span><span class="sxs-lookup"><span data-stu-id="f4edc-119">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="f4edc-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="f4edc-120">-Location</span></span>
<span data-ttu-id="f4edc-121">Az értesítés helye</span><span class="sxs-lookup"><span data-stu-id="f4edc-121">The location for this alert</span></span>

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

### <span data-ttu-id="f4edc-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f4edc-122">-Name</span></span>
<span data-ttu-id="f4edc-123">A riasztás neve</span><span class="sxs-lookup"><span data-stu-id="f4edc-123">The alert name</span></span>

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

### <span data-ttu-id="f4edc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4edc-124">-ResourceGroupName</span></span>
<span data-ttu-id="f4edc-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="f4edc-125">The resource group name</span></span>

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

### <span data-ttu-id="f4edc-126">– Ütemezés</span><span class="sxs-lookup"><span data-stu-id="f4edc-126">-Schedule</span></span>
<span data-ttu-id="f4edc-127">Az ütemezett lekérdezési szabály ütemezése</span><span class="sxs-lookup"><span data-stu-id="f4edc-127">The scheduled query rule schedule</span></span>

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

### <span data-ttu-id="f4edc-128">-Forrás</span><span class="sxs-lookup"><span data-stu-id="f4edc-128">-Source</span></span>
<span data-ttu-id="f4edc-129">Az ütemezett lekérdezési szabály forrása</span><span class="sxs-lookup"><span data-stu-id="f4edc-129">The scheduled query rule source</span></span>

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

### <span data-ttu-id="f4edc-130">-Címke</span><span class="sxs-lookup"><span data-stu-id="f4edc-130">-Tag</span></span>
<span data-ttu-id="f4edc-131">Erőforrás-Címkék</span><span class="sxs-lookup"><span data-stu-id="f4edc-131">Resource tags</span></span>

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

### <span data-ttu-id="f4edc-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f4edc-132">-Confirm</span></span>
<span data-ttu-id="f4edc-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f4edc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4edc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4edc-134">-WhatIf</span></span>
<span data-ttu-id="f4edc-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f4edc-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4edc-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f4edc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4edc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4edc-137">CommonParameters</span></span>
<span data-ttu-id="f4edc-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f4edc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4edc-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f4edc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4edc-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4edc-140">INPUTS</span></span>

### <span data-ttu-id="f4edc-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f4edc-141">System.String</span></span>

## <span data-ttu-id="f4edc-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4edc-142">OUTPUTS</span></span>

### <span data-ttu-id="f4edc-143">Microsoft. Azure. commands. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="f4edc-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="f4edc-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f4edc-144">NOTES</span></span>

## <span data-ttu-id="f4edc-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4edc-145">RELATED LINKS</span></span>
