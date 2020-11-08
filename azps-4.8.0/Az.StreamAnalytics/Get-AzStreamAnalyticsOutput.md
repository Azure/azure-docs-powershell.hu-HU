---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 04A6FD47-482C-4EA6-9375-D8B6FD1F2659
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
ms.openlocfilehash: a2f20aa2c372261fe8f36599884c516563170293
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017494"
---
# <span data-ttu-id="839fb-101">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="839fb-101">Get-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="839fb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="839fb-102">SYNOPSIS</span></span>
<span data-ttu-id="839fb-103">A megadott adatfolyam-munkafolyamatban vagy kimenetben meghatározott kimeneteket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="839fb-103">Gets the outputs defined in a specified Stream Analytics job or output.</span></span>

## <span data-ttu-id="839fb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="839fb-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="839fb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="839fb-105">DESCRIPTION</span></span>
<span data-ttu-id="839fb-106">A **Get-AzStreamAnalyticsOutput** parancsmag felsorolja a megadott adatfolyam-adatforrásban definiált összes kimenetet, illetve információt kap egy adott kimenetről.</span><span class="sxs-lookup"><span data-stu-id="839fb-106">The **Get-AzStreamAnalyticsOutput** cmdlet lists all of the outputs that are defined in a specified Stream Analytics job or gets information about a specific output.</span></span>

## <span data-ttu-id="839fb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="839fb-107">EXAMPLES</span></span>

### <span data-ttu-id="839fb-108">1. példa: adatok beszerzése a projekt kimenetéről</span><span class="sxs-lookup"><span data-stu-id="839fb-108">Example 1: Get information about job outputs</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="839fb-109">Ez a parancs információt ad eredményül a projekt StreamingJob meghatározott kimenetekről.</span><span class="sxs-lookup"><span data-stu-id="839fb-109">This command returns information about the outputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="839fb-110">2. példa: információk kérése egy adott projekt kimenetéről</span><span class="sxs-lookup"><span data-stu-id="839fb-110">Example 2: Get information about a specific job output</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="839fb-111">Ez a parancs információt ad eredményül a projekt StreamingJob definiált kimenetről.</span><span class="sxs-lookup"><span data-stu-id="839fb-111">This command returns information about the output named Output defined on the job StreamingJob.</span></span>

## <span data-ttu-id="839fb-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="839fb-112">PARAMETERS</span></span>

### <span data-ttu-id="839fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="839fb-113">-DefaultProfile</span></span>
<span data-ttu-id="839fb-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="839fb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="839fb-115">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="839fb-115">-JobName</span></span>
<span data-ttu-id="839fb-116">Annak az Azure stream-Analytics-feladatnak a neve, amelyhez az Azure stream Analytics kimenete tartozik.</span><span class="sxs-lookup"><span data-stu-id="839fb-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="839fb-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="839fb-117">-Name</span></span>
<span data-ttu-id="839fb-118">A lekérdezni kívánt Azure stream Analytics-kimenet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="839fb-118">Specifies the name of the Azure Stream Analytics output to retrieve.</span></span>

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

### <span data-ttu-id="839fb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="839fb-119">-ResourceGroupName</span></span>
<span data-ttu-id="839fb-120">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics kimenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="839fb-120">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="839fb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="839fb-121">CommonParameters</span></span>
<span data-ttu-id="839fb-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="839fb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="839fb-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="839fb-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="839fb-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="839fb-124">INPUTS</span></span>

### <span data-ttu-id="839fb-125">System. String</span><span class="sxs-lookup"><span data-stu-id="839fb-125">System.String</span></span>

## <span data-ttu-id="839fb-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="839fb-126">OUTPUTS</span></span>

### <span data-ttu-id="839fb-127">Microsoft. Azure. Command. StreamAnalytics. models. PSOutput</span><span class="sxs-lookup"><span data-stu-id="839fb-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="839fb-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="839fb-128">NOTES</span></span>

## <span data-ttu-id="839fb-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="839fb-129">RELATED LINKS</span></span>

[<span data-ttu-id="839fb-130">Új – AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="839fb-130">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="839fb-131">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="839fb-131">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="839fb-132">Teszt-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="839fb-132">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


