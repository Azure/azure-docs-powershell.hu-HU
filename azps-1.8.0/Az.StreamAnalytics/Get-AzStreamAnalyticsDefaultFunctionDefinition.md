---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EF16CE43-1035-4ED0-B9D1-E475DF659ECE
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsdefaultfunctiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
ms.openlocfilehash: 217b9f8775f38635cf2285215a0be10a92b832c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668467"
---
# <span data-ttu-id="7efbb-101">Get-AzStreamAnalyticsDefaultFunctionDefinition</span><span class="sxs-lookup"><span data-stu-id="7efbb-101">Get-AzStreamAnalyticsDefaultFunctionDefinition</span></span>

## <span data-ttu-id="7efbb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7efbb-102">SYNOPSIS</span></span>
<span data-ttu-id="7efbb-103">Az adatfolyam-elemzés függvény alapértelmezett definícióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7efbb-103">Gets the default definition of a function in Stream Analytics.</span></span>

## <span data-ttu-id="7efbb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7efbb-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsDefaultFunctionDefinition [-JobName] <String> [-Name] <String> [-File] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7efbb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7efbb-105">DESCRIPTION</span></span>
<span data-ttu-id="7efbb-106">A **Get-AzStreamAnalyticsDefaultFunctionDefinition** parancsmag az Azure stream Analytics függvény alapértelmezett definícióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7efbb-106">The **Get-AzStreamAnalyticsDefaultFunctionDefinition** cmdlet gets the default definition of a function in Azure Stream Analytics.</span></span>
<span data-ttu-id="7efbb-107">Az alapértelmezett definíció és a New-AzStreamAnalyticsFunction parancsmag használatával is létrehozhatja a függvényeket.</span><span class="sxs-lookup"><span data-stu-id="7efbb-107">You can use the default definition and the New-AzStreamAnalyticsFunction cmdlet to create a function.</span></span>
<span data-ttu-id="7efbb-108">A függvény létrehozása előtt módosíthatja az alapértelmezett definíciót.</span><span class="sxs-lookup"><span data-stu-id="7efbb-108">You can modify the default definition before you create a function.</span></span>

## <span data-ttu-id="7efbb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7efbb-109">EXAMPLES</span></span>

### <span data-ttu-id="7efbb-110">Példa 1: az adatfolyam-elemzés függvény alapértelmezett definíciójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="7efbb-110">Example 1: Get the default definition of a Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsDefaultFunctionDefinition -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\RetrieveDefaultDefinitionRequest.json" -Name "ScoreTweet"
```

<span data-ttu-id="7efbb-111">Ez a parancs a ScoreTweet nevű függvény alapértelmezett definícióját kapja meg a fájl RetrieveDefaultDefinitionRequest.jsben megadott paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="7efbb-111">This command gets the default definition of the function named ScoreTweet by using the parameters specified in the RetrieveDefaultDefinitionRequest.json file.</span></span>

## <span data-ttu-id="7efbb-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7efbb-112">PARAMETERS</span></span>

### <span data-ttu-id="7efbb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7efbb-113">-DefaultProfile</span></span>
<span data-ttu-id="7efbb-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7efbb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7efbb-115">-Fájl</span><span class="sxs-lookup"><span data-stu-id="7efbb-115">-File</span></span>
<span data-ttu-id="7efbb-116">Annak a. JSON fájlnak az elérési útját adja meg, amely a kérelem törzsének alapértelmezett függvény-definíciós kérésének beolvasására szolgáló JavaScript-objektum jelölését (JSON) tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="7efbb-116">Specifies the path of a .json file that contains the JavaScript Object Notation (JSON) representation of the request body for the retrieve default function definition request.</span></span>

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

### <span data-ttu-id="7efbb-117">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="7efbb-117">-JobName</span></span>
<span data-ttu-id="7efbb-118">Annak az adatfolyam-elemzési feladatnak a nevét adja meg, amelybe a függvény tartozik.</span><span class="sxs-lookup"><span data-stu-id="7efbb-118">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="7efbb-119">Ez a parancsmag a megfelelő függvény alapértelmezett definícióját adja meg a projektben, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="7efbb-119">This cmdlet gets the default definition for a function in the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="7efbb-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7efbb-120">-Name</span></span>
<span data-ttu-id="7efbb-121">Annak az adatfolyam-elemzési függvénynek a nevét adja meg, amelyhez ez a parancsmag az alapértelmezett definíciót kapja.</span><span class="sxs-lookup"><span data-stu-id="7efbb-121">Specifies the name of the Stream Analytics function for which this cmdlet gets the default definition.</span></span>

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

### <span data-ttu-id="7efbb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7efbb-122">-ResourceGroupName</span></span>
<span data-ttu-id="7efbb-123">Annak az erőforráscsoportnek a nevét adja meg, amelybe az adatfolyam-elemzés függvény tartozik.</span><span class="sxs-lookup"><span data-stu-id="7efbb-123">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="7efbb-124">Ez a parancsmag a paraméter által megadott csoport függvényének definícióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7efbb-124">This cmdlet gets a function definition for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7efbb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7efbb-125">CommonParameters</span></span>
<span data-ttu-id="7efbb-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7efbb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7efbb-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7efbb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7efbb-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7efbb-128">INPUTS</span></span>

### <span data-ttu-id="7efbb-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7efbb-129">System.String</span></span>

## <span data-ttu-id="7efbb-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7efbb-130">OUTPUTS</span></span>

### <span data-ttu-id="7efbb-131">Microsoft. Azure. Command. StreamAnalytics. models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="7efbb-131">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="7efbb-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7efbb-132">NOTES</span></span>

## <span data-ttu-id="7efbb-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7efbb-133">RELATED LINKS</span></span>

[<span data-ttu-id="7efbb-134">Új – AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="7efbb-134">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)


