---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
ms.openlocfilehash: 94cb37a6f98195534e7effcbff8c19b2613923d8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469086"
---
# <span data-ttu-id="cbad6-101">Get-AzAlert</span><span class="sxs-lookup"><span data-stu-id="cbad6-101">Get-AzAlert</span></span>

## <span data-ttu-id="cbad6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbad6-102">SYNOPSIS</span></span>
<span data-ttu-id="cbad6-103">Értesítési információk lekérte</span><span class="sxs-lookup"><span data-stu-id="cbad6-103">Get Alerts Information</span></span>

## <span data-ttu-id="cbad6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cbad6-104">SYNTAX</span></span>

### <span data-ttu-id="cbad6-105">AlertsListByFilter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cbad6-105">AlertsListByFilter (Default)</span></span>
```
Get-AzAlert [-TargetResourceType <String>] [-TargetResourceGroup <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-SmartGroupId <String>] [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>]
 [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbad6-106">AlertById</span><span class="sxs-lookup"><span data-stu-id="cbad6-106">AlertById</span></span>
```
Get-AzAlert -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbad6-107">AlertsListByTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="cbad6-107">AlertsListByTargetResourceIdFilter</span></span>
```
Get-AzAlert [-TargetResourceId <String>] [-MonitorService <String>] [-MonitorCondition <String>]
 [-Severity <String>] [-State <String>] [-AlertRuleId <String>] [-SmartGroupId <String>]
 [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>] [-SortBy <String>]
 [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbad6-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cbad6-108">DESCRIPTION</span></span>
<span data-ttu-id="cbad6-109">**A Get-AzAlert parancsmag** riasztási példányokat kap.</span><span class="sxs-lookup"><span data-stu-id="cbad6-109">**Get-AzAlert** cmdlet gets fired alert instances.</span></span>

## <span data-ttu-id="cbad6-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cbad6-110">EXAMPLES</span></span>

### <span data-ttu-id="cbad6-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="cbad6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAlert -Severity "Sev2" -MonitorCondition "Fired" -IncludeContext true
```

<span data-ttu-id="cbad6-112">List all alerts with Sev2 severity and Abes monitor condition.</span><span class="sxs-lookup"><span data-stu-id="cbad6-112">List all alerts with Sev2 severity and Fired monitor condition.</span></span> <span data-ttu-id="cbad6-113">Az IncludeContext igaz érték beállítása egyéni hasznos értesítésekkel.</span><span class="sxs-lookup"><span data-stu-id="cbad6-113">Setting IncludeContext to true, include custom payload of alert.</span></span>
<span data-ttu-id="cbad6-114">A Format-List a lista összes riasztásának részletes adatait.</span><span class="sxs-lookup"><span data-stu-id="cbad6-114">Use Format-List to get the complete details of each alert in list.</span></span>

### <span data-ttu-id="cbad6-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="cbad6-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAlert -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="cbad6-116">Értesítés részleteinek lekérte azonosító (GUID) vagy erőforrás-azonosító (Complete ARM Id) szerint</span><span class="sxs-lookup"><span data-stu-id="cbad6-116">Get Alert details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

### <span data-ttu-id="cbad6-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="cbad6-117">Example 3</span></span>

