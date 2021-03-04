---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/get-azalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
ms.openlocfilehash: dc2fd6492e611e84ef3db5aba57bec204985c203
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923130"
---
# <span data-ttu-id="dcf04-101">Get-AzAlert</span><span class="sxs-lookup"><span data-stu-id="dcf04-101">Get-AzAlert</span></span>

## <span data-ttu-id="dcf04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcf04-102">SYNOPSIS</span></span>
<span data-ttu-id="dcf04-103">Értesítési információk lekérte</span><span class="sxs-lookup"><span data-stu-id="dcf04-103">Get Alerts Information</span></span>

## <span data-ttu-id="dcf04-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dcf04-104">SYNTAX</span></span>

### <span data-ttu-id="dcf04-105">AlertsListByFilter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dcf04-105">AlertsListByFilter (Default)</span></span>
```
Get-AzAlert [-TargetResourceType <String>] [-TargetResourceGroup <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-SmartGroupId <String>] [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>]
 [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcf04-106">AlertById</span><span class="sxs-lookup"><span data-stu-id="dcf04-106">AlertById</span></span>
```
Get-AzAlert -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcf04-107">AlertsListByTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="dcf04-107">AlertsListByTargetResourceIdFilter</span></span>
```
Get-AzAlert [-TargetResourceId <String>] [-MonitorService <String>] [-MonitorCondition <String>]
 [-Severity <String>] [-State <String>] [-AlertRuleId <String>] [-SmartGroupId <String>]
 [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>] [-SortBy <String>]
 [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcf04-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dcf04-108">DESCRIPTION</span></span>
<span data-ttu-id="dcf04-109">**A Get-AzAlert parancsmag** riasztási példányokat kap.</span><span class="sxs-lookup"><span data-stu-id="dcf04-109">**Get-AzAlert** cmdlet gets fired alert instances.</span></span>

## <span data-ttu-id="dcf04-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dcf04-110">EXAMPLES</span></span>

### <span data-ttu-id="dcf04-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="dcf04-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAlert -Severity "Sev2" -MonitorCondition "Fired" -IncludeContext true
```

<span data-ttu-id="dcf04-112">List all alerts with Sev2 severity and Abes monitor condition.</span><span class="sxs-lookup"><span data-stu-id="dcf04-112">List all alerts with Sev2 severity and Fired monitor condition.</span></span> <span data-ttu-id="dcf04-113">Az IncludeContext igaz érték beállítása egyéni hasznos értesítésekkel.</span><span class="sxs-lookup"><span data-stu-id="dcf04-113">Setting IncludeContext to true, include custom payload of alert.</span></span>
<span data-ttu-id="dcf04-114">A Format-List a lista összes riasztásának részletes adatait.</span><span class="sxs-lookup"><span data-stu-id="dcf04-114">Use Format-List to get the complete details of each alert in list.</span></span>

### <span data-ttu-id="dcf04-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="dcf04-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAlert -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="dcf04-116">Értesítés részleteinek lekérte azonosító (GUID) vagy erőforrás-azonosító (Complete ARM Id) szerint</span><span class="sxs-lookup"><span data-stu-id="dcf04-116">Get Alert details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

### <span data-ttu-id="dcf04-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="dcf04-117">Example 3</span></span>

