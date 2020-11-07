---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 513BE097-EB4A-4C49-9F7F-42A2BED09022
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappmetrics
schema: 2.0.0
ms.openlocfilehash: 1382ec0f4a2eaa61493e05a762616d9fac54a7f2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848610"
---
# <span data-ttu-id="eb3c3-101">Get-AzureRmWebAppMetrics</span><span class="sxs-lookup"><span data-stu-id="eb3c3-101">Get-AzureRmWebAppMetrics</span></span>

## <span data-ttu-id="eb3c3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eb3c3-102">SYNOPSIS</span></span>
<span data-ttu-id="eb3c3-103">Azure Web App metrikáit kapja.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-103">Gets Azure Web App metrics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb3c3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eb3c3-104">SYNTAX</span></span>

### <span data-ttu-id="eb3c3-105">S1</span><span class="sxs-lookup"><span data-stu-id="eb3c3-105">S1</span></span>
```
Get-AzureRmWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb3c3-106">S2</span><span class="sxs-lookup"><span data-stu-id="eb3c3-106">S2</span></span>
```
Get-AzureRmWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb3c3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="eb3c3-107">DESCRIPTION</span></span>
<span data-ttu-id="eb3c3-108">A **Get-AzureRmWebAppMetrics** webalkalmazás metrikáját kapja.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-108">The **Get-AzureRmWebAppMetrics** gets Web App metrics.</span></span>

## <span data-ttu-id="eb3c3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="eb3c3-109">EXAMPLES</span></span>

### <span data-ttu-id="eb3c3-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="eb3c3-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="eb3c3-111">Ez a parancs a Web App ContosoWebApp percenkénti kérelmeket kapja meg (PT1M-szavazási idő 1 perc) a kezdési időpont és a befejezési időpont között</span><span class="sxs-lookup"><span data-stu-id="eb3c3-111">This command gets Requests of the Web App ContosoWebApp per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="eb3c3-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eb3c3-112">PARAMETERS</span></span>

### <span data-ttu-id="eb3c3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb3c3-113">-DefaultProfile</span></span>
<span data-ttu-id="eb3c3-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eb3c3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb3c3-115">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="eb3c3-115">-EndTime</span></span>
<span data-ttu-id="eb3c3-116">Befejezési időpont az UTC-ban</span><span class="sxs-lookup"><span data-stu-id="eb3c3-116">End Time in UTC</span></span>

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

### <span data-ttu-id="eb3c3-117">-Részletesség</span><span class="sxs-lookup"><span data-stu-id="eb3c3-117">-Granularity</span></span>
<span data-ttu-id="eb3c3-118">Granularitása</span><span class="sxs-lookup"><span data-stu-id="eb3c3-118">Granularity</span></span>

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

### <span data-ttu-id="eb3c3-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="eb3c3-119">-InstanceDetails</span></span>
<span data-ttu-id="eb3c3-120">Példány részletei</span><span class="sxs-lookup"><span data-stu-id="eb3c3-120">Instance Details</span></span>

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

### <span data-ttu-id="eb3c3-121">-Metrikák</span><span class="sxs-lookup"><span data-stu-id="eb3c3-121">-Metrics</span></span>
<span data-ttu-id="eb3c3-122">Metrikák karakterlánc-tömbként</span><span class="sxs-lookup"><span data-stu-id="eb3c3-122">Metrics as a string array</span></span>

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

### <span data-ttu-id="eb3c3-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eb3c3-123">-Name</span></span>
<span data-ttu-id="eb3c3-124">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="eb3c3-124">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb3c3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb3c3-125">-ResourceGroupName</span></span>
<span data-ttu-id="eb3c3-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="eb3c3-126">Resource Group Name</span></span>

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

### <span data-ttu-id="eb3c3-127">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="eb3c3-127">-StartTime</span></span>
<span data-ttu-id="eb3c3-128">Kezdési időpont az UTC-ban</span><span class="sxs-lookup"><span data-stu-id="eb3c3-128">Start Time in UTC</span></span>

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

### <span data-ttu-id="eb3c3-129">-WebApp</span><span class="sxs-lookup"><span data-stu-id="eb3c3-129">-WebApp</span></span>
<span data-ttu-id="eb3c3-130">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="eb3c3-130">WebApp object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb3c3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb3c3-131">CommonParameters</span></span>
<span data-ttu-id="eb3c3-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eb3c3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb3c3-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb3c3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb3c3-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb3c3-134">INPUTS</span></span>

### <span data-ttu-id="eb3c3-135">Webhely</span><span class="sxs-lookup"><span data-stu-id="eb3c3-135">Site</span></span>
<span data-ttu-id="eb3c3-136">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="eb3c3-136">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="eb3c3-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb3c3-137">OUTPUTS</span></span>

## <span data-ttu-id="eb3c3-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eb3c3-138">NOTES</span></span>

## <span data-ttu-id="eb3c3-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb3c3-139">RELATED LINKS</span></span>

[<span data-ttu-id="eb3c3-140">Get-AzureRmWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="eb3c3-140">Get-AzureRmWebAppCertificate</span></span>](./Get-AzureRmWebAppCertificate.md)

