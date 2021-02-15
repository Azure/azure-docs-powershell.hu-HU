---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7915A7AC-5A47-4868-B846-2896BCEBFAB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetricdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
ms.openlocfilehash: 9ca873736ad86eaac17dd2795ad61716197ceaba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152202"
---
# <span data-ttu-id="121da-101">Get-AzMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="121da-101">Get-AzMetricDefinition</span></span>

## <span data-ttu-id="121da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="121da-102">SYNOPSIS</span></span>
<span data-ttu-id="121da-103">Metrikus definíciókat kap.</span><span class="sxs-lookup"><span data-stu-id="121da-103">Gets metric definitions.</span></span>

## <span data-ttu-id="121da-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="121da-104">SYNTAX</span></span>

```
Get-AzMetricDefinition [-ResourceId] <String> [-MetricName <String[]>] [-MetricNamespace <String>]
 [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="121da-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="121da-105">DESCRIPTION</span></span>
<span data-ttu-id="121da-106">A **Get-AzMetricDefinition** parancsmag metrikus definíciókat kap.</span><span class="sxs-lookup"><span data-stu-id="121da-106">The **Get-AzMetricDefinition** cmdlet gets metric definitions.</span></span>

## <span data-ttu-id="121da-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="121da-107">EXAMPLES</span></span>

### <span data-ttu-id="121da-108">1. példa: Metrikus definíciók lekérte egy erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="121da-108">Example 1: Get metric definitions for a resource</span></span>
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

<span data-ttu-id="121da-109">Ez a parancs a megadott erőforrás metrikákat definiáló definícióit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="121da-109">This command gets the metrics definitions for the specified resource.</span></span>

### <span data-ttu-id="121da-110">2. példa: Metrikus definíciók lekérte részletes kimenettel</span><span class="sxs-lookup"><span data-stu-id="121da-110">Example 2: Get metric definitions with detailed output</span></span>
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

<span data-ttu-id="121da-111">Ez a parancs a webhely2 metrikus definícióit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="121da-111">This command gets the metric definitions for website2.</span></span>
<span data-ttu-id="121da-112">A kimenet részletes.</span><span class="sxs-lookup"><span data-stu-id="121da-112">The output is detailed.</span></span>

### <span data-ttu-id="121da-113">3. példa: Metrikadefiníciók lekérte név szerint</span><span class="sxs-lookup"><span data-stu-id="121da-113">Example 3: Get metric definitions by name</span></span>
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

<span data-ttu-id="121da-114">Ez a parancs a BytesSent és a CpuTime metrikák definícióit kapja.</span><span class="sxs-lookup"><span data-stu-id="121da-114">This command gets definitions for the BytesSent and CpuTime metrics.</span></span>
<span data-ttu-id="121da-115">A kimenet részletes.</span><span class="sxs-lookup"><span data-stu-id="121da-115">The output is detailed.</span></span>

## <span data-ttu-id="121da-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="121da-116">PARAMETERS</span></span>

### <span data-ttu-id="121da-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="121da-117">-DefaultProfile</span></span>
<span data-ttu-id="121da-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="121da-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="121da-119">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="121da-119">-DetailedOutput</span></span>
<span data-ttu-id="121da-120">Azt jelzi, hogy a művelet részletes kimenetet tartalmazott.</span><span class="sxs-lookup"><span data-stu-id="121da-120">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="121da-121">Ha nem adja meg ezt a paramétert, a kimenet összegzi a kimenetet.</span><span class="sxs-lookup"><span data-stu-id="121da-121">If you do not specify this parameter, the output is summarized.</span></span>

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

### <span data-ttu-id="121da-122">-MetricName</span><span class="sxs-lookup"><span data-stu-id="121da-122">-MetricName</span></span>
<span data-ttu-id="121da-123">A metrikák neveinek tömbje.</span><span class="sxs-lookup"><span data-stu-id="121da-123">Specifies an array of names of metrics.</span></span>

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

### <span data-ttu-id="121da-124">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="121da-124">-MetricNamespace</span></span>
<span data-ttu-id="121da-125">Meghatározza a metrikus névteret, amelynél lekérdezi a metrikák definícióit.</span><span class="sxs-lookup"><span data-stu-id="121da-125">Specifies the metric namespace to query metric definitions for.</span></span>

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

### <span data-ttu-id="121da-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="121da-126">-ResourceId</span></span>
<span data-ttu-id="121da-127">Az erőforrásazonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="121da-127">Specifies the resource ID.</span></span>

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

### <span data-ttu-id="121da-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="121da-128">CommonParameters</span></span>
<span data-ttu-id="121da-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="121da-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="121da-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="121da-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="121da-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="121da-131">INPUTS</span></span>

### <span data-ttu-id="121da-132">System.String</span><span class="sxs-lookup"><span data-stu-id="121da-132">System.String</span></span>

### <span data-ttu-id="121da-133">System.String[]</span><span class="sxs-lookup"><span data-stu-id="121da-133">System.String[]</span></span>

## <span data-ttu-id="121da-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="121da-134">OUTPUTS</span></span>

### <span data-ttu-id="121da-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="121da-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition</span></span>

## <span data-ttu-id="121da-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="121da-136">NOTES</span></span>

<span data-ttu-id="121da-137">A támogatott metrikákról további információt a következő oldalon talál: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span><span class="sxs-lookup"><span data-stu-id="121da-137">More information about the supported metrics may be found at: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span></span>

## <span data-ttu-id="121da-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="121da-138">RELATED LINKS</span></span>

<span data-ttu-id="121da-139">[Get-AzMetric](./Get-AzMetric.md) 
 [New-AzMetricFilter](./New-AzMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="121da-139">[Get-AzMetric](./Get-AzMetric.md)
[New-AzMetricFilter](./New-AzMetricFilter.md)</span></span>


