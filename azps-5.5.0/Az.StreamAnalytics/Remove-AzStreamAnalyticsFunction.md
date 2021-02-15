---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 75B0776E-32D5-4EE4-B35C-73E13185A4F1
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
ms.openlocfilehash: d481cf5ba28a87e098691d4b3fa5c179670d881d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150186"
---
# <span data-ttu-id="b60dc-101">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="b60dc-101">Remove-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="b60dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b60dc-102">SYNOPSIS</span></span>
<span data-ttu-id="b60dc-103">Egy függvény törlése egy Stream Analytics-feladatból.</span><span class="sxs-lookup"><span data-stu-id="b60dc-103">Deletes a function from a Stream Analytics job.</span></span>

## <span data-ttu-id="b60dc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b60dc-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b60dc-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b60dc-105">DESCRIPTION</span></span>
<span data-ttu-id="b60dc-106">A **Remove-AzStreamAnalyticsFunction** parancsmag aszinkron módon töröl egy függvényt az Azure Stream Analytics-feladatból.</span><span class="sxs-lookup"><span data-stu-id="b60dc-106">The **Remove-AzStreamAnalyticsFunction** cmdlet deletes a function asynchronously from an Azure Stream Analytics job.</span></span>

## <span data-ttu-id="b60dc-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b60dc-107">EXAMPLES</span></span>

### <span data-ttu-id="b60dc-108">1. példa: Stream Analytics függvény eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b60dc-108">Example 1: Remove a Stream Analytics function</span></span>
```
PS C:\>Remove-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="b60dc-109">Ez a parancs eltávolítja a ScoreTweet nevű függvényt a Stream Job22 nevű feladatból.</span><span class="sxs-lookup"><span data-stu-id="b60dc-109">This command removes the function named ScoreTweet from the job named StreamJob22.</span></span>

## <span data-ttu-id="b60dc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b60dc-110">PARAMETERS</span></span>

### <span data-ttu-id="b60dc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b60dc-111">-DefaultProfile</span></span>
<span data-ttu-id="b60dc-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b60dc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b60dc-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="b60dc-113">-JobName</span></span>
<span data-ttu-id="b60dc-114">Annak a Stream Analytics-feladatnak a nevét adja meg, amelyhez egy függvény tartozik.</span><span class="sxs-lookup"><span data-stu-id="b60dc-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>
<span data-ttu-id="b60dc-115">Ez a parancsmag eltávolít egy függvényt a paraméter által megadott feladatból.</span><span class="sxs-lookup"><span data-stu-id="b60dc-115">This cmdlet removes a function from the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="b60dc-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b60dc-116">-Name</span></span>
<span data-ttu-id="b60dc-117">A parancsmag által eltávolított Stream Analytics függvény neve.</span><span class="sxs-lookup"><span data-stu-id="b60dc-117">Specifies the name of the Stream Analytics function that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b60dc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b60dc-118">-ResourceGroupName</span></span>
<span data-ttu-id="b60dc-119">Annak az erőforráscsoportnak a nevét adja meg, amelyhez egy Stream Analytics függvény tartozik.</span><span class="sxs-lookup"><span data-stu-id="b60dc-119">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="b60dc-120">Ez a parancsmag törli a paraméter által megadott erőforráscsoport egyik függvényét.</span><span class="sxs-lookup"><span data-stu-id="b60dc-120">This cmdlet deletes a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b60dc-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b60dc-121">-Confirm</span></span>
<span data-ttu-id="b60dc-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b60dc-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b60dc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b60dc-123">-WhatIf</span></span>
<span data-ttu-id="b60dc-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b60dc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b60dc-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b60dc-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b60dc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b60dc-126">CommonParameters</span></span>
<span data-ttu-id="b60dc-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b60dc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b60dc-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b60dc-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b60dc-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b60dc-129">INPUTS</span></span>

### <span data-ttu-id="b60dc-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b60dc-130">System.String</span></span>

## <span data-ttu-id="b60dc-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b60dc-131">OUTPUTS</span></span>

### <span data-ttu-id="b60dc-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b60dc-132">System.Boolean</span></span>

## <span data-ttu-id="b60dc-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b60dc-133">NOTES</span></span>

## <span data-ttu-id="b60dc-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b60dc-134">RELATED LINKS</span></span>

[<span data-ttu-id="b60dc-135">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="b60dc-135">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="b60dc-136">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="b60dc-136">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="b60dc-137">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="b60dc-137">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


