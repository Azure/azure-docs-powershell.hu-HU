---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 69e9d06a790fa473a278e50e79ad90be93f0527c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150122"
---
# <span data-ttu-id="d2006-101">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="d2006-101">Test-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="d2006-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2006-102">SYNOPSIS</span></span>
<span data-ttu-id="d2006-103">Egy kimenet kapcsolati állapotát teszteli.</span><span class="sxs-lookup"><span data-stu-id="d2006-103">Tests the connection status of an output.</span></span>

## <span data-ttu-id="d2006-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d2006-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2006-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d2006-105">DESCRIPTION</span></span>
<span data-ttu-id="d2006-106">A **Test-AzStreamAnalyticsOutput** parancsmag teszteli, hogy a Stream Analytics képes-e csatlakozni egy kimenethez.</span><span class="sxs-lookup"><span data-stu-id="d2006-106">The **Test-AzStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="d2006-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d2006-107">EXAMPLES</span></span>

### <span data-ttu-id="d2006-108">1. példa: Kimenet kapcsolati állapotának tesztelése</span><span class="sxs-lookup"><span data-stu-id="d2006-108">Example 1: Test the connection status of an output</span></span>
```powershell
PS C:\>Test-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="d2006-109">Ez teszteli a Stream Streaming Streaming kimeneti kimenetének kapcsolati állapotát.</span><span class="sxs-lookup"><span data-stu-id="d2006-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="d2006-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2006-110">PARAMETERS</span></span>

### <span data-ttu-id="d2006-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2006-111">-DefaultProfile</span></span>
<span data-ttu-id="d2006-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d2006-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2006-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="d2006-113">-JobName</span></span>
<span data-ttu-id="d2006-114">Annak az Azure Stream Analytics-feladatnak a neve, amelyhez a kívánt Azure Stream Analytics-kimenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="d2006-114">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="d2006-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d2006-115">-Name</span></span>
<span data-ttu-id="d2006-116">A tesztelni megfelelő Azure Stream Analytics-kimenet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d2006-116">Specifies the name of the Azure Stream Analytics output to test.</span></span>

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

### <span data-ttu-id="d2006-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2006-117">-ResourceGroupName</span></span>
<span data-ttu-id="d2006-118">Annak az erőforráscsoportnak a neve, amelyhez az Azure Stream Analytics kimenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="d2006-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="d2006-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2006-119">CommonParameters</span></span>
<span data-ttu-id="d2006-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2006-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2006-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2006-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2006-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2006-122">INPUTS</span></span>

### <span data-ttu-id="d2006-123">System.String</span><span class="sxs-lookup"><span data-stu-id="d2006-123">System.String</span></span>

## <span data-ttu-id="d2006-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2006-124">OUTPUTS</span></span>

### <span data-ttu-id="d2006-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d2006-125">System.Boolean</span></span>

## <span data-ttu-id="d2006-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d2006-126">NOTES</span></span>

## <span data-ttu-id="d2006-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d2006-127">RELATED LINKS</span></span>

[<span data-ttu-id="d2006-128">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="d2006-128">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="d2006-129">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="d2006-129">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="d2006-130">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="d2006-130">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)


