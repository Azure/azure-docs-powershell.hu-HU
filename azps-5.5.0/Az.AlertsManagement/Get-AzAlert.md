---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
ms.openlocfilehash: 94cb37a6f98195534e7effcbff8c19b2613923d8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167042"
---
# <span data-ttu-id="24929-101">Get-AzAlert</span><span class="sxs-lookup"><span data-stu-id="24929-101">Get-AzAlert</span></span>

## <span data-ttu-id="24929-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24929-102">SYNOPSIS</span></span>
<span data-ttu-id="24929-103">Értesítési információk lekérte</span><span class="sxs-lookup"><span data-stu-id="24929-103">Get Alerts Information</span></span>

## <span data-ttu-id="24929-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="24929-104">SYNTAX</span></span>

### <span data-ttu-id="24929-105">AlertsListByFilter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="24929-105">AlertsListByFilter (Default)</span></span>
```
Get-AzAlert [-TargetResourceType <String>] [-TargetResourceGroup <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-SmartGroupId <String>] [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>]
 [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24929-106">AlertById</span><span class="sxs-lookup"><span data-stu-id="24929-106">AlertById</span></span>
```
Get-AzAlert -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24929-107">AlertsListByTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="24929-107">AlertsListByTargetResourceIdFilter</span></span>
```
Get-AzAlert [-TargetResourceId <String>] [-MonitorService <String>] [-MonitorCondition <String>]
 [-Severity <String>] [-State <String>] [-AlertRuleId <String>] [-SmartGroupId <String>]
 [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>] [-SortBy <String>]
 [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24929-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="24929-108">DESCRIPTION</span></span>
<span data-ttu-id="24929-109">**A Get-AzAlert parancsmag** riasztási példányokat kap.</span><span class="sxs-lookup"><span data-stu-id="24929-109">**Get-AzAlert** cmdlet gets fired alert instances.</span></span>

## <span data-ttu-id="24929-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="24929-110">EXAMPLES</span></span>

### <span data-ttu-id="24929-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="24929-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAlert -Severity "Sev2" -MonitorCondition "Fired" -IncludeContext true
```

<span data-ttu-id="24929-112">List all alerts with Sev2 severity and Abes monitor condition.</span><span class="sxs-lookup"><span data-stu-id="24929-112">List all alerts with Sev2 severity and Fired monitor condition.</span></span> <span data-ttu-id="24929-113">Az IncludeContext igaz érték beállítása egyéni hasznos értesítésekkel.</span><span class="sxs-lookup"><span data-stu-id="24929-113">Setting IncludeContext to true, include custom payload of alert.</span></span>
<span data-ttu-id="24929-114">A Format-List a lista összes riasztásának részletes adatait.</span><span class="sxs-lookup"><span data-stu-id="24929-114">Use Format-List to get the complete details of each alert in list.</span></span>

### <span data-ttu-id="24929-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="24929-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAlert -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="24929-116">Értesítés részleteinek lekérte azonosító (GUID) vagy erőforrás-azonosító (Complete ARM Id) szerint</span><span class="sxs-lookup"><span data-stu-id="24929-116">Get Alert details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

### <span data-ttu-id="24929-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="24929-117">Example 3</span></span>

