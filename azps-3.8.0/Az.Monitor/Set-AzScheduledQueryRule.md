---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzScheduledQueryRule.md
ms.openlocfilehash: 5a335aaed12a39653d57c5a72e54d6a3caa53828
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845085"
---
# <span data-ttu-id="012d2-101">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="012d2-101">Set-AzScheduledQueryRule</span></span>

## <span data-ttu-id="012d2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="012d2-102">SYNOPSIS</span></span>
<span data-ttu-id="012d2-103">Naplózási riasztási szabály frissítése</span><span class="sxs-lookup"><span data-stu-id="012d2-103">Updates a Log Alert Rule</span></span>

## <span data-ttu-id="012d2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="012d2-104">SYNTAX</span></span>

### <span data-ttu-id="012d2-105">ByRuleName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="012d2-105">ByRuleName (Default)</span></span>
```
Set-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> [-Schedule <PSScheduledQueryRuleSchedule>]
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -ResourceGroupName <String> [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="012d2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="012d2-106">ByInputObject</span></span>
```
Set-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-Source <PSScheduledQueryRuleSource>]
 [-Schedule <PSScheduledQueryRuleSchedule>] [-Action <PSScheduledQueryRuleAlertingAction>] [-Location <String>]
 [-Description <String>] [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="012d2-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="012d2-107">ByResourceId</span></span>
```
Set-AzScheduledQueryRule -ResourceId <String> -Source <PSScheduledQueryRuleSource>
 [-Schedule <PSScheduledQueryRuleSchedule>] -Action <PSScheduledQueryRuleAlertingAction> -Location <String>
 [-Description <String>] [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="012d2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="012d2-108">DESCRIPTION</span></span>
<span data-ttu-id="012d2-109">A naplózási riasztási szabály frissítése a szemantikai adatokkal</span><span class="sxs-lookup"><span data-stu-id="012d2-109">Updates a Log Alert Rule by PUT semantics</span></span>

## <span data-ttu-id="012d2-110">Példák</span><span class="sxs-lookup"><span data-stu-id="012d2-110">EXAMPLES</span></span>

### <span data-ttu-id="012d2-111">Példa 1 – szabály nevének beállítása</span><span class="sxs-lookup"><span data-stu-id="012d2-111">Example 1 - Set by rule name</span></span>
```powershell
PS C:\> Set-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1" -Enabled $true -Location "centralindia" -Action $alertingAction -Description "log alert description" -Schedule $schedule -Source $source

Description       : log alert description
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:45:04 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="012d2-112">Példa 2 – beviteli objektum szerinti beállítás</span><span class="sxs-lookup"><span data-stu-id="012d2-112">Example 2 - Set by Input Object</span></span>
```powershell
PS C:\> Set-AzScheduledQueryRule -InputObject $sqr -Description "changed description"

Description       : changed description
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:46:38 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="012d2-113">Példa 3 – erőforrás-azonosító szerint beállítva</span><span class="sxs-lookup"><span data-stu-id="012d2-113">Example 3 - Set by resource Id</span></span>
```powershell
PS C:\> Set-AzScheduledQueryRule -ResourceId "/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1" -Enabled $true -Location "centralindia" -Action $alertingAction -Description "change description again" -Schedule $schedule -Source $source

Description       : change description again
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:47:59 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

## <span data-ttu-id="012d2-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="012d2-114">PARAMETERS</span></span>

### <span data-ttu-id="012d2-115">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="012d2-115">-Action</span></span>
<span data-ttu-id="012d2-116">Az ütemezett lekérdezési szabály értesítési hatása</span><span class="sxs-lookup"><span data-stu-id="012d2-116">The scheduled query rule Alerting Action</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction
Parameter Sets: ByRuleName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="012d2-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="012d2-117">-AsJob</span></span>
<span data-ttu-id="012d2-118">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="012d2-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="012d2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="012d2-119">-DefaultProfile</span></span>
<span data-ttu-id="012d2-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="012d2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="012d2-121">-Leírás</span><span class="sxs-lookup"><span data-stu-id="012d2-121">-Description</span></span>
<span data-ttu-id="012d2-122">Az értesítés leírása</span><span class="sxs-lookup"><span data-stu-id="012d2-122">The description for this alert</span></span>

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

### <span data-ttu-id="012d2-123">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="012d2-123">-Enabled</span></span>
<span data-ttu-id="012d2-124">Az Azure riasztási állapota – érvényes értékek – $true, $false</span><span class="sxs-lookup"><span data-stu-id="012d2-124">The azure alert state - valid values - $true, $false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="012d2-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="012d2-125">-InputObject</span></span>
<span data-ttu-id="012d2-126">Az ütemezett lekérdezési szabály erőforrás</span><span class="sxs-lookup"><span data-stu-id="012d2-126">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="012d2-127">-Hely</span><span class="sxs-lookup"><span data-stu-id="012d2-127">-Location</span></span>
<span data-ttu-id="012d2-128">Az értesítés helye</span><span class="sxs-lookup"><span data-stu-id="012d2-128">The location for this alert</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="012d2-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="012d2-129">-Name</span></span>
<span data-ttu-id="012d2-130">A riasztás neve</span><span class="sxs-lookup"><span data-stu-id="012d2-130">The alert name</span></span>

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

### <span data-ttu-id="012d2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="012d2-131">-ResourceGroupName</span></span>
<span data-ttu-id="012d2-132">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="012d2-132">The resource group name</span></span>

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

### <span data-ttu-id="012d2-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="012d2-133">-ResourceId</span></span>
<span data-ttu-id="012d2-134">Az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="012d2-134">The resource Id</span></span>

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

### <span data-ttu-id="012d2-135">– Ütemezés</span><span class="sxs-lookup"><span data-stu-id="012d2-135">-Schedule</span></span>
<span data-ttu-id="012d2-136">Az ütemezett lekérdezési szabály ütemezése</span><span class="sxs-lookup"><span data-stu-id="012d2-136">The scheduled query rule schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="012d2-137">-Forrás</span><span class="sxs-lookup"><span data-stu-id="012d2-137">-Source</span></span>
<span data-ttu-id="012d2-138">Az ütemezett lekérdezési szabály forrása</span><span class="sxs-lookup"><span data-stu-id="012d2-138">The scheduled query rule source</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource
Parameter Sets: ByRuleName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="012d2-139">-Címke</span><span class="sxs-lookup"><span data-stu-id="012d2-139">-Tag</span></span>
<span data-ttu-id="012d2-140">Erőforrás-Címkék</span><span class="sxs-lookup"><span data-stu-id="012d2-140">Resource tags</span></span>

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

### <span data-ttu-id="012d2-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="012d2-141">-Confirm</span></span>
<span data-ttu-id="012d2-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="012d2-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="012d2-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="012d2-143">-WhatIf</span></span>
<span data-ttu-id="012d2-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="012d2-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="012d2-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="012d2-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="012d2-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="012d2-146">CommonParameters</span></span>
<span data-ttu-id="012d2-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="012d2-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="012d2-148">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="012d2-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="012d2-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="012d2-149">INPUTS</span></span>

### <span data-ttu-id="012d2-150">Microsoft. Azure. commands. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="012d2-150">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="012d2-151">System. String</span><span class="sxs-lookup"><span data-stu-id="012d2-151">System.String</span></span>

### <span data-ttu-id="012d2-152">Microsoft. Azure. commands. OutputClasses. PSScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="012d2-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

### <span data-ttu-id="012d2-153">Microsoft. Azure. commands. OutputClasses. PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="012d2-153">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

### <span data-ttu-id="012d2-154">Microsoft. Azure. commands. OutputClasses. PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="012d2-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="012d2-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="012d2-155">OUTPUTS</span></span>

### <span data-ttu-id="012d2-156">Microsoft. Azure. commands. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="012d2-156">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="012d2-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="012d2-157">NOTES</span></span>

## <span data-ttu-id="012d2-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="012d2-158">RELATED LINKS</span></span>
