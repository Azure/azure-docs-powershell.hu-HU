---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: EF16CE43-1035-4ED0-B9D1-E475DF659ECE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsDefaultFunctionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsDefaultFunctionDefinition.md
ms.openlocfilehash: 307a07254f61bcbd37127a2a4d15bb41944a3508
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495517"
---
# <span data-ttu-id="f2d18-101">Get-AzureRmStreamAnalyticsDefaultFunctionDefinition</span><span class="sxs-lookup"><span data-stu-id="f2d18-101">Get-AzureRmStreamAnalyticsDefaultFunctionDefinition</span></span>

## <span data-ttu-id="f2d18-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f2d18-102">SYNOPSIS</span></span>
<span data-ttu-id="f2d18-103">Az adatfolyam-elemzés függvény alapértelmezett definícióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f2d18-103">Gets the default definition of a function in Stream Analytics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2d18-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f2d18-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsDefaultFunctionDefinition [-JobName] <String> [-Name] <String> [-File] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2d18-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f2d18-105">DESCRIPTION</span></span>
<span data-ttu-id="f2d18-106">A **Get-AzureRmStreamAnalyticsDefaultFunctionDefinition** parancsmag az Azure stream Analytics függvény alapértelmezett definícióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f2d18-106">The **Get-AzureRmStreamAnalyticsDefaultFunctionDefinition** cmdlet gets the default definition of a function in Azure Stream Analytics.</span></span>
<span data-ttu-id="f2d18-107">Az alapértelmezett definíció és a New-AzureRmStreamAnalyticsFunction parancsmag használatával is létrehozhatja a függvényeket.</span><span class="sxs-lookup"><span data-stu-id="f2d18-107">You can use the default definition and the New-AzureRmStreamAnalyticsFunction cmdlet to create a function.</span></span>
<span data-ttu-id="f2d18-108">A függvény létrehozása előtt módosíthatja az alapértelmezett definíciót.</span><span class="sxs-lookup"><span data-stu-id="f2d18-108">You can modify the default definition before you create a function.</span></span>

## <span data-ttu-id="f2d18-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f2d18-109">EXAMPLES</span></span>

### <span data-ttu-id="f2d18-110">Példa 1: az adatfolyam-elemzés függvény alapértelmezett definíciójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="f2d18-110">Example 1: Get the default definition of a Stream Analytics function</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsDefaultFunctionDefinition -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\RetrieveDefaultDefinitionRequest.json" -Name "ScoreTweet"
```

<span data-ttu-id="f2d18-111">Ez a parancs a ScoreTweet nevű függvény alapértelmezett definícióját kapja meg a fájl RetrieveDefaultDefinitionRequest.jsben megadott paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="f2d18-111">This command gets the default definition of the function named ScoreTweet by using the parameters specified in the RetrieveDefaultDefinitionRequest.json file.</span></span>

## <span data-ttu-id="f2d18-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f2d18-112">PARAMETERS</span></span>

### <span data-ttu-id="f2d18-113">-Fájl</span><span class="sxs-lookup"><span data-stu-id="f2d18-113">-File</span></span>
<span data-ttu-id="f2d18-114">Annak a. JSON fájlnak az elérési útját adja meg, amely a kérelem törzsének alapértelmezett függvény-definíciós kérésének beolvasására szolgáló JavaScript-objektum jelölését (JSON) tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="f2d18-114">Specifies the path of a .json file that contains the JavaScript Object Notation (JSON) representation of the request body for the retrieve default function definition request.</span></span>

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

### <span data-ttu-id="f2d18-115">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="f2d18-115">-JobName</span></span>
<span data-ttu-id="f2d18-116">Annak az adatfolyam-elemzési feladatnak a nevét adja meg, amelybe a függvény tartozik.</span><span class="sxs-lookup"><span data-stu-id="f2d18-116">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="f2d18-117">Ez a parancsmag a megfelelő függvény alapértelmezett definícióját adja meg a projektben, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="f2d18-117">This cmdlet gets the default definition for a function in the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="f2d18-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f2d18-118">-Name</span></span>
<span data-ttu-id="f2d18-119">Annak az adatfolyam-elemzési függvénynek a nevét adja meg, amelyhez ez a parancsmag az alapértelmezett definíciót kapja.</span><span class="sxs-lookup"><span data-stu-id="f2d18-119">Specifies the name of the Stream Analytics function for which this cmdlet gets the default definition.</span></span>

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

### <span data-ttu-id="f2d18-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2d18-120">-ResourceGroupName</span></span>
<span data-ttu-id="f2d18-121">Annak az erőforráscsoportnek a nevét adja meg, amelybe az adatfolyam-elemzés függvény tartozik.</span><span class="sxs-lookup"><span data-stu-id="f2d18-121">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="f2d18-122">Ez a parancsmag a paraméter által megadott csoport függvényének definícióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f2d18-122">This cmdlet gets a function definition for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f2d18-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2d18-123">-DefaultProfile</span></span>
<span data-ttu-id="f2d18-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f2d18-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2d18-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2d18-125">CommonParameters</span></span>
<span data-ttu-id="f2d18-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f2d18-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2d18-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2d18-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2d18-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2d18-128">INPUTS</span></span>

## <span data-ttu-id="f2d18-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2d18-129">OUTPUTS</span></span>

### <span data-ttu-id="f2d18-130">Microsoft. Azure. Command. StreamAnalytics. models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="f2d18-130">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="f2d18-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f2d18-131">NOTES</span></span>

## <span data-ttu-id="f2d18-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2d18-132">RELATED LINKS</span></span>

[<span data-ttu-id="f2d18-133">Új – AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="f2d18-133">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)