<span data-ttu-id="dcf04-118">Értesítési információk lekérte.</span><span class="sxs-lookup"><span data-stu-id="dcf04-118">Get Alerts Information.</span></span> <span data-ttu-id="dcf04-119">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="dcf04-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzAlert -IncludeContext $true -TimeRange '1h'
```

## <span data-ttu-id="dcf04-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dcf04-120">PARAMETERS</span></span>

### <span data-ttu-id="dcf04-121">-AlertId</span><span class="sxs-lookup"><span data-stu-id="dcf04-121">-AlertId</span></span>
<span data-ttu-id="dcf04-122">Riasztás/Erőforrásazonosító egyedi azonosítója.</span><span class="sxs-lookup"><span data-stu-id="dcf04-122">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="dcf04-123">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="dcf04-123">-AlertRuleId</span></span>
<span data-ttu-id="dcf04-124">Szűrés riasztási szabályazonosító alapján</span><span class="sxs-lookup"><span data-stu-id="dcf04-124">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="dcf04-125">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="dcf04-125">-CustomTimeRange</span></span>
<span data-ttu-id="dcf04-126">Támogatott formátum \<start-time\> / \<end-time\> – az idő ISO-8601 formátumban</span><span class="sxs-lookup"><span data-stu-id="dcf04-126">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="dcf04-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcf04-127">-DefaultProfile</span></span>
<span data-ttu-id="dcf04-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dcf04-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcf04-129">-IncludeContext</span><span class="sxs-lookup"><span data-stu-id="dcf04-129">-IncludeContext</span></span>
<span data-ttu-id="dcf04-130">Riasztás környezetének (egyéni hasznos terhelésének) beírása</span><span class="sxs-lookup"><span data-stu-id="dcf04-130">Include context (custom payload) of alert</span></span>

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

### <span data-ttu-id="dcf04-131">-IncludeEgressConfig</span><span class="sxs-lookup"><span data-stu-id="dcf04-131">-IncludeEgressConfig</span></span>
<span data-ttu-id="dcf04-132">EgressConfig is</span><span class="sxs-lookup"><span data-stu-id="dcf04-132">Include EgressConfig</span></span>

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

### <span data-ttu-id="dcf04-133">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="dcf04-133">-MonitorCondition</span></span>
<span data-ttu-id="dcf04-134">Szűrés figyelő feltétel alapján</span><span class="sxs-lookup"><span data-stu-id="dcf04-134">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="dcf04-135">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="dcf04-135">-MonitorService</span></span>
<span data-ttu-id="dcf04-136">Szűrés a Moniter szolgáltatáson</span><span class="sxs-lookup"><span data-stu-id="dcf04-136">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="dcf04-137">-PageCount</span><span class="sxs-lookup"><span data-stu-id="dcf04-137">-PageCount</span></span>
<span data-ttu-id="dcf04-138">A lapon lehívható értesítések száma.</span><span class="sxs-lookup"><span data-stu-id="dcf04-138">Number of alerts to be fetched in a page.</span></span>

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

### <span data-ttu-id="dcf04-139">-Válassza a</span><span class="sxs-lookup"><span data-stu-id="dcf04-139">-Select</span></span>
<span data-ttu-id="dcf04-140">Kivetíti a szükséges mezőket a lényegből.</span><span class="sxs-lookup"><span data-stu-id="dcf04-140">Project the required fields out of essentials.</span></span>
<span data-ttu-id="dcf04-141">A várt bemenet vesszővel van elválasztva.</span><span class="sxs-lookup"><span data-stu-id="dcf04-141">Expected input is comma-separated.</span></span>

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

### <span data-ttu-id="dcf04-142">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="dcf04-142">-Severity</span></span>
<span data-ttu-id="dcf04-143">Szűrő a riasztás súlyossága alapján</span><span class="sxs-lookup"><span data-stu-id="dcf04-143">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="dcf04-144">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="dcf04-144">-SmartGroupId</span></span>
<span data-ttu-id="dcf04-145">Az intelligens csoportazonosítóval rendelkező összes riasztás szűrése</span><span class="sxs-lookup"><span data-stu-id="dcf04-145">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="dcf04-146">-SortBy</span><span class="sxs-lookup"><span data-stu-id="dcf04-146">-SortBy</span></span>
<span data-ttu-id="dcf04-147">A rendezéshez használható Riasztás tulajdonság</span><span class="sxs-lookup"><span data-stu-id="dcf04-147">Alert property to use while sorting</span></span>

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

### <span data-ttu-id="dcf04-148">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="dcf04-148">-SortOrder</span></span>
<span data-ttu-id="dcf04-149">Rendezési sorrend</span><span class="sxs-lookup"><span data-stu-id="dcf04-149">Sort Order</span></span>

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

### <span data-ttu-id="dcf04-150">-State</span><span class="sxs-lookup"><span data-stu-id="dcf04-150">-State</span></span>
<span data-ttu-id="dcf04-151">Szűrés a riasztás állapota alapján</span><span class="sxs-lookup"><span data-stu-id="dcf04-151">Filter on State of alert</span></span>

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

### <span data-ttu-id="dcf04-152">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="dcf04-152">-TargetResourceGroup</span></span>
<span data-ttu-id="dcf04-153">Szűrő a riasztás célforrásának Erőforráscsoport neve alapján</span><span class="sxs-lookup"><span data-stu-id="dcf04-153">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="dcf04-154">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="dcf04-154">-TargetResourceId</span></span>
<span data-ttu-id="dcf04-155">Szűrő a riasztás célforrásának erőforrás-azonosítója alapján</span><span class="sxs-lookup"><span data-stu-id="dcf04-155">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="dcf04-156">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="dcf04-156">-TargetResourceType</span></span>
<span data-ttu-id="dcf04-157">Szűrés a riasztás célforrásának erőforrástípusa alapján</span><span class="sxs-lookup"><span data-stu-id="dcf04-157">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="dcf04-158">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="dcf04-158">-TimeRange</span></span>
<span data-ttu-id="dcf04-159">Támogatott időtartomány-értékek – 1h, 1d, 7d, 30d (Az alapértelmezett érték 1d)</span><span class="sxs-lookup"><span data-stu-id="dcf04-159">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="dcf04-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcf04-160">CommonParameters</span></span>
<span data-ttu-id="dcf04-161">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcf04-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcf04-162">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dcf04-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcf04-163">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dcf04-163">INPUTS</span></span>

### <span data-ttu-id="dcf04-164">Nincs</span><span class="sxs-lookup"><span data-stu-id="dcf04-164">None</span></span>

## <span data-ttu-id="dcf04-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dcf04-165">OUTPUTS</span></span>

### <span data-ttu-id="dcf04-166">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span><span class="sxs-lookup"><span data-stu-id="dcf04-166">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="dcf04-167">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dcf04-167">NOTES</span></span>

## <span data-ttu-id="dcf04-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dcf04-168">RELATED LINKS</span></span>
