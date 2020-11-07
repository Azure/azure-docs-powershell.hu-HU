---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azappserviceplanmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlanMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlanMetric.md
ms.openlocfilehash: a090498a4ddb829fb8ca8a1faf2d3e80c839a19c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668369"
---
# <span data-ttu-id="a9849-101">Get-AzAppServicePlanMetric</span><span class="sxs-lookup"><span data-stu-id="a9849-101">Get-AzAppServicePlanMetric</span></span>

## <span data-ttu-id="a9849-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a9849-102">SYNOPSIS</span></span>

## <span data-ttu-id="a9849-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a9849-103">SYNTAX</span></span>

### <span data-ttu-id="a9849-104">S1</span><span class="sxs-lookup"><span data-stu-id="a9849-104">S1</span></span>
```
Get-AzAppServicePlanMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9849-105">S2</span><span class="sxs-lookup"><span data-stu-id="a9849-105">S2</span></span>
```
Get-AzAppServicePlanMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9849-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="a9849-106">DESCRIPTION</span></span>
<span data-ttu-id="a9849-107">A **Get-AzAppServicePlanMetric** elérhetővé válik az App Service Plan mérőszámai.</span><span class="sxs-lookup"><span data-stu-id="a9849-107">The **Get-AzAppServicePlanMetric** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="a9849-108">Példák</span><span class="sxs-lookup"><span data-stu-id="a9849-108">EXAMPLES</span></span>

### <span data-ttu-id="a9849-109">1:</span><span class="sxs-lookup"><span data-stu-id="a9849-109">1:</span></span>
```
PS C:\>Get-AzAppServicePlanMetric -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics "CPU Percentage"
```

<span data-ttu-id="a9849-110">Ez a parancs az App-csomag (PT1M-szavazási idő 1 perc) CPU-százalékát kapja meg a kezdő időpont és a Befejezés között</span><span class="sxs-lookup"><span data-stu-id="a9849-110">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="a9849-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a9849-111">PARAMETERS</span></span>

### <span data-ttu-id="a9849-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a9849-112">-AppServicePlan</span></span>
<span data-ttu-id="a9849-113">Alkalmazás-szolgáltatási terv objektum</span><span class="sxs-lookup"><span data-stu-id="a9849-113">App Service Plan Object</span></span>

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

### <span data-ttu-id="a9849-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9849-114">-DefaultProfile</span></span>
<span data-ttu-id="a9849-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a9849-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9849-116">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="a9849-116">-EndTime</span></span>
<span data-ttu-id="a9849-117">Befejezési időpont az UTC-ban</span><span class="sxs-lookup"><span data-stu-id="a9849-117">End Time in UTC</span></span>

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

### <span data-ttu-id="a9849-118">-Részletesség</span><span class="sxs-lookup"><span data-stu-id="a9849-118">-Granularity</span></span>
<span data-ttu-id="a9849-119">Granularitása</span><span class="sxs-lookup"><span data-stu-id="a9849-119">Granularity</span></span>

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

### <span data-ttu-id="a9849-120">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="a9849-120">-InstanceDetails</span></span>
<span data-ttu-id="a9849-121">Példány részletei</span><span class="sxs-lookup"><span data-stu-id="a9849-121">Instance Details</span></span>

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

### <span data-ttu-id="a9849-122">-Metrikák</span><span class="sxs-lookup"><span data-stu-id="a9849-122">-Metrics</span></span>
<span data-ttu-id="a9849-123">Metrikák</span><span class="sxs-lookup"><span data-stu-id="a9849-123">Metrics</span></span>

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

### <span data-ttu-id="a9849-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a9849-124">-Name</span></span>
<span data-ttu-id="a9849-125">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="a9849-125">App Service Plan Name</span></span>

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

### <span data-ttu-id="a9849-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9849-126">-ResourceGroupName</span></span>
<span data-ttu-id="a9849-127">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="a9849-127">Resource Group Name</span></span>

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

### <span data-ttu-id="a9849-128">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="a9849-128">-StartTime</span></span>
<span data-ttu-id="a9849-129">Kezdési időpont az UTC-ban</span><span class="sxs-lookup"><span data-stu-id="a9849-129">Start Time in UTC</span></span>

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

### <span data-ttu-id="a9849-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9849-130">CommonParameters</span></span>
<span data-ttu-id="a9849-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a9849-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9849-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9849-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9849-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9849-133">INPUTS</span></span>

### <span data-ttu-id="a9849-134">Microsoft. Azure. Command. WebApps. models. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a9849-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="a9849-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9849-135">OUTPUTS</span></span>

### <span data-ttu-id="a9849-136">Microsoft. Azure. Management. WebSites. models. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="a9849-136">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="a9849-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a9849-137">NOTES</span></span>

## <span data-ttu-id="a9849-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9849-138">RELATED LINKS</span></span>
