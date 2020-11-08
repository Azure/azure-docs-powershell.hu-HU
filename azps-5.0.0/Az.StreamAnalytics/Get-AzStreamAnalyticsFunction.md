---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 7F08A880-1FC5-4542-8AB8-927BB999A552
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
ms.openlocfilehash: ceedee89473385202037cfedb23e4373995b6f98
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186615"
---
# <span data-ttu-id="da864-101">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="da864-101">Get-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="da864-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="da864-102">SYNOPSIS</span></span>
<span data-ttu-id="da864-103">Az adatfolyam-elemzési feladatok függvényeit kapja.</span><span class="sxs-lookup"><span data-stu-id="da864-103">Gets functions in a Stream Analytics job.</span></span>

## <span data-ttu-id="da864-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="da864-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da864-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="da864-105">DESCRIPTION</span></span>
<span data-ttu-id="da864-106">A **Get-AzStreamAnalyticsFunction** parancsmag az Azure stream Analytics-feladatban definiált és egy adott függvényre vonatkozó információkat tartalmazó listát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="da864-106">The **Get-AzStreamAnalyticsFunction** cmdlet gets a list of the functions that are defined in an Azure Stream Analytics job or information about a specific function.</span></span>

## <span data-ttu-id="da864-107">Példák</span><span class="sxs-lookup"><span data-stu-id="da864-107">EXAMPLES</span></span>

### <span data-ttu-id="da864-108">Példa 1: az adatfolyam-elemzés minden függvényének beolvasása</span><span class="sxs-lookup"><span data-stu-id="da864-108">Example 1: Get all Stream Analytics functions</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

<span data-ttu-id="da864-109">Ez a parancs a StreamJob22 nevű feladaton megadott függvényeket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="da864-109">This command gets the functions defined on the job named StreamJob22.</span></span>

### <span data-ttu-id="da864-110">2. példa: adott adatfolyam-elemzési függvény beszerzése</span><span class="sxs-lookup"><span data-stu-id="da864-110">Example 2: Get a specific Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="da864-111">Ez a parancs információt kap a ScoreTweet nevű StreamJob22 nevű feladatról.</span><span class="sxs-lookup"><span data-stu-id="da864-111">This command gets information about the function named ScoreTweet defined on the job named StreamJob22.</span></span>

## <span data-ttu-id="da864-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="da864-112">PARAMETERS</span></span>

### <span data-ttu-id="da864-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da864-113">-DefaultProfile</span></span>
<span data-ttu-id="da864-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da864-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da864-115">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="da864-115">-JobName</span></span>
<span data-ttu-id="da864-116">Annak az adatfolyam-elemzési feladatnak a nevét adja meg, amelybe a függvény tartozik.</span><span class="sxs-lookup"><span data-stu-id="da864-116">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="da864-117">Ez a parancsmag a paraméter által megadott feladathoz ad függvényeket.</span><span class="sxs-lookup"><span data-stu-id="da864-117">This cmdlet gets functions for the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="da864-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="da864-118">-Name</span></span>
<span data-ttu-id="da864-119">A parancsmag által beolvasott adatfolyam-elemzési függvény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="da864-119">Specifies the name of the Stream Analytics function that this cmdlet gets.</span></span>

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

### <span data-ttu-id="da864-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da864-120">-ResourceGroupName</span></span>
<span data-ttu-id="da864-121">Annak az erőforráscsoportnek a nevét adja meg, amelybe az adatfolyam-elemzés függvény tartozik.</span><span class="sxs-lookup"><span data-stu-id="da864-121">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="da864-122">Ez a parancsmag a paraméter által megadott csoport függvényeit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="da864-122">This cmdlet gets functions for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="da864-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da864-123">CommonParameters</span></span>
<span data-ttu-id="da864-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="da864-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da864-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da864-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da864-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="da864-126">INPUTS</span></span>

### <span data-ttu-id="da864-127">System. String</span><span class="sxs-lookup"><span data-stu-id="da864-127">System.String</span></span>

## <span data-ttu-id="da864-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da864-128">OUTPUTS</span></span>

### <span data-ttu-id="da864-129">Microsoft. Azure. Command. StreamAnalytics. models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="da864-129">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="da864-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="da864-130">NOTES</span></span>

## <span data-ttu-id="da864-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da864-131">RELATED LINKS</span></span>

[<span data-ttu-id="da864-132">Új – AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="da864-132">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="da864-133">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="da864-133">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="da864-134">Teszt-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="da864-134">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


