---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/set-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
ms.openlocfilehash: 75a2071e8f60ed15420b69815eba22d6f82e9f82
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329633"
---
# <span data-ttu-id="e86e1-101">Set-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="e86e1-101">Set-AzActionRule</span></span>

## <span data-ttu-id="e86e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e86e1-102">SYNOPSIS</span></span>
<span data-ttu-id="e86e1-103">Hozzon létre vagy frissítsen egy műveletszabályt.</span><span class="sxs-lookup"><span data-stu-id="e86e1-103">Create or update an action rule.</span></span>

## <span data-ttu-id="e86e1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e86e1-104">SYNTAX</span></span>

### <span data-ttu-id="e86e1-105">BySimplifiedFormatDiagnosticsActionRule (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e86e1-105">BySimplifiedFormatDiagnosticsActionRule (Default)</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e86e1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e86e1-106">ByInputObject</span></span>
```
Set-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e86e1-107">BySimplifiedFormatActionGroupActionRule</span><span class="sxs-lookup"><span data-stu-id="e86e1-107">BySimplifiedFormatActionGroupActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ActionGroupId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e86e1-108">BySimplifiedFormatSuppressionActionRule</span><span class="sxs-lookup"><span data-stu-id="e86e1-108">BySimplifiedFormatSuppressionActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ReccurenceType <String> [-SuppressionStartTime <String>]
 [-SuppressionEndTime <String>] [-ReccurentValue <Int32[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e86e1-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e86e1-109">DESCRIPTION</span></span>
<span data-ttu-id="e86e1-110">**A Set-AzActionRule létrehoz** vagy frissíti a műveletszabályt.</span><span class="sxs-lookup"><span data-stu-id="e86e1-110">**Set-AzActionRule** creates or updates an action rule.</span></span>

## <span data-ttu-id="e86e1-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e86e1-111">EXAMPLES</span></span>

### <span data-ttu-id="e86e1-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="e86e1-112">Example 1</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Suppression" -ReccurenceType "Weekly" -SuppressionStartTime "06/26/2018 06:00:00" -SuppressionEndTime "07/27/2018 06:00:00" -ReccurentValue 1,4,6
```

<span data-ttu-id="e86e1-113">Ez a parancsmag egy akciószabályt hoz létre az előfizetés hatókörével.</span><span class="sxs-lookup"><span data-stu-id="e86e1-113">This cmdlet creates an action rule for supression, with a subscription scope.</span></span>

### <span data-ttu-id="e86e1-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="e86e1-114">Example 2</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "ActionGroup" -ActionGroupId "/subscriptions/1e3ff1c0-771a-4119-a03b-be82a51e232d/resourceGroups/alertscorrelationrg/providers/Microsoft.insights/actiongroups/testAG"
```

<span data-ttu-id="e86e1-115">Ez a parancsmag létrehoz egy műveletszabályt a műveletcsoporthoz az erőforráscsoportok hatókörének listájával.</span><span class="sxs-lookup"><span data-stu-id="e86e1-115">This cmdlet creates an action rule for action group, with a list of resource groups scope.</span></span>

### <span data-ttu-id="e86e1-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="e86e1-116">Example 3</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab/providers/microsoft.insights/metricAlerts/Total Requests Exceeded" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Diagnostics"
```

<span data-ttu-id="e86e1-117">Ez a parancsmag létrehoz egy műveletszabályt a diagnosztikai beállításokhoz, egy erőforrás-hatókörrel.</span><span class="sxs-lookup"><span data-stu-id="e86e1-117">This cmdlet creates an action rule for diagnostics settings, with a resource scope.</span></span>

## <span data-ttu-id="e86e1-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e86e1-118">PARAMETERS</span></span>

