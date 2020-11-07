---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 75B0776E-32D5-4EE4-B35C-73E13185A4F1
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
ms.openlocfilehash: bf5c869e8831fd37a10f9923d415a91f88fd0960
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839811"
---
# <span data-ttu-id="c5554-101">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="c5554-101">Remove-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="c5554-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c5554-102">SYNOPSIS</span></span>
<span data-ttu-id="c5554-103">Az adatfolyam-elemzési feladatokből származó függvény törlése</span><span class="sxs-lookup"><span data-stu-id="c5554-103">Deletes a function from a Stream Analytics job.</span></span>

## <span data-ttu-id="c5554-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c5554-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5554-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c5554-105">DESCRIPTION</span></span>
<span data-ttu-id="c5554-106">A **Remove-AzStreamAnalyticsFunction** parancsmag az Azure stream Analytics-feladatokból aszinkron függvényt töröl.</span><span class="sxs-lookup"><span data-stu-id="c5554-106">The **Remove-AzStreamAnalyticsFunction** cmdlet deletes a function asynchronously from an Azure Stream Analytics job.</span></span>

## <span data-ttu-id="c5554-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c5554-107">EXAMPLES</span></span>

### <span data-ttu-id="c5554-108">1. példa: az adatfolyam-elemzés függvény eltávolítása</span><span class="sxs-lookup"><span data-stu-id="c5554-108">Example 1: Remove a Stream Analytics function</span></span>
```
PS C:\>Remove-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="c5554-109">Ez a parancs eltávolítja a ScoreTweet nevű függvényt a StreamJob22 nevű feladatból.</span><span class="sxs-lookup"><span data-stu-id="c5554-109">This command removes the function named ScoreTweet from the job named StreamJob22.</span></span>

## <span data-ttu-id="c5554-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c5554-110">PARAMETERS</span></span>

### <span data-ttu-id="c5554-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5554-111">-DefaultProfile</span></span>
<span data-ttu-id="c5554-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c5554-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5554-113">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="c5554-113">-JobName</span></span>
<span data-ttu-id="c5554-114">Annak az adatfolyam-elemzési feladatnak a neve, amelyhez egy függvény tartozik.</span><span class="sxs-lookup"><span data-stu-id="c5554-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>
<span data-ttu-id="c5554-115">Ez a parancsmag egy olyan függvényt távolít el a projektből, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="c5554-115">This cmdlet removes a function from the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="c5554-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c5554-116">-Name</span></span>
<span data-ttu-id="c5554-117">A parancsmag által eltávolított stream-Analytics függvény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5554-117">Specifies the name of the Stream Analytics function that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c5554-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5554-118">-ResourceGroupName</span></span>
<span data-ttu-id="c5554-119">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez az adatfolyam-elemzés függvény tartozik.</span><span class="sxs-lookup"><span data-stu-id="c5554-119">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="c5554-120">Ez a parancsmag törli a függvényt abban az erőforráscsoport-csoportban, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5554-120">This cmdlet deletes a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c5554-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c5554-121">-Confirm</span></span>
<span data-ttu-id="c5554-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c5554-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5554-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5554-123">-WhatIf</span></span>
<span data-ttu-id="c5554-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c5554-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5554-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c5554-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5554-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5554-126">CommonParameters</span></span>
<span data-ttu-id="c5554-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c5554-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5554-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5554-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5554-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5554-129">INPUTS</span></span>

### <span data-ttu-id="c5554-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c5554-130">System.String</span></span>

## <span data-ttu-id="c5554-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5554-131">OUTPUTS</span></span>

### <span data-ttu-id="c5554-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c5554-132">System.Boolean</span></span>

## <span data-ttu-id="c5554-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c5554-133">NOTES</span></span>

## <span data-ttu-id="c5554-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5554-134">RELATED LINKS</span></span>

[<span data-ttu-id="c5554-135">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="c5554-135">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="c5554-136">Új – AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="c5554-136">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="c5554-137">Teszt-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="c5554-137">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


