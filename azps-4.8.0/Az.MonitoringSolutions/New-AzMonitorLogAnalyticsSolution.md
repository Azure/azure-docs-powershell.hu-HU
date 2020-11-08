---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/new-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 6747a53f9e714926c5a4d1358e15cb387ddae69a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181784"
---
# <span data-ttu-id="e6cf9-101">New-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="e6cf9-101">New-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="e6cf9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e6cf9-102">SYNOPSIS</span></span>
<span data-ttu-id="e6cf9-103">Naplózó elemzési megoldást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e6cf9-103">Creates a log analytics solution.</span></span>

## <span data-ttu-id="e6cf9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e6cf9-104">SYNTAX</span></span>

```
New-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> -Location <String> -Type <String>
 -WorkspaceResourceId <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e6cf9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e6cf9-105">DESCRIPTION</span></span>
<span data-ttu-id="e6cf9-106">Naplózó elemzési megoldást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e6cf9-106">Creates a log analytics solution.</span></span>

## <span data-ttu-id="e6cf9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e6cf9-107">EXAMPLES</span></span>

### <span data-ttu-id="e6cf9-108">Példa 1: a log Analytics-munkaterülethez tartozó monitor log-elemzési megoldás létrehozása</span><span class="sxs-lookup"><span data-stu-id="e6cf9-108">Example 1: Create a monitor log analytics solution for the log analytics workspace</span></span>
```powershell
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName azureps-manual-test -Name monitoringworkspace-2vob7n
PS C:\> New-AzMonitorLogAnalyticsSolution -Type Containers -ResourceGroupName azureps-manual-test -Location $workspace.Location -WorkspaceResourceId $workspace.ResourceId

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="e6cf9-109">Ez a parancs létrehoz egy monitor log-elemzési megoldást a log Analytics-munkaterülethez.</span><span class="sxs-lookup"><span data-stu-id="e6cf9-109">This command creates a monitor log analytics solution for the log analytics workspace.</span></span>

<span data-ttu-id="e6cf9-110">A leggyakrabban használt típusok a következők:</span><span class="sxs-lookup"><span data-stu-id="e6cf9-110">Commonly used types are:</span></span>

