---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/powershell/module/az.monitoringsolutions/new-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: ff9a54852d84d7c1183e81cb8b597279f357ebe8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925482"
---
# <span data-ttu-id="f9cd6-101">New-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="f9cd6-101">New-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="f9cd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9cd6-102">SYNOPSIS</span></span>
<span data-ttu-id="f9cd6-103">Naplóelemzési megoldást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f9cd6-103">Creates a log analytics solution.</span></span>

## <span data-ttu-id="f9cd6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f9cd6-104">SYNTAX</span></span>

```
New-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> -Location <String> -Type <String>
 -WorkspaceResourceId <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f9cd6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f9cd6-105">DESCRIPTION</span></span>
<span data-ttu-id="f9cd6-106">Naplóelemzési megoldást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f9cd6-106">Creates a log analytics solution.</span></span>

## <span data-ttu-id="f9cd6-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f9cd6-107">EXAMPLES</span></span>

### <span data-ttu-id="f9cd6-108">1. példa: Figyeléselemzési megoldás létrehozása a naplóelemzési munkaterülethez</span><span class="sxs-lookup"><span data-stu-id="f9cd6-108">Example 1: Create a monitor log analytics solution for the log analytics workspace</span></span>
```powershell
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName azureps-manual-test -Name monitoringworkspace-2vob7n
PS C:\> New-AzMonitorLogAnalyticsSolution -Type Containers -ResourceGroupName azureps-manual-test -Location $workspace.Location -WorkspaceResourceId $workspace.ResourceId

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="f9cd6-109">Ez a parancs monitornapló-elemzési megoldást hoz létre a naplóelemzés munkaterületéhez.</span><span class="sxs-lookup"><span data-stu-id="f9cd6-109">This command creates a monitor log analytics solution for the log analytics workspace.</span></span>

<span data-ttu-id="f9cd6-110">A gyakran használt típusok:</span><span class="sxs-lookup"><span data-stu-id="f9cd6-110">Commonly used types are:</span></span>

