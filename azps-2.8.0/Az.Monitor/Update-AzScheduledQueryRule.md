---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
ms.openlocfilehash: 0a2214abfd6e48dc96ad675610a85a0ec7e8e5fd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837721"
---
# <span data-ttu-id="e6fb1-101">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e6fb1-101">Update-AzScheduledQueryRule</span></span>

## <span data-ttu-id="e6fb1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e6fb1-102">SYNOPSIS</span></span>
<span data-ttu-id="e6fb1-103">Naplózási riasztási szabály frissítése</span><span class="sxs-lookup"><span data-stu-id="e6fb1-103">Updates a Log Alert rule</span></span>

## <span data-ttu-id="e6fb1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e6fb1-104">SYNTAX</span></span>

### <span data-ttu-id="e6fb1-105">ByRuleName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e6fb1-105">ByRuleName (Default)</span></span>
```
Update-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6fb1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e6fb1-106">ByInputObject</span></span>
```
Update-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6fb1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e6fb1-107">ByResourceId</span></span>
```
Update-AzScheduledQueryRule -ResourceId <String> -Enabled <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6fb1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e6fb1-108">DESCRIPTION</span></span>
<span data-ttu-id="e6fb1-109">Naplózási riasztási szabály frissítése, ha a parancs támogatja a csak az "enabled" tulajdonság frissítését.</span><span class="sxs-lookup"><span data-stu-id="e6fb1-109">Updates a Log Alert rule, updating only "Enabled" property is supported by this command.</span></span>
<span data-ttu-id="e6fb1-110">A többi tulajdonság frissítéséről a "set-AzScheduledQueryRule" parancs nyújt tájékoztatást.</span><span class="sxs-lookup"><span data-stu-id="e6fb1-110">To update other properties, see "Set-AzScheduledQueryRule" command.</span></span>

## <span data-ttu-id="e6fb1-111">Példák</span><span class="sxs-lookup"><span data-stu-id="e6fb1-111">EXAMPLES</span></span>

### <span data-ttu-id="e6fb1-112">Példa 1 – szabály nevének frissítése</span><span class="sxs-lookup"><span data-stu-id="e6fb1-112">Example 1 - Update by rule name</span></span>
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

### <span data-ttu-id="e6fb1-113">Példa 2 – beviteli objektum általi frissítés</span><span class="sxs-lookup"><span data-stu-id="e6fb1-113">Example 2 - Update by input object</span></span>
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

### <span data-ttu-id="e6fb1-114">Példa 3 – erőforrás-azonosítóval való frissítés</span><span class="sxs-lookup"><span data-stu-id="e6fb1-114">Example 3 - Update by resource Id</span></span>
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

## <span data-ttu-id="e6fb1-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e6fb1-115">PARAMETERS</span></span>

### <span data-ttu-id="e6fb1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6fb1-116">-DefaultProfile</span></span>
<span data-ttu-id="e6fb1-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6fb1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6fb1-118">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="e6fb1-118">-Enabled</span></span>
<span data-ttu-id="e6fb1-119">Az Azure riasztási állapota – érvényes értékek – $true, $false</span><span class="sxs-lookup"><span data-stu-id="e6fb1-119">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="e6fb1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6fb1-120">-InputObject</span></span>
<span data-ttu-id="e6fb1-121">Az ütemezett lekérdezési szabály erőforrás</span><span class="sxs-lookup"><span data-stu-id="e6fb1-121">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="e6fb1-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e6fb1-122">-Name</span></span>
<span data-ttu-id="e6fb1-123">A riasztás neve</span><span class="sxs-lookup"><span data-stu-id="e6fb1-123">The alert name</span></span>

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

### <span data-ttu-id="e6fb1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6fb1-124">-ResourceGroupName</span></span>
<span data-ttu-id="e6fb1-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e6fb1-125">The resource group name</span></span>

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

### <span data-ttu-id="e6fb1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6fb1-126">-ResourceId</span></span>
<span data-ttu-id="e6fb1-127">Az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="e6fb1-127">The resource Id</span></span>

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

### <span data-ttu-id="e6fb1-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e6fb1-128">-Confirm</span></span>
<span data-ttu-id="e6fb1-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e6fb1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6fb1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6fb1-130">-WhatIf</span></span>
<span data-ttu-id="e6fb1-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e6fb1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6fb1-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e6fb1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6fb1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6fb1-133">CommonParameters</span></span>
<span data-ttu-id="e6fb1-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e6fb1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6fb1-135">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e6fb1-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6fb1-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6fb1-136">INPUTS</span></span>

### <span data-ttu-id="e6fb1-137">Microsoft. Azure. commands. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="e6fb1-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="e6fb1-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e6fb1-138">System.String</span></span>

## <span data-ttu-id="e6fb1-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6fb1-139">OUTPUTS</span></span>

### <span data-ttu-id="e6fb1-140">Microsoft. Azure. commands. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="e6fb1-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="e6fb1-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e6fb1-141">NOTES</span></span>

## <span data-ttu-id="e6fb1-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6fb1-142">RELATED LINKS</span></span>
