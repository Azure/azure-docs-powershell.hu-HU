---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountapiproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
ms.openlocfilehash: 97cf393d0d95dbc9ecfec06f53795713f59aecbd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299669"
---
# <span data-ttu-id="94a38-101">New-AzCognitiveServicesAccountApiProperty</span><span class="sxs-lookup"><span data-stu-id="94a38-101">New-AzCognitiveServicesAccountApiProperty</span></span>

## <span data-ttu-id="94a38-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="94a38-102">SYNOPSIS</span></span>
<span data-ttu-id="94a38-103">A kognitív Services-fiók ApiProperties új példányának létrehozása</span><span class="sxs-lookup"><span data-stu-id="94a38-103">Generate a new instance of Cognitive Services Account ApiProperties</span></span>

## <span data-ttu-id="94a38-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="94a38-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountApiProperty [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94a38-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="94a38-105">DESCRIPTION</span></span>
<span data-ttu-id="94a38-106">Hozza létre a kognitív Services-fiók ApiProperties új példányát.</span><span class="sxs-lookup"><span data-stu-id="94a38-106">Generate a new instance of Cognitive Services Account ApiProperties.</span></span>
<span data-ttu-id="94a38-107">Új fiók létrehozásakor vagy meglévő fiók frissítésekor használhatja a ApiProperties.</span><span class="sxs-lookup"><span data-stu-id="94a38-107">ApiProperties can be used when creating a new account or updating an existing account.</span></span>
<span data-ttu-id="94a38-108">Az ApiProperties bizonyos típusú fiókokhoz szükséges.</span><span class="sxs-lookup"><span data-stu-id="94a38-108">ApiProperties is required by certain account types.</span></span>

## <span data-ttu-id="94a38-109">Példák</span><span class="sxs-lookup"><span data-stu-id="94a38-109">EXAMPLES</span></span>

### <span data-ttu-id="94a38-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="94a38-110">Example 1</span></span>
```powershell
PS C:\> $apiProperties = New-AzCognitiveServicesAccountApiProperty
PS C:\> $apiProperties.QnaRuntimeEndpoint = "https://qnamaker.azurewebsites.net"
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name qnamaker -Type QnAMaker -SkuName S0 -Locatio WestUS -ApiProperty $apiProperties
```

<span data-ttu-id="94a38-111">A fenti példa létrehoz egy QnAMaker-fiókot, az API tulajdonság "QnaRuntimeEndpoint".</span><span class="sxs-lookup"><span data-stu-id="94a38-111">Above example will create an QnAMaker account, with API property "QnaRuntimeEndpoint".</span></span>


## <span data-ttu-id="94a38-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="94a38-112">PARAMETERS</span></span>

### <span data-ttu-id="94a38-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94a38-113">-DefaultProfile</span></span>
<span data-ttu-id="94a38-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94a38-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94a38-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="94a38-115">-Confirm</span></span>
<span data-ttu-id="94a38-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="94a38-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94a38-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94a38-117">-WhatIf</span></span>
<span data-ttu-id="94a38-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="94a38-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94a38-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="94a38-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94a38-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94a38-120">CommonParameters</span></span>
<span data-ttu-id="94a38-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="94a38-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94a38-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="94a38-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94a38-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="94a38-123">INPUTS</span></span>

### <span data-ttu-id="94a38-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="94a38-124">None</span></span>

## <span data-ttu-id="94a38-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94a38-125">OUTPUTS</span></span>

### <span data-ttu-id="94a38-126">Microsoft. Azure. Management. CognitiveServices. models. CognitiveServicesAccountApiProperties</span><span class="sxs-lookup"><span data-stu-id="94a38-126">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties</span></span>

## <span data-ttu-id="94a38-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="94a38-127">NOTES</span></span>

## <span data-ttu-id="94a38-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94a38-128">RELATED LINKS</span></span>
