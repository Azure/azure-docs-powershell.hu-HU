---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: CA67985F-C5D5-4CF4-81A4-C35FD769AF0A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmUsage.md
ms.openlocfilehash: 9f02a1c9dfe0c4c41fa1e873201dbeb1d849dd77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501847"
---
# <span data-ttu-id="864ce-101">Get-AzureRmUsage</span><span class="sxs-lookup"><span data-stu-id="864ce-101">Get-AzureRmUsage</span></span>

## <span data-ttu-id="864ce-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="864ce-102">SYNOPSIS</span></span>
<span data-ttu-id="864ce-103">Az erőforrás használati metrikáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="864ce-103">Gets the usage metrics for a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="864ce-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="864ce-104">SYNTAX</span></span>

```
Get-AzureRmUsage [-ResourceId] <String> [-ApiVersion <String>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-MetricNames <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="864ce-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="864ce-105">DESCRIPTION</span></span>
<span data-ttu-id="864ce-106">A **Get-AzureRmUsage** parancsmag a megadott erőforrás használati metrikáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="864ce-106">The **Get-AzureRmUsage** cmdlet gets the usage metrics for a specified resource.</span></span>

## <span data-ttu-id="864ce-107">Példák</span><span class="sxs-lookup"><span data-stu-id="864ce-107">EXAMPLES</span></span>

### <span data-ttu-id="864ce-108">Példa 1: használati metrikák beszerzése erőforrás-AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="864ce-108">Example 1: Get usage metrics by resource ID</span></span>
```
PS C:\>Get-AzureRmUsage -ResourceId "/subscriptions/bcdeb07f-1c43-20be-1f3b-4f0febc10f5b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/pattifuller"
```

<span data-ttu-id="864ce-109">Ez a parancs a megadott webhely használati metrikáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="864ce-109">This command gets the usage metrics for the specified website.</span></span>

## <span data-ttu-id="864ce-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="864ce-110">PARAMETERS</span></span>

### <span data-ttu-id="864ce-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="864ce-111">-ApiVersion</span></span>
<span data-ttu-id="864ce-112">Egy API-verzió karakterláncát adja meg, például 2014-04-01, amelyet az erőforrás-szolgáltató fogad el.</span><span class="sxs-lookup"><span data-stu-id="864ce-112">Specifies an API version string, for example, 2014-04-01, which is accepted by the resource provider.</span></span>

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

### <span data-ttu-id="864ce-113">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="864ce-113">-EndTime</span></span>
<span data-ttu-id="864ce-114">A keresés legkésőbbi időpontját és dátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="864ce-114">Specifies the latest time and date to search.</span></span>

<span data-ttu-id="864ce-115">A Get-Date parancsmaggal **datetime** -objektumot is beszerezhet.</span><span class="sxs-lookup"><span data-stu-id="864ce-115">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="864ce-116">-MetricNames</span><span class="sxs-lookup"><span data-stu-id="864ce-116">-MetricNames</span></span>
<span data-ttu-id="864ce-117">A metrikák neveinek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="864ce-117">Specifies an array of names of metrics.</span></span>

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

### <span data-ttu-id="864ce-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="864ce-118">-ResourceId</span></span>
<span data-ttu-id="864ce-119">A metrika erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="864ce-119">Specifies the ID of the resource for the metric.</span></span>

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

### <span data-ttu-id="864ce-120">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="864ce-120">-StartTime</span></span>
<span data-ttu-id="864ce-121">A kereséshez legkorábbi dátumot és dátumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="864ce-121">Specifies the earliest time and date to search.</span></span>

<span data-ttu-id="864ce-122">A Get-Date parancsmaggal **datetime** -objektumot is beszerezhet.</span><span class="sxs-lookup"><span data-stu-id="864ce-122">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="864ce-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="864ce-123">-DefaultProfile</span></span>
<span data-ttu-id="864ce-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="864ce-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="864ce-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="864ce-125">CommonParameters</span></span>
<span data-ttu-id="864ce-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="864ce-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="864ce-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="864ce-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="864ce-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="864ce-128">INPUTS</span></span>

## <span data-ttu-id="864ce-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="864ce-129">OUTPUTS</span></span>

### <span data-ttu-id="864ce-130">Microsoft. Azure. Command. detekintés. OutputClasses. PSUsageMetric []</span><span class="sxs-lookup"><span data-stu-id="864ce-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSUsageMetric[]</span></span>

## <span data-ttu-id="864ce-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="864ce-131">NOTES</span></span>

## <span data-ttu-id="864ce-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="864ce-132">RELATED LINKS</span></span>

[<span data-ttu-id="864ce-133">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="864ce-133">Get-AzureRmMetric</span></span>](./Get-AzureRmMetric.md)


