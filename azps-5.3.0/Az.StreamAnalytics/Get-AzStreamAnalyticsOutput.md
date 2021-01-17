---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 04A6FD47-482C-4EA6-9375-D8B6FD1F2659
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
ms.openlocfilehash: a2f20aa2c372261fe8f36599884c516563170293
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479346"
---
# <span data-ttu-id="26401-101">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="26401-101">Get-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="26401-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26401-102">SYNOPSIS</span></span>
<span data-ttu-id="26401-103">Egy adott Stream Analytics-feladatban vagy -kimenetben definiált kimeneteket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="26401-103">Gets the outputs defined in a specified Stream Analytics job or output.</span></span>

## <span data-ttu-id="26401-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="26401-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26401-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="26401-105">DESCRIPTION</span></span>
<span data-ttu-id="26401-106">A **Get-AzStreamAnalyticsOutput** parancsmag felsorolja az adott Stream Analytics-feladatban definiált összes kimenetet, vagy információt kap egy adott kimenetről.</span><span class="sxs-lookup"><span data-stu-id="26401-106">The **Get-AzStreamAnalyticsOutput** cmdlet lists all of the outputs that are defined in a specified Stream Analytics job or gets information about a specific output.</span></span>

## <span data-ttu-id="26401-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="26401-107">EXAMPLES</span></span>

### <span data-ttu-id="26401-108">1. példa: Információk a kimeneti eredményekről</span><span class="sxs-lookup"><span data-stu-id="26401-108">Example 1: Get information about job outputs</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="26401-109">Ez a parancs információkat ad vissza a Streaming Jobon definiált kimenetekkel kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="26401-109">This command returns information about the outputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="26401-110">2. példa: Információ lekérte egy adott kimenetről</span><span class="sxs-lookup"><span data-stu-id="26401-110">Example 2: Get information about a specific job output</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="26401-111">Ez a parancs információkat ad vissza a Streaming feladaton definiált Kimenet nevű kimenetről.</span><span class="sxs-lookup"><span data-stu-id="26401-111">This command returns information about the output named Output defined on the job StreamingJob.</span></span>

## <span data-ttu-id="26401-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26401-112">PARAMETERS</span></span>

### <span data-ttu-id="26401-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26401-113">-DefaultProfile</span></span>
<span data-ttu-id="26401-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="26401-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26401-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="26401-115">-JobName</span></span>
<span data-ttu-id="26401-116">Annak az Azure Stream Analytics-feladatnak a neve, amelyhez az Azure Stream Analytics kimenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="26401-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="26401-117">-Name</span><span class="sxs-lookup"><span data-stu-id="26401-117">-Name</span></span>
<span data-ttu-id="26401-118">A beolvassa az Azure Stream Analytics kimenetének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="26401-118">Specifies the name of the Azure Stream Analytics output to retrieve.</span></span>

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

### <span data-ttu-id="26401-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26401-119">-ResourceGroupName</span></span>
<span data-ttu-id="26401-120">Annak az erőforráscsoportnak a neve, amelyhez az Azure Stream Analytics kimenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="26401-120">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="26401-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26401-121">CommonParameters</span></span>
<span data-ttu-id="26401-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26401-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26401-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26401-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26401-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26401-124">INPUTS</span></span>

### <span data-ttu-id="26401-125">System.String</span><span class="sxs-lookup"><span data-stu-id="26401-125">System.String</span></span>

## <span data-ttu-id="26401-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26401-126">OUTPUTS</span></span>

### <span data-ttu-id="26401-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span><span class="sxs-lookup"><span data-stu-id="26401-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="26401-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="26401-128">NOTES</span></span>

## <span data-ttu-id="26401-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26401-129">RELATED LINKS</span></span>

[<span data-ttu-id="26401-130">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="26401-130">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="26401-131">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="26401-131">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="26401-132">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="26401-132">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


