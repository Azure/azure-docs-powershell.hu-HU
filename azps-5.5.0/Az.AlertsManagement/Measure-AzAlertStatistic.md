---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/measure-azalertstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
ms.openlocfilehash: 96b83f6792babed9fed7c39cad44aec0ea0f26ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205895"
---
# <span data-ttu-id="41500-101">Measure-AzAlertStatistic</span><span class="sxs-lookup"><span data-stu-id="41500-101">Measure-AzAlertStatistic</span></span>

## <span data-ttu-id="41500-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41500-102">SYNOPSIS</span></span>
<span data-ttu-id="41500-103">Értesítés összegző információit kapja</span><span class="sxs-lookup"><span data-stu-id="41500-103">Gets Alert Summary Information</span></span>

## <span data-ttu-id="41500-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="41500-104">SYNTAX</span></span>

### <span data-ttu-id="41500-105">SummaryTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="41500-105">SummaryTargetResourceIdFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceId <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41500-106">SummaryFilter</span><span class="sxs-lookup"><span data-stu-id="41500-106">SummaryFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceType <String>] [-TargetResourceGroup <String>]
 [-MonitorService <String>] [-MonitorCondition <String>] [-Severity <String>] [-State <String>]
 [-AlertRuleId <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41500-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="41500-107">DESCRIPTION</span></span>
<span data-ttu-id="41500-108">**A Measure-AzAlertStatistic** parancsmag a riasztások összegző adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="41500-108">**Measure-AzAlertStatistic** cmdlet gets alert summary details.</span></span>

## <span data-ttu-id="41500-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="41500-109">EXAMPLES</span></span>

### <span data-ttu-id="41500-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="41500-110">Example 1</span></span>
```powershell
PS C:\> Measure-AzAlertStatistic -GroupBy "severity,alertstate" -State "Active"
```

<span data-ttu-id="41500-111">A riasztások számát az aktív állapot szerint szűrt súlyosság és állapot szerint csoportosítva összegzi.</span><span class="sxs-lookup"><span data-stu-id="41500-111">Summarize alerts count grouped by severity and state filtered by Active state.</span></span>

## <span data-ttu-id="41500-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41500-112">PARAMETERS</span></span>

### <span data-ttu-id="41500-113">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="41500-113">-AlertRuleId</span></span>
<span data-ttu-id="41500-114">Szűrés riasztási szabályazonosító alapján</span><span class="sxs-lookup"><span data-stu-id="41500-114">Filter on Alert Rule Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41500-115">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="41500-115">-CustomTimeRange</span></span>
<span data-ttu-id="41500-116">Támogatott formátum \<start-time\> / \<end-time\> – az idő ISO-8601 formátumban</span><span class="sxs-lookup"><span data-stu-id="41500-116">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41500-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41500-117">-DefaultProfile</span></span>
<span data-ttu-id="41500-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="41500-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41500-119">-GroupBy</span><span class="sxs-lookup"><span data-stu-id="41500-119">-GroupBy</span></span>
<span data-ttu-id="41500-120">Summarize by tulajdonság</span><span class="sxs-lookup"><span data-stu-id="41500-120">Summarize by property</span></span>

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

### <span data-ttu-id="41500-121">-IncludeSmartGroupsCount</span><span class="sxs-lookup"><span data-stu-id="41500-121">-IncludeSmartGroupsCount</span></span>
<span data-ttu-id="41500-122">SmartGroups-csoportok számának beleszámol</span><span class="sxs-lookup"><span data-stu-id="41500-122">Include SmartGroups Count</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41500-123">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="41500-123">-MonitorCondition</span></span>
<span data-ttu-id="41500-124">Szűrés figyelő feltétel alapján</span><span class="sxs-lookup"><span data-stu-id="41500-124">Filter on Monitor Condition</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41500-125">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="41500-125">-MonitorService</span></span>
<span data-ttu-id="41500-126">Szűrés a Moniter szolgáltatáson</span><span class="sxs-lookup"><span data-stu-id="41500-126">Filter on Moniter Service</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41500-127">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="41500-127">-Severity</span></span>
<span data-ttu-id="41500-128">Szűrő a riasztás súlyossága alapján</span><span class="sxs-lookup"><span data-stu-id="41500-128">Filter on Severity of alert</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41500-129">-State</span><span class="sxs-lookup"><span data-stu-id="41500-129">-State</span></span>
<span data-ttu-id="41500-130">Szűrés a riasztás állapota alapján</span><span class="sxs-lookup"><span data-stu-id="41500-130">Filter on State of alert</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41500-131">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="41500-131">-TargetResourceGroup</span></span>
<span data-ttu-id="41500-132">Szűrő a riasztás célforrásának Erőforráscsoport neve alapján</span><span class="sxs-lookup"><span data-stu-id="41500-132">Filter on Resource group name of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SummaryFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41500-133">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="41500-133">-TargetResourceId</span></span>
<span data-ttu-id="41500-134">Szűrő a riasztás célforrásának erőforrás-azonosítója alapján</span><span class="sxs-lookup"><span data-stu-id="41500-134">Filter on Resource Id of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SummaryTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41500-135">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="41500-135">-TargetResourceType</span></span>
<span data-ttu-id="41500-136">Szűrés a riasztás célforrásának erőforrástípusa alapján</span><span class="sxs-lookup"><span data-stu-id="41500-136">Filter on Resource type of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SummaryFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41500-137">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="41500-137">-TimeRange</span></span>
<span data-ttu-id="41500-138">Támogatott időtartomány-értékek – 1h, 1d, 7d, 30d (Az alapértelmezett érték 1d)</span><span class="sxs-lookup"><span data-stu-id="41500-138">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41500-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41500-139">CommonParameters</span></span>
<span data-ttu-id="41500-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41500-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41500-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="41500-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41500-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="41500-142">INPUTS</span></span>

### <span data-ttu-id="41500-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="41500-143">None</span></span>

## <span data-ttu-id="41500-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41500-144">OUTPUTS</span></span>

### <span data-ttu-id="41500-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span><span class="sxs-lookup"><span data-stu-id="41500-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span></span>

## <span data-ttu-id="41500-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="41500-146">NOTES</span></span>

## <span data-ttu-id="41500-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41500-147">RELATED LINKS</span></span>