<span data-ttu-id="24929-118">Értesítési információk lekérte.</span><span class="sxs-lookup"><span data-stu-id="24929-118">Get Alerts Information.</span></span> <span data-ttu-id="24929-119">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="24929-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzAlert -IncludeContext $true -TimeRange '1h'
```

## <span data-ttu-id="24929-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24929-120">PARAMETERS</span></span>

### <span data-ttu-id="24929-121">-AlertId</span><span class="sxs-lookup"><span data-stu-id="24929-121">-AlertId</span></span>
<span data-ttu-id="24929-122">Riasztás/Erőforrásazonosító egyedi azonosítója.</span><span class="sxs-lookup"><span data-stu-id="24929-122">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="24929-123">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="24929-123">-AlertRuleId</span></span>
<span data-ttu-id="24929-124">Szűrés riasztási szabályazonosító alapján</span><span class="sxs-lookup"><span data-stu-id="24929-124">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="24929-125">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="24929-125">-CustomTimeRange</span></span>
<span data-ttu-id="24929-126">Támogatott formátum \<start-time\> / \<end-time\> – az idő ISO-8601 formátumban</span><span class="sxs-lookup"><span data-stu-id="24929-126">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="24929-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24929-127">-DefaultProfile</span></span>
<span data-ttu-id="24929-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="24929-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24929-129">-IncludeContext</span><span class="sxs-lookup"><span data-stu-id="24929-129">-IncludeContext</span></span>
<span data-ttu-id="24929-130">Riasztás környezetének (egyéni hasznos terhelésének) beírása</span><span class="sxs-lookup"><span data-stu-id="24929-130">Include context (custom payload) of alert</span></span>

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

### <span data-ttu-id="24929-131">-IncludeEgressConfig</span><span class="sxs-lookup"><span data-stu-id="24929-131">-IncludeEgressConfig</span></span>
<span data-ttu-id="24929-132">EgressConfig is</span><span class="sxs-lookup"><span data-stu-id="24929-132">Include EgressConfig</span></span>

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

### <span data-ttu-id="24929-133">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="24929-133">-MonitorCondition</span></span>
<span data-ttu-id="24929-134">Szűrés figyelő feltétel alapján</span><span class="sxs-lookup"><span data-stu-id="24929-134">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="24929-135">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="24929-135">-MonitorService</span></span>
<span data-ttu-id="24929-136">Szűrés a Moniter szolgáltatáson</span><span class="sxs-lookup"><span data-stu-id="24929-136">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="24929-137">-PageCount</span><span class="sxs-lookup"><span data-stu-id="24929-137">-PageCount</span></span>
<span data-ttu-id="24929-138">A lapon lehívható értesítések száma.</span><span class="sxs-lookup"><span data-stu-id="24929-138">Number of alerts to be fetched in a page.</span></span>

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

### <span data-ttu-id="24929-139">-Válassza a</span><span class="sxs-lookup"><span data-stu-id="24929-139">-Select</span></span>
<span data-ttu-id="24929-140">Kivetíti a szükséges mezőket a lényegből.</span><span class="sxs-lookup"><span data-stu-id="24929-140">Project the required fields out of essentials.</span></span>
<span data-ttu-id="24929-141">A várt bemenet vesszővel van elválasztva.</span><span class="sxs-lookup"><span data-stu-id="24929-141">Expected input is comma-separated.</span></span>

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

### <span data-ttu-id="24929-142">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="24929-142">-Severity</span></span>
<span data-ttu-id="24929-143">Szűrő a riasztás súlyossága alapján</span><span class="sxs-lookup"><span data-stu-id="24929-143">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="24929-144">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="24929-144">-SmartGroupId</span></span>
<span data-ttu-id="24929-145">Az intelligens csoportazonosítóval rendelkező összes riasztás szűrése</span><span class="sxs-lookup"><span data-stu-id="24929-145">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="24929-146">-SortBy</span><span class="sxs-lookup"><span data-stu-id="24929-146">-SortBy</span></span>
<span data-ttu-id="24929-147">A rendezéshez használható Riasztás tulajdonság</span><span class="sxs-lookup"><span data-stu-id="24929-147">Alert property to use while sorting</span></span>

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

### <span data-ttu-id="24929-148">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="24929-148">-SortOrder</span></span>
<span data-ttu-id="24929-149">Rendezési sorrend</span><span class="sxs-lookup"><span data-stu-id="24929-149">Sort Order</span></span>

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

### <span data-ttu-id="24929-150">-State</span><span class="sxs-lookup"><span data-stu-id="24929-150">-State</span></span>
<span data-ttu-id="24929-151">Szűrés a riasztás állapota alapján</span><span class="sxs-lookup"><span data-stu-id="24929-151">Filter on State of alert</span></span>

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

### <span data-ttu-id="24929-152">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="24929-152">-TargetResourceGroup</span></span>
<span data-ttu-id="24929-153">Szűrő a riasztás célforrásának Erőforráscsoport neve alapján</span><span class="sxs-lookup"><span data-stu-id="24929-153">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="24929-154">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="24929-154">-TargetResourceId</span></span>
<span data-ttu-id="24929-155">Szűrő a riasztás célforrásának erőforrás-azonosítója alapján</span><span class="sxs-lookup"><span data-stu-id="24929-155">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="24929-156">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="24929-156">-TargetResourceType</span></span>
<span data-ttu-id="24929-157">Szűrés a riasztás célforrásának erőforrástípusa alapján</span><span class="sxs-lookup"><span data-stu-id="24929-157">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="24929-158">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="24929-158">-TimeRange</span></span>
<span data-ttu-id="24929-159">Támogatott időtartomány-értékek – 1h, 1d, 7d, 30d (Az alapértelmezett érték 1d)</span><span class="sxs-lookup"><span data-stu-id="24929-159">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="24929-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24929-160">CommonParameters</span></span>
<span data-ttu-id="24929-161">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24929-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24929-162">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24929-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24929-163">INPUTS</span><span class="sxs-lookup"><span data-stu-id="24929-163">INPUTS</span></span>

### <span data-ttu-id="24929-164">Nincs</span><span class="sxs-lookup"><span data-stu-id="24929-164">None</span></span>

## <span data-ttu-id="24929-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24929-165">OUTPUTS</span></span>

### <span data-ttu-id="24929-166">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span><span class="sxs-lookup"><span data-stu-id="24929-166">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="24929-167">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="24929-167">NOTES</span></span>

## <span data-ttu-id="24929-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24929-168">RELATED LINKS</span></span>
