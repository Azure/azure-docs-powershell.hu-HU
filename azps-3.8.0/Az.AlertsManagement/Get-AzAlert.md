---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
ms.openlocfilehash: da462e5a8fd95b32275e37097bef18a2e7928d6e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011207"
---
# <span data-ttu-id="c4c2d-101">Get-AzAlert</span><span class="sxs-lookup"><span data-stu-id="c4c2d-101">Get-AzAlert</span></span>

## <span data-ttu-id="c4c2d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c4c2d-102">SYNOPSIS</span></span>
<span data-ttu-id="c4c2d-103">Riasztási adatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="c4c2d-103">Get Alerts Information</span></span>

## <span data-ttu-id="c4c2d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c4c2d-104">SYNTAX</span></span>

### <span data-ttu-id="c4c2d-105">AlertsListByFilter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c4c2d-105">AlertsListByFilter (Default)</span></span>
```
Get-AzAlert [-TargetResourceType <String>] [-TargetResourceGroup <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-SmartGroupId <String>] [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>]
 [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4c2d-106">AlertById</span><span class="sxs-lookup"><span data-stu-id="c4c2d-106">AlertById</span></span>
```
Get-AzAlert -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4c2d-107">AlertsListByTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="c4c2d-107">AlertsListByTargetResourceIdFilter</span></span>
```
Get-AzAlert [-TargetResourceId <String>] [-MonitorService <String>] [-MonitorCondition <String>]
 [-Severity <String>] [-State <String>] [-AlertRuleId <String>] [-SmartGroupId <String>]
 [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>] [-SortBy <String>]
 [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4c2d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c4c2d-108">DESCRIPTION</span></span>
<span data-ttu-id="c4c2d-109">A **Get-AzAlert** parancsmag riasztási példányokat kap.</span><span class="sxs-lookup"><span data-stu-id="c4c2d-109">**Get-AzAlert** cmdlet gets fired alert instances.</span></span>

## <span data-ttu-id="c4c2d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c4c2d-110">EXAMPLES</span></span>

### <span data-ttu-id="c4c2d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c4c2d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAlert -Severity "Sev2" -MonitorCondition "Fired" -IncludeContext true
```

<span data-ttu-id="c4c2d-112">A Sev2 súlyosságát és a kilőtt figyelési feltételt tartalmazó összes riasztás felsorolása.</span><span class="sxs-lookup"><span data-stu-id="c4c2d-112">List all alerts with Sev2 severity and Fired monitor condition.</span></span> <span data-ttu-id="c4c2d-113">Ha a IncludeContext igaz értékre állítja, a riasztás egyéni adattartalmát is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="c4c2d-113">Setting IncludeContext to true, include custom payload of alert.</span></span>
<span data-ttu-id="c4c2d-114">A Format-List használatával megtudhatja, hogy miként jelenítheti meg az egyes értesítések teljes tartalmát a listáról.</span><span class="sxs-lookup"><span data-stu-id="c4c2d-114">Use Format-List to get the complete details of each alert in list.</span></span>

### <span data-ttu-id="c4c2d-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="c4c2d-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAlert -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="c4c2d-116">Értesítési adatok beszerzése azonosítóval (GUID) vagy erőforrás-azonosítóval (teljes kar-azonosító)</span><span class="sxs-lookup"><span data-stu-id="c4c2d-116">Get Alert details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

## <span data-ttu-id="c4c2d-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c4c2d-117">PARAMETERS</span></span>

### <span data-ttu-id="c4c2d-118">-AlertId</span><span class="sxs-lookup"><span data-stu-id="c4c2d-118">-AlertId</span></span>
<span data-ttu-id="c4c2d-119">Értesítési/ResourceId egyedi azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c4c2d-119">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="c4c2d-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="c4c2d-120">-AlertRuleId</span></span>
<span data-ttu-id="c4c2d-121">Szűrés riasztási szabály azonosítójával</span><span class="sxs-lookup"><span data-stu-id="c4c2d-121">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="c4c2d-122">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="c4c2d-122">-CustomTimeRange</span></span>
<span data-ttu-id="c4c2d-123">Támogatott formátum – \< a kezdési idő záró időpontja, \> / \< Ha az \> idő az ISO-8601 formátumban van</span><span class="sxs-lookup"><span data-stu-id="c4c2d-123">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="c4c2d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4c2d-124">-DefaultProfile</span></span>
<span data-ttu-id="c4c2d-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c4c2d-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4c2d-126">-IncludeContext</span><span class="sxs-lookup"><span data-stu-id="c4c2d-126">-IncludeContext</span></span>
<span data-ttu-id="c4c2d-127">A riasztás környezete (egyéni adattartalom) befoglalása</span><span class="sxs-lookup"><span data-stu-id="c4c2d-127">Include context (custom payload) of alert</span></span>

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

### <span data-ttu-id="c4c2d-128">-IncludeEgressConfig</span><span class="sxs-lookup"><span data-stu-id="c4c2d-128">-IncludeEgressConfig</span></span>
<span data-ttu-id="c4c2d-129">EgressConfig belefoglalása</span><span class="sxs-lookup"><span data-stu-id="c4c2d-129">Include EgressConfig</span></span>

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

