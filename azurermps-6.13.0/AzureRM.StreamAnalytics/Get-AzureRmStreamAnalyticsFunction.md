---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 7F08A880-1FC5-4542-8AB8-927BB999A552
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: cd947a29a9312c056133e5e7e302b130623bd698
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491842"
---
# <span data-ttu-id="16e05-101">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="16e05-101">Get-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="16e05-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="16e05-102">SYNOPSIS</span></span>
<span data-ttu-id="16e05-103">Az adatfolyam-elemzési feladatok függvényeit kapja.</span><span class="sxs-lookup"><span data-stu-id="16e05-103">Gets functions in a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16e05-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="16e05-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16e05-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="16e05-105">DESCRIPTION</span></span>
<span data-ttu-id="16e05-106">A **Get-AzureRmStreamAnalyticsFunction** parancsmag az Azure stream Analytics-feladatban definiált és egy adott függvényre vonatkozó információkat tartalmazó listát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="16e05-106">The **Get-AzureRmStreamAnalyticsFunction** cmdlet gets a list of the functions that are defined in an Azure Stream Analytics job or information about a specific function.</span></span>

## <span data-ttu-id="16e05-107">Példák</span><span class="sxs-lookup"><span data-stu-id="16e05-107">EXAMPLES</span></span>

### <span data-ttu-id="16e05-108">Példa 1: az adatfolyam-elemzés minden függvényének beolvasása</span><span class="sxs-lookup"><span data-stu-id="16e05-108">Example 1: Get all Stream Analytics functions</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

<span data-ttu-id="16e05-109">Ez a parancs a StreamJob22 nevű feladaton megadott függvényeket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="16e05-109">This command gets the functions defined on the job named StreamJob22.</span></span>

### <span data-ttu-id="16e05-110">2. példa: adott adatfolyam-elemzési függvény beszerzése</span><span class="sxs-lookup"><span data-stu-id="16e05-110">Example 2: Get a specific Stream Analytics function</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="16e05-111">Ez a parancs információt kap a ScoreTweet nevű StreamJob22 nevű feladatról.</span><span class="sxs-lookup"><span data-stu-id="16e05-111">This command gets information about the function named ScoreTweet defined on the job named StreamJob22.</span></span>

## <span data-ttu-id="16e05-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="16e05-112">PARAMETERS</span></span>

### <span data-ttu-id="16e05-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16e05-113">-DefaultProfile</span></span>
<span data-ttu-id="16e05-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="16e05-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16e05-115">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="16e05-115">-JobName</span></span>
<span data-ttu-id="16e05-116">Annak az adatfolyam-elemzési feladatnak a nevét adja meg, amelybe a függvény tartozik.</span><span class="sxs-lookup"><span data-stu-id="16e05-116">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="16e05-117">Ez a parancsmag a paraméter által megadott feladathoz ad függvényeket.</span><span class="sxs-lookup"><span data-stu-id="16e05-117">This cmdlet gets functions for the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="16e05-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="16e05-118">-Name</span></span>
<span data-ttu-id="16e05-119">A parancsmag által beolvasott adatfolyam-elemzési függvény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="16e05-119">Specifies the name of the Stream Analytics function that this cmdlet gets.</span></span>

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

### <span data-ttu-id="16e05-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16e05-120">-ResourceGroupName</span></span>
<span data-ttu-id="16e05-121">Annak az erőforráscsoportnek a nevét adja meg, amelybe az adatfolyam-elemzés függvény tartozik.</span><span class="sxs-lookup"><span data-stu-id="16e05-121">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="16e05-122">Ez a parancsmag a paraméter által megadott csoport függvényeit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="16e05-122">This cmdlet gets functions for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="16e05-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16e05-123">CommonParameters</span></span>
<span data-ttu-id="16e05-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="16e05-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16e05-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16e05-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16e05-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="16e05-126">INPUTS</span></span>

### <span data-ttu-id="16e05-127">System. String</span><span class="sxs-lookup"><span data-stu-id="16e05-127">System.String</span></span>

## <span data-ttu-id="16e05-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="16e05-128">OUTPUTS</span></span>

### <span data-ttu-id="16e05-129">Microsoft. Azure. Command. StreamAnalytics. models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="16e05-129">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="16e05-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="16e05-130">NOTES</span></span>

## <span data-ttu-id="16e05-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="16e05-131">RELATED LINKS</span></span>

[<span data-ttu-id="16e05-132">Új – AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="16e05-132">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="16e05-133">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="16e05-133">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="16e05-134">Teszt-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="16e05-134">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)