<span data-ttu-id="cbad6-118">Értesítési információk lekérte.</span><span class="sxs-lookup"><span data-stu-id="cbad6-118">Get Alerts Information.</span></span> <span data-ttu-id="cbad6-119">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="cbad6-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzAlert -IncludeContext $true -TimeRange '1h'
```

## <span data-ttu-id="cbad6-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cbad6-120">PARAMETERS</span></span>

### <span data-ttu-id="cbad6-121">-AlertId</span><span class="sxs-lookup"><span data-stu-id="cbad6-121">-AlertId</span></span>
<span data-ttu-id="cbad6-122">Riasztás/Erőforrásazonosító egyedi azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cbad6-122">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="cbad6-123">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="cbad6-123">-AlertRuleId</span></span>
<span data-ttu-id="cbad6-124">Szűrés riasztási szabályazonosító alapján</span><span class="sxs-lookup"><span data-stu-id="cbad6-124">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="cbad6-125">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="cbad6-125">-CustomTimeRange</span></span>
<span data-ttu-id="cbad6-126">Támogatott formátum \<start-time\> / \<end-time\> – az idő ISO-8601 formátumban</span><span class="sxs-lookup"><span data-stu-id="cbad6-126">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="cbad6-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbad6-127">-DefaultProfile</span></span>
<span data-ttu-id="cbad6-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cbad6-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbad6-129">-IncludeContext</span><span class="sxs-lookup"><span data-stu-id="cbad6-129">-IncludeContext</span></span>
<span data-ttu-id="cbad6-130">Riasztás környezetének (egyéni hasznos terhelésének) beírása</span><span class="sxs-lookup"><span data-stu-id="cbad6-130">Include context (custom payload) of alert</span></span>

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

### <span data-ttu-id="cbad6-131">-IncludeEgressConfig</span><span class="sxs-lookup"><span data-stu-id="cbad6-131">-IncludeEgressConfig</span></span>
<span data-ttu-id="cbad6-132">EgressConfig is</span><span class="sxs-lookup"><span data-stu-id="cbad6-132">Include EgressConfig</span></span>

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

### <span data-ttu-id="cbad6-133">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="cbad6-133">-MonitorCondition</span></span>
<span data-ttu-id="cbad6-134">Szűrés figyelő feltétel alapján</span><span class="sxs-lookup"><span data-stu-id="cbad6-134">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="cbad6-135">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="cbad6-135">-MonitorService</span></span>
<span data-ttu-id="cbad6-136">Szűrés a Moniter szolgáltatáson</span><span class="sxs-lookup"><span data-stu-id="cbad6-136">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="cbad6-137">-PageCount</span><span class="sxs-lookup"><span data-stu-id="cbad6-137">-PageCount</span></span>
<span data-ttu-id="cbad6-138">A lapon lehívható értesítések száma.</span><span class="sxs-lookup"><span data-stu-id="cbad6-138">Number of alerts to be fetched in a page.</span></span>

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

### <span data-ttu-id="cbad6-139">-Válassza a</span><span class="sxs-lookup"><span data-stu-id="cbad6-139">-Select</span></span>
<span data-ttu-id="cbad6-140">Kivetíti a szükséges mezőket a lényegből.</span><span class="sxs-lookup"><span data-stu-id="cbad6-140">Project the required fields out of essentials.</span></span>
<span data-ttu-id="cbad6-141">A várt bemenet vesszővel van elválasztva.</span><span class="sxs-lookup"><span data-stu-id="cbad6-141">Expected input is comma-separated.</span></span>

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

### <span data-ttu-id="cbad6-142">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="cbad6-142">-Severity</span></span>
<span data-ttu-id="cbad6-143">Szűrő a riasztás súlyossága alapján</span><span class="sxs-lookup"><span data-stu-id="cbad6-143">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="cbad6-144">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="cbad6-144">-SmartGroupId</span></span>
<span data-ttu-id="cbad6-145">Az intelligens csoportazonosítóval rendelkező összes riasztás szűrése</span><span class="sxs-lookup"><span data-stu-id="cbad6-145">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="cbad6-146">-SortBy</span><span class="sxs-lookup"><span data-stu-id="cbad6-146">-SortBy</span></span>
<span data-ttu-id="cbad6-147">A rendezéshez használható Riasztás tulajdonság</span><span class="sxs-lookup"><span data-stu-id="cbad6-147">Alert property to use while sorting</span></span>

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

### <span data-ttu-id="cbad6-148">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="cbad6-148">-SortOrder</span></span>
<span data-ttu-id="cbad6-149">Rendezési sorrend</span><span class="sxs-lookup"><span data-stu-id="cbad6-149">Sort Order</span></span>

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

### <span data-ttu-id="cbad6-150">-State</span><span class="sxs-lookup"><span data-stu-id="cbad6-150">-State</span></span>
<span data-ttu-id="cbad6-151">Szűrés a riasztás állapota alapján</span><span class="sxs-lookup"><span data-stu-id="cbad6-151">Filter on State of alert</span></span>

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

### <span data-ttu-id="cbad6-152">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cbad6-152">-TargetResourceGroup</span></span>
<span data-ttu-id="cbad6-153">Szűrő a riasztás célforrásának Erőforráscsoport neve alapján</span><span class="sxs-lookup"><span data-stu-id="cbad6-153">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="cbad6-154">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="cbad6-154">-TargetResourceId</span></span>
<span data-ttu-id="cbad6-155">Szűrő a riasztás célforrásának erőforrás-azonosítója alapján</span><span class="sxs-lookup"><span data-stu-id="cbad6-155">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="cbad6-156">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="cbad6-156">-TargetResourceType</span></span>
<span data-ttu-id="cbad6-157">Szűrés a riasztás célforrásának erőforrástípusa alapján</span><span class="sxs-lookup"><span data-stu-id="cbad6-157">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="cbad6-158">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="cbad6-158">-TimeRange</span></span>
<span data-ttu-id="cbad6-159">Támogatott időtartomány-értékek – 1h, 1d, 7d, 30d (Az alapértelmezett érték 1d)</span><span class="sxs-lookup"><span data-stu-id="cbad6-159">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="cbad6-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbad6-160">CommonParameters</span></span>
<span data-ttu-id="cbad6-161">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbad6-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbad6-162">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cbad6-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbad6-163">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cbad6-163">INPUTS</span></span>

### <span data-ttu-id="cbad6-164">Nincs</span><span class="sxs-lookup"><span data-stu-id="cbad6-164">None</span></span>

## <span data-ttu-id="cbad6-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbad6-165">OUTPUTS</span></span>

### <span data-ttu-id="cbad6-166">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span><span class="sxs-lookup"><span data-stu-id="cbad6-166">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="cbad6-167">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cbad6-167">NOTES</span></span>

## <span data-ttu-id="cbad6-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cbad6-168">RELATED LINKS</span></span>
