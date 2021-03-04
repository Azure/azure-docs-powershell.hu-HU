---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/start-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
ms.openlocfilehash: cd7d6aaa9a295f888d8e765d12b4088525eff1fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939834"
---
# <span data-ttu-id="6f4ac-101">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6f4ac-101">Start-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="6f4ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f4ac-102">SYNOPSIS</span></span>
<span data-ttu-id="6f4ac-103">Elindít egy Stream Analytics-feladatot.</span><span class="sxs-lookup"><span data-stu-id="6f4ac-103">Starts a Stream Analytics job.</span></span>

## <span data-ttu-id="6f4ac-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6f4ac-104">SYNTAX</span></span>

```
Start-AzStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f4ac-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6f4ac-105">DESCRIPTION</span></span>
<span data-ttu-id="6f4ac-106">A **Start-AzStreamAnalyticsSync** parancsmag aszinkron módon telepíti és elindítja a Stream Analytics feladatot az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="6f4ac-106">The **Start-AzStreamAnalyticsJob** cmdlet asynchronously deploys and starts a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="6f4ac-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6f4ac-107">EXAMPLES</span></span>

### <span data-ttu-id="6f4ac-108">1. példa: Stream Analytics-feladat kezdése</span><span class="sxs-lookup"><span data-stu-id="6f4ac-108">Example 1: Start a Stream Analytics job</span></span>
```powershell
PS C:\> Start-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

<span data-ttu-id="6f4ac-109">Ez a parancs elindítja a StreamingStreamelési feladatot, és megadja, hogy a kimeneti esemény streamelése a timestamp 2014-07-03T01:00Z időpontban indul.</span><span class="sxs-lookup"><span data-stu-id="6f4ac-109">This command starts the job StreamingJob and specifies that the output event stream should start at timestamp 2014-07-03T01:00Z.</span></span>

## <span data-ttu-id="6f4ac-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f4ac-110">PARAMETERS</span></span>

### <span data-ttu-id="6f4ac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f4ac-111">-DefaultProfile</span></span>
<span data-ttu-id="6f4ac-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6f4ac-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f4ac-113">-Name</span><span class="sxs-lookup"><span data-stu-id="6f4ac-113">-Name</span></span>
<span data-ttu-id="6f4ac-114">Megadja a elindított Azure Stream Analytics-feladat nevét.</span><span class="sxs-lookup"><span data-stu-id="6f4ac-114">Specifies the name of the Azure Stream Analytics job to start.</span></span>

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

### <span data-ttu-id="6f4ac-115">-OutputStartMode</span><span class="sxs-lookup"><span data-stu-id="6f4ac-115">-OutputStartMode</span></span>
<span data-ttu-id="6f4ac-116">A feladat indítási módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6f4ac-116">Specifies the start mode for the job.</span></span>
<span data-ttu-id="6f4ac-117">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="6f4ac-117">Valid values are:</span></span> 
- <span data-ttu-id="6f4ac-118">JobStartTime – Ez az érték azt jelzi, hogy a kimeneti esemény adatfolyamának kezdőpontját a feladat kezdtek elindítani.</span><span class="sxs-lookup"><span data-stu-id="6f4ac-118">JobStartTime - This value indicates that the starting point of the output event stream should start when the job is started.</span></span>
- <span data-ttu-id="6f4ac-119">CustomTime – Ez az érték azt jelzi, hogy a kimeneti esemény adatfolyamának kezdőpontját a *OutputStartTime* paraméterben megadott egyéni időpontban kell kezdeni.</span><span class="sxs-lookup"><span data-stu-id="6f4ac-119">CustomTime - This value indicates that the starting point of the output event stream should start at a custom time that is specified in the *OutputStartTime* parameter.</span></span> 
 - <span data-ttu-id="6f4ac-120">LastOutputEventTime – Ez az érték azt jelzi, hogy a kimeneti esemény adatfolyamának kiindulási pontja az utolsó esemény kimeneti ideje.</span><span class="sxs-lookup"><span data-stu-id="6f4ac-120">LastOutputEventTime - This value indicates that the starting point of the output event stream should start from the last event output time.</span></span>
<span data-ttu-id="6f4ac-121">Ha a tulajdonság hiányzik, az alapértelmezett beállítás a JobStartTime.</span><span class="sxs-lookup"><span data-stu-id="6f4ac-121">If the property is absent, the default is JobStartTime.</span></span>

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

### <span data-ttu-id="6f4ac-122">-OutputStartTime</span><span class="sxs-lookup"><span data-stu-id="6f4ac-122">-OutputStartTime</span></span>
<span data-ttu-id="6f4ac-123">A kimenet kezdési idejét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6f4ac-123">Specifies the output start time.</span></span>
<span data-ttu-id="6f4ac-124">Ez az érték vagy egy ISO-8601 formátumú időbélyeg, amely a kimeneti eseményfolyam kezdőpontját jelzi, vagy $Null, amely azt jelzi, hogy a kimeneti eseményfolyam a streamelési feladat minden megkezdésekor elindul.</span><span class="sxs-lookup"><span data-stu-id="6f4ac-124">This value is either an ISO-8601 formatted time stamp that indicates the starting point of the output event stream, or $Null to indicate that the output event stream will start whenever the streaming job is started.</span></span>
<span data-ttu-id="6f4ac-125">Ennek a tulajdonságnak értéke kell, hogy legyen, ha *az OutputStartMode* értéke CustomTime.</span><span class="sxs-lookup"><span data-stu-id="6f4ac-125">This property must have a value if *OutputStartMode* is set to CustomTime.</span></span>

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

### <span data-ttu-id="6f4ac-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f4ac-126">-ResourceGroupName</span></span>
<span data-ttu-id="6f4ac-127">Annak az erőforráscsoportnak a nevét adja meg, amelyhez az Azure Stream Analytics-feladat tartozik.</span><span class="sxs-lookup"><span data-stu-id="6f4ac-127">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="6f4ac-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f4ac-128">CommonParameters</span></span>
<span data-ttu-id="6f4ac-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f4ac-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f4ac-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f4ac-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f4ac-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6f4ac-131">INPUTS</span></span>

### <span data-ttu-id="6f4ac-132">System.String</span><span class="sxs-lookup"><span data-stu-id="6f4ac-132">System.String</span></span>

### <span data-ttu-id="6f4ac-133">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6f4ac-133">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="6f4ac-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f4ac-134">OUTPUTS</span></span>

### <span data-ttu-id="6f4ac-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6f4ac-135">System.Boolean</span></span>

## <span data-ttu-id="6f4ac-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6f4ac-136">NOTES</span></span>

## <span data-ttu-id="6f4ac-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6f4ac-137">RELATED LINKS</span></span>

[<span data-ttu-id="6f4ac-138">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6f4ac-138">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="6f4ac-139">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6f4ac-139">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="6f4ac-140">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6f4ac-140">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="6f4ac-141">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6f4ac-141">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


