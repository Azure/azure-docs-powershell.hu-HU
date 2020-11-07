---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azappserviceplanmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlanMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlanMetric.md
ms.openlocfilehash: 04f07e435f8656ef18e452538d97b3728179c969
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839954"
---
# <span data-ttu-id="17fc2-101">Get-AzAppServicePlanMetric</span><span class="sxs-lookup"><span data-stu-id="17fc2-101">Get-AzAppServicePlanMetric</span></span>

## <span data-ttu-id="17fc2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="17fc2-102">SYNOPSIS</span></span>

## <span data-ttu-id="17fc2-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="17fc2-103">SYNTAX</span></span>

### <span data-ttu-id="17fc2-104">S1</span><span class="sxs-lookup"><span data-stu-id="17fc2-104">S1</span></span>
```
Get-AzAppServicePlanMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17fc2-105">S2</span><span class="sxs-lookup"><span data-stu-id="17fc2-105">S2</span></span>
```
Get-AzAppServicePlanMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17fc2-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="17fc2-106">DESCRIPTION</span></span>
<span data-ttu-id="17fc2-107">A **Get-AzAppServicePlanMetric** elérhetővé válik az App Service Plan mérőszámai.</span><span class="sxs-lookup"><span data-stu-id="17fc2-107">The **Get-AzAppServicePlanMetric** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="17fc2-108">Példák</span><span class="sxs-lookup"><span data-stu-id="17fc2-108">EXAMPLES</span></span>

### <span data-ttu-id="17fc2-109">1:</span><span class="sxs-lookup"><span data-stu-id="17fc2-109">1:</span></span>
```
PS C:\>Get-AzAppServicePlanMetric -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics "CPU Percentage"
```

<span data-ttu-id="17fc2-110">Ez a parancs az App-csomag (PT1M-szavazási idő 1 perc) CPU-százalékát kapja meg a kezdő időpont és a Befejezés között</span><span class="sxs-lookup"><span data-stu-id="17fc2-110">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="17fc2-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="17fc2-111">PARAMETERS</span></span>

### <span data-ttu-id="17fc2-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="17fc2-112">-AppServicePlan</span></span>
<span data-ttu-id="17fc2-113">Alkalmazás-szolgáltatási terv objektum</span><span class="sxs-lookup"><span data-stu-id="17fc2-113">App Service Plan Object</span></span>

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

### <span data-ttu-id="17fc2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17fc2-114">-DefaultProfile</span></span>
<span data-ttu-id="17fc2-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="17fc2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17fc2-116">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="17fc2-116">-EndTime</span></span>
<span data-ttu-id="17fc2-117">Befejezési időpont az UTC-ban</span><span class="sxs-lookup"><span data-stu-id="17fc2-117">End Time in UTC</span></span>

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

### <span data-ttu-id="17fc2-118">-Részletesség</span><span class="sxs-lookup"><span data-stu-id="17fc2-118">-Granularity</span></span>
<span data-ttu-id="17fc2-119">Granularitása</span><span class="sxs-lookup"><span data-stu-id="17fc2-119">Granularity</span></span>

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

### <span data-ttu-id="17fc2-120">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="17fc2-120">-InstanceDetails</span></span>
<span data-ttu-id="17fc2-121">Példány részletei</span><span class="sxs-lookup"><span data-stu-id="17fc2-121">Instance Details</span></span>

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

### <span data-ttu-id="17fc2-122">-Metrikák</span><span class="sxs-lookup"><span data-stu-id="17fc2-122">-Metrics</span></span>
<span data-ttu-id="17fc2-123">Metrikák</span><span class="sxs-lookup"><span data-stu-id="17fc2-123">Metrics</span></span>

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

### <span data-ttu-id="17fc2-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="17fc2-124">-Name</span></span>
<span data-ttu-id="17fc2-125">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="17fc2-125">App Service Plan Name</span></span>

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

### <span data-ttu-id="17fc2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17fc2-126">-ResourceGroupName</span></span>
<span data-ttu-id="17fc2-127">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="17fc2-127">Resource Group Name</span></span>

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

### <span data-ttu-id="17fc2-128">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="17fc2-128">-StartTime</span></span>
<span data-ttu-id="17fc2-129">Kezdési időpont az UTC-ban</span><span class="sxs-lookup"><span data-stu-id="17fc2-129">Start Time in UTC</span></span>

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

### <span data-ttu-id="17fc2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17fc2-130">CommonParameters</span></span>
<span data-ttu-id="17fc2-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="17fc2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17fc2-132">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="17fc2-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17fc2-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="17fc2-133">INPUTS</span></span>

### <span data-ttu-id="17fc2-134">Microsoft. Azure. Command. WebApps. models. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="17fc2-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="17fc2-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="17fc2-135">OUTPUTS</span></span>

### <span data-ttu-id="17fc2-136">Microsoft. Azure. Management. WebSites. models. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="17fc2-136">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="17fc2-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="17fc2-137">NOTES</span></span>

## <span data-ttu-id="17fc2-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="17fc2-138">RELATED LINKS</span></span>