| <span data-ttu-id="f9cd6-111">Típus</span><span class="sxs-lookup"><span data-stu-id="f9cd6-111">Type</span></span> | <span data-ttu-id="f9cd6-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="f9cd6-112">Description</span></span> |
| :-----| :----- |
| <span data-ttu-id="f9cd6-113">SecurityCenterFree</span><span class="sxs-lookup"><span data-stu-id="f9cd6-113">SecurityCenterFree</span></span> |  <span data-ttu-id="f9cd6-114">Azure Security Center – Free Edition</span><span class="sxs-lookup"><span data-stu-id="f9cd6-114">Azure Security Center – Free Edition</span></span> |
| <span data-ttu-id="f9cd6-115">Biztonság</span><span class="sxs-lookup"><span data-stu-id="f9cd6-115">Security</span></span> | <span data-ttu-id="f9cd6-116">Azure Biztonsági központ</span><span class="sxs-lookup"><span data-stu-id="f9cd6-116">Azure Security Center</span></span> |
| <span data-ttu-id="f9cd6-117">Frissítések</span><span class="sxs-lookup"><span data-stu-id="f9cd6-117">Updates</span></span> | <span data-ttu-id="f9cd6-118">Frissítéskezelés</span><span class="sxs-lookup"><span data-stu-id="f9cd6-118">Update Management</span></span> |
| <span data-ttu-id="f9cd6-119">ContainerInsights</span><span class="sxs-lookup"><span data-stu-id="f9cd6-119">ContainerInsights</span></span> | <span data-ttu-id="f9cd6-120">Tárolók Azure Monitora</span><span class="sxs-lookup"><span data-stu-id="f9cd6-120">Azure Monitor for Containers</span></span> |
| <span data-ttu-id="f9cd6-121">ServiceMap</span><span class="sxs-lookup"><span data-stu-id="f9cd6-121">ServiceMap</span></span> | <span data-ttu-id="f9cd6-122">Szolgáltatástérkép</span><span class="sxs-lookup"><span data-stu-id="f9cd6-122">Service Map</span></span> |
| <span data-ttu-id="f9cd6-123">AzureActivity</span><span class="sxs-lookup"><span data-stu-id="f9cd6-123">AzureActivity</span></span> | <span data-ttu-id="f9cd6-124">Tevékenységnapló-elemzések</span><span class="sxs-lookup"><span data-stu-id="f9cd6-124">Activity log analytics</span></span> |
| <span data-ttu-id="f9cd6-125">ChangeTracking</span><span class="sxs-lookup"><span data-stu-id="f9cd6-125">ChangeTracking</span></span> | <span data-ttu-id="f9cd6-126">A nyomon követés és a készlet módosítása</span><span class="sxs-lookup"><span data-stu-id="f9cd6-126">Change tracking and inventory</span></span> |
| <span data-ttu-id="f9cd6-127">VMInsights</span><span class="sxs-lookup"><span data-stu-id="f9cd6-127">VMInsights</span></span> | <span data-ttu-id="f9cd6-128">Azure Monitor vMs-hez</span><span class="sxs-lookup"><span data-stu-id="f9cd6-128">Azure Monitor for VMs</span></span> |
| <span data-ttu-id="f9cd6-129">SecurityInsights</span><span class="sxs-lookup"><span data-stu-id="f9cd6-129">SecurityInsights</span></span> | <span data-ttu-id="f9cd6-130">Azure Sentinel</span><span class="sxs-lookup"><span data-stu-id="f9cd6-130">Azure Sentinel</span></span> |
| <span data-ttu-id="f9cd6-131">NetworkMonitoring</span><span class="sxs-lookup"><span data-stu-id="f9cd6-131">NetworkMonitoring</span></span> | <span data-ttu-id="f9cd6-132">Hálózati teljesítményfigyelő</span><span class="sxs-lookup"><span data-stu-id="f9cd6-132">Network Performance Monitor</span></span> |
| <span data-ttu-id="f9cd6-133">SQLVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="f9cd6-133">SQLVulnerabilityAssessment</span></span> | <span data-ttu-id="f9cd6-134">SQL-biztonsági rés felmérése</span><span class="sxs-lookup"><span data-stu-id="f9cd6-134">SQL Vulnerability Assessment</span></span> |
| <span data-ttu-id="f9cd6-135">SQLAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="f9cd6-135">SQLAdvancedThreatProtection</span></span> | <span data-ttu-id="f9cd6-136">SQL Komplex veszélyforrások elleni védelem</span><span class="sxs-lookup"><span data-stu-id="f9cd6-136">SQL Advanced Threat Protection</span></span> |
| <span data-ttu-id="f9cd6-137">Kártevőirtó</span><span class="sxs-lookup"><span data-stu-id="f9cd6-137">AntiMalware</span></span> | <span data-ttu-id="f9cd6-138">Kártevőirtó felmérés</span><span class="sxs-lookup"><span data-stu-id="f9cd6-138">Antimalware Assessment</span></span> |
| <span data-ttu-id="f9cd6-139">AzureAutomation</span><span class="sxs-lookup"><span data-stu-id="f9cd6-139">AzureAutomation</span></span> | <span data-ttu-id="f9cd6-140">Automatizálási hibrid dolgozó</span><span class="sxs-lookup"><span data-stu-id="f9cd6-140">Automation Hybrid Worker</span></span> |
| <span data-ttu-id="f9cd6-141">LogicAppsManagement</span><span class="sxs-lookup"><span data-stu-id="f9cd6-141">LogicAppsManagement</span></span> | <span data-ttu-id="f9cd6-142">Logic Apps Management</span><span class="sxs-lookup"><span data-stu-id="f9cd6-142">Logic Apps Management</span></span> |
| <span data-ttu-id="f9cd6-143">SQLDataClassification</span><span class="sxs-lookup"><span data-stu-id="f9cd6-143">SQLDataClassification</span></span> | <span data-ttu-id="f9cd6-144">SQL Data Discovery & Besorolás</span><span class="sxs-lookup"><span data-stu-id="f9cd6-144">SQL Data Discovery & Classification</span></span> |

