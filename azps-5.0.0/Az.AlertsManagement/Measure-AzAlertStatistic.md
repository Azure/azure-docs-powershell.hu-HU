---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/measure-azalertstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
ms.openlocfilehash: 96b83f6792babed9fed7c39cad44aec0ea0f26ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185635"
---
# <span data-ttu-id="35608-101">Measure-AzAlertStatistic</span><span class="sxs-lookup"><span data-stu-id="35608-101">Measure-AzAlertStatistic</span></span>

## <span data-ttu-id="35608-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="35608-102">SYNOPSIS</span></span>
<span data-ttu-id="35608-103">Értesítési adatok összegzése</span><span class="sxs-lookup"><span data-stu-id="35608-103">Gets Alert Summary Information</span></span>

## <span data-ttu-id="35608-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="35608-104">SYNTAX</span></span>

### <span data-ttu-id="35608-105">SummaryTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="35608-105">SummaryTargetResourceIdFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceId <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35608-106">SummaryFilter</span><span class="sxs-lookup"><span data-stu-id="35608-106">SummaryFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceType <String>] [-TargetResourceGroup <String>]
 [-MonitorService <String>] [-MonitorCondition <String>] [-Severity <String>] [-State <String>]
 [-AlertRuleId <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35608-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="35608-107">DESCRIPTION</span></span>
<span data-ttu-id="35608-108">**Mérték – a AzAlertStatistic** parancsmag figyelmeztetés-összefoglaló adatokat kap.</span><span class="sxs-lookup"><span data-stu-id="35608-108">**Measure-AzAlertStatistic** cmdlet gets alert summary details.</span></span>

## <span data-ttu-id="35608-109">Példák</span><span class="sxs-lookup"><span data-stu-id="35608-109">EXAMPLES</span></span>

### <span data-ttu-id="35608-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="35608-110">Example 1</span></span>
```powershell
PS C:\> Measure-AzAlertStatistic -GroupBy "severity,alertstate" -State "Active"
```

<span data-ttu-id="35608-111">A riasztások számának összegzése súlyosságuk szerint és az állapot szűrése aktív állapot szerint</span><span class="sxs-lookup"><span data-stu-id="35608-111">Summarize alerts count grouped by severity and state filtered by Active state.</span></span>

## <span data-ttu-id="35608-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="35608-112">PARAMETERS</span></span>

### <span data-ttu-id="35608-113">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="35608-113">-AlertRuleId</span></span>
<span data-ttu-id="35608-114">Szűrés riasztási szabály azonosítójával</span><span class="sxs-lookup"><span data-stu-id="35608-114">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="35608-115">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="35608-115">-CustomTimeRange</span></span>
<span data-ttu-id="35608-116">Támogatott formátum – az \<start-time\> / \<end-time\> idő ISO-8601 formátumú</span><span class="sxs-lookup"><span data-stu-id="35608-116">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="35608-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35608-117">-DefaultProfile</span></span>
<span data-ttu-id="35608-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="35608-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35608-119">-GroupBy</span><span class="sxs-lookup"><span data-stu-id="35608-119">-GroupBy</span></span>
<span data-ttu-id="35608-120">Összegzés tulajdonság szerint</span><span class="sxs-lookup"><span data-stu-id="35608-120">Summarize by property</span></span>

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

### <span data-ttu-id="35608-121">-IncludeSmartGroupsCount</span><span class="sxs-lookup"><span data-stu-id="35608-121">-IncludeSmartGroupsCount</span></span>
<span data-ttu-id="35608-122">SmartGroups számának belefoglalása</span><span class="sxs-lookup"><span data-stu-id="35608-122">Include SmartGroups Count</span></span>

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

### <span data-ttu-id="35608-123">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="35608-123">-MonitorCondition</span></span>
<span data-ttu-id="35608-124">Szűrés a monitor feltételén</span><span class="sxs-lookup"><span data-stu-id="35608-124">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="35608-125">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="35608-125">-MonitorService</span></span>
<span data-ttu-id="35608-126">Szűrés a moniter szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="35608-126">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="35608-127">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="35608-127">-Severity</span></span>
<span data-ttu-id="35608-128">Az értesítés súlyosságának szűrése</span><span class="sxs-lookup"><span data-stu-id="35608-128">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="35608-129">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="35608-129">-State</span></span>
<span data-ttu-id="35608-130">A riasztási állapot szűrése</span><span class="sxs-lookup"><span data-stu-id="35608-130">Filter on State of alert</span></span>

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

### <span data-ttu-id="35608-131">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="35608-131">-TargetResourceGroup</span></span>
<span data-ttu-id="35608-132">Szűrés a riasztás céljára szolgáló erőforrás erőforráscsoport nevében</span><span class="sxs-lookup"><span data-stu-id="35608-132">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="35608-133">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="35608-133">-TargetResourceId</span></span>
<span data-ttu-id="35608-134">Szűri az értesítés cél erőforrásának erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="35608-134">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="35608-135">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="35608-135">-TargetResourceType</span></span>
<span data-ttu-id="35608-136">Szűrés az értesítés cél erőforrásának erőforrás-típusára vonatkozóan</span><span class="sxs-lookup"><span data-stu-id="35608-136">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="35608-137">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="35608-137">-TimeRange</span></span>
<span data-ttu-id="35608-138">Támogatott időtartomány-értékek – 1h, 1d, 7D, 30d (alapérték: 1d)</span><span class="sxs-lookup"><span data-stu-id="35608-138">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="35608-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35608-139">CommonParameters</span></span>
<span data-ttu-id="35608-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="35608-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35608-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="35608-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35608-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="35608-142">INPUTS</span></span>

### <span data-ttu-id="35608-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="35608-143">None</span></span>

## <span data-ttu-id="35608-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="35608-144">OUTPUTS</span></span>

### <span data-ttu-id="35608-145">Microsoft. Azure. Command. AlertsManagement. OutputModels. PSAlertsSummary</span><span class="sxs-lookup"><span data-stu-id="35608-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span></span>

## <span data-ttu-id="35608-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="35608-146">NOTES</span></span>

## <span data-ttu-id="35608-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="35608-147">RELATED LINKS</span></span>