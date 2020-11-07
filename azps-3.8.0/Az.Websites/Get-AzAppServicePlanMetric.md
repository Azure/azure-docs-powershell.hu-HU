---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azappserviceplanmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlanMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlanMetric.md
ms.openlocfilehash: d3a2cd8d0907d26a137df547f1599c9ed09cb7b3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845934"
---
# <span data-ttu-id="3137f-101">Get-AzAppServicePlanMetric</span><span class="sxs-lookup"><span data-stu-id="3137f-101">Get-AzAppServicePlanMetric</span></span>

## <span data-ttu-id="3137f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3137f-102">SYNOPSIS</span></span>

## <span data-ttu-id="3137f-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3137f-103">SYNTAX</span></span>

### <span data-ttu-id="3137f-104">S1</span><span class="sxs-lookup"><span data-stu-id="3137f-104">S1</span></span>
```
Get-AzAppServicePlanMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3137f-105">S2</span><span class="sxs-lookup"><span data-stu-id="3137f-105">S2</span></span>
```
Get-AzAppServicePlanMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3137f-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="3137f-106">DESCRIPTION</span></span>
<span data-ttu-id="3137f-107">A **Get-AzAppServicePlanMetric** elérhetővé válik az App Service Plan mérőszámai.</span><span class="sxs-lookup"><span data-stu-id="3137f-107">The **Get-AzAppServicePlanMetric** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="3137f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="3137f-108">EXAMPLES</span></span>

### <span data-ttu-id="3137f-109">1:</span><span class="sxs-lookup"><span data-stu-id="3137f-109">1:</span></span>
```
PS C:\>Get-AzAppServicePlanMetric -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics "CPU Percentage"
```

<span data-ttu-id="3137f-110">Ez a parancs az App-csomag (PT1M-szavazási idő 1 perc) CPU-százalékát kapja meg a kezdő időpont és a Befejezés között</span><span class="sxs-lookup"><span data-stu-id="3137f-110">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="3137f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3137f-111">PARAMETERS</span></span>

### <span data-ttu-id="3137f-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3137f-112">-AppServicePlan</span></span>
<span data-ttu-id="3137f-113">Alkalmazás-szolgáltatási terv objektum</span><span class="sxs-lookup"><span data-stu-id="3137f-113">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3137f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3137f-114">-DefaultProfile</span></span>
<span data-ttu-id="3137f-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3137f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3137f-116">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="3137f-116">-EndTime</span></span>
<span data-ttu-id="3137f-117">Befejezési időpont az UTC-ban</span><span class="sxs-lookup"><span data-stu-id="3137f-117">End Time in UTC</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3137f-118">-Részletesség</span><span class="sxs-lookup"><span data-stu-id="3137f-118">-Granularity</span></span>
<span data-ttu-id="3137f-119">Granularitása</span><span class="sxs-lookup"><span data-stu-id="3137f-119">Granularity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PT1M, PT1H, P1D

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3137f-120">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="3137f-120">-InstanceDetails</span></span>
<span data-ttu-id="3137f-121">Példány részletei</span><span class="sxs-lookup"><span data-stu-id="3137f-121">Instance Details</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3137f-122">-Metrikák</span><span class="sxs-lookup"><span data-stu-id="3137f-122">-Metrics</span></span>
<span data-ttu-id="3137f-123">Metrikák</span><span class="sxs-lookup"><span data-stu-id="3137f-123">Metrics</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3137f-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3137f-124">-Name</span></span>
<span data-ttu-id="3137f-125">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="3137f-125">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3137f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3137f-126">-ResourceGroupName</span></span>
<span data-ttu-id="3137f-127">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="3137f-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3137f-128">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="3137f-128">-StartTime</span></span>
<span data-ttu-id="3137f-129">Kezdési időpont az UTC-ban</span><span class="sxs-lookup"><span data-stu-id="3137f-129">Start Time in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3137f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3137f-130">CommonParameters</span></span>
<span data-ttu-id="3137f-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3137f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3137f-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3137f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3137f-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3137f-133">INPUTS</span></span>

### <span data-ttu-id="3137f-134">Microsoft. Azure. Command. WebApps. models. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3137f-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="3137f-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3137f-135">OUTPUTS</span></span>

### <span data-ttu-id="3137f-136">Microsoft. Azure. Management. WebSites. models. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="3137f-136">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="3137f-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3137f-137">NOTES</span></span>

## <span data-ttu-id="3137f-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3137f-138">RELATED LINKS</span></span>
