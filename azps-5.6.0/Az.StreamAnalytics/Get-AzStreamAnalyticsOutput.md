---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 04A6FD47-482C-4EA6-9375-D8B6FD1F2659
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 1f959f96b02296d4cc25cca06ae6c95bdef98af7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929545"
---
# <span data-ttu-id="324f5-101">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="324f5-101">Get-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="324f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="324f5-102">SYNOPSIS</span></span>
<span data-ttu-id="324f5-103">Egy adott Stream Analytics-feladatban vagy -kimenetben definiált kimeneteket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="324f5-103">Gets the outputs defined in a specified Stream Analytics job or output.</span></span>

## <span data-ttu-id="324f5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="324f5-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="324f5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="324f5-105">DESCRIPTION</span></span>
<span data-ttu-id="324f5-106">A **Get-AzStreamAnalyticsOutput** parancsmag felsorolja az adott Stream Analytics-feladatban definiált összes kimenetet, vagy információt kap egy adott kimenetről.</span><span class="sxs-lookup"><span data-stu-id="324f5-106">The **Get-AzStreamAnalyticsOutput** cmdlet lists all of the outputs that are defined in a specified Stream Analytics job or gets information about a specific output.</span></span>

## <span data-ttu-id="324f5-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="324f5-107">EXAMPLES</span></span>

### <span data-ttu-id="324f5-108">1. példa: Információk a kimeneti eredményekről</span><span class="sxs-lookup"><span data-stu-id="324f5-108">Example 1: Get information about job outputs</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="324f5-109">Ez a parancs információkat ad vissza a Streaming Jobon definiált kimenetekkel kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="324f5-109">This command returns information about the outputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="324f5-110">2. példa: Információ lekérte egy adott kimenetről</span><span class="sxs-lookup"><span data-stu-id="324f5-110">Example 2: Get information about a specific job output</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="324f5-111">Ez a parancs információkat ad vissza a Streaming Streaming Streaming feladaton definiált Kimenet nevű kimenetről.</span><span class="sxs-lookup"><span data-stu-id="324f5-111">This command returns information about the output named Output defined on the job StreamingJob.</span></span>

## <span data-ttu-id="324f5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="324f5-112">PARAMETERS</span></span>

### <span data-ttu-id="324f5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="324f5-113">-DefaultProfile</span></span>
<span data-ttu-id="324f5-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="324f5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="324f5-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="324f5-115">-JobName</span></span>
<span data-ttu-id="324f5-116">Annak az Azure Stream Analytics-feladatnak a neve, amelyhez az Azure Stream Analytics kimenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="324f5-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="324f5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="324f5-117">-Name</span></span>
<span data-ttu-id="324f5-118">A beolvassa az Azure Stream Analytics kimenetének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="324f5-118">Specifies the name of the Azure Stream Analytics output to retrieve.</span></span>

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

### <span data-ttu-id="324f5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="324f5-119">-ResourceGroupName</span></span>
<span data-ttu-id="324f5-120">Annak az erőforráscsoportnak a nevét adja meg, amelyhez az Azure Stream Analytics kimenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="324f5-120">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="324f5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="324f5-121">CommonParameters</span></span>
<span data-ttu-id="324f5-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="324f5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="324f5-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="324f5-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="324f5-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="324f5-124">INPUTS</span></span>

### <span data-ttu-id="324f5-125">System.String</span><span class="sxs-lookup"><span data-stu-id="324f5-125">System.String</span></span>

## <span data-ttu-id="324f5-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="324f5-126">OUTPUTS</span></span>

### <span data-ttu-id="324f5-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span><span class="sxs-lookup"><span data-stu-id="324f5-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="324f5-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="324f5-128">NOTES</span></span>

## <span data-ttu-id="324f5-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="324f5-129">RELATED LINKS</span></span>

[<span data-ttu-id="324f5-130">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="324f5-130">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="324f5-131">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="324f5-131">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="324f5-132">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="324f5-132">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


