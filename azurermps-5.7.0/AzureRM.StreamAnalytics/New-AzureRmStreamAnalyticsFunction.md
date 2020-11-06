---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 79EB2AD9-BFE1-49BE-870F-7DFC99D6FE17
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/new-azurermstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: 0351a7b139b8bf68f8d7154b65949c1cdda4bbdd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498675"
---
# <span data-ttu-id="26f54-101">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="26f54-101">New-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="26f54-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="26f54-102">SYNOPSIS</span></span>
<span data-ttu-id="26f54-103">Az adatfolyam-elemzési feladatok függvényének létrehozása vagy cseréje.</span><span class="sxs-lookup"><span data-stu-id="26f54-103">Creates or replaces a function in a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26f54-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="26f54-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="26f54-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="26f54-105">DESCRIPTION</span></span>
<span data-ttu-id="26f54-106">A **New-AzureRmStreamAnalyticsFunction** parancsmag létrehoz egy függvényt egy Azure stream Analytics-munkahelyen, vagy lecserél egy meglévő függvényt.</span><span class="sxs-lookup"><span data-stu-id="26f54-106">The **New-AzureRmStreamAnalyticsFunction** cmdlet creates a function in an Azure Stream Analytics job or replaces an existing function.</span></span>
<span data-ttu-id="26f54-107">Definiálja a függvényt egy JavaScript-objektum megjelölése (JSON) fájlban.</span><span class="sxs-lookup"><span data-stu-id="26f54-107">Define the function in a JavaScript Object Notation (JSON) file.</span></span>

<span data-ttu-id="26f54-108">A függvény nevét a *Name* vagy a. JSON fájlban adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="26f54-108">You can specify the name of the function by using the *Name* parameter or in the .json file.</span></span>
<span data-ttu-id="26f54-109">Ha mindkét módon adja meg a nevet, a névnek egyeznie kell.</span><span class="sxs-lookup"><span data-stu-id="26f54-109">If you specify the name in both ways, the names must match.</span></span>

<span data-ttu-id="26f54-110">Meglévő függvény lecseréléséhez adja meg a meglévő függvény nevét.</span><span class="sxs-lookup"><span data-stu-id="26f54-110">To replace an existing function, specify the name of the existing function.</span></span>

## <span data-ttu-id="26f54-111">Példák</span><span class="sxs-lookup"><span data-stu-id="26f54-111">EXAMPLES</span></span>

### <span data-ttu-id="26f54-112">Példa 1: stream-Analytics-függvény létrehozása</span><span class="sxs-lookup"><span data-stu-id="26f54-112">Example 1: Create a Stream Analytics function</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob07" -File "C:\Function07.json"
```

<span data-ttu-id="26f54-113">A parancs a fájl Function07.jsból hoz létre függvényt.</span><span class="sxs-lookup"><span data-stu-id="26f54-113">This command creates a function from the file Function07.json.</span></span>
<span data-ttu-id="26f54-114">A függvény neve megtalálható a. JSON fájlban.</span><span class="sxs-lookup"><span data-stu-id="26f54-114">The name of the function is stored in the .json file.</span></span>

### <span data-ttu-id="26f54-115">2. példa: ScoreTweet nevű adatfolyam-elemzési függvény létrehozása</span><span class="sxs-lookup"><span data-stu-id="26f54-115">Example 2: Create a Stream Analytics function named ScoreTweet</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet"
```

<span data-ttu-id="26f54-116">Ez a parancs létrehoz egy függvényt a ScoreTweet nevű feladathoz.</span><span class="sxs-lookup"><span data-stu-id="26f54-116">This command creates a function on the job named ScoreTweet.</span></span>

### <span data-ttu-id="26f54-117">3. példa: stream-Analytics függvény cseréje</span><span class="sxs-lookup"><span data-stu-id="26f54-117">Example 3: Replace a Stream Analytics function</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet" -Force
```

<span data-ttu-id="26f54-118">Ez a parancs felülírja a ScoreTweet nevű meglévő függvény definícióját, és a meghatározást Function22.jsbe értékre.</span><span class="sxs-lookup"><span data-stu-id="26f54-118">This command replaces the definition of the existing function named ScoreTweet with the definition in Function22.json.</span></span>

## <span data-ttu-id="26f54-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="26f54-119">PARAMETERS</span></span>

### <span data-ttu-id="26f54-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26f54-120">-DefaultProfile</span></span>
<span data-ttu-id="26f54-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="26f54-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f54-122">-Fájl</span><span class="sxs-lookup"><span data-stu-id="26f54-122">-File</span></span>
<span data-ttu-id="26f54-123">Annak a. JSON fájlnak az elérési útját adja meg, amely az adatfolyam-elemzés függvény JSON-adatábrázolását tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="26f54-123">Specifies the path of a .json file that contains the JSON representation of the Stream Analytics function.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f54-124">-Force</span><span class="sxs-lookup"><span data-stu-id="26f54-124">-Force</span></span>
<span data-ttu-id="26f54-125">Jelzi, hogy ez a parancsmag egy meglévő adatfolyam-elemzési függvényt cserél le anélkül, hogy megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="26f54-125">Indicates that this cmdlet replaces an existing Stream Analytics function without prompting you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f54-126">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="26f54-126">-JobName</span></span>
<span data-ttu-id="26f54-127">Annak az adatfolyam-elemzési feladatnak a nevét adja meg, amelyben ez a parancsmag adatfolyam-elemzési függvényt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="26f54-127">Specifies the name of the Stream Analytics job under which this cmdlet creates a Stream Analytics function.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26f54-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="26f54-128">-Name</span></span>
<span data-ttu-id="26f54-129">A parancsmag által létrehozott stream-Analytics függvény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="26f54-129">Specifies the name of the Stream Analytics function that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26f54-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26f54-130">-ResourceGroupName</span></span>
<span data-ttu-id="26f54-131">Annak az erőforrás-csoportnak a nevét adja meg, amelyben ez a parancsmag adatfolyam-elemzési függvényt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="26f54-131">Specifies the name of the resource group under which this cmdlet creates a Stream Analytics function.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26f54-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="26f54-132">-Confirm</span></span>
<span data-ttu-id="26f54-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="26f54-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f54-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26f54-134">-WhatIf</span></span>
<span data-ttu-id="26f54-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="26f54-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26f54-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="26f54-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f54-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26f54-137">CommonParameters</span></span>
<span data-ttu-id="26f54-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="26f54-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26f54-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26f54-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26f54-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="26f54-140">INPUTS</span></span>

### <span data-ttu-id="26f54-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="26f54-141">None</span></span>
<span data-ttu-id="26f54-142">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="26f54-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="26f54-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26f54-143">OUTPUTS</span></span>

### <span data-ttu-id="26f54-144">Microsoft. Azure. Command. StreamAnalytics. models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="26f54-144">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="26f54-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="26f54-145">NOTES</span></span>

## <span data-ttu-id="26f54-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26f54-146">RELATED LINKS</span></span>

[<span data-ttu-id="26f54-147">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="26f54-147">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="26f54-148">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="26f54-148">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="26f54-149">Teszt-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="26f54-149">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)


