---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: a2f577286a411287886c27863eb72e574b771bd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673088"
---
# <span data-ttu-id="a7587-101">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="a7587-101">Test-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="a7587-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a7587-102">SYNOPSIS</span></span>
<span data-ttu-id="a7587-103">Annak vizsgálata, hogy az adatfolyam-elemzés csatlakozhat-e egy függvényhez.</span><span class="sxs-lookup"><span data-stu-id="a7587-103">Tests whether Stream Analytics can connect to a function.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7587-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a7587-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7587-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a7587-105">DESCRIPTION</span></span>
<span data-ttu-id="a7587-106">A **AzureRmStreamAnalyticsFunction-** parancsmag azt vizsgálja, hogy az Azure stream Analytics tud-e csatlakozni egy függvényhez.</span><span class="sxs-lookup"><span data-stu-id="a7587-106">The **Test-AzureRmStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="a7587-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a7587-107">EXAMPLES</span></span>

### <span data-ttu-id="a7587-108">Példa 1: stream-Analytics függvény tesztelése</span><span class="sxs-lookup"><span data-stu-id="a7587-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="a7587-109">Ez a parancs a ScoreTweet nevű függvény kapcsolati állapotát teszteli a StreamJob22 nevű feladatban.</span><span class="sxs-lookup"><span data-stu-id="a7587-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="a7587-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a7587-110">PARAMETERS</span></span>

### <span data-ttu-id="a7587-111">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="a7587-111">-JobName</span></span>
<span data-ttu-id="a7587-112">Annak az adatfolyam-elemzési feladatnak a neve, amelyhez egy függvény tartozik.</span><span class="sxs-lookup"><span data-stu-id="a7587-112">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="a7587-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a7587-113">-Name</span></span>
<span data-ttu-id="a7587-114">Annak az adatfolyam-elemzési függvénynek a nevét adja meg, amelyet a parancsmag tesztel.</span><span class="sxs-lookup"><span data-stu-id="a7587-114">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

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

### <span data-ttu-id="a7587-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7587-115">-ResourceGroupName</span></span>
<span data-ttu-id="a7587-116">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez az adatfolyam-elemzés függvény tartozik.</span><span class="sxs-lookup"><span data-stu-id="a7587-116">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="a7587-117">Ez a parancsmag egy olyan függvényt tesztel az erőforráscsoportben, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="a7587-117">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a7587-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7587-118">-DefaultProfile</span></span>
<span data-ttu-id="a7587-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a7587-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7587-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7587-120">CommonParameters</span></span>
<span data-ttu-id="a7587-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a7587-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7587-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7587-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7587-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7587-123">INPUTS</span></span>

## <span data-ttu-id="a7587-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7587-124">OUTPUTS</span></span>

### <span data-ttu-id="a7587-125">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="a7587-125">System.Object</span></span>

## <span data-ttu-id="a7587-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a7587-126">NOTES</span></span>

## <span data-ttu-id="a7587-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a7587-127">RELATED LINKS</span></span>

[<span data-ttu-id="a7587-128">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="a7587-128">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="a7587-129">Új – AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="a7587-129">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="a7587-130">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="a7587-130">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)


