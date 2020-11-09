---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
ms.openlocfilehash: 94cb37a6f98195534e7effcbff8c19b2613923d8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303896"
---
# <span data-ttu-id="dd2f3-101">Get-AzAlert</span><span class="sxs-lookup"><span data-stu-id="dd2f3-101">Get-AzAlert</span></span>

## <span data-ttu-id="dd2f3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dd2f3-102">SYNOPSIS</span></span>
<span data-ttu-id="dd2f3-103">Riasztási adatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="dd2f3-103">Get Alerts Information</span></span>

## <span data-ttu-id="dd2f3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dd2f3-104">SYNTAX</span></span>

### <span data-ttu-id="dd2f3-105">AlertsListByFilter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dd2f3-105">AlertsListByFilter (Default)</span></span>
```
Get-AzAlert [-TargetResourceType <String>] [-TargetResourceGroup <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-SmartGroupId <String>] [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>]
 [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd2f3-106">AlertById</span><span class="sxs-lookup"><span data-stu-id="dd2f3-106">AlertById</span></span>
```
Get-AzAlert -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd2f3-107">AlertsListByTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="dd2f3-107">AlertsListByTargetResourceIdFilter</span></span>
```
Get-AzAlert [-TargetResourceId <String>] [-MonitorService <String>] [-MonitorCondition <String>]
 [-Severity <String>] [-State <String>] [-AlertRuleId <String>] [-SmartGroupId <String>]
 [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>] [-SortBy <String>]
 [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd2f3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="dd2f3-108">DESCRIPTION</span></span>
<span data-ttu-id="dd2f3-109">A **Get-AzAlert** parancsmag riasztási példányokat kap.</span><span class="sxs-lookup"><span data-stu-id="dd2f3-109">**Get-AzAlert** cmdlet gets fired alert instances.</span></span>

## <span data-ttu-id="dd2f3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="dd2f3-110">EXAMPLES</span></span>

### <span data-ttu-id="dd2f3-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="dd2f3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAlert -Severity "Sev2" -MonitorCondition "Fired" -IncludeContext true
```

<span data-ttu-id="dd2f3-112">A Sev2 súlyosságát és a kilőtt figyelési feltételt tartalmazó összes riasztás felsorolása.</span><span class="sxs-lookup"><span data-stu-id="dd2f3-112">List all alerts with Sev2 severity and Fired monitor condition.</span></span> <span data-ttu-id="dd2f3-113">Ha a IncludeContext igaz értékre állítja, a riasztás egyéni adattartalmát is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="dd2f3-113">Setting IncludeContext to true, include custom payload of alert.</span></span>
<span data-ttu-id="dd2f3-114">A Format-List használatával megtudhatja, hogy miként jelenítheti meg az egyes értesítések teljes tartalmát a listáról.</span><span class="sxs-lookup"><span data-stu-id="dd2f3-114">Use Format-List to get the complete details of each alert in list.</span></span>

### <span data-ttu-id="dd2f3-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="dd2f3-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAlert -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="dd2f3-116">Értesítési adatok beszerzése azonosítóval (GUID) vagy erőforrás-azonosítóval (teljes kar-azonosító)</span><span class="sxs-lookup"><span data-stu-id="dd2f3-116">Get Alert details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

### <span data-ttu-id="dd2f3-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="dd2f3-117">Example 3</span></span>

