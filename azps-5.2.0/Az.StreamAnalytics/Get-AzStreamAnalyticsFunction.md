---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 7F08A880-1FC5-4542-8AB8-927BB999A552
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
ms.openlocfilehash: ceedee89473385202037cfedb23e4373995b6f98
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366461"
---
# <span data-ttu-id="77149-101">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="77149-101">Get-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="77149-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77149-102">SYNOPSIS</span></span>
<span data-ttu-id="77149-103">Függvényeket használ a Stream Analytics-feladatban.</span><span class="sxs-lookup"><span data-stu-id="77149-103">Gets functions in a Stream Analytics job.</span></span>

## <span data-ttu-id="77149-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="77149-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77149-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="77149-105">DESCRIPTION</span></span>
<span data-ttu-id="77149-106">A **Get-AzStreamAnalyticsFunction** parancsmag lekérte az Azure Stream Analytics-feladatban definiált függvények listáját vagy egy adott függvény adatait.</span><span class="sxs-lookup"><span data-stu-id="77149-106">The **Get-AzStreamAnalyticsFunction** cmdlet gets a list of the functions that are defined in an Azure Stream Analytics job or information about a specific function.</span></span>

## <span data-ttu-id="77149-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="77149-107">EXAMPLES</span></span>

### <span data-ttu-id="77149-108">1. példa: Az összes Stream Analytics függvény lekérte</span><span class="sxs-lookup"><span data-stu-id="77149-108">Example 1: Get all Stream Analytics functions</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

<span data-ttu-id="77149-109">Ez a parancs a Stream Job22 nevű feladaton definiált függvényeket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="77149-109">This command gets the functions defined on the job named StreamJob22.</span></span>

### <span data-ttu-id="77149-110">2. példa: Adott Stream Analytics függvény lekérte</span><span class="sxs-lookup"><span data-stu-id="77149-110">Example 2: Get a specific Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="77149-111">Ez a parancs információt kap a ScoreTweet nevű függvényről, amely a Stream Job22 nevű feladaton van definiálva.</span><span class="sxs-lookup"><span data-stu-id="77149-111">This command gets information about the function named ScoreTweet defined on the job named StreamJob22.</span></span>

## <span data-ttu-id="77149-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77149-112">PARAMETERS</span></span>

### <span data-ttu-id="77149-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77149-113">-DefaultProfile</span></span>
<span data-ttu-id="77149-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="77149-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77149-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="77149-115">-JobName</span></span>
<span data-ttu-id="77149-116">Annak a Stream Analytics-feladatnak a nevét adja meg, amelyhez a függvények tartoznak.</span><span class="sxs-lookup"><span data-stu-id="77149-116">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="77149-117">Ez a parancsmag függvényeket kap a paraméter által megadott feladathoz.</span><span class="sxs-lookup"><span data-stu-id="77149-117">This cmdlet gets functions for the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="77149-118">-Name</span><span class="sxs-lookup"><span data-stu-id="77149-118">-Name</span></span>
<span data-ttu-id="77149-119">Annak a Stream Analytics függvénynek a nevét adja meg, amelybe ez a parancsmag kerül.</span><span class="sxs-lookup"><span data-stu-id="77149-119">Specifies the name of the Stream Analytics function that this cmdlet gets.</span></span>

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

### <span data-ttu-id="77149-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77149-120">-ResourceGroupName</span></span>
<span data-ttu-id="77149-121">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a Stream Analytics függvény tartozik.</span><span class="sxs-lookup"><span data-stu-id="77149-121">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="77149-122">Ez a parancsmag a paraméter által megadott csoport függvényei.</span><span class="sxs-lookup"><span data-stu-id="77149-122">This cmdlet gets functions for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="77149-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77149-123">CommonParameters</span></span>
<span data-ttu-id="77149-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77149-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77149-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77149-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77149-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="77149-126">INPUTS</span></span>

### <span data-ttu-id="77149-127">System.String</span><span class="sxs-lookup"><span data-stu-id="77149-127">System.String</span></span>

## <span data-ttu-id="77149-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="77149-128">OUTPUTS</span></span>

### <span data-ttu-id="77149-129">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span><span class="sxs-lookup"><span data-stu-id="77149-129">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="77149-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="77149-130">NOTES</span></span>

## <span data-ttu-id="77149-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="77149-131">RELATED LINKS</span></span>

[<span data-ttu-id="77149-132">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="77149-132">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="77149-133">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="77149-133">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="77149-134">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="77149-134">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


