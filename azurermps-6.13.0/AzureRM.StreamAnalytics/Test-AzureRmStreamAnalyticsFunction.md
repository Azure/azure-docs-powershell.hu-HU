---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/test-azurermstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: c62d829da193ae36f10a64149260cf34c6bc20ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502815"
---
# <span data-ttu-id="6cf86-101">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="6cf86-101">Test-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="6cf86-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6cf86-102">SYNOPSIS</span></span>
<span data-ttu-id="6cf86-103">Annak vizsgálata, hogy az adatfolyam-elemzés csatlakozhat-e egy függvényhez.</span><span class="sxs-lookup"><span data-stu-id="6cf86-103">Tests whether Stream Analytics can connect to a function.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cf86-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6cf86-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cf86-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6cf86-105">DESCRIPTION</span></span>
<span data-ttu-id="6cf86-106">A **AzureRmStreamAnalyticsFunction-** parancsmag azt vizsgálja, hogy az Azure stream Analytics tud-e csatlakozni egy függvényhez.</span><span class="sxs-lookup"><span data-stu-id="6cf86-106">The **Test-AzureRmStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="6cf86-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6cf86-107">EXAMPLES</span></span>

### <span data-ttu-id="6cf86-108">Példa 1: stream-Analytics függvény tesztelése</span><span class="sxs-lookup"><span data-stu-id="6cf86-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="6cf86-109">Ez a parancs a ScoreTweet nevű függvény kapcsolati állapotát teszteli a StreamJob22 nevű feladatban.</span><span class="sxs-lookup"><span data-stu-id="6cf86-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="6cf86-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6cf86-110">PARAMETERS</span></span>

### <span data-ttu-id="6cf86-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cf86-111">-DefaultProfile</span></span>
<span data-ttu-id="6cf86-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6cf86-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cf86-113">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="6cf86-113">-JobName</span></span>
<span data-ttu-id="6cf86-114">Annak az adatfolyam-elemzési feladatnak a neve, amelyhez egy függvény tartozik.</span><span class="sxs-lookup"><span data-stu-id="6cf86-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="6cf86-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6cf86-115">-Name</span></span>
<span data-ttu-id="6cf86-116">Annak az adatfolyam-elemzési függvénynek a nevét adja meg, amelyet a parancsmag tesztel.</span><span class="sxs-lookup"><span data-stu-id="6cf86-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cf86-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cf86-117">-ResourceGroupName</span></span>
<span data-ttu-id="6cf86-118">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez az adatfolyam-elemzés függvény tartozik.</span><span class="sxs-lookup"><span data-stu-id="6cf86-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="6cf86-119">Ez a parancsmag egy olyan függvényt tesztel az erőforráscsoportben, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cf86-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6cf86-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cf86-120">CommonParameters</span></span>
<span data-ttu-id="6cf86-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6cf86-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cf86-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cf86-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cf86-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cf86-123">INPUTS</span></span>

### <span data-ttu-id="6cf86-124">System. String</span><span class="sxs-lookup"><span data-stu-id="6cf86-124">System.String</span></span>

## <span data-ttu-id="6cf86-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cf86-125">OUTPUTS</span></span>

### <span data-ttu-id="6cf86-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6cf86-126">System.Boolean</span></span>

## <span data-ttu-id="6cf86-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6cf86-127">NOTES</span></span>

## <span data-ttu-id="6cf86-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6cf86-128">RELATED LINKS</span></span>

[<span data-ttu-id="6cf86-129">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="6cf86-129">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="6cf86-130">Új – AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="6cf86-130">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="6cf86-131">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="6cf86-131">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)

