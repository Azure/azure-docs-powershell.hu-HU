---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 75B0776E-32D5-4EE4-B35C-73E13185A4F1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: 10687094bcbbc6cc9a52e648d830d46eac089c4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503148"
---
# <span data-ttu-id="3d571-101">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="3d571-101">Remove-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="3d571-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3d571-102">SYNOPSIS</span></span>
<span data-ttu-id="3d571-103">Az adatfolyam-elemzési feladatokből származó függvény törlése</span><span class="sxs-lookup"><span data-stu-id="3d571-103">Deletes a function from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d571-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3d571-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d571-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3d571-105">DESCRIPTION</span></span>
<span data-ttu-id="3d571-106">A **Remove-AzureRmStreamAnalyticsFunction** parancsmag az Azure stream Analytics-feladatokból aszinkron függvényt töröl.</span><span class="sxs-lookup"><span data-stu-id="3d571-106">The **Remove-AzureRmStreamAnalyticsFunction** cmdlet deletes a function asynchronously from an Azure Stream Analytics job.</span></span>

## <span data-ttu-id="3d571-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3d571-107">EXAMPLES</span></span>

### <span data-ttu-id="3d571-108">1. példa: az adatfolyam-elemzés függvény eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3d571-108">Example 1: Remove a Stream Analytics function</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="3d571-109">Ez a parancs eltávolítja a ScoreTweet nevű függvényt a StreamJob22 nevű feladatból.</span><span class="sxs-lookup"><span data-stu-id="3d571-109">This command removes the function named ScoreTweet from the job named StreamJob22.</span></span>

## <span data-ttu-id="3d571-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3d571-110">PARAMETERS</span></span>

### <span data-ttu-id="3d571-111">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="3d571-111">-JobName</span></span>
<span data-ttu-id="3d571-112">Annak az adatfolyam-elemzési feladatnak a neve, amelyhez egy függvény tartozik.</span><span class="sxs-lookup"><span data-stu-id="3d571-112">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>
<span data-ttu-id="3d571-113">Ez a parancsmag egy olyan függvényt távolít el a projektből, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="3d571-113">This cmdlet removes a function from the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="3d571-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3d571-114">-Name</span></span>
<span data-ttu-id="3d571-115">A parancsmag által eltávolított stream-Analytics függvény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3d571-115">Specifies the name of the Stream Analytics function that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3d571-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d571-116">-ResourceGroupName</span></span>
<span data-ttu-id="3d571-117">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez az adatfolyam-elemzés függvény tartozik.</span><span class="sxs-lookup"><span data-stu-id="3d571-117">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="3d571-118">Ez a parancsmag törli a függvényt abban az erőforráscsoport-csoportban, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="3d571-118">This cmdlet deletes a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3d571-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3d571-119">-Confirm</span></span>
<span data-ttu-id="3d571-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3d571-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d571-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d571-121">-WhatIf</span></span>
<span data-ttu-id="3d571-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3d571-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d571-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3d571-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d571-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d571-124">-DefaultProfile</span></span>
<span data-ttu-id="3d571-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3d571-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d571-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d571-126">CommonParameters</span></span>
<span data-ttu-id="3d571-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3d571-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d571-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d571-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d571-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d571-129">INPUTS</span></span>

## <span data-ttu-id="3d571-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d571-130">OUTPUTS</span></span>

### <span data-ttu-id="3d571-131">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="3d571-131">System.Object</span></span>

## <span data-ttu-id="3d571-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3d571-132">NOTES</span></span>

## <span data-ttu-id="3d571-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3d571-133">RELATED LINKS</span></span>

[<span data-ttu-id="3d571-134">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="3d571-134">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="3d571-135">Új – AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="3d571-135">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="3d571-136">Teszt-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="3d571-136">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)


