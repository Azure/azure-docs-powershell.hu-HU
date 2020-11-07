---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
ms.openlocfilehash: e3a5cbe95bf524a70194cfce7e0b8bb80b701dec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668190"
---
# <span data-ttu-id="e79f6-101">Get-AzAlert</span><span class="sxs-lookup"><span data-stu-id="e79f6-101">Get-AzAlert</span></span>

## <span data-ttu-id="e79f6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e79f6-102">SYNOPSIS</span></span>
<span data-ttu-id="e79f6-103">Riasztási adatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="e79f6-103">Get Alerts Information</span></span>

## <span data-ttu-id="e79f6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e79f6-104">SYNTAX</span></span>

### <span data-ttu-id="e79f6-105">AlertsListByFilter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e79f6-105">AlertsListByFilter (Default)</span></span>
```
Get-AzAlert [-TargetResourceType <String>] [-TargetResourceGroup <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-SmartGroupId <String>] [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>]
 [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e79f6-106">AlertById</span><span class="sxs-lookup"><span data-stu-id="e79f6-106">AlertById</span></span>
```
Get-AzAlert -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e79f6-107">AlertsListByTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="e79f6-107">AlertsListByTargetResourceIdFilter</span></span>
```
Get-AzAlert [-TargetResourceId <String>] [-MonitorService <String>] [-MonitorCondition <String>]
 [-Severity <String>] [-State <String>] [-AlertRuleId <String>] [-SmartGroupId <String>]
 [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>] [-SortBy <String>]
 [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e79f6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e79f6-108">DESCRIPTION</span></span>
<span data-ttu-id="e79f6-109">A **Get-AzAlert** parancsmag riasztási példányokat kap.</span><span class="sxs-lookup"><span data-stu-id="e79f6-109">**Get-AzAlert** cmdlet gets fired alert instances.</span></span>

## <span data-ttu-id="e79f6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e79f6-110">EXAMPLES</span></span>

### <span data-ttu-id="e79f6-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e79f6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAlert -Severity "Sev2" -MonitorCondition "Fired" -IncludeContext true
```

<span data-ttu-id="e79f6-112">A Sev2 súlyosságát és a kilőtt figyelési feltételt tartalmazó összes riasztás felsorolása.</span><span class="sxs-lookup"><span data-stu-id="e79f6-112">List all alerts with Sev2 severity and Fired monitor condition.</span></span> <span data-ttu-id="e79f6-113">Ha a IncludeContext igaz értékre állítja, a riasztás egyéni adattartalmát is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="e79f6-113">Setting IncludeContext to true, include custom payload of alert.</span></span>
<span data-ttu-id="e79f6-114">A Format-List használatával megtudhatja, hogy miként jelenítheti meg az egyes értesítések teljes tartalmát a listáról.</span><span class="sxs-lookup"><span data-stu-id="e79f6-114">Use Format-List to get the complete details of each alert in list.</span></span>

### <span data-ttu-id="e79f6-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="e79f6-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAlert -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="e79f6-116">Értesítési adatok beszerzése azonosítóval (GUID) vagy erőforrás-azonosítóval (teljes kar-azonosító)</span><span class="sxs-lookup"><span data-stu-id="e79f6-116">Get Alert details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

## <span data-ttu-id="e79f6-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e79f6-117">PARAMETERS</span></span>

### <span data-ttu-id="e79f6-118">-AlertId</span><span class="sxs-lookup"><span data-stu-id="e79f6-118">-AlertId</span></span>
<span data-ttu-id="e79f6-119">Értesítési/ResourceId egyedi azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e79f6-119">Unique Identifier of Alert / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e79f6-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="e79f6-120">-AlertRuleId</span></span>
<span data-ttu-id="e79f6-121">Szűrés riasztási szabály azonosítójával</span><span class="sxs-lookup"><span data-stu-id="e79f6-121">Filter on Alert Rule Id</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e79f6-122">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="e79f6-122">-CustomTimeRange</span></span>
<span data-ttu-id="e79f6-123">Támogatott formátum – \< a kezdési idő záró időpontja, \> / \< Ha az \> idő az ISO-8601 formátumban van</span><span class="sxs-lookup"><span data-stu-id="e79f6-123">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e79f6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e79f6-124">-DefaultProfile</span></span>
<span data-ttu-id="e79f6-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e79f6-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e79f6-126">-IncludeContext</span><span class="sxs-lookup"><span data-stu-id="e79f6-126">-IncludeContext</span></span>
<span data-ttu-id="e79f6-127">A riasztás környezete (egyéni adattartalom) befoglalása</span><span class="sxs-lookup"><span data-stu-id="e79f6-127">Include context (custom payload) of alert</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e79f6-128">-IncludeEgressConfig</span><span class="sxs-lookup"><span data-stu-id="e79f6-128">-IncludeEgressConfig</span></span>
<span data-ttu-id="e79f6-129">EgressConfig belefoglalása</span><span class="sxs-lookup"><span data-stu-id="e79f6-129">Include EgressConfig</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e79f6-130">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="e79f6-130">-MonitorCondition</span></span>
<span data-ttu-id="e79f6-131">Szűrés a monitor feltételén</span><span class="sxs-lookup"><span data-stu-id="e79f6-131">Filter on Monitor Condition</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e79f6-132">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="e79f6-132">-MonitorService</span></span>
<span data-ttu-id="e79f6-133">Szűrés a moniter szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="e79f6-133">Filter on Moniter Service</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e79f6-134">-PageCount</span><span class="sxs-lookup"><span data-stu-id="e79f6-134">-PageCount</span></span>
<span data-ttu-id="e79f6-135">A lapon beolvasott értesítések száma.</span><span class="sxs-lookup"><span data-stu-id="e79f6-135">Number of alerts to be fetched in a page.</span></span>

