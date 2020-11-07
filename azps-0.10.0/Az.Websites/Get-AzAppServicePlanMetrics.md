---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azappserviceplanmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzAppServicePlanMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzAppServicePlanMetrics.md
ms.openlocfilehash: c08ae63999582fd220005dde84316a2f4421d7b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842805"
---
# <span data-ttu-id="6c503-101">Get-AzAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="6c503-101">Get-AzAppServicePlanMetrics</span></span>

## <span data-ttu-id="6c503-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6c503-102">SYNOPSIS</span></span>
<span data-ttu-id="6c503-103">Az Azure webszolgáltatás-csomag metrikáit kapja.</span><span class="sxs-lookup"><span data-stu-id="6c503-103">Gets Azure Web service plan metrics.</span></span>

## <span data-ttu-id="6c503-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6c503-104">SYNTAX</span></span>

### <span data-ttu-id="6c503-105">S1</span><span class="sxs-lookup"><span data-stu-id="6c503-105">S1</span></span>
```
Get-AzAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c503-106">S2</span><span class="sxs-lookup"><span data-stu-id="6c503-106">S2</span></span>
```
Get-AzAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <AppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c503-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6c503-107">DESCRIPTION</span></span>
<span data-ttu-id="6c503-108">A **Get-AzAppServicePlanMetrics** elérhetővé válik az App Service Plan mérőszámai.</span><span class="sxs-lookup"><span data-stu-id="6c503-108">The **Get-AzAppServicePlanMetrics** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="6c503-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6c503-109">EXAMPLES</span></span>

### <span data-ttu-id="6c503-110">1:</span><span class="sxs-lookup"><span data-stu-id="6c503-110">1:</span></span>
```
PS C:\>Get-AzAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["CPU Percentage"]
```

<span data-ttu-id="6c503-111">Ez a parancs az App-csomag (PT1M-szavazási idő 1 perc) CPU-százalékát kapja meg a kezdő időpont és a Befejezés között</span><span class="sxs-lookup"><span data-stu-id="6c503-111">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="6c503-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6c503-112">PARAMETERS</span></span>

### <span data-ttu-id="6c503-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6c503-113">-AppServicePlan</span></span>
<span data-ttu-id="6c503-114">Alkalmazás-szolgáltatási terv objektum</span><span class="sxs-lookup"><span data-stu-id="6c503-114">App Service Plan Object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c503-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c503-115">-DefaultProfile</span></span>
<span data-ttu-id="6c503-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6c503-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c503-117">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="6c503-117">-EndTime</span></span>
<span data-ttu-id="6c503-118">Befejezési időpont az UTC-ban</span><span class="sxs-lookup"><span data-stu-id="6c503-118">End Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c503-119">-Részletesség</span><span class="sxs-lookup"><span data-stu-id="6c503-119">-Granularity</span></span>
<span data-ttu-id="6c503-120">Granularitása</span><span class="sxs-lookup"><span data-stu-id="6c503-120">Granularity</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PT1M, PT1H, P1D

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c503-121">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="6c503-121">-InstanceDetails</span></span>
<span data-ttu-id="6c503-122">Példány részletei</span><span class="sxs-lookup"><span data-stu-id="6c503-122">Instance Details</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c503-123">-Metrikák</span><span class="sxs-lookup"><span data-stu-id="6c503-123">-Metrics</span></span>
<span data-ttu-id="6c503-124">Metrikák</span><span class="sxs-lookup"><span data-stu-id="6c503-124">Metrics</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c503-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6c503-125">-Name</span></span>
<span data-ttu-id="6c503-126">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="6c503-126">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c503-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c503-127">-ResourceGroupName</span></span>
<span data-ttu-id="6c503-128">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="6c503-128">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c503-129">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="6c503-129">-StartTime</span></span>
<span data-ttu-id="6c503-130">Kezdési időpont az UTC-ban</span><span class="sxs-lookup"><span data-stu-id="6c503-130">Start Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c503-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c503-131">CommonParameters</span></span>
<span data-ttu-id="6c503-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6c503-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c503-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c503-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c503-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c503-134">INPUTS</span></span>

### <span data-ttu-id="6c503-135">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="6c503-135">ServerFarmWithRichSku</span></span>
<span data-ttu-id="6c503-136">A ' AppServicePlan ' paraméter az "ServerFarmWithRichSku" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="6c503-136">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="6c503-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c503-137">OUTPUTS</span></span>

## <span data-ttu-id="6c503-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6c503-138">NOTES</span></span>

## <span data-ttu-id="6c503-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6c503-139">RELATED LINKS</span></span>

