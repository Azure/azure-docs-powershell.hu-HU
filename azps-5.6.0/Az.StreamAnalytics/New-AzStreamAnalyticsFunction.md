---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 79EB2AD9-BFE1-49BE-870F-7DFC99D6FE17
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/new-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsFunction.md
ms.openlocfilehash: ac303b4e458e836238a148f1a33b009e9c0b0e24
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929530"
---
# <span data-ttu-id="4d532-101">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="4d532-101">New-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="4d532-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d532-102">SYNOPSIS</span></span>
<span data-ttu-id="4d532-103">Függvényt hoz létre vagy cserél le egy Stream Analytics-feladatban.</span><span class="sxs-lookup"><span data-stu-id="4d532-103">Creates or replaces a function in a Stream Analytics job.</span></span>

## <span data-ttu-id="4d532-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4d532-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d532-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4d532-105">DESCRIPTION</span></span>
<span data-ttu-id="4d532-106">A **New-AzStreamAnalyticsFunction** parancsmag létrehoz egy függvényt egy Azure Stream Analytics-feladatban, vagy lecserél egy meglévő függvényt.</span><span class="sxs-lookup"><span data-stu-id="4d532-106">The **New-AzStreamAnalyticsFunction** cmdlet creates a function in an Azure Stream Analytics job or replaces an existing function.</span></span>
<span data-ttu-id="4d532-107">A függvény definiálása JavaScript-objektum-notation (JSON) fájlban.</span><span class="sxs-lookup"><span data-stu-id="4d532-107">Define the function in a JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="4d532-108">A függvény nevét a Name paraméter  vagy a .json fájl használatával adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="4d532-108">You can specify the name of the function by using the *Name* parameter or in the .json file.</span></span>
<span data-ttu-id="4d532-109">Ha mindkét módon megadja a nevet, a neveknek egyezniük kell.</span><span class="sxs-lookup"><span data-stu-id="4d532-109">If you specify the name in both ways, the names must match.</span></span>
<span data-ttu-id="4d532-110">Meglévő függvény cseréjéhez adja meg a meglévő függvény nevét.</span><span class="sxs-lookup"><span data-stu-id="4d532-110">To replace an existing function, specify the name of the existing function.</span></span>

## <span data-ttu-id="4d532-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4d532-111">EXAMPLES</span></span>

### <span data-ttu-id="4d532-112">1. példa: Stream Analytics függvény létrehozása</span><span class="sxs-lookup"><span data-stu-id="4d532-112">Example 1: Create a Stream Analytics function</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob07" -File "C:\Function07.json"
```

<span data-ttu-id="4d532-113">Ez a parancs egy függvényt hoz létre a be van Function07.jsfájlból.</span><span class="sxs-lookup"><span data-stu-id="4d532-113">This command creates a function from the file Function07.json.</span></span>
<span data-ttu-id="4d532-114">A függvény nevét a .json fájl tárolja.</span><span class="sxs-lookup"><span data-stu-id="4d532-114">The name of the function is stored in the .json file.</span></span>

### <span data-ttu-id="4d532-115">2. példa: ScoreTweet nevű Stream Analytics függvény létrehozása</span><span class="sxs-lookup"><span data-stu-id="4d532-115">Example 2: Create a Stream Analytics function named ScoreTweet</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet"
```

<span data-ttu-id="4d532-116">Ez a parancs létrehoz egy függvényt a ScoreTweet nevű feladaton.</span><span class="sxs-lookup"><span data-stu-id="4d532-116">This command creates a function on the job named ScoreTweet.</span></span>

### <span data-ttu-id="4d532-117">3. példa: Stream Analytics függvény cseréje</span><span class="sxs-lookup"><span data-stu-id="4d532-117">Example 3: Replace a Stream Analytics function</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet" -Force
```

<span data-ttu-id="4d532-118">Ez a parancs felváltja a ScoreTweet nevű meglévő függvény definícióját a Function22.jsdefinícióra.</span><span class="sxs-lookup"><span data-stu-id="4d532-118">This command replaces the definition of the existing function named ScoreTweet with the definition in Function22.json.</span></span>

## <span data-ttu-id="4d532-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d532-119">PARAMETERS</span></span>

### <span data-ttu-id="4d532-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d532-120">-DefaultProfile</span></span>
<span data-ttu-id="4d532-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4d532-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d532-122">-File</span><span class="sxs-lookup"><span data-stu-id="4d532-122">-File</span></span>
<span data-ttu-id="4d532-123">A Stream Analytics függvény JSON-ábrázolását tartalmazó .json fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4d532-123">Specifies the path of a .json file that contains the JSON representation of the Stream Analytics function.</span></span>

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

### <span data-ttu-id="4d532-124">-Force</span><span class="sxs-lookup"><span data-stu-id="4d532-124">-Force</span></span>
<span data-ttu-id="4d532-125">Azt jelzi, hogy ez a parancsmag egy meglévő Stream Analytics-függvényt vált fel megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="4d532-125">Indicates that this cmdlet replaces an existing Stream Analytics function without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="4d532-126">-JobName</span><span class="sxs-lookup"><span data-stu-id="4d532-126">-JobName</span></span>
<span data-ttu-id="4d532-127">Annak a Stream Analytics-feladatnak a nevét adja meg, amely alatt ez a parancsmag létrehozza a Stream Analytics függvényt.</span><span class="sxs-lookup"><span data-stu-id="4d532-127">Specifies the name of the Stream Analytics job under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="4d532-128">-Name</span><span class="sxs-lookup"><span data-stu-id="4d532-128">-Name</span></span>
<span data-ttu-id="4d532-129">A parancsmag által létrehozott Stream Analytics függvény neve.</span><span class="sxs-lookup"><span data-stu-id="4d532-129">Specifies the name of the Stream Analytics function that this cmdlet creates.</span></span>

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

### <span data-ttu-id="4d532-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d532-130">-ResourceGroupName</span></span>
<span data-ttu-id="4d532-131">Annak az erőforráscsoportnak a nevét adja meg, amely alatt ez a parancsmag létrehozza a Stream Analytics függvényt.</span><span class="sxs-lookup"><span data-stu-id="4d532-131">Specifies the name of the resource group under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="4d532-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d532-132">-Confirm</span></span>
<span data-ttu-id="4d532-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4d532-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d532-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d532-134">-WhatIf</span></span>
<span data-ttu-id="4d532-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4d532-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d532-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4d532-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d532-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d532-137">CommonParameters</span></span>
<span data-ttu-id="4d532-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d532-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d532-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d532-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d532-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4d532-140">INPUTS</span></span>

### <span data-ttu-id="4d532-141">System.String</span><span class="sxs-lookup"><span data-stu-id="4d532-141">System.String</span></span>

## <span data-ttu-id="4d532-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d532-142">OUTPUTS</span></span>

### <span data-ttu-id="4d532-143">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span><span class="sxs-lookup"><span data-stu-id="4d532-143">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="4d532-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4d532-144">NOTES</span></span>

## <span data-ttu-id="4d532-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d532-145">RELATED LINKS</span></span>

[<span data-ttu-id="4d532-146">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="4d532-146">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="4d532-147">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="4d532-147">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="4d532-148">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="4d532-148">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