```yaml
Type: System.Int32
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e79f6-136">-Válassza a</span><span class="sxs-lookup"><span data-stu-id="e79f6-136">-Select</span></span>
<span data-ttu-id="e79f6-137">Végezze el a szükséges mezőket a Essentials csomagból.</span><span class="sxs-lookup"><span data-stu-id="e79f6-137">Project the required fields out of essentials.</span></span>
<span data-ttu-id="e79f6-138">A várt bemenet pontosvesszővel elválasztva.</span><span class="sxs-lookup"><span data-stu-id="e79f6-138">Expected input is comma-separated.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e79f6-139">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="e79f6-139">-Severity</span></span>
<span data-ttu-id="e79f6-140">Az értesítés súlyosságának szűrése</span><span class="sxs-lookup"><span data-stu-id="e79f6-140">Filter on Severity of alert</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e79f6-141">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="e79f6-141">-SmartGroupId</span></span>
<span data-ttu-id="e79f6-142">Az intelligens csoport azonosítóját azonosító értesítések szűrése</span><span class="sxs-lookup"><span data-stu-id="e79f6-142">Filter all the alerts having the Smart Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e79f6-143">-SortBy</span><span class="sxs-lookup"><span data-stu-id="e79f6-143">-SortBy</span></span>
<span data-ttu-id="e79f6-144">A rendezés során használni kívánt riasztási tulajdonság</span><span class="sxs-lookup"><span data-stu-id="e79f6-144">Alert property to use while sorting</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e79f6-145">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="e79f6-145">-SortOrder</span></span>
<span data-ttu-id="e79f6-146">Rendezési sorrend</span><span class="sxs-lookup"><span data-stu-id="e79f6-146">Sort Order</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e79f6-147">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="e79f6-147">-State</span></span>
<span data-ttu-id="e79f6-148">A riasztási állapot szűrése</span><span class="sxs-lookup"><span data-stu-id="e79f6-148">Filter on State of alert</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e79f6-149">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e79f6-149">-TargetResourceGroup</span></span>
<span data-ttu-id="e79f6-150">Szűrés a riasztás céljára szolgáló erőforrás erőforráscsoport nevében</span><span class="sxs-lookup"><span data-stu-id="e79f6-150">Filter on Resource group name of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e79f6-151">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="e79f6-151">-TargetResourceId</span></span>
<span data-ttu-id="e79f6-152">Szűri az értesítés cél erőforrásának erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="e79f6-152">Filter on Resource Id of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e79f6-153">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="e79f6-153">-TargetResourceType</span></span>
<span data-ttu-id="e79f6-154">Szűrés az értesítés cél erőforrásának erőforrás-típusára vonatkozóan</span><span class="sxs-lookup"><span data-stu-id="e79f6-154">Filter on Resource type of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e79f6-155">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="e79f6-155">-TimeRange</span></span>
<span data-ttu-id="e79f6-156">Támogatott időtartomány-értékek – 1h, 1d, 7D, 30d (alapérték: 1d)</span><span class="sxs-lookup"><span data-stu-id="e79f6-156">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e79f6-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e79f6-157">CommonParameters</span></span>
<span data-ttu-id="e79f6-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e79f6-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e79f6-159">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e79f6-159">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e79f6-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e79f6-160">INPUTS</span></span>

### <span data-ttu-id="e79f6-161">Nincs</span><span class="sxs-lookup"><span data-stu-id="e79f6-161">None</span></span>

## <span data-ttu-id="e79f6-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e79f6-162">OUTPUTS</span></span>

### <span data-ttu-id="e79f6-163">Microsoft. Azure. Command. AlertsManagement. OutputModels. PSAlert</span><span class="sxs-lookup"><span data-stu-id="e79f6-163">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="e79f6-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e79f6-164">NOTES</span></span>

## <span data-ttu-id="e79f6-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e79f6-165">RELATED LINKS</span></span>