| <span data-ttu-id="e6cf9-111">Írja be</span><span class="sxs-lookup"><span data-stu-id="e6cf9-111">Type</span></span> | <span data-ttu-id="e6cf9-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="e6cf9-112">Description</span></span> |
| :-----| :----- |
| <span data-ttu-id="e6cf9-113">SecurityCenterFree</span><span class="sxs-lookup"><span data-stu-id="e6cf9-113">SecurityCenterFree</span></span> |  <span data-ttu-id="e6cf9-114">Azure Security Center – ingyenes kiadás</span><span class="sxs-lookup"><span data-stu-id="e6cf9-114">Azure Security Center – Free Edition</span></span> |
| <span data-ttu-id="e6cf9-115">Biztonsági</span><span class="sxs-lookup"><span data-stu-id="e6cf9-115">Security</span></span> | <span data-ttu-id="e6cf9-116">Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="e6cf9-116">Azure Security Center</span></span> |
| <span data-ttu-id="e6cf9-117">Frissítések</span><span class="sxs-lookup"><span data-stu-id="e6cf9-117">Updates</span></span> | <span data-ttu-id="e6cf9-118">Frissítés kezelése</span><span class="sxs-lookup"><span data-stu-id="e6cf9-118">Update Management</span></span> |
| <span data-ttu-id="e6cf9-119">ContainerInsights</span><span class="sxs-lookup"><span data-stu-id="e6cf9-119">ContainerInsights</span></span> | <span data-ttu-id="e6cf9-120">Azure monitor konténerekhez</span><span class="sxs-lookup"><span data-stu-id="e6cf9-120">Azure Monitor for Containers</span></span> |
| <span data-ttu-id="e6cf9-121">ServiceMap</span><span class="sxs-lookup"><span data-stu-id="e6cf9-121">ServiceMap</span></span> | <span data-ttu-id="e6cf9-122">Szolgáltatási Térkép</span><span class="sxs-lookup"><span data-stu-id="e6cf9-122">Service Map</span></span> |
| <span data-ttu-id="e6cf9-123">AzureActivity</span><span class="sxs-lookup"><span data-stu-id="e6cf9-123">AzureActivity</span></span> | <span data-ttu-id="e6cf9-124">Műveletnapló-elemzés</span><span class="sxs-lookup"><span data-stu-id="e6cf9-124">Activity log analytics</span></span> |
| <span data-ttu-id="e6cf9-125">ChangeTracking</span><span class="sxs-lookup"><span data-stu-id="e6cf9-125">ChangeTracking</span></span> | <span data-ttu-id="e6cf9-126">A nyomon követés és a leltár módosítása</span><span class="sxs-lookup"><span data-stu-id="e6cf9-126">Change tracking and inventory</span></span> |
| <span data-ttu-id="e6cf9-127">VMInsights</span><span class="sxs-lookup"><span data-stu-id="e6cf9-127">VMInsights</span></span> | <span data-ttu-id="e6cf9-128">Azure monitor VMs-hez</span><span class="sxs-lookup"><span data-stu-id="e6cf9-128">Azure Monitor for VMs</span></span> |
| <span data-ttu-id="e6cf9-129">SecurityInsights</span><span class="sxs-lookup"><span data-stu-id="e6cf9-129">SecurityInsights</span></span> | <span data-ttu-id="e6cf9-130">Azure Sentinel</span><span class="sxs-lookup"><span data-stu-id="e6cf9-130">Azure Sentinel</span></span> |
| <span data-ttu-id="e6cf9-131">NetworkMonitoring</span><span class="sxs-lookup"><span data-stu-id="e6cf9-131">NetworkMonitoring</span></span> | <span data-ttu-id="e6cf9-132">Hálózati Teljesítményfigyelő</span><span class="sxs-lookup"><span data-stu-id="e6cf9-132">Network Performance Monitor</span></span> |
| <span data-ttu-id="e6cf9-133">SQLVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="e6cf9-133">SQLVulnerabilityAssessment</span></span> | <span data-ttu-id="e6cf9-134">Az SQL sebezhetőségi felmérése</span><span class="sxs-lookup"><span data-stu-id="e6cf9-134">SQL Vulnerability Assessment</span></span> |
| <span data-ttu-id="e6cf9-135">SQLAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="e6cf9-135">SQLAdvancedThreatProtection</span></span> | <span data-ttu-id="e6cf9-136">Az SQL Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="e6cf9-136">SQL Advanced Threat Protection</span></span> |
| <span data-ttu-id="e6cf9-137">Kártevőirtási</span><span class="sxs-lookup"><span data-stu-id="e6cf9-137">AntiMalware</span></span> | <span data-ttu-id="e6cf9-138">Antimalware-felmérés</span><span class="sxs-lookup"><span data-stu-id="e6cf9-138">Antimalware Assessment</span></span> |
| <span data-ttu-id="e6cf9-139">AzureAutomation</span><span class="sxs-lookup"><span data-stu-id="e6cf9-139">AzureAutomation</span></span> | <span data-ttu-id="e6cf9-140">Automatizálás hibrid munkás</span><span class="sxs-lookup"><span data-stu-id="e6cf9-140">Automation Hybrid Worker</span></span> |
| <span data-ttu-id="e6cf9-141">LogicAppsManagement</span><span class="sxs-lookup"><span data-stu-id="e6cf9-141">LogicAppsManagement</span></span> | <span data-ttu-id="e6cf9-142">Logikai alkalmazások kezelése</span><span class="sxs-lookup"><span data-stu-id="e6cf9-142">Logic Apps Management</span></span> |
| <span data-ttu-id="e6cf9-143">SQLDataClassification</span><span class="sxs-lookup"><span data-stu-id="e6cf9-143">SQLDataClassification</span></span> | <span data-ttu-id="e6cf9-144">SQL-adatfeltárási & osztályozása</span><span class="sxs-lookup"><span data-stu-id="e6cf9-144">SQL Data Discovery & Classification</span></span> |

