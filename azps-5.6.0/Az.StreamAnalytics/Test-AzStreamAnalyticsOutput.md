---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/test-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 28a595b3e63a01439417ed07f6fd47c1cfc40a79
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933594"
---
# <span data-ttu-id="5e7e0-101">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="5e7e0-101">Test-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="5e7e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e7e0-102">SYNOPSIS</span></span>
<span data-ttu-id="5e7e0-103">Egy kimenet kapcsolati állapotát teszteli.</span><span class="sxs-lookup"><span data-stu-id="5e7e0-103">Tests the connection status of an output.</span></span>

## <span data-ttu-id="5e7e0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5e7e0-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e7e0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5e7e0-105">DESCRIPTION</span></span>
<span data-ttu-id="5e7e0-106">A **Test-AzStreamAnalyticsOutput** parancsmag teszteli, hogy a Stream Analytics képes-e csatlakozni egy kimenethez.</span><span class="sxs-lookup"><span data-stu-id="5e7e0-106">The **Test-AzStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="5e7e0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5e7e0-107">EXAMPLES</span></span>

### <span data-ttu-id="5e7e0-108">1. példa: Kimenet kapcsolati állapotának tesztelése</span><span class="sxs-lookup"><span data-stu-id="5e7e0-108">Example 1: Test the connection status of an output</span></span>
```powershell
PS C:\>Test-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="5e7e0-109">Ez teszteli a kimenet kapcsolati állapotát a Streaming Streaming Streamingben.</span><span class="sxs-lookup"><span data-stu-id="5e7e0-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="5e7e0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e7e0-110">PARAMETERS</span></span>

### <span data-ttu-id="5e7e0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e7e0-111">-DefaultProfile</span></span>
<span data-ttu-id="5e7e0-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5e7e0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e7e0-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="5e7e0-113">-JobName</span></span>
<span data-ttu-id="5e7e0-114">Megadja annak az Azure Stream Analytics-feladatnak a nevét, amelyhez a kívánt Azure Stream Analytics-kimenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="5e7e0-114">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="5e7e0-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5e7e0-115">-Name</span></span>
<span data-ttu-id="5e7e0-116">A tesztelni megfelelő Azure Stream Analytics-kimenet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5e7e0-116">Specifies the name of the Azure Stream Analytics output to test.</span></span>

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

### <span data-ttu-id="5e7e0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e7e0-117">-ResourceGroupName</span></span>
<span data-ttu-id="5e7e0-118">Annak az erőforráscsoportnak a nevét adja meg, amelyhez az Azure Stream Analytics kimenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="5e7e0-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="5e7e0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e7e0-119">CommonParameters</span></span>
<span data-ttu-id="5e7e0-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e7e0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e7e0-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e7e0-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e7e0-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5e7e0-122">INPUTS</span></span>

### <span data-ttu-id="5e7e0-123">System.String</span><span class="sxs-lookup"><span data-stu-id="5e7e0-123">System.String</span></span>

## <span data-ttu-id="5e7e0-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e7e0-124">OUTPUTS</span></span>

### <span data-ttu-id="5e7e0-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5e7e0-125">System.Boolean</span></span>

## <span data-ttu-id="5e7e0-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5e7e0-126">NOTES</span></span>

## <span data-ttu-id="5e7e0-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5e7e0-127">RELATED LINKS</span></span>

[<span data-ttu-id="5e7e0-128">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="5e7e0-128">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="5e7e0-129">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="5e7e0-129">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="5e7e0-130">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="5e7e0-130">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)


