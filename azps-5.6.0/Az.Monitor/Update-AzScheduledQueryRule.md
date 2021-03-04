---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/update-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
ms.openlocfilehash: 8b1658ef2ff2779243d42461f4b94964017a6847
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935681"
---
# <span data-ttu-id="fbb48-101">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="fbb48-101">Update-AzScheduledQueryRule</span></span>

## <span data-ttu-id="fbb48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbb48-102">SYNOPSIS</span></span>
<span data-ttu-id="fbb48-103">Naplóriasztás szabályának frissítése</span><span class="sxs-lookup"><span data-stu-id="fbb48-103">Updates a Log Alert rule</span></span>

## <span data-ttu-id="fbb48-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fbb48-104">SYNTAX</span></span>

### <span data-ttu-id="fbb48-105">ByRuleName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fbb48-105">ByRuleName (Default)</span></span>
```
Update-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbb48-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fbb48-106">ByInputObject</span></span>
```
Update-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbb48-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fbb48-107">ByResourceId</span></span>
```
Update-AzScheduledQueryRule -ResourceId <String> -Enabled <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbb48-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fbb48-108">DESCRIPTION</span></span>
<span data-ttu-id="fbb48-109">A naplóriasztás szabályának frissítése esetén ez a parancs csak az "Enabled" tulajdonság frissítését támogatja.</span><span class="sxs-lookup"><span data-stu-id="fbb48-109">Updates a Log Alert rule, updating only "Enabled" property is supported by this command.</span></span>
<span data-ttu-id="fbb48-110">A többi tulajdonság frissítéséhez lásd a [Set-AzScheduledQueryRule](https://docs.microsoft.com/powershell/module/az.monitor/set-azscheduledqueryrule) parancsot.</span><span class="sxs-lookup"><span data-stu-id="fbb48-110">To update other properties, see [Set-AzScheduledQueryRule](https://docs.microsoft.com/powershell/module/az.monitor/set-azscheduledqueryrule) command.</span></span>

## <span data-ttu-id="fbb48-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fbb48-111">EXAMPLES</span></span>

### <span data-ttu-id="fbb48-112">1. példa: Frissítés szabálynév szerint</span><span class="sxs-lookup"><span data-stu-id="fbb48-112">Example 1: Update by rule name</span></span>
```powershell
PS C:\> Update-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1" -Enabled $false

Description       : description
Enabled           : false
LastUpdatedTime   : 19-Apr-19 12:49:15 PM
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

### <span data-ttu-id="fbb48-113">2. példa: Frissítés bemeneti objektum alapján</span><span class="sxs-lookup"><span data-stu-id="fbb48-113">Example 2: Update by input object</span></span>
```powershell
PS C:\> Update-AzScheduledQueryRule -InputObject $sqr -Enabled $false

Description       : description
Enabled           : false
LastUpdatedTime   : 19-Apr-19 12:50:18 PM
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

### <span data-ttu-id="fbb48-114">3. példa: Frissítés erőforrás-azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="fbb48-114">Example 3: Update by resource Id</span></span>
```powershell
PS C:\> Update-AzScheduledQueryRule -ResourceId /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1 -Enabled $true

Description       : description
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:51:14 PM
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

## <span data-ttu-id="fbb48-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbb48-115">PARAMETERS</span></span>

### <span data-ttu-id="fbb48-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbb48-116">-DefaultProfile</span></span>
<span data-ttu-id="fbb48-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fbb48-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbb48-118">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="fbb48-118">-Enabled</span></span>
<span data-ttu-id="fbb48-119">Az Azure riasztási állapota – érvényes értékek – $true, $false</span><span class="sxs-lookup"><span data-stu-id="fbb48-119">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="fbb48-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fbb48-120">-InputObject</span></span>
<span data-ttu-id="fbb48-121">Az ütemezett lekérdezési szabály erőforrás</span><span class="sxs-lookup"><span data-stu-id="fbb48-121">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="fbb48-122">-Name</span><span class="sxs-lookup"><span data-stu-id="fbb48-122">-Name</span></span>
<span data-ttu-id="fbb48-123">A riasztás neve</span><span class="sxs-lookup"><span data-stu-id="fbb48-123">The alert name</span></span>

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

### <span data-ttu-id="fbb48-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbb48-124">-ResourceGroupName</span></span>
<span data-ttu-id="fbb48-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="fbb48-125">The resource group name</span></span>

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

### <span data-ttu-id="fbb48-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fbb48-126">-ResourceId</span></span>
<span data-ttu-id="fbb48-127">Az erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="fbb48-127">The resource Id</span></span>

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

### <span data-ttu-id="fbb48-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fbb48-128">-Confirm</span></span>
<span data-ttu-id="fbb48-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fbb48-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbb48-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbb48-130">-WhatIf</span></span>
<span data-ttu-id="fbb48-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fbb48-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbb48-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fbb48-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbb48-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbb48-133">CommonParameters</span></span>
<span data-ttu-id="fbb48-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbb48-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbb48-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fbb48-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbb48-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fbb48-136">INPUTS</span></span>

### <span data-ttu-id="fbb48-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="fbb48-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="fbb48-138">System.String</span><span class="sxs-lookup"><span data-stu-id="fbb48-138">System.String</span></span>

## <span data-ttu-id="fbb48-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbb48-139">OUTPUTS</span></span>

### <span data-ttu-id="fbb48-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="fbb48-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="fbb48-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fbb48-141">NOTES</span></span>

## <span data-ttu-id="fbb48-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fbb48-142">RELATED LINKS</span></span>