## <span data-ttu-id="e6cf9-145">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e6cf9-145">PARAMETERS</span></span>

### <span data-ttu-id="e6cf9-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6cf9-146">-DefaultProfile</span></span>
<span data-ttu-id="e6cf9-147">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6cf9-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6cf9-148">-Hely</span><span class="sxs-lookup"><span data-stu-id="e6cf9-148">-Location</span></span>
<span data-ttu-id="e6cf9-149">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="e6cf9-149">Resource location.</span></span>
<span data-ttu-id="e6cf9-150">Egyeznie kell a napló analitikus munkaterületével.</span><span class="sxs-lookup"><span data-stu-id="e6cf9-150">Must be the same as the log analytic workspace.</span></span>

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

### <span data-ttu-id="e6cf9-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6cf9-151">-ResourceGroupName</span></span>
<span data-ttu-id="e6cf9-152">A beolvasott erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e6cf9-152">The name of the resource group to get.</span></span>
<span data-ttu-id="e6cf9-153">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="e6cf9-153">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e6cf9-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e6cf9-154">-SubscriptionId</span></span>
<span data-ttu-id="e6cf9-155">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e6cf9-155">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e6cf9-156">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="e6cf9-156">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e6cf9-157">-Címke</span><span class="sxs-lookup"><span data-stu-id="e6cf9-157">-Tag</span></span>
<span data-ttu-id="e6cf9-158">Erőforrás-Címkék</span><span class="sxs-lookup"><span data-stu-id="e6cf9-158">Resource tags</span></span>

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

### <span data-ttu-id="e6cf9-159">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="e6cf9-159">-Type</span></span>
<span data-ttu-id="e6cf9-160">A létrehozandó megoldás típusa.</span><span class="sxs-lookup"><span data-stu-id="e6cf9-160">Type of the solution to be created.</span></span>
<span data-ttu-id="e6cf9-161">Például "Container".</span><span class="sxs-lookup"><span data-stu-id="e6cf9-161">For example "Container".</span></span>

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

### <span data-ttu-id="e6cf9-162">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="e6cf9-162">-WorkspaceResourceId</span></span>
<span data-ttu-id="e6cf9-163">Annak a munkaterületnek az Azure Resource ID azonosítója, ahol a megoldást telepíteni vagy engedélyezni kívánja.</span><span class="sxs-lookup"><span data-stu-id="e6cf9-163">The Azure resource ID for the workspace where the solution will be deployed/enabled.</span></span>

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

### <span data-ttu-id="e6cf9-164">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e6cf9-164">-Confirm</span></span>
<span data-ttu-id="e6cf9-165">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e6cf9-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6cf9-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6cf9-166">-WhatIf</span></span>
<span data-ttu-id="e6cf9-167">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e6cf9-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6cf9-168">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e6cf9-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6cf9-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6cf9-169">CommonParameters</span></span>
<span data-ttu-id="e6cf9-170">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e6cf9-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6cf9-171">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e6cf9-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6cf9-172">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6cf9-172">INPUTS</span></span>

## <span data-ttu-id="e6cf9-173">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6cf9-173">OUTPUTS</span></span>

### <span data-ttu-id="e6cf9-174">Microsoft. Azure. PowerShell. parancsmagok. MonitoringSolutions. modellek. Api20151101Preview. ISolution</span><span class="sxs-lookup"><span data-stu-id="e6cf9-174">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="e6cf9-175">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e6cf9-175">NOTES</span></span>

<span data-ttu-id="e6cf9-176">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e6cf9-176">ALIASES</span></span>

## <span data-ttu-id="e6cf9-177">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6cf9-177">RELATED LINKS</span></span>



[<span data-ttu-id="e6cf9-178">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="e6cf9-178">Get-AzOperationalInsightsWorkspace</span></span>](https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace)

