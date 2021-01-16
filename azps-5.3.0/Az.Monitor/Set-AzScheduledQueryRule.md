---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzScheduledQueryRule.md
ms.openlocfilehash: 0351d6920c4af7f781ef27f4dfbc36a13e0c50cd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468301"
---
# <span data-ttu-id="19857-101">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="19857-101">Set-AzScheduledQueryRule</span></span>

## <span data-ttu-id="19857-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19857-102">SYNOPSIS</span></span>
<span data-ttu-id="19857-103">Naplóriasztás szabályának frissítése</span><span class="sxs-lookup"><span data-stu-id="19857-103">Updates a Log Alert Rule</span></span>

## <span data-ttu-id="19857-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="19857-104">SYNTAX</span></span>

### <span data-ttu-id="19857-105">ByRuleName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="19857-105">ByRuleName (Default)</span></span>
```
Set-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> [-Schedule <PSScheduledQueryRuleSchedule>]
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -ResourceGroupName <String> [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19857-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="19857-106">ByInputObject</span></span>
```
Set-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-Source <PSScheduledQueryRuleSource>]
 [-Schedule <PSScheduledQueryRuleSchedule>] [-Action <PSScheduledQueryRuleAlertingAction>] [-Location <String>]
 [-Description <String>] [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19857-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="19857-107">ByResourceId</span></span>
```
Set-AzScheduledQueryRule -ResourceId <String> -Source <PSScheduledQueryRuleSource>
 [-Schedule <PSScheduledQueryRuleSchedule>] -Action <PSScheduledQueryRuleAlertingAction> -Location <String>
 [-Description <String>] [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19857-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="19857-108">DESCRIPTION</span></span>
<span data-ttu-id="19857-109">Naplóriasztás szabályának frissítése PUT szemantikai adatok alapján</span><span class="sxs-lookup"><span data-stu-id="19857-109">Updates a Log Alert Rule by PUT semantics</span></span>

## <span data-ttu-id="19857-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="19857-110">EXAMPLES</span></span>

### <span data-ttu-id="19857-111">1. példa: Beállítás szabálynév szerint</span><span class="sxs-lookup"><span data-stu-id="19857-111">Example 1: Set by rule name</span></span>
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

### <span data-ttu-id="19857-112">2. példa: Bemeneti objektum által beállítva</span><span class="sxs-lookup"><span data-stu-id="19857-112">Example 2: Set by Input Object</span></span>
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

### <span data-ttu-id="19857-113">3. példa: Beállítás erőforrás-azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="19857-113">Example 3: Set by resource Id</span></span>
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

## <span data-ttu-id="19857-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19857-114">PARAMETERS</span></span>

### <span data-ttu-id="19857-115">-Művelet</span><span class="sxs-lookup"><span data-stu-id="19857-115">-Action</span></span>
<span data-ttu-id="19857-116">Az ütemezett lekérdezési szabály riasztási művelete</span><span class="sxs-lookup"><span data-stu-id="19857-116">The scheduled query rule Alerting Action</span></span>

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

### <span data-ttu-id="19857-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19857-117">-AsJob</span></span>
<span data-ttu-id="19857-118">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="19857-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="19857-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19857-119">-DefaultProfile</span></span>
<span data-ttu-id="19857-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="19857-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19857-121">-Leírás</span><span class="sxs-lookup"><span data-stu-id="19857-121">-Description</span></span>
<span data-ttu-id="19857-122">A riasztás leírása</span><span class="sxs-lookup"><span data-stu-id="19857-122">The description for this alert</span></span>

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

### <span data-ttu-id="19857-123">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="19857-123">-Enabled</span></span>
<span data-ttu-id="19857-124">Az Azure riasztási állapota – érvényes értékek – $true, $false</span><span class="sxs-lookup"><span data-stu-id="19857-124">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="19857-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19857-125">-InputObject</span></span>
<span data-ttu-id="19857-126">Az ütemezett lekérdezési szabály erőforrás</span><span class="sxs-lookup"><span data-stu-id="19857-126">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="19857-127">-Location</span><span class="sxs-lookup"><span data-stu-id="19857-127">-Location</span></span>
<span data-ttu-id="19857-128">A riasztás helye</span><span class="sxs-lookup"><span data-stu-id="19857-128">The location for this alert</span></span>

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

### <span data-ttu-id="19857-129">-Name</span><span class="sxs-lookup"><span data-stu-id="19857-129">-Name</span></span>
<span data-ttu-id="19857-130">A riasztás neve</span><span class="sxs-lookup"><span data-stu-id="19857-130">The alert name</span></span>

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

### <span data-ttu-id="19857-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19857-131">-ResourceGroupName</span></span>
<span data-ttu-id="19857-132">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="19857-132">The resource group name</span></span>

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

### <span data-ttu-id="19857-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19857-133">-ResourceId</span></span>
<span data-ttu-id="19857-134">Az erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="19857-134">The resource Id</span></span>

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

### <span data-ttu-id="19857-135">-Schedule</span><span class="sxs-lookup"><span data-stu-id="19857-135">-Schedule</span></span>
<span data-ttu-id="19857-136">Az ütemezett lekérdezési szabály ütemezése</span><span class="sxs-lookup"><span data-stu-id="19857-136">The scheduled query rule schedule</span></span>

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

### <span data-ttu-id="19857-137">-Source</span><span class="sxs-lookup"><span data-stu-id="19857-137">-Source</span></span>
<span data-ttu-id="19857-138">Az ütemezett lekérdezési szabályforrás</span><span class="sxs-lookup"><span data-stu-id="19857-138">The scheduled query rule source</span></span>

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

### <span data-ttu-id="19857-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="19857-139">-Tag</span></span>
<span data-ttu-id="19857-140">Erőforráscímkék</span><span class="sxs-lookup"><span data-stu-id="19857-140">Resource tags</span></span>

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

### <span data-ttu-id="19857-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19857-141">-Confirm</span></span>
<span data-ttu-id="19857-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="19857-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19857-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19857-143">-WhatIf</span></span>
<span data-ttu-id="19857-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="19857-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19857-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="19857-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19857-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19857-146">CommonParameters</span></span>
<span data-ttu-id="19857-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19857-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19857-148">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19857-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19857-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19857-149">INPUTS</span></span>

### <span data-ttu-id="19857-150">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="19857-150">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="19857-151">System.String</span><span class="sxs-lookup"><span data-stu-id="19857-151">System.String</span></span>

### <span data-ttu-id="19857-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="19857-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

### <span data-ttu-id="19857-153">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="19857-153">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

### <span data-ttu-id="19857-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="19857-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="19857-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19857-155">OUTPUTS</span></span>

### <span data-ttu-id="19857-156">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="19857-156">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="19857-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="19857-157">NOTES</span></span>

## <span data-ttu-id="19857-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19857-158">RELATED LINKS</span></span>