### <span data-ttu-id="c4c2d-130">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="c4c2d-130">-MonitorCondition</span></span>
<span data-ttu-id="c4c2d-131">Szűrés a monitor feltételén</span><span class="sxs-lookup"><span data-stu-id="c4c2d-131">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="c4c2d-132">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="c4c2d-132">-MonitorService</span></span>
<span data-ttu-id="c4c2d-133">Szűrés a moniter szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="c4c2d-133">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="c4c2d-134">-PageCount</span><span class="sxs-lookup"><span data-stu-id="c4c2d-134">-PageCount</span></span>
<span data-ttu-id="c4c2d-135">A lapon beolvasott értesítések száma.</span><span class="sxs-lookup"><span data-stu-id="c4c2d-135">Number of alerts to be fetched in a page.</span></span>

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

### <span data-ttu-id="c4c2d-136">-Válassza a</span><span class="sxs-lookup"><span data-stu-id="c4c2d-136">-Select</span></span>
<span data-ttu-id="c4c2d-137">Végezze el a szükséges mezőket a Essentials csomagból.</span><span class="sxs-lookup"><span data-stu-id="c4c2d-137">Project the required fields out of essentials.</span></span>
<span data-ttu-id="c4c2d-138">A várt bemenet pontosvesszővel elválasztva.</span><span class="sxs-lookup"><span data-stu-id="c4c2d-138">Expected input is comma-separated.</span></span>

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

### <span data-ttu-id="c4c2d-139">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="c4c2d-139">-Severity</span></span>
<span data-ttu-id="c4c2d-140">Az értesítés súlyosságának szűrése</span><span class="sxs-lookup"><span data-stu-id="c4c2d-140">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="c4c2d-141">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="c4c2d-141">-SmartGroupId</span></span>
<span data-ttu-id="c4c2d-142">Az intelligens csoport azonosítóját azonosító értesítések szűrése</span><span class="sxs-lookup"><span data-stu-id="c4c2d-142">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="c4c2d-143">-SortBy</span><span class="sxs-lookup"><span data-stu-id="c4c2d-143">-SortBy</span></span>
<span data-ttu-id="c4c2d-144">A rendezés során használni kívánt riasztási tulajdonság</span><span class="sxs-lookup"><span data-stu-id="c4c2d-144">Alert property to use while sorting</span></span>

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

### <span data-ttu-id="c4c2d-145">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="c4c2d-145">-SortOrder</span></span>
<span data-ttu-id="c4c2d-146">Rendezési sorrend</span><span class="sxs-lookup"><span data-stu-id="c4c2d-146">Sort Order</span></span>

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

### <span data-ttu-id="c4c2d-147">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="c4c2d-147">-State</span></span>
<span data-ttu-id="c4c2d-148">A riasztási állapot szűrése</span><span class="sxs-lookup"><span data-stu-id="c4c2d-148">Filter on State of alert</span></span>

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

### <span data-ttu-id="c4c2d-149">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c4c2d-149">-TargetResourceGroup</span></span>
<span data-ttu-id="c4c2d-150">Szűrés a riasztás céljára szolgáló erőforrás erőforráscsoport nevében</span><span class="sxs-lookup"><span data-stu-id="c4c2d-150">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="c4c2d-151">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="c4c2d-151">-TargetResourceId</span></span>
<span data-ttu-id="c4c2d-152">Szűri az értesítés cél erőforrásának erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="c4c2d-152">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="c4c2d-153">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="c4c2d-153">-TargetResourceType</span></span>
<span data-ttu-id="c4c2d-154">Szűrés az értesítés cél erőforrásának erőforrás-típusára vonatkozóan</span><span class="sxs-lookup"><span data-stu-id="c4c2d-154">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="c4c2d-155">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="c4c2d-155">-TimeRange</span></span>
<span data-ttu-id="c4c2d-156">Támogatott időtartomány-értékek – 1h, 1d, 7D, 30d (alapérték: 1d)</span><span class="sxs-lookup"><span data-stu-id="c4c2d-156">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="c4c2d-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4c2d-157">CommonParameters</span></span>
<span data-ttu-id="c4c2d-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c4c2d-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4c2d-159">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c4c2d-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4c2d-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4c2d-160">INPUTS</span></span>

### <span data-ttu-id="c4c2d-161">Nincs</span><span class="sxs-lookup"><span data-stu-id="c4c2d-161">None</span></span>

## <span data-ttu-id="c4c2d-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4c2d-162">OUTPUTS</span></span>

### <span data-ttu-id="c4c2d-163">Microsoft. Azure. Command. AlertsManagement. OutputModels. PSAlert</span><span class="sxs-lookup"><span data-stu-id="c4c2d-163">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="c4c2d-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c4c2d-164">NOTES</span></span>

## <span data-ttu-id="c4c2d-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4c2d-165">RELATED LINKS</span></span>
