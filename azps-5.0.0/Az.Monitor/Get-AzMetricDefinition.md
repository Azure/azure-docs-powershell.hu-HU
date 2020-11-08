---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7915A7AC-5A47-4868-B846-2896BCEBFAB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetricdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
ms.openlocfilehash: 9ca873736ad86eaac17dd2795ad61716197ceaba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195749"
---
# <span data-ttu-id="72ea2-101">Get-AzMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="72ea2-101">Get-AzMetricDefinition</span></span>

## <span data-ttu-id="72ea2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="72ea2-102">SYNOPSIS</span></span>
<span data-ttu-id="72ea2-103">Metrikus definíciókat kap.</span><span class="sxs-lookup"><span data-stu-id="72ea2-103">Gets metric definitions.</span></span>

## <span data-ttu-id="72ea2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="72ea2-104">SYNTAX</span></span>

```
Get-AzMetricDefinition [-ResourceId] <String> [-MetricName <String[]>] [-MetricNamespace <String>]
 [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72ea2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="72ea2-105">DESCRIPTION</span></span>
<span data-ttu-id="72ea2-106">A **Get-AzMetricDefinition** parancsmag metrikus definíciókat kap.</span><span class="sxs-lookup"><span data-stu-id="72ea2-106">The **Get-AzMetricDefinition** cmdlet gets metric definitions.</span></span>

## <span data-ttu-id="72ea2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="72ea2-107">EXAMPLES</span></span>

### <span data-ttu-id="72ea2-108">Példa 1: egy erőforrás metrikus definícióinak beolvasása</span><span class="sxs-lookup"><span data-stu-id="72ea2-108">Example 1: Get metric definitions for a resource</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2"
Name                   : CpuTime
Dimensions             : {}
MetricAvailabilities   : {Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability}
PrimaryAggregationType : Total
Properties             : {}
ResourceUri            : 
Unit                   : Seconds
Name                   : Requests
Dimensions             : {}
MetricAvailabilities   : {Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability}
PrimaryAggregationType : Total
Properties             : {}
ResourceUri            : 
Unit                   : Count
```

<span data-ttu-id="72ea2-109">Ez a parancs a megadott erőforrás metrikájának definícióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="72ea2-109">This command gets the metrics definitions for the specified resource.</span></span>

### <span data-ttu-id="72ea2-110">2. példa: metrikus definíciók beszerzése részletes kimenettel</span><span class="sxs-lookup"><span data-stu-id="72ea2-110">Example 2: Get metric definitions with detailed output</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : CpuTime
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Seconds
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : Requests
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Count
```

<span data-ttu-id="72ea2-111">Ez a parancs a website2 metrikájának definícióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="72ea2-111">This command gets the metric definitions for website2.</span></span>
<span data-ttu-id="72ea2-112">A kimenet részletezve van.</span><span class="sxs-lookup"><span data-stu-id="72ea2-112">The output is detailed.</span></span>

### <span data-ttu-id="72ea2-113">3. példa: metrikus definíciók beolvasása név szerint</span><span class="sxs-lookup"><span data-stu-id="72ea2-113">Example 3: Get metric definitions by name</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput -MetricName "BytesSent,CpuTime"
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : CpuTime
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Seconds
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : BytesSent
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Bytes
```

<span data-ttu-id="72ea2-114">Ez a parancs a BytesSent és a CpuTime metrikájának definícióit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="72ea2-114">This command gets definitions for the BytesSent and CpuTime metrics.</span></span>
<span data-ttu-id="72ea2-115">A kimenet részletezve van.</span><span class="sxs-lookup"><span data-stu-id="72ea2-115">The output is detailed.</span></span>

## <span data-ttu-id="72ea2-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="72ea2-116">PARAMETERS</span></span>

### <span data-ttu-id="72ea2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72ea2-117">-DefaultProfile</span></span>
<span data-ttu-id="72ea2-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="72ea2-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72ea2-119">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="72ea2-119">-DetailedOutput</span></span>
<span data-ttu-id="72ea2-120">Jelzi, hogy ez a művelet a részletes kimenetet is tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="72ea2-120">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="72ea2-121">Ha nem adja meg ezt a paramétert, a program összesíti a kimenetet.</span><span class="sxs-lookup"><span data-stu-id="72ea2-121">If you do not specify this parameter, the output is summarized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72ea2-122">-MetricName</span><span class="sxs-lookup"><span data-stu-id="72ea2-122">-MetricName</span></span>
<span data-ttu-id="72ea2-123">A metrikák neveinek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72ea2-123">Specifies an array of names of metrics.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72ea2-124">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="72ea2-124">-MetricNamespace</span></span>
<span data-ttu-id="72ea2-125">A metrikus névteret adja meg a mérőszámok definícióinak lekérdezéséhez.</span><span class="sxs-lookup"><span data-stu-id="72ea2-125">Specifies the metric namespace to query metric definitions for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72ea2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72ea2-126">-ResourceId</span></span>
<span data-ttu-id="72ea2-127">Az erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="72ea2-127">Specifies the resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72ea2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72ea2-128">CommonParameters</span></span>
<span data-ttu-id="72ea2-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="72ea2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72ea2-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="72ea2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72ea2-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="72ea2-131">INPUTS</span></span>

### <span data-ttu-id="72ea2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="72ea2-132">System.String</span></span>

### <span data-ttu-id="72ea2-133">System. string []</span><span class="sxs-lookup"><span data-stu-id="72ea2-133">System.String[]</span></span>

## <span data-ttu-id="72ea2-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72ea2-134">OUTPUTS</span></span>

### <span data-ttu-id="72ea2-135">Microsoft. Azure. commands. OutputClasses. PSMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="72ea2-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition</span></span>

## <span data-ttu-id="72ea2-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="72ea2-136">NOTES</span></span>

<span data-ttu-id="72ea2-137">A támogatott metrikákkal kapcsolatos további tudnivalók a következő webhelyről érhetők el: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span><span class="sxs-lookup"><span data-stu-id="72ea2-137">More information about the supported metrics may be found at: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span></span>

## <span data-ttu-id="72ea2-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72ea2-138">RELATED LINKS</span></span>

<span data-ttu-id="72ea2-139">[Get-AzMetric](./Get-AzMetric.md) 
 [Új – AzMetricFilter](./New-AzMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="72ea2-139">[Get-AzMetric](./Get-AzMetric.md)
[New-AzMetricFilter](./New-AzMetricFilter.md)</span></span>


