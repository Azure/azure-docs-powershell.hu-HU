---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 1f2c7e653e96f697a714fef9f7b56c70240f0456
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302880"
---
# <span data-ttu-id="1ca84-101">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="1ca84-101">Test-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="1ca84-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1ca84-102">SYNOPSIS</span></span>
<span data-ttu-id="1ca84-103">Annak vizsgálata, hogy az adatfolyam-elemzés csatlakozhat-e egy függvényhez.</span><span class="sxs-lookup"><span data-stu-id="1ca84-103">Tests whether Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="1ca84-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1ca84-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ca84-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1ca84-105">DESCRIPTION</span></span>
<span data-ttu-id="1ca84-106">A **AzStreamAnalyticsFunction-** parancsmag azt vizsgálja, hogy az Azure stream Analytics tud-e csatlakozni egy függvényhez.</span><span class="sxs-lookup"><span data-stu-id="1ca84-106">The **Test-AzStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="1ca84-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1ca84-107">EXAMPLES</span></span>

### <span data-ttu-id="1ca84-108">Példa 1: stream-Analytics függvény tesztelése</span><span class="sxs-lookup"><span data-stu-id="1ca84-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="1ca84-109">Ez a parancs a ScoreTweet nevű függvény kapcsolati állapotát teszteli a StreamJob22 nevű feladatban.</span><span class="sxs-lookup"><span data-stu-id="1ca84-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="1ca84-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1ca84-110">PARAMETERS</span></span>

### <span data-ttu-id="1ca84-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ca84-111">-DefaultProfile</span></span>
<span data-ttu-id="1ca84-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1ca84-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ca84-113">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="1ca84-113">-JobName</span></span>
<span data-ttu-id="1ca84-114">Annak az adatfolyam-elemzési feladatnak a neve, amelyhez egy függvény tartozik.</span><span class="sxs-lookup"><span data-stu-id="1ca84-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="1ca84-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1ca84-115">-Name</span></span>
<span data-ttu-id="1ca84-116">Annak az adatfolyam-elemzési függvénynek a nevét adja meg, amelyet a parancsmag tesztel.</span><span class="sxs-lookup"><span data-stu-id="1ca84-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

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

### <span data-ttu-id="1ca84-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ca84-117">-ResourceGroupName</span></span>
<span data-ttu-id="1ca84-118">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez az adatfolyam-elemzés függvény tartozik.</span><span class="sxs-lookup"><span data-stu-id="1ca84-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="1ca84-119">Ez a parancsmag egy olyan függvényt tesztel az erőforráscsoportben, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ca84-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1ca84-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ca84-120">CommonParameters</span></span>
<span data-ttu-id="1ca84-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1ca84-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ca84-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ca84-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ca84-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ca84-123">INPUTS</span></span>

### <span data-ttu-id="1ca84-124">System. String</span><span class="sxs-lookup"><span data-stu-id="1ca84-124">System.String</span></span>

## <span data-ttu-id="1ca84-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ca84-125">OUTPUTS</span></span>

### <span data-ttu-id="1ca84-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1ca84-126">System.Boolean</span></span>

## <span data-ttu-id="1ca84-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1ca84-127">NOTES</span></span>

## <span data-ttu-id="1ca84-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ca84-128">RELATED LINKS</span></span>

[<span data-ttu-id="1ca84-129">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="1ca84-129">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="1ca84-130">Új – AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="1ca84-130">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="1ca84-131">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="1ca84-131">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)