<span data-ttu-id="dd2f3-118">Riasztási adatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="dd2f3-118">Get Alerts Information.</span></span> <span data-ttu-id="dd2f3-119">autogenerated</span><span class="sxs-lookup"><span data-stu-id="dd2f3-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzAlert -IncludeContext $true -TimeRange '1h'
```

## <span data-ttu-id="dd2f3-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dd2f3-120">PARAMETERS</span></span>

### <span data-ttu-id="dd2f3-121">-AlertId</span><span class="sxs-lookup"><span data-stu-id="dd2f3-121">-AlertId</span></span>
<span data-ttu-id="dd2f3-122">Értesítési/ResourceId egyedi azonosítója.</span><span class="sxs-lookup"><span data-stu-id="dd2f3-122">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="dd2f3-123">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="dd2f3-123">-AlertRuleId</span></span>
<span data-ttu-id="dd2f3-124">Szűrés riasztási szabály azonosítójával</span><span class="sxs-lookup"><span data-stu-id="dd2f3-124">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="dd2f3-125">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="dd2f3-125">-CustomTimeRange</span></span>
<span data-ttu-id="dd2f3-126">Támogatott formátum – az \<start-time\> / \<end-time\> idő ISO-8601 formátumú</span><span class="sxs-lookup"><span data-stu-id="dd2f3-126">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="dd2f3-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd2f3-127">-DefaultProfile</span></span>
<span data-ttu-id="dd2f3-128">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dd2f3-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd2f3-129">-IncludeContext</span><span class="sxs-lookup"><span data-stu-id="dd2f3-129">-IncludeContext</span></span>
<span data-ttu-id="dd2f3-130">A riasztás környezete (egyéni adattartalom) befoglalása</span><span class="sxs-lookup"><span data-stu-id="dd2f3-130">Include context (custom payload) of alert</span></span>

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

### <span data-ttu-id="dd2f3-131">-IncludeEgressConfig</span><span class="sxs-lookup"><span data-stu-id="dd2f3-131">-IncludeEgressConfig</span></span>
<span data-ttu-id="dd2f3-132">EgressConfig belefoglalása</span><span class="sxs-lookup"><span data-stu-id="dd2f3-132">Include EgressConfig</span></span>

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

### <span data-ttu-id="dd2f3-133">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="dd2f3-133">-MonitorCondition</span></span>
<span data-ttu-id="dd2f3-134">Szűrés a monitor feltételén</span><span class="sxs-lookup"><span data-stu-id="dd2f3-134">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="dd2f3-135">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="dd2f3-135">-MonitorService</span></span>
<span data-ttu-id="dd2f3-136">Szűrés a moniter szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="dd2f3-136">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="dd2f3-137">-PageCount</span><span class="sxs-lookup"><span data-stu-id="dd2f3-137">-PageCount</span></span>
<span data-ttu-id="dd2f3-138">A lapon beolvasott értesítések száma.</span><span class="sxs-lookup"><span data-stu-id="dd2f3-138">Number of alerts to be fetched in a page.</span></span>

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

### <span data-ttu-id="dd2f3-139">-Válassza a</span><span class="sxs-lookup"><span data-stu-id="dd2f3-139">-Select</span></span>
<span data-ttu-id="dd2f3-140">Végezze el a szükséges mezőket a Essentials csomagból.</span><span class="sxs-lookup"><span data-stu-id="dd2f3-140">Project the required fields out of essentials.</span></span>
<span data-ttu-id="dd2f3-141">A várt bemenet pontosvesszővel elválasztva.</span><span class="sxs-lookup"><span data-stu-id="dd2f3-141">Expected input is comma-separated.</span></span>

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

### <span data-ttu-id="dd2f3-142">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="dd2f3-142">-Severity</span></span>
<span data-ttu-id="dd2f3-143">Az értesítés súlyosságának szűrése</span><span class="sxs-lookup"><span data-stu-id="dd2f3-143">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="dd2f3-144">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="dd2f3-144">-SmartGroupId</span></span>
<span data-ttu-id="dd2f3-145">Az intelligens csoport azonosítóját azonosító értesítések szűrése</span><span class="sxs-lookup"><span data-stu-id="dd2f3-145">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="dd2f3-146">-SortBy</span><span class="sxs-lookup"><span data-stu-id="dd2f3-146">-SortBy</span></span>
<span data-ttu-id="dd2f3-147">A rendezés során használni kívánt riasztási tulajdonság</span><span class="sxs-lookup"><span data-stu-id="dd2f3-147">Alert property to use while sorting</span></span>

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

### <span data-ttu-id="dd2f3-148">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="dd2f3-148">-SortOrder</span></span>
<span data-ttu-id="dd2f3-149">Rendezési sorrend</span><span class="sxs-lookup"><span data-stu-id="dd2f3-149">Sort Order</span></span>

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

### <span data-ttu-id="dd2f3-150">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="dd2f3-150">-State</span></span>
<span data-ttu-id="dd2f3-151">A riasztási állapot szűrése</span><span class="sxs-lookup"><span data-stu-id="dd2f3-151">Filter on State of alert</span></span>

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

### <span data-ttu-id="dd2f3-152">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="dd2f3-152">-TargetResourceGroup</span></span>
<span data-ttu-id="dd2f3-153">Szűrés a riasztás céljára szolgáló erőforrás erőforráscsoport nevében</span><span class="sxs-lookup"><span data-stu-id="dd2f3-153">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="dd2f3-154">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="dd2f3-154">-TargetResourceId</span></span>
<span data-ttu-id="dd2f3-155">Szűri az értesítés cél erőforrásának erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="dd2f3-155">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="dd2f3-156">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="dd2f3-156">-TargetResourceType</span></span>
<span data-ttu-id="dd2f3-157">Szűrés az értesítés cél erőforrásának erőforrás-típusára vonatkozóan</span><span class="sxs-lookup"><span data-stu-id="dd2f3-157">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="dd2f3-158">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="dd2f3-158">-TimeRange</span></span>
<span data-ttu-id="dd2f3-159">Támogatott időtartomány-értékek – 1h, 1d, 7D, 30d (alapérték: 1d)</span><span class="sxs-lookup"><span data-stu-id="dd2f3-159">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="dd2f3-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd2f3-160">CommonParameters</span></span>
<span data-ttu-id="dd2f3-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dd2f3-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd2f3-162">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="dd2f3-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd2f3-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd2f3-163">INPUTS</span></span>

### <span data-ttu-id="dd2f3-164">Nincs</span><span class="sxs-lookup"><span data-stu-id="dd2f3-164">None</span></span>

## <span data-ttu-id="dd2f3-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd2f3-165">OUTPUTS</span></span>

### <span data-ttu-id="dd2f3-166">Microsoft. Azure. Command. AlertsManagement. OutputModels. PSAlert</span><span class="sxs-lookup"><span data-stu-id="dd2f3-166">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="dd2f3-167">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dd2f3-167">NOTES</span></span>

## <span data-ttu-id="dd2f3-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd2f3-168">RELATED LINKS</span></span>
