---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/start-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Start-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Start-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 20bd934a35fdf0cf907e83f22c8148fdfe5425db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502816"
---
# <span data-ttu-id="e069d-101">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e069d-101">Start-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="e069d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e069d-102">SYNOPSIS</span></span>
<span data-ttu-id="e069d-103">Adatfolyam-elemzési feladat indítása.</span><span class="sxs-lookup"><span data-stu-id="e069d-103">Starts a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e069d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e069d-104">SYNTAX</span></span>

```
Start-AzureRmStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e069d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e069d-105">DESCRIPTION</span></span>
<span data-ttu-id="e069d-106">A **Start-AzureRmStreamAnalyticsJob** parancsmag aszinkron módon telepíti és elindítja az adatfolyam-elemzési feladatot az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="e069d-106">The **Start-AzureRmStreamAnalyticsJob** cmdlet asynchronously deploys and starts a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="e069d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e069d-107">EXAMPLES</span></span>

### <span data-ttu-id="e069d-108">1. példa: adatfolyam-elemzési feladat indítása</span><span class="sxs-lookup"><span data-stu-id="e069d-108">EXAMPLE 1: Start a Stream Analytics job</span></span>
```
PS C:\>Start-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

<span data-ttu-id="e069d-109">Ez a parancs elindítja a feladat StreamingJob, és azt adja meg, hogy a kimeneti esemény folyama az időbélyegző 2014 – 07 – 03T01:00Z.</span><span class="sxs-lookup"><span data-stu-id="e069d-109">This command starts the job StreamingJob and specifies that the output event stream should start at timestamp 2014-07-03T01:00Z.</span></span>

## <span data-ttu-id="e069d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e069d-110">PARAMETERS</span></span>

### <span data-ttu-id="e069d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e069d-111">-DefaultProfile</span></span>
<span data-ttu-id="e069d-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e069d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e069d-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e069d-113">-Name</span></span>
<span data-ttu-id="e069d-114">A kezdéshez az Azure stream Analytics-feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e069d-114">Specifies the name of the Azure Stream Analytics job to start.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e069d-115">-OutputStartMode</span><span class="sxs-lookup"><span data-stu-id="e069d-115">-OutputStartMode</span></span>
<span data-ttu-id="e069d-116">A feladat indítási módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e069d-116">Specifies the start mode for the job.</span></span>
<span data-ttu-id="e069d-117">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="e069d-117">Valid values are:</span></span> 
- <span data-ttu-id="e069d-118">JobStartTime – ez az érték azt jelzi, hogy a kimeneti esemény folyam kezdőpontjának meg kell kezdődnie a feladat indításakor.</span><span class="sxs-lookup"><span data-stu-id="e069d-118">JobStartTime - This value indicates that the starting point of the output event stream should start when the job is started.</span></span>
- <span data-ttu-id="e069d-119">CustomTime – ez az érték azt jelzi, hogy a kimenet-esemény folyam kezdőpontjának a *OutputStartTime* paraméterben megadott egyéni időpontra kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="e069d-119">CustomTime - This value indicates that the starting point of the output event stream should start at a custom time that is specified in the *OutputStartTime* parameter.</span></span> 
 <span data-ttu-id="e069d-120">---LastOutputEventTime – ez az érték azt jelzi, hogy a kimeneti esemény folyam kezdőpontja a legutóbbi esemény kimeneti időpontjától kezdődik.</span><span class="sxs-lookup"><span data-stu-id="e069d-120">-- LastOutputEventTime - This value indicates that the starting point of the output event stream should start from the last event output time.</span></span>
<span data-ttu-id="e069d-121">Ha a tulajdonság hiányzik, az alapértelmezett érték a JobStartTime.</span><span class="sxs-lookup"><span data-stu-id="e069d-121">If the property is absent, the default is JobStartTime.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e069d-122">-OutputStartTime</span><span class="sxs-lookup"><span data-stu-id="e069d-122">-OutputStartTime</span></span>
<span data-ttu-id="e069d-123">A kimenet kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e069d-123">Specifies the output start time.</span></span>
<span data-ttu-id="e069d-124">Ez az érték az ISO-8601 formázott időbélyegzője, amely jelzi a kimeneti esemény folyam kezdőpontját, vagy $Null jelzi, hogy a kimeneti esemény folyama elindul a folyamatos adatfolyam-továbbítási feladat indításakor.</span><span class="sxs-lookup"><span data-stu-id="e069d-124">This value is either an ISO-8601 formatted time stamp that indicates the starting point of the output event stream, or $Null to indicate that the output event stream will start whenever the streaming job is started.</span></span>
<span data-ttu-id="e069d-125">Ennek a tulajdonságnak tartalmaznia kell egy értéket, ha a *OutputStartMode* értéke CustomTime.</span><span class="sxs-lookup"><span data-stu-id="e069d-125">This property must have a value if *OutputStartMode* is set to CustomTime.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e069d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e069d-126">-ResourceGroupName</span></span>
<span data-ttu-id="e069d-127">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics-feladat tartozik.</span><span class="sxs-lookup"><span data-stu-id="e069d-127">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="e069d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e069d-128">CommonParameters</span></span>
<span data-ttu-id="e069d-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e069d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e069d-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e069d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e069d-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e069d-131">INPUTS</span></span>

### <span data-ttu-id="e069d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e069d-132">System.String</span></span>

### <span data-ttu-id="e069d-133">System. null ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e069d-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="e069d-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e069d-134">OUTPUTS</span></span>

### <span data-ttu-id="e069d-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e069d-135">System.Boolean</span></span>

## <span data-ttu-id="e069d-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e069d-136">NOTES</span></span>

## <span data-ttu-id="e069d-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e069d-137">RELATED LINKS</span></span>

[<span data-ttu-id="e069d-138">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e069d-138">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="e069d-139">Új – AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e069d-139">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="e069d-140">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e069d-140">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="e069d-141">Stop-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e069d-141">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)