### <span data-ttu-id="e86e1-119">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="e86e1-119">-ActionGroupId</span></span>
<span data-ttu-id="e86e1-120">Értesítésre kijelölt műveletcsoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e86e1-120">Action Group Id which is to be notified.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatActionGroupActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e86e1-121">-ActionRuleType</span><span class="sxs-lookup"><span data-stu-id="e86e1-121">-ActionRuleType</span></span>
<span data-ttu-id="e86e1-122">Action rule Json format</span><span class="sxs-lookup"><span data-stu-id="e86e1-122">Action rule Json format</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e86e1-123">-AlertContextCondition</span><span class="sxs-lookup"><span data-stu-id="e86e1-123">-AlertContextCondition</span></span>
<span data-ttu-id="e86e1-124">Várható formátum – { \<operation\> : \<comma separated list of values\> } Például.</span><span class="sxs-lookup"><span data-stu-id="e86e1-124">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="e86e1-125">Tartalmazza:intelligens csoportok</span><span class="sxs-lookup"><span data-stu-id="e86e1-125">Contains:smartgroups</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e86e1-126">-AlertRuleIdCondition</span><span class="sxs-lookup"><span data-stu-id="e86e1-126">-AlertRuleIdCondition</span></span>
<span data-ttu-id="e86e1-127">Várható formátum – { \<operation\> : \<comma separated list of values\> } Például.</span><span class="sxs-lookup"><span data-stu-id="e86e1-127">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="e86e1-128">Egyenlő:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abva csoportházirend/providers/microsoft.insights/metricAlerts/test-mrmc-vm-abva insights</span><span class="sxs-lookup"><span data-stu-id="e86e1-128">Equals:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abvarma/providers/microsoft.insights/metricAlerts/test-mrmc-vm-abvarma</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e86e1-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e86e1-129">-DefaultProfile</span></span>
<span data-ttu-id="e86e1-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e86e1-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e86e1-131">-Leírás</span><span class="sxs-lookup"><span data-stu-id="e86e1-131">-Description</span></span>
<span data-ttu-id="e86e1-132">A műveletszabály leírása</span><span class="sxs-lookup"><span data-stu-id="e86e1-132">Description of Action Rule</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e86e1-133">-DescriptionCondition</span><span class="sxs-lookup"><span data-stu-id="e86e1-133">-DescriptionCondition</span></span>
<span data-ttu-id="e86e1-134">Várható formátum – { \<operation\> : \<comma separated list of values\> } Például.</span><span class="sxs-lookup"><span data-stu-id="e86e1-134">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="e86e1-135">Contains:Test Alert</span><span class="sxs-lookup"><span data-stu-id="e86e1-135">Contains:Test Alert</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e86e1-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e86e1-136">-InputObject</span></span>
<span data-ttu-id="e86e1-137">A műveletszabály-erőforrás</span><span class="sxs-lookup"><span data-stu-id="e86e1-137">The action rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e86e1-138">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="e86e1-138">-MonitorCondition</span></span>
<span data-ttu-id="e86e1-139">Várható formátum – { \<operation\> : \<comma separated list of values\> } Például.</span><span class="sxs-lookup"><span data-stu-id="e86e1-139">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="e86e1-140">NotEquals:Resolved</span><span class="sxs-lookup"><span data-stu-id="e86e1-140">NotEquals:Resolved</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e86e1-141">-MonitorServiceCondition</span><span class="sxs-lookup"><span data-stu-id="e86e1-141">-MonitorServiceCondition</span></span>
<span data-ttu-id="e86e1-142">Várható formátum – { \<operation\> : \<comma separated list of values\> } Például.</span><span class="sxs-lookup"><span data-stu-id="e86e1-142">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="e86e1-143">Egyenlő:Platform,Log Analytics</span><span class="sxs-lookup"><span data-stu-id="e86e1-143">Equals:Platform,Log Analytics</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e86e1-144">-Name</span><span class="sxs-lookup"><span data-stu-id="e86e1-144">-Name</span></span>
<span data-ttu-id="e86e1-145">Műveletszabály neve</span><span class="sxs-lookup"><span data-stu-id="e86e1-145">Action rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e86e1-146">-ReccurenceType</span><span class="sxs-lookup"><span data-stu-id="e86e1-146">-ReccurenceType</span></span>
<span data-ttu-id="e86e1-147">Azt az időtartamot adja meg, amikor a vizsgálatnak megfelelő időtartamot kell alkalmazni.</span><span class="sxs-lookup"><span data-stu-id="e86e1-147">Specifies the duration when the suppression should be applied.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e86e1-148">-ReccurentValue</span><span class="sxs-lookup"><span data-stu-id="e86e1-148">-ReccurentValue</span></span>
<span data-ttu-id="e86e1-149">Reccurent values, if applicable. Heti - \[ 1,2 \] Eset: Havi - \[ 1,3,5,30\]</span><span class="sxs-lookup"><span data-stu-id="e86e1-149">Reccurent values, if applicable.In case of Weekly - \[1,2\] In case of Monthly - \[1,3,5,30\]</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e86e1-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e86e1-150">-ResourceGroupName</span></span>
<span data-ttu-id="e86e1-151">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e86e1-151">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e86e1-152">-Scope</span><span class="sxs-lookup"><span data-stu-id="e86e1-152">-Scope</span></span>
<span data-ttu-id="e86e1-153">Értékek vesszővel elválasztott listája</span><span class="sxs-lookup"><span data-stu-id="e86e1-153">Comma separated list of values</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e86e1-154">-SeverityCondition</span><span class="sxs-lookup"><span data-stu-id="e86e1-154">-SeverityCondition</span></span>
<span data-ttu-id="e86e1-155">Várható formátum – { \<operation\> : \<comma separated list of values\> } Például.</span><span class="sxs-lookup"><span data-stu-id="e86e1-155">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="e86e1-156">Egyenlő:Sev0,Sev1</span><span class="sxs-lookup"><span data-stu-id="e86e1-156">Equals:Sev0,Sev1</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e86e1-157">-Állapot</span><span class="sxs-lookup"><span data-stu-id="e86e1-157">-Status</span></span>
<span data-ttu-id="e86e1-158">A műveletszabály állapota.</span><span class="sxs-lookup"><span data-stu-id="e86e1-158">Status of Action Rule.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e86e1-159">-A1111-2007-400</span><span class="sxs-lookup"><span data-stu-id="e86e1-159">-SuppressionEndTime</span></span>
<span data-ttu-id="e86e1-160">A záró időpontok.</span><span class="sxs-lookup"><span data-stu-id="e86e1-160">Suppression End Time.</span></span>
<span data-ttu-id="e86e1-161">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly vagy Monthly.</span><span class="sxs-lookup"><span data-stu-id="e86e1-161">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e86e1-162">–StartTime</span><span class="sxs-lookup"><span data-stu-id="e86e1-162">-SuppressionStartTime</span></span>
<span data-ttu-id="e86e1-163">A kezdési időpont.</span><span class="sxs-lookup"><span data-stu-id="e86e1-163">Suppression Start Time.</span></span>
<span data-ttu-id="e86e1-164">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly vagy Monthly.</span><span class="sxs-lookup"><span data-stu-id="e86e1-164">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e86e1-165">-TargetResourceTypeCondition</span><span class="sxs-lookup"><span data-stu-id="e86e1-165">-TargetResourceTypeCondition</span></span>
<span data-ttu-id="e86e1-166">Várható formátum – { \<operation\> : \<comma separated list of values\> } Például.</span><span class="sxs-lookup"><span data-stu-id="e86e1-166">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="e86e1-167">Tartalmazza: Virtuális gépek, Tárfiók</span><span class="sxs-lookup"><span data-stu-id="e86e1-167">Contains:Virtual Machines,Storage Account</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e86e1-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e86e1-168">-Confirm</span></span>
<span data-ttu-id="e86e1-169">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e86e1-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e86e1-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e86e1-170">-WhatIf</span></span>
<span data-ttu-id="e86e1-171">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e86e1-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e86e1-172">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e86e1-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e86e1-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e86e1-173">CommonParameters</span></span>
<span data-ttu-id="e86e1-174">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e86e1-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e86e1-175">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e86e1-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e86e1-176">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e86e1-176">INPUTS</span></span>

### <span data-ttu-id="e86e1-177">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="e86e1-177">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="e86e1-178">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e86e1-178">OUTPUTS</span></span>

### <span data-ttu-id="e86e1-179">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="e86e1-179">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="e86e1-180">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e86e1-180">NOTES</span></span>

## <span data-ttu-id="e86e1-181">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e86e1-181">RELATED LINKS</span></span>
