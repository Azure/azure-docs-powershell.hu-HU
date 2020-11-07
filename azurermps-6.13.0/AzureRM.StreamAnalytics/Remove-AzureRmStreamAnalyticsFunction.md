---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 75B0776E-32D5-4EE4-B35C-73E13185A4F1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: 4429142b19e64939b9fcc90d56c80f67c5296c15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672712"
---
# <span data-ttu-id="e4850-101">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="e4850-101">Remove-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="e4850-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e4850-102">SYNOPSIS</span></span>
<span data-ttu-id="e4850-103">Az adatfolyam-elemzési feladatokből származó függvény törlése</span><span class="sxs-lookup"><span data-stu-id="e4850-103">Deletes a function from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4850-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e4850-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4850-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e4850-105">DESCRIPTION</span></span>
<span data-ttu-id="e4850-106">A **Remove-AzureRmStreamAnalyticsFunction** parancsmag az Azure stream Analytics-feladatokból aszinkron függvényt töröl.</span><span class="sxs-lookup"><span data-stu-id="e4850-106">The **Remove-AzureRmStreamAnalyticsFunction** cmdlet deletes a function asynchronously from an Azure Stream Analytics job.</span></span>

## <span data-ttu-id="e4850-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e4850-107">EXAMPLES</span></span>

### <span data-ttu-id="e4850-108">1. példa: az adatfolyam-elemzés függvény eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e4850-108">Example 1: Remove a Stream Analytics function</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="e4850-109">Ez a parancs eltávolítja a ScoreTweet nevű függvényt a StreamJob22 nevű feladatból.</span><span class="sxs-lookup"><span data-stu-id="e4850-109">This command removes the function named ScoreTweet from the job named StreamJob22.</span></span>

## <span data-ttu-id="e4850-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e4850-110">PARAMETERS</span></span>

### <span data-ttu-id="e4850-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4850-111">-DefaultProfile</span></span>
<span data-ttu-id="e4850-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e4850-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4850-113">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="e4850-113">-JobName</span></span>
<span data-ttu-id="e4850-114">Annak az adatfolyam-elemzési feladatnak a neve, amelyhez egy függvény tartozik.</span><span class="sxs-lookup"><span data-stu-id="e4850-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>
<span data-ttu-id="e4850-115">Ez a parancsmag egy olyan függvényt távolít el a projektből, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="e4850-115">This cmdlet removes a function from the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="e4850-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e4850-116">-Name</span></span>
<span data-ttu-id="e4850-117">A parancsmag által eltávolított stream-Analytics függvény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4850-117">Specifies the name of the Stream Analytics function that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e4850-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4850-118">-ResourceGroupName</span></span>
<span data-ttu-id="e4850-119">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez az adatfolyam-elemzés függvény tartozik.</span><span class="sxs-lookup"><span data-stu-id="e4850-119">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="e4850-120">Ez a parancsmag törli a függvényt abban az erőforráscsoport-csoportban, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4850-120">This cmdlet deletes a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e4850-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e4850-121">-Confirm</span></span>
<span data-ttu-id="e4850-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e4850-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4850-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4850-123">-WhatIf</span></span>
<span data-ttu-id="e4850-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e4850-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4850-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e4850-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4850-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4850-126">CommonParameters</span></span>
<span data-ttu-id="e4850-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e4850-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4850-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4850-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4850-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4850-129">INPUTS</span></span>

### <span data-ttu-id="e4850-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e4850-130">System.String</span></span>

## <span data-ttu-id="e4850-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4850-131">OUTPUTS</span></span>

### <span data-ttu-id="e4850-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e4850-132">System.Boolean</span></span>

## <span data-ttu-id="e4850-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e4850-133">NOTES</span></span>

## <span data-ttu-id="e4850-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4850-134">RELATED LINKS</span></span>

[<span data-ttu-id="e4850-135">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="e4850-135">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="e4850-136">Új – AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="e4850-136">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="e4850-137">Teszt-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="e4850-137">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)


