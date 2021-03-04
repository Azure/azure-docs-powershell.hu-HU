---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/measure-azalertstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
ms.openlocfilehash: 27fb22a5cded5e196a4bef0aa8b504771abef864
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942738"
---
# <span data-ttu-id="8c806-101">Measure-AzAlertStatistic</span><span class="sxs-lookup"><span data-stu-id="8c806-101">Measure-AzAlertStatistic</span></span>

## <span data-ttu-id="8c806-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c806-102">SYNOPSIS</span></span>
<span data-ttu-id="8c806-103">Értesítés összegző információit kapja</span><span class="sxs-lookup"><span data-stu-id="8c806-103">Gets Alert Summary Information</span></span>

## <span data-ttu-id="8c806-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8c806-104">SYNTAX</span></span>

### <span data-ttu-id="8c806-105">SummaryTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="8c806-105">SummaryTargetResourceIdFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceId <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c806-106">SummaryFilter</span><span class="sxs-lookup"><span data-stu-id="8c806-106">SummaryFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceType <String>] [-TargetResourceGroup <String>]
 [-MonitorService <String>] [-MonitorCondition <String>] [-Severity <String>] [-State <String>]
 [-AlertRuleId <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c806-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8c806-107">DESCRIPTION</span></span>
<span data-ttu-id="8c806-108">**A Measure-AzAlertStatistic** parancsmag a riasztások összegző adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8c806-108">**Measure-AzAlertStatistic** cmdlet gets alert summary details.</span></span>

## <span data-ttu-id="8c806-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8c806-109">EXAMPLES</span></span>

### <span data-ttu-id="8c806-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="8c806-110">Example 1</span></span>
```powershell
PS C:\> Measure-AzAlertStatistic -GroupBy "severity,alertstate" -State "Active"
```

<span data-ttu-id="8c806-111">A riasztások számát az aktív állapot szerint szűrt súlyosság és állapot szerint csoportosítva összegzi.</span><span class="sxs-lookup"><span data-stu-id="8c806-111">Summarize alerts count grouped by severity and state filtered by Active state.</span></span>

## <span data-ttu-id="8c806-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c806-112">PARAMETERS</span></span>

### <span data-ttu-id="8c806-113">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="8c806-113">-AlertRuleId</span></span>
<span data-ttu-id="8c806-114">Szűrés riasztási szabályazonosító alapján</span><span class="sxs-lookup"><span data-stu-id="8c806-114">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="8c806-115">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="8c806-115">-CustomTimeRange</span></span>
<span data-ttu-id="8c806-116">Támogatott formátum \<start-time\> / \<end-time\> – az idő ISO-8601 formátumban</span><span class="sxs-lookup"><span data-stu-id="8c806-116">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="8c806-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c806-117">-DefaultProfile</span></span>
<span data-ttu-id="8c806-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8c806-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c806-119">-GroupBy</span><span class="sxs-lookup"><span data-stu-id="8c806-119">-GroupBy</span></span>
<span data-ttu-id="8c806-120">Summarize by tulajdonság</span><span class="sxs-lookup"><span data-stu-id="8c806-120">Summarize by property</span></span>

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

### <span data-ttu-id="8c806-121">-IncludeSmartGroupsCount</span><span class="sxs-lookup"><span data-stu-id="8c806-121">-IncludeSmartGroupsCount</span></span>
<span data-ttu-id="8c806-122">SmartGroups-csoportok száma</span><span class="sxs-lookup"><span data-stu-id="8c806-122">Include SmartGroups Count</span></span>

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

### <span data-ttu-id="8c806-123">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="8c806-123">-MonitorCondition</span></span>
<span data-ttu-id="8c806-124">Szűrés figyelő feltétel alapján</span><span class="sxs-lookup"><span data-stu-id="8c806-124">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="8c806-125">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="8c806-125">-MonitorService</span></span>
<span data-ttu-id="8c806-126">Szűrés a Moniter szolgáltatáson</span><span class="sxs-lookup"><span data-stu-id="8c806-126">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="8c806-127">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="8c806-127">-Severity</span></span>
<span data-ttu-id="8c806-128">Szűrő a riasztás súlyossága alapján</span><span class="sxs-lookup"><span data-stu-id="8c806-128">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="8c806-129">-State</span><span class="sxs-lookup"><span data-stu-id="8c806-129">-State</span></span>
<span data-ttu-id="8c806-130">Szűrés a riasztás állapota alapján</span><span class="sxs-lookup"><span data-stu-id="8c806-130">Filter on State of alert</span></span>

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

### <span data-ttu-id="8c806-131">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8c806-131">-TargetResourceGroup</span></span>
<span data-ttu-id="8c806-132">Szűrő a riasztás célforrásának Erőforráscsoport neve alapján</span><span class="sxs-lookup"><span data-stu-id="8c806-132">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="8c806-133">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="8c806-133">-TargetResourceId</span></span>
<span data-ttu-id="8c806-134">Szűrő a riasztás célforrásának erőforrás-azonosítója alapján</span><span class="sxs-lookup"><span data-stu-id="8c806-134">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="8c806-135">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="8c806-135">-TargetResourceType</span></span>
<span data-ttu-id="8c806-136">Szűrés a riasztás célforrásának erőforrástípusa alapján</span><span class="sxs-lookup"><span data-stu-id="8c806-136">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="8c806-137">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="8c806-137">-TimeRange</span></span>
<span data-ttu-id="8c806-138">Támogatott időtartomány-értékek – 1h, 1d, 7d, 30d (Az alapértelmezett érték 1d)</span><span class="sxs-lookup"><span data-stu-id="8c806-138">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="8c806-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c806-139">CommonParameters</span></span>
<span data-ttu-id="8c806-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c806-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c806-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c806-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c806-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c806-142">INPUTS</span></span>

### <span data-ttu-id="8c806-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="8c806-143">None</span></span>

## <span data-ttu-id="8c806-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c806-144">OUTPUTS</span></span>

### <span data-ttu-id="8c806-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span><span class="sxs-lookup"><span data-stu-id="8c806-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span></span>

## <span data-ttu-id="8c806-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8c806-146">NOTES</span></span>

## <span data-ttu-id="8c806-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c806-147">RELATED LINKS</span></span>
