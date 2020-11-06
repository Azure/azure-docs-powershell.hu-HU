---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 79EB2AD9-BFE1-49BE-870F-7DFC99D6FE17
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: 6b05bb1d379a5d9072cc286505a507d3718aa33e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495510"
---
# <span data-ttu-id="9fd82-101">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="9fd82-101">New-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="9fd82-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9fd82-102">SYNOPSIS</span></span>
<span data-ttu-id="9fd82-103">Az adatfolyam-elemzési feladatok függvényének létrehozása vagy cseréje.</span><span class="sxs-lookup"><span data-stu-id="9fd82-103">Creates or replaces a function in a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fd82-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9fd82-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9fd82-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9fd82-105">DESCRIPTION</span></span>
<span data-ttu-id="9fd82-106">A **New-AzureRmStreamAnalyticsFunction** parancsmag létrehoz egy függvényt egy Azure stream Analytics-munkahelyen, vagy lecserél egy meglévő függvényt.</span><span class="sxs-lookup"><span data-stu-id="9fd82-106">The **New-AzureRmStreamAnalyticsFunction** cmdlet creates a function in an Azure Stream Analytics job or replaces an existing function.</span></span>
<span data-ttu-id="9fd82-107">Definiálja a függvényt egy JavaScript-objektum megjelölése (JSON) fájlban.</span><span class="sxs-lookup"><span data-stu-id="9fd82-107">Define the function in a JavaScript Object Notation (JSON) file.</span></span>

<span data-ttu-id="9fd82-108">A függvény nevét a *Name* vagy a. JSON fájlban adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="9fd82-108">You can specify the name of the function by using the *Name* parameter or in the .json file.</span></span>
<span data-ttu-id="9fd82-109">Ha mindkét módon adja meg a nevet, a névnek egyeznie kell.</span><span class="sxs-lookup"><span data-stu-id="9fd82-109">If you specify the name in both ways, the names must match.</span></span>

<span data-ttu-id="9fd82-110">Meglévő függvény lecseréléséhez adja meg a meglévő függvény nevét.</span><span class="sxs-lookup"><span data-stu-id="9fd82-110">To replace an existing function, specify the name of the existing function.</span></span>

## <span data-ttu-id="9fd82-111">Példák</span><span class="sxs-lookup"><span data-stu-id="9fd82-111">EXAMPLES</span></span>

### <span data-ttu-id="9fd82-112">Példa 1: stream-Analytics-függvény létrehozása</span><span class="sxs-lookup"><span data-stu-id="9fd82-112">Example 1: Create a Stream Analytics function</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob07" -File "C:\Function07.json"
```

<span data-ttu-id="9fd82-113">A parancs a fájl Function07.jsból hoz létre függvényt.</span><span class="sxs-lookup"><span data-stu-id="9fd82-113">This command creates a function from the file Function07.json.</span></span>
<span data-ttu-id="9fd82-114">A függvény neve megtalálható a. JSON fájlban.</span><span class="sxs-lookup"><span data-stu-id="9fd82-114">The name of the function is stored in the .json file.</span></span>

### <span data-ttu-id="9fd82-115">2. példa: ScoreTweet nevű adatfolyam-elemzési függvény létrehozása</span><span class="sxs-lookup"><span data-stu-id="9fd82-115">Example 2: Create a Stream Analytics function named ScoreTweet</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet"
```

<span data-ttu-id="9fd82-116">Ez a parancs létrehoz egy függvényt a ScoreTweet nevű feladathoz.</span><span class="sxs-lookup"><span data-stu-id="9fd82-116">This command creates a function on the job named ScoreTweet.</span></span>

### <span data-ttu-id="9fd82-117">3. példa: stream-Analytics függvény cseréje</span><span class="sxs-lookup"><span data-stu-id="9fd82-117">Example 3: Replace a Stream Analytics function</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet" -Force
```

<span data-ttu-id="9fd82-118">Ez a parancs felülírja a ScoreTweet nevű meglévő függvény definícióját, és a meghatározást Function22.jsbe értékre.</span><span class="sxs-lookup"><span data-stu-id="9fd82-118">This command replaces the definition of the existing function named ScoreTweet with the definition in Function22.json.</span></span>

## <span data-ttu-id="9fd82-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9fd82-119">PARAMETERS</span></span>

### <span data-ttu-id="9fd82-120">-Fájl</span><span class="sxs-lookup"><span data-stu-id="9fd82-120">-File</span></span>
<span data-ttu-id="9fd82-121">Annak a. JSON fájlnak az elérési útját adja meg, amely az adatfolyam-elemzés függvény JSON-adatábrázolását tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="9fd82-121">Specifies the path of a .json file that contains the JSON representation of the Stream Analytics function.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fd82-122">-Force</span><span class="sxs-lookup"><span data-stu-id="9fd82-122">-Force</span></span>
<span data-ttu-id="9fd82-123">Jelzi, hogy ez a parancsmag egy meglévő adatfolyam-elemzési függvényt cserél le anélkül, hogy megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9fd82-123">Indicates that this cmdlet replaces an existing Stream Analytics function without prompting you for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fd82-124">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="9fd82-124">-JobName</span></span>
<span data-ttu-id="9fd82-125">Annak az adatfolyam-elemzési feladatnak a nevét adja meg, amelyben ez a parancsmag adatfolyam-elemzési függvényt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9fd82-125">Specifies the name of the Stream Analytics job under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="9fd82-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9fd82-126">-Name</span></span>
<span data-ttu-id="9fd82-127">A parancsmag által létrehozott stream-Analytics függvény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fd82-127">Specifies the name of the Stream Analytics function that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fd82-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fd82-128">-ResourceGroupName</span></span>
<span data-ttu-id="9fd82-129">Annak az erőforrás-csoportnak a nevét adja meg, amelyben ez a parancsmag adatfolyam-elemzési függvényt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9fd82-129">Specifies the name of the resource group under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="9fd82-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9fd82-130">-Confirm</span></span>
<span data-ttu-id="9fd82-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9fd82-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fd82-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fd82-132">-WhatIf</span></span>
<span data-ttu-id="9fd82-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9fd82-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fd82-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9fd82-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fd82-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fd82-135">-DefaultProfile</span></span>
<span data-ttu-id="9fd82-136">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9fd82-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fd82-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fd82-137">CommonParameters</span></span>
<span data-ttu-id="9fd82-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9fd82-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fd82-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fd82-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fd82-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9fd82-140">INPUTS</span></span>

## <span data-ttu-id="9fd82-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9fd82-141">OUTPUTS</span></span>

### <span data-ttu-id="9fd82-142">Microsoft. Azure. Command. StreamAnalytics. models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="9fd82-142">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="9fd82-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9fd82-143">NOTES</span></span>

## <span data-ttu-id="9fd82-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9fd82-144">RELATED LINKS</span></span>

[<span data-ttu-id="9fd82-145">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="9fd82-145">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="9fd82-146">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="9fd82-146">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="9fd82-147">Teszt-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="9fd82-147">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)


