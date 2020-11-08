---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
ms.openlocfilehash: 5a896bedd7e0dd6e220fb4b8dae2cc2e87ae0fcb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187292"
---
# <span data-ttu-id="da7d6-101">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="da7d6-101">New-AzScheduledQueryRule</span></span>

## <span data-ttu-id="da7d6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="da7d6-102">SYNOPSIS</span></span>
<span data-ttu-id="da7d6-103">Naplózási riasztási szabály létrehozása (ütemezett lekérdezési szabály típusa)</span><span class="sxs-lookup"><span data-stu-id="da7d6-103">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="da7d6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="da7d6-104">SYNTAX</span></span>

```
New-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> -Schedule <PSScheduledQueryRuleSchedule>
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -Enabled <Boolean> -ResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da7d6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="da7d6-105">DESCRIPTION</span></span>
<span data-ttu-id="da7d6-106">Naplózási riasztási szabály létrehozása (ütemezett lekérdezési szabály típusa)</span><span class="sxs-lookup"><span data-stu-id="da7d6-106">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="da7d6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="da7d6-107">EXAMPLES</span></span>

### <span data-ttu-id="da7d6-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="da7d6-108">Example 1</span></span>
```powershell
PS C:\> New-AzScheduledQueryRule -Location "West Europe" -Action $alertingAction -Enabled $true -Description "log alert foo" -Schedule $schedule -Source $source -Name "LogAlertRule1"
```

## <span data-ttu-id="da7d6-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="da7d6-109">PARAMETERS</span></span>

### <span data-ttu-id="da7d6-110">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="da7d6-110">-Action</span></span>
<span data-ttu-id="da7d6-111">Az ütemezett lekérdezési szabály értesítési hatása</span><span class="sxs-lookup"><span data-stu-id="da7d6-111">The scheduled query rule Alerting Action</span></span>

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

### <span data-ttu-id="da7d6-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da7d6-112">-AsJob</span></span>
<span data-ttu-id="da7d6-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="da7d6-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="da7d6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da7d6-114">-DefaultProfile</span></span>
<span data-ttu-id="da7d6-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da7d6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da7d6-116">-Leírás</span><span class="sxs-lookup"><span data-stu-id="da7d6-116">-Description</span></span>
<span data-ttu-id="da7d6-117">Az értesítés leírása</span><span class="sxs-lookup"><span data-stu-id="da7d6-117">The description for this alert</span></span>

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

### <span data-ttu-id="da7d6-118">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="da7d6-118">-Enabled</span></span>
<span data-ttu-id="da7d6-119">Az Azure riasztási állapota – érvényes értékek – $true, $false</span><span class="sxs-lookup"><span data-stu-id="da7d6-119">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="da7d6-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="da7d6-120">-Location</span></span>
<span data-ttu-id="da7d6-121">Az értesítés helye</span><span class="sxs-lookup"><span data-stu-id="da7d6-121">The location for this alert</span></span>

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

### <span data-ttu-id="da7d6-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="da7d6-122">-Name</span></span>
<span data-ttu-id="da7d6-123">A riasztás neve</span><span class="sxs-lookup"><span data-stu-id="da7d6-123">The alert name</span></span>

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

### <span data-ttu-id="da7d6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da7d6-124">-ResourceGroupName</span></span>
<span data-ttu-id="da7d6-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="da7d6-125">The resource group name</span></span>

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

### <span data-ttu-id="da7d6-126">– Ütemezés</span><span class="sxs-lookup"><span data-stu-id="da7d6-126">-Schedule</span></span>
<span data-ttu-id="da7d6-127">Az ütemezett lekérdezési szabály ütemezése</span><span class="sxs-lookup"><span data-stu-id="da7d6-127">The scheduled query rule schedule</span></span>

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

### <span data-ttu-id="da7d6-128">-Forrás</span><span class="sxs-lookup"><span data-stu-id="da7d6-128">-Source</span></span>
<span data-ttu-id="da7d6-129">Az ütemezett lekérdezési szabály forrása</span><span class="sxs-lookup"><span data-stu-id="da7d6-129">The scheduled query rule source</span></span>

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

### <span data-ttu-id="da7d6-130">-Címke</span><span class="sxs-lookup"><span data-stu-id="da7d6-130">-Tag</span></span>
<span data-ttu-id="da7d6-131">Erőforrás-Címkék</span><span class="sxs-lookup"><span data-stu-id="da7d6-131">Resource tags</span></span>

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

### <span data-ttu-id="da7d6-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="da7d6-132">-Confirm</span></span>
<span data-ttu-id="da7d6-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="da7d6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da7d6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da7d6-134">-WhatIf</span></span>
<span data-ttu-id="da7d6-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="da7d6-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da7d6-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="da7d6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da7d6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da7d6-137">CommonParameters</span></span>
<span data-ttu-id="da7d6-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="da7d6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da7d6-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="da7d6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da7d6-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="da7d6-140">INPUTS</span></span>

### <span data-ttu-id="da7d6-141">System. String</span><span class="sxs-lookup"><span data-stu-id="da7d6-141">System.String</span></span>

## <span data-ttu-id="da7d6-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da7d6-142">OUTPUTS</span></span>

### <span data-ttu-id="da7d6-143">Microsoft. Azure. commands. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="da7d6-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="da7d6-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="da7d6-144">NOTES</span></span>

## <span data-ttu-id="da7d6-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da7d6-145">RELATED LINKS</span></span>
