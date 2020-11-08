---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/start-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
ms.openlocfilehash: 1194a730293d6f0f7b4aca58f508f808a2c6193e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025856"
---
# <span data-ttu-id="73a9c-101">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="73a9c-101">Start-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="73a9c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="73a9c-102">SYNOPSIS</span></span>
<span data-ttu-id="73a9c-103">Adatfolyam-elemzési feladat indítása.</span><span class="sxs-lookup"><span data-stu-id="73a9c-103">Starts a Stream Analytics job.</span></span>

## <span data-ttu-id="73a9c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="73a9c-104">SYNTAX</span></span>

```
Start-AzStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73a9c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="73a9c-105">DESCRIPTION</span></span>
<span data-ttu-id="73a9c-106">A **Start-AzStreamAnalyticsJob** parancsmag aszinkron módon telepíti és elindítja az adatfolyam-elemzési feladatot az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="73a9c-106">The **Start-AzStreamAnalyticsJob** cmdlet asynchronously deploys and starts a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="73a9c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="73a9c-107">EXAMPLES</span></span>

### <span data-ttu-id="73a9c-108">1. példa: adatfolyam-elemzési feladat indítása</span><span class="sxs-lookup"><span data-stu-id="73a9c-108">Example 1: Start a Stream Analytics job</span></span>
```powershell
PS C:\> Start-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

<span data-ttu-id="73a9c-109">Ez a parancs elindítja a feladat StreamingJob, és azt adja meg, hogy a kimeneti esemény folyama az időbélyegző 2014 – 07 – 03T01:00Z.</span><span class="sxs-lookup"><span data-stu-id="73a9c-109">This command starts the job StreamingJob and specifies that the output event stream should start at timestamp 2014-07-03T01:00Z.</span></span>

## <span data-ttu-id="73a9c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="73a9c-110">PARAMETERS</span></span>

### <span data-ttu-id="73a9c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73a9c-111">-DefaultProfile</span></span>
<span data-ttu-id="73a9c-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="73a9c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73a9c-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="73a9c-113">-Name</span></span>
<span data-ttu-id="73a9c-114">A kezdéshez az Azure stream Analytics-feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="73a9c-114">Specifies the name of the Azure Stream Analytics job to start.</span></span>

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

### <span data-ttu-id="73a9c-115">-OutputStartMode</span><span class="sxs-lookup"><span data-stu-id="73a9c-115">-OutputStartMode</span></span>
<span data-ttu-id="73a9c-116">A feladat indítási módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="73a9c-116">Specifies the start mode for the job.</span></span>
<span data-ttu-id="73a9c-117">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="73a9c-117">Valid values are:</span></span> 
- <span data-ttu-id="73a9c-118">JobStartTime – ez az érték azt jelzi, hogy a kimeneti esemény folyam kezdőpontjának meg kell kezdődnie a feladat indításakor.</span><span class="sxs-lookup"><span data-stu-id="73a9c-118">JobStartTime - This value indicates that the starting point of the output event stream should start when the job is started.</span></span>
- <span data-ttu-id="73a9c-119">CustomTime – ez az érték azt jelzi, hogy a kimenet-esemény folyam kezdőpontjának a *OutputStartTime* paraméterben megadott egyéni időpontra kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="73a9c-119">CustomTime - This value indicates that the starting point of the output event stream should start at a custom time that is specified in the *OutputStartTime* parameter.</span></span> 
 - <span data-ttu-id="73a9c-120">LastOutputEventTime – ez az érték azt jelzi, hogy a kimeneti esemény folyam kezdőpontja a legutóbbi esemény kimeneti időpontjától kezdődik.</span><span class="sxs-lookup"><span data-stu-id="73a9c-120">LastOutputEventTime - This value indicates that the starting point of the output event stream should start from the last event output time.</span></span>
<span data-ttu-id="73a9c-121">Ha a tulajdonság hiányzik, az alapértelmezett érték a JobStartTime.</span><span class="sxs-lookup"><span data-stu-id="73a9c-121">If the property is absent, the default is JobStartTime.</span></span>

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

### <span data-ttu-id="73a9c-122">-OutputStartTime</span><span class="sxs-lookup"><span data-stu-id="73a9c-122">-OutputStartTime</span></span>
<span data-ttu-id="73a9c-123">A kimenet kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="73a9c-123">Specifies the output start time.</span></span>
<span data-ttu-id="73a9c-124">Ez az érték az ISO-8601 formázott időbélyegzője, amely jelzi a kimeneti esemény folyam kezdőpontját, vagy $Null jelzi, hogy a kimeneti esemény folyama elindul a folyamatos adatfolyam-továbbítási feladat indításakor.</span><span class="sxs-lookup"><span data-stu-id="73a9c-124">This value is either an ISO-8601 formatted time stamp that indicates the starting point of the output event stream, or $Null to indicate that the output event stream will start whenever the streaming job is started.</span></span>
<span data-ttu-id="73a9c-125">Ennek a tulajdonságnak tartalmaznia kell egy értéket, ha a *OutputStartMode* értéke CustomTime.</span><span class="sxs-lookup"><span data-stu-id="73a9c-125">This property must have a value if *OutputStartMode* is set to CustomTime.</span></span>

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

### <span data-ttu-id="73a9c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73a9c-126">-ResourceGroupName</span></span>
<span data-ttu-id="73a9c-127">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics-feladat tartozik.</span><span class="sxs-lookup"><span data-stu-id="73a9c-127">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="73a9c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73a9c-128">CommonParameters</span></span>
<span data-ttu-id="73a9c-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="73a9c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73a9c-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73a9c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73a9c-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="73a9c-131">INPUTS</span></span>

### <span data-ttu-id="73a9c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="73a9c-132">System.String</span></span>

### <span data-ttu-id="73a9c-133">System. null ' 1 [[System. DateTime, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="73a9c-133">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="73a9c-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="73a9c-134">OUTPUTS</span></span>

### <span data-ttu-id="73a9c-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="73a9c-135">System.Boolean</span></span>

## <span data-ttu-id="73a9c-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="73a9c-136">NOTES</span></span>

## <span data-ttu-id="73a9c-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="73a9c-137">RELATED LINKS</span></span>

[<span data-ttu-id="73a9c-138">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="73a9c-138">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="73a9c-139">Új – AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="73a9c-139">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="73a9c-140">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="73a9c-140">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="73a9c-141">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="73a9c-141">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


