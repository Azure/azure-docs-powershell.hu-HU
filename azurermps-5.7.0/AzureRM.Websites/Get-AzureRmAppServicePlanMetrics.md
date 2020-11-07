---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermappserviceplanmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlanMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlanMetrics.md
ms.openlocfilehash: f3376f40246640b8de52ffa138912c768486a3dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679239"
---
# <span data-ttu-id="88dad-101">Get-AzureRmAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="88dad-101">Get-AzureRmAppServicePlanMetrics</span></span>

## <span data-ttu-id="88dad-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="88dad-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88dad-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="88dad-103">SYNTAX</span></span>

### <span data-ttu-id="88dad-104">S1</span><span class="sxs-lookup"><span data-stu-id="88dad-104">S1</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88dad-105">S2</span><span class="sxs-lookup"><span data-stu-id="88dad-105">S2</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <ServerFarmWithRichSku>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88dad-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="88dad-106">DESCRIPTION</span></span>
<span data-ttu-id="88dad-107">A **Get-AzureRmAppServicePlanMetrics** elérhetővé válik az App Service Plan mérőszámai.</span><span class="sxs-lookup"><span data-stu-id="88dad-107">The **Get-AzureRmAppServicePlanMetrics** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="88dad-108">Példák</span><span class="sxs-lookup"><span data-stu-id="88dad-108">EXAMPLES</span></span>

### <span data-ttu-id="88dad-109">1:</span><span class="sxs-lookup"><span data-stu-id="88dad-109">1:</span></span>
```
PS C:\>Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["CPU Percentage"]
```

<span data-ttu-id="88dad-110">Ez a parancs az App-csomag (PT1M-szavazási idő 1 perc) CPU-százalékát kapja meg a kezdő időpont és a Befejezés között</span><span class="sxs-lookup"><span data-stu-id="88dad-110">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="88dad-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="88dad-111">PARAMETERS</span></span>

### <span data-ttu-id="88dad-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="88dad-112">-AppServicePlan</span></span>
<span data-ttu-id="88dad-113">Alkalmazás-szolgáltatási terv objektum</span><span class="sxs-lookup"><span data-stu-id="88dad-113">App Service Plan Object</span></span>

```yaml
Type: ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88dad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88dad-114">-DefaultProfile</span></span>
<span data-ttu-id="88dad-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="88dad-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88dad-116">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="88dad-116">-EndTime</span></span>
<span data-ttu-id="88dad-117">Befejezési időpont az UTC-ban</span><span class="sxs-lookup"><span data-stu-id="88dad-117">End Time in UTC</span></span>

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

### <span data-ttu-id="88dad-118">-Részletesség</span><span class="sxs-lookup"><span data-stu-id="88dad-118">-Granularity</span></span>
<span data-ttu-id="88dad-119">Granularitása</span><span class="sxs-lookup"><span data-stu-id="88dad-119">Granularity</span></span>

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

### <span data-ttu-id="88dad-120">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="88dad-120">-InstanceDetails</span></span>
<span data-ttu-id="88dad-121">Példány részletei</span><span class="sxs-lookup"><span data-stu-id="88dad-121">Instance Details</span></span>

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

### <span data-ttu-id="88dad-122">-Metrikák</span><span class="sxs-lookup"><span data-stu-id="88dad-122">-Metrics</span></span>
<span data-ttu-id="88dad-123">Metrikák</span><span class="sxs-lookup"><span data-stu-id="88dad-123">Metrics</span></span>

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

### <span data-ttu-id="88dad-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="88dad-124">-Name</span></span>
<span data-ttu-id="88dad-125">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="88dad-125">App Service Plan Name</span></span>

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

### <span data-ttu-id="88dad-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88dad-126">-ResourceGroupName</span></span>
<span data-ttu-id="88dad-127">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="88dad-127">Resource Group Name</span></span>

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

### <span data-ttu-id="88dad-128">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="88dad-128">-StartTime</span></span>
<span data-ttu-id="88dad-129">Kezdési időpont az UTC-ban</span><span class="sxs-lookup"><span data-stu-id="88dad-129">Start Time in UTC</span></span>

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

### <span data-ttu-id="88dad-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88dad-130">CommonParameters</span></span>
<span data-ttu-id="88dad-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="88dad-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88dad-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88dad-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88dad-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="88dad-133">INPUTS</span></span>

### <span data-ttu-id="88dad-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="88dad-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="88dad-135">A ' AppServicePlan ' paraméter az "ServerFarmWithRichSku" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="88dad-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="88dad-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="88dad-136">OUTPUTS</span></span>

## <span data-ttu-id="88dad-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="88dad-137">NOTES</span></span>

## <span data-ttu-id="88dad-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="88dad-138">RELATED LINKS</span></span>