## <span data-ttu-id="f9cd6-145">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9cd6-145">PARAMETERS</span></span>

### <span data-ttu-id="f9cd6-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9cd6-146">-DefaultProfile</span></span>
<span data-ttu-id="f9cd6-147">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f9cd6-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9cd6-148">-Location</span><span class="sxs-lookup"><span data-stu-id="f9cd6-148">-Location</span></span>
<span data-ttu-id="f9cd6-149">Erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="f9cd6-149">Resource location.</span></span>
<span data-ttu-id="f9cd6-150">A napló analytic munkaterületének meg kell egyennek lennie.</span><span class="sxs-lookup"><span data-stu-id="f9cd6-150">Must be the same as the log analytic workspace.</span></span>

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

### <span data-ttu-id="f9cd6-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9cd6-151">-ResourceGroupName</span></span>
<span data-ttu-id="f9cd6-152">A lekért erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f9cd6-152">The name of the resource group to get.</span></span>
<span data-ttu-id="f9cd6-153">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="f9cd6-153">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f9cd6-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f9cd6-154">-SubscriptionId</span></span>
<span data-ttu-id="f9cd6-155">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="f9cd6-155">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f9cd6-156">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="f9cd6-156">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9cd6-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="f9cd6-157">-Tag</span></span>
<span data-ttu-id="f9cd6-158">Erőforráscímkék</span><span class="sxs-lookup"><span data-stu-id="f9cd6-158">Resource tags</span></span>

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

### <span data-ttu-id="f9cd6-159">-Type</span><span class="sxs-lookup"><span data-stu-id="f9cd6-159">-Type</span></span>
<span data-ttu-id="f9cd6-160">A létrehozható megoldás típusa.</span><span class="sxs-lookup"><span data-stu-id="f9cd6-160">Type of the solution to be created.</span></span>
<span data-ttu-id="f9cd6-161">Példa: "Tároló".</span><span class="sxs-lookup"><span data-stu-id="f9cd6-161">For example "Container".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SolutionType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9cd6-162">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="f9cd6-162">-WorkspaceResourceId</span></span>
<span data-ttu-id="f9cd6-163">Annak a munkaterületnek az Azure-erőforrás-azonosítója, ahol a megoldás telepítve/engedélyezve lesz.</span><span class="sxs-lookup"><span data-stu-id="f9cd6-163">The Azure resource ID for the workspace where the solution will be deployed/enabled.</span></span>

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

### <span data-ttu-id="f9cd6-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9cd6-164">-Confirm</span></span>
<span data-ttu-id="f9cd6-165">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f9cd6-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9cd6-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9cd6-166">-WhatIf</span></span>
<span data-ttu-id="f9cd6-167">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f9cd6-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9cd6-168">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f9cd6-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9cd6-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9cd6-169">CommonParameters</span></span>
<span data-ttu-id="f9cd6-170">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9cd6-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9cd6-171">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9cd6-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9cd6-172">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f9cd6-172">INPUTS</span></span>

## <span data-ttu-id="f9cd6-173">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9cd6-173">OUTPUTS</span></span>

### <span data-ttu-id="f9cd6-174">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="f9cd6-174">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="f9cd6-175">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f9cd6-175">NOTES</span></span>

<span data-ttu-id="f9cd6-176">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f9cd6-176">ALIASES</span></span>

## <span data-ttu-id="f9cd6-177">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f9cd6-177">RELATED LINKS</span></span>



[<span data-ttu-id="f9cd6-178">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="f9cd6-178">Get-AzOperationalInsightsWorkspace</span></span>](https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace)

