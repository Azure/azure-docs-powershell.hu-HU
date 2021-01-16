---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EF16CE43-1035-4ED0-B9D1-E475DF659ECE
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsdefaultfunctiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
ms.openlocfilehash: 1854c2e060dbbc83ba196043debb0ba08c9a933e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366462"
---
# <span data-ttu-id="59bf6-101">Get-AzStreamAnalyticsDefaultFunctionDefinition</span><span class="sxs-lookup"><span data-stu-id="59bf6-101">Get-AzStreamAnalyticsDefaultFunctionDefinition</span></span>

## <span data-ttu-id="59bf6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59bf6-102">SYNOPSIS</span></span>
<span data-ttu-id="59bf6-103">A Stream Analytics függvényének alapértelmezett definícióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="59bf6-103">Gets the default definition of a function in Stream Analytics.</span></span>

## <span data-ttu-id="59bf6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="59bf6-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsDefaultFunctionDefinition [-JobName] <String> [-Name] <String> [-File] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59bf6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="59bf6-105">DESCRIPTION</span></span>
<span data-ttu-id="59bf6-106">A **Get-AzStreamAnalyticsDefaultFunctionDefinition Parancsmag** megkapja az Azure Stream Analytics egy függvényének alapértelmezett definícióját.</span><span class="sxs-lookup"><span data-stu-id="59bf6-106">The **Get-AzStreamAnalyticsDefaultFunctionDefinition** cmdlet gets the default definition of a function in Azure Stream Analytics.</span></span>
<span data-ttu-id="59bf6-107">A függvények létrehozásához használhatja New-AzStreamAnalyticsFunction alapértelmezett definíciót és parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="59bf6-107">You can use the default definition and the New-AzStreamAnalyticsFunction cmdlet to create a function.</span></span>
<span data-ttu-id="59bf6-108">A függvények létrehozása előtt módosíthatja az alapértelmezett definíciót.</span><span class="sxs-lookup"><span data-stu-id="59bf6-108">You can modify the default definition before you create a function.</span></span>

## <span data-ttu-id="59bf6-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="59bf6-109">EXAMPLES</span></span>

### <span data-ttu-id="59bf6-110">1. példa: A Stream Analytics függvény alapértelmezett definíciójának lekérte</span><span class="sxs-lookup"><span data-stu-id="59bf6-110">Example 1: Get the default definition of a Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsDefaultFunctionDefinition -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\RetrieveDefaultDefinitionRequest.json" -Name "ScoreTweet"
```

<span data-ttu-id="59bf6-111">Ez a parancs a ScoreTweet nevű függvény alapértelmezett definícióját kapja meg a fájlon RetrieveDefaultDefinitionRequest.jsparaméterekkel.</span><span class="sxs-lookup"><span data-stu-id="59bf6-111">This command gets the default definition of the function named ScoreTweet by using the parameters specified in the RetrieveDefaultDefinitionRequest.json file.</span></span>

## <span data-ttu-id="59bf6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59bf6-112">PARAMETERS</span></span>

### <span data-ttu-id="59bf6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59bf6-113">-DefaultProfile</span></span>
<span data-ttu-id="59bf6-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="59bf6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59bf6-115">-File</span><span class="sxs-lookup"><span data-stu-id="59bf6-115">-File</span></span>
<span data-ttu-id="59bf6-116">Egy .json fájl elérési útját adja meg, amely a lekérés alapértelmezett függvénydefiníciós kérésének JSON (JavaScript Object Notation) ábrázolását tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="59bf6-116">Specifies the path of a .json file that contains the JavaScript Object Notation (JSON) representation of the request body for the retrieve default function definition request.</span></span>

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

### <span data-ttu-id="59bf6-117">-JobName</span><span class="sxs-lookup"><span data-stu-id="59bf6-117">-JobName</span></span>
<span data-ttu-id="59bf6-118">Annak a Stream Analytics-feladatnak a nevét adja meg, amelyhez a függvények tartoznak.</span><span class="sxs-lookup"><span data-stu-id="59bf6-118">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="59bf6-119">Ez a parancsmag a paraméter által megadott feladat egyik függvényének alapértelmezett definícióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="59bf6-119">This cmdlet gets the default definition for a function in the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="59bf6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="59bf6-120">-Name</span></span>
<span data-ttu-id="59bf6-121">Annak a Stream Analytics függvénynek a neve, amelyhez ez a parancsmag az alapértelmezett definíciót kapja.</span><span class="sxs-lookup"><span data-stu-id="59bf6-121">Specifies the name of the Stream Analytics function for which this cmdlet gets the default definition.</span></span>

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

### <span data-ttu-id="59bf6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59bf6-122">-ResourceGroupName</span></span>
<span data-ttu-id="59bf6-123">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a Stream Analytics függvény tartozik.</span><span class="sxs-lookup"><span data-stu-id="59bf6-123">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="59bf6-124">Ez a parancsmag a paraméter által megadott csoporthoz függvénydefiníciót kap.</span><span class="sxs-lookup"><span data-stu-id="59bf6-124">This cmdlet gets a function definition for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="59bf6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59bf6-125">CommonParameters</span></span>
<span data-ttu-id="59bf6-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59bf6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59bf6-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59bf6-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59bf6-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="59bf6-128">INPUTS</span></span>

### <span data-ttu-id="59bf6-129">System.String</span><span class="sxs-lookup"><span data-stu-id="59bf6-129">System.String</span></span>

## <span data-ttu-id="59bf6-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59bf6-130">OUTPUTS</span></span>

### <span data-ttu-id="59bf6-131">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span><span class="sxs-lookup"><span data-stu-id="59bf6-131">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="59bf6-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="59bf6-132">NOTES</span></span>

## <span data-ttu-id="59bf6-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59bf6-133">RELATED LINKS</span></span>

[<span data-ttu-id="59bf6-134">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="59bf6-134">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)


