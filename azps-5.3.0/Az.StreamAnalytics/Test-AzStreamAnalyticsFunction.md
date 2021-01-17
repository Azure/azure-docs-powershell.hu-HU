---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 1f2c7e653e96f697a714fef9f7b56c70240f0456
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479330"
---
# <span data-ttu-id="427d1-101">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="427d1-101">Test-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="427d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="427d1-102">SYNOPSIS</span></span>
<span data-ttu-id="427d1-103">Azt teszteli, hogy a Stream Analytics tud-e függvényhez csatlakozni.</span><span class="sxs-lookup"><span data-stu-id="427d1-103">Tests whether Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="427d1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="427d1-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="427d1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="427d1-105">DESCRIPTION</span></span>
<span data-ttu-id="427d1-106">A **Test-AzStreamAnalyticsFunction** parancsmag teszteli, hogy az Azure Stream Analytics képes-e csatlakozni egy függvényhez.</span><span class="sxs-lookup"><span data-stu-id="427d1-106">The **Test-AzStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="427d1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="427d1-107">EXAMPLES</span></span>

### <span data-ttu-id="427d1-108">1. példa: Stream Analytics függvény tesztelése</span><span class="sxs-lookup"><span data-stu-id="427d1-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="427d1-109">Ez a parancs teszteli a ScoreTweet nevű függvény kapcsolati állapotát a Stream Job22 nevű feladatban.</span><span class="sxs-lookup"><span data-stu-id="427d1-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="427d1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="427d1-110">PARAMETERS</span></span>

### <span data-ttu-id="427d1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="427d1-111">-DefaultProfile</span></span>
<span data-ttu-id="427d1-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="427d1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="427d1-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="427d1-113">-JobName</span></span>
<span data-ttu-id="427d1-114">Annak a Stream Analytics-feladatnak a nevét adja meg, amelyhez egy függvény tartozik.</span><span class="sxs-lookup"><span data-stu-id="427d1-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="427d1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="427d1-115">-Name</span></span>
<span data-ttu-id="427d1-116">A parancsmag által tesztelett Stream Analytics függvény neve.</span><span class="sxs-lookup"><span data-stu-id="427d1-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

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

### <span data-ttu-id="427d1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="427d1-117">-ResourceGroupName</span></span>
<span data-ttu-id="427d1-118">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a Stream Analytics függvény tartozik.</span><span class="sxs-lookup"><span data-stu-id="427d1-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="427d1-119">Ez a parancsmag a paraméter által megadott erőforráscsoport egyik függvényét teszteli.</span><span class="sxs-lookup"><span data-stu-id="427d1-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="427d1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="427d1-120">CommonParameters</span></span>
<span data-ttu-id="427d1-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="427d1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="427d1-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="427d1-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="427d1-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="427d1-123">INPUTS</span></span>

### <span data-ttu-id="427d1-124">System.String</span><span class="sxs-lookup"><span data-stu-id="427d1-124">System.String</span></span>

## <span data-ttu-id="427d1-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="427d1-125">OUTPUTS</span></span>

### <span data-ttu-id="427d1-126">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="427d1-126">System.Boolean</span></span>

## <span data-ttu-id="427d1-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="427d1-127">NOTES</span></span>

## <span data-ttu-id="427d1-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="427d1-128">RELATED LINKS</span></span>

[<span data-ttu-id="427d1-129">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="427d1-129">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="427d1-130">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="427d1-130">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="427d1-131">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="427d1-131">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)


