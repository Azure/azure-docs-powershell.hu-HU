---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/start-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
ms.openlocfilehash: 1194a730293d6f0f7b4aca58f508f808a2c6193e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150147"
---
# <span data-ttu-id="deaba-101">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="deaba-101">Start-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="deaba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="deaba-102">SYNOPSIS</span></span>
<span data-ttu-id="deaba-103">Elindít egy Stream Analytics-feladatot.</span><span class="sxs-lookup"><span data-stu-id="deaba-103">Starts a Stream Analytics job.</span></span>

## <span data-ttu-id="deaba-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="deaba-104">SYNTAX</span></span>

```
Start-AzStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="deaba-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="deaba-105">DESCRIPTION</span></span>
<span data-ttu-id="deaba-106">A **Start-AzStreamAnalyticsSync** parancsmag aszinkron módon telepíti és elindítja a Stream Analytics feladatot az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="deaba-106">The **Start-AzStreamAnalyticsJob** cmdlet asynchronously deploys and starts a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="deaba-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="deaba-107">EXAMPLES</span></span>

### <span data-ttu-id="deaba-108">1. példa: Stream Analytics-feladat kezdése</span><span class="sxs-lookup"><span data-stu-id="deaba-108">Example 1: Start a Stream Analytics job</span></span>
```powershell
PS C:\> Start-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

<span data-ttu-id="deaba-109">Ez a parancs elindítja a Streaming StreamingOt, és megadja, hogy a kimeneti eseményfolyamnak a timestamp 2014-07-03T01:00Z időpontban kell elindulni.</span><span class="sxs-lookup"><span data-stu-id="deaba-109">This command starts the job StreamingJob and specifies that the output event stream should start at timestamp 2014-07-03T01:00Z.</span></span>

## <span data-ttu-id="deaba-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="deaba-110">PARAMETERS</span></span>

### <span data-ttu-id="deaba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deaba-111">-DefaultProfile</span></span>
<span data-ttu-id="deaba-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="deaba-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="deaba-113">-Name</span><span class="sxs-lookup"><span data-stu-id="deaba-113">-Name</span></span>
<span data-ttu-id="deaba-114">Megadja a elindított Azure Stream Analytics-feladat nevét.</span><span class="sxs-lookup"><span data-stu-id="deaba-114">Specifies the name of the Azure Stream Analytics job to start.</span></span>

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

### <span data-ttu-id="deaba-115">-OutputStartMode</span><span class="sxs-lookup"><span data-stu-id="deaba-115">-OutputStartMode</span></span>
<span data-ttu-id="deaba-116">A feladat indítási módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="deaba-116">Specifies the start mode for the job.</span></span>
<span data-ttu-id="deaba-117">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="deaba-117">Valid values are:</span></span> 
- <span data-ttu-id="deaba-118">JobStartTime – Ez az érték azt jelzi, hogy a kimeneti esemény adatfolyamának kezdőpontját a feladat kezdtek elindítani.</span><span class="sxs-lookup"><span data-stu-id="deaba-118">JobStartTime - This value indicates that the starting point of the output event stream should start when the job is started.</span></span>
- <span data-ttu-id="deaba-119">CustomTime – Ez az érték azt jelzi, hogy a kimeneti esemény adatfolyamának kezdőpontját a *OutputStartTime* paraméterben megadott egyéni időpontban kell kezdeni.</span><span class="sxs-lookup"><span data-stu-id="deaba-119">CustomTime - This value indicates that the starting point of the output event stream should start at a custom time that is specified in the *OutputStartTime* parameter.</span></span> 
 - <span data-ttu-id="deaba-120">LastOutputEventTime – Ez az érték azt jelzi, hogy a kimeneti esemény adatfolyamának kiindulási pontja az utolsó esemény kimeneti ideje.</span><span class="sxs-lookup"><span data-stu-id="deaba-120">LastOutputEventTime - This value indicates that the starting point of the output event stream should start from the last event output time.</span></span>
<span data-ttu-id="deaba-121">Ha a tulajdonság hiányzik, az alapértelmezett beállítás a JobStartTime.</span><span class="sxs-lookup"><span data-stu-id="deaba-121">If the property is absent, the default is JobStartTime.</span></span>

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

### <span data-ttu-id="deaba-122">-OutputStartTime</span><span class="sxs-lookup"><span data-stu-id="deaba-122">-OutputStartTime</span></span>
<span data-ttu-id="deaba-123">A kimenet kezdési idejét adja meg.</span><span class="sxs-lookup"><span data-stu-id="deaba-123">Specifies the output start time.</span></span>
<span data-ttu-id="deaba-124">Ez az érték vagy egy ISO-8601 formátumú időbélyeg, amely a kimeneti eseményfolyam kezdőpontját jelzi, vagy $Null, amely azt jelzi, hogy a kimeneti eseményfolyam a streamelési feladat minden megkezdésekor elindul.</span><span class="sxs-lookup"><span data-stu-id="deaba-124">This value is either an ISO-8601 formatted time stamp that indicates the starting point of the output event stream, or $Null to indicate that the output event stream will start whenever the streaming job is started.</span></span>
<span data-ttu-id="deaba-125">Ennek a tulajdonságnak értéke kell, hogy legyen, ha *az OutputStartMode* értéke CustomTime.</span><span class="sxs-lookup"><span data-stu-id="deaba-125">This property must have a value if *OutputStartMode* is set to CustomTime.</span></span>

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

### <span data-ttu-id="deaba-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="deaba-126">-ResourceGroupName</span></span>
<span data-ttu-id="deaba-127">Annak az erőforráscsoportnak a neve, amelyhez az Azure Stream Analytics-feladat tartozik.</span><span class="sxs-lookup"><span data-stu-id="deaba-127">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="deaba-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deaba-128">CommonParameters</span></span>
<span data-ttu-id="deaba-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="deaba-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deaba-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="deaba-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deaba-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="deaba-131">INPUTS</span></span>

### <span data-ttu-id="deaba-132">System.String</span><span class="sxs-lookup"><span data-stu-id="deaba-132">System.String</span></span>

### <span data-ttu-id="deaba-133">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="deaba-133">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="deaba-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="deaba-134">OUTPUTS</span></span>

### <span data-ttu-id="deaba-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="deaba-135">System.Boolean</span></span>

## <span data-ttu-id="deaba-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="deaba-136">NOTES</span></span>

## <span data-ttu-id="deaba-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="deaba-137">RELATED LINKS</span></span>

[<span data-ttu-id="deaba-138">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="deaba-138">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="deaba-139">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="deaba-139">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="deaba-140">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="deaba-140">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="deaba-141">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="deaba-141">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


