---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountapiproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
ms.openlocfilehash: 97cf393d0d95dbc9ecfec06f53795713f59aecbd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329634"
---
# <span data-ttu-id="a2aef-101">New-AzCognitiveServicesAccountApiProperty</span><span class="sxs-lookup"><span data-stu-id="a2aef-101">New-AzCognitiveServicesAccountApiProperty</span></span>

## <span data-ttu-id="a2aef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2aef-102">SYNOPSIS</span></span>
<span data-ttu-id="a2aef-103">A Kognitív Szolgáltatások-fiók ApiProperties új példányának létrehozása</span><span class="sxs-lookup"><span data-stu-id="a2aef-103">Generate a new instance of Cognitive Services Account ApiProperties</span></span>

## <span data-ttu-id="a2aef-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a2aef-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountApiProperty [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a2aef-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a2aef-105">DESCRIPTION</span></span>
<span data-ttu-id="a2aef-106">A Kognitív Szolgáltatások-fiók ApiProperties új példányának létrehozása.</span><span class="sxs-lookup"><span data-stu-id="a2aef-106">Generate a new instance of Cognitive Services Account ApiProperties.</span></span>
<span data-ttu-id="a2aef-107">Az ApiProperties használható új fiók létrehozásakor vagy meglévő fiók frissítésekkor.</span><span class="sxs-lookup"><span data-stu-id="a2aef-107">ApiProperties can be used when creating a new account or updating an existing account.</span></span>
<span data-ttu-id="a2aef-108">Bizonyos fióktípusokhoz apiProperties szükséges.</span><span class="sxs-lookup"><span data-stu-id="a2aef-108">ApiProperties is required by certain account types.</span></span>

## <span data-ttu-id="a2aef-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a2aef-109">EXAMPLES</span></span>

### <span data-ttu-id="a2aef-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="a2aef-110">Example 1</span></span>
```powershell
PS C:\> $apiProperties = New-AzCognitiveServicesAccountApiProperty
PS C:\> $apiProperties.QnaRuntimeEndpoint = "https://qnamaker.azurewebsites.net"
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name qnamaker -Type QnAMaker -SkuName S0 -Locatio WestUS -ApiProperty $apiProperties
```

<span data-ttu-id="a2aef-111">A fenti példa létrehoz egy QnAMaker-fiókot a "QnaRuntimeEndpoint" API-tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="a2aef-111">Above example will create an QnAMaker account, with API property "QnaRuntimeEndpoint".</span></span>


## <span data-ttu-id="a2aef-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2aef-112">PARAMETERS</span></span>

### <span data-ttu-id="a2aef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2aef-113">-DefaultProfile</span></span>
<span data-ttu-id="a2aef-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2aef-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2aef-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2aef-115">-Confirm</span></span>
<span data-ttu-id="a2aef-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a2aef-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2aef-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2aef-117">-WhatIf</span></span>
<span data-ttu-id="a2aef-118">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a2aef-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2aef-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a2aef-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2aef-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2aef-120">CommonParameters</span></span>
<span data-ttu-id="a2aef-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2aef-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2aef-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2aef-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2aef-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a2aef-123">INPUTS</span></span>

### <span data-ttu-id="a2aef-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="a2aef-124">None</span></span>

## <span data-ttu-id="a2aef-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2aef-125">OUTPUTS</span></span>

### <span data-ttu-id="a2aef-126">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties</span><span class="sxs-lookup"><span data-stu-id="a2aef-126">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties</span></span>

## <span data-ttu-id="a2aef-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a2aef-127">NOTES</span></span>

## <span data-ttu-id="a2aef-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2aef-128">RELATED LINKS</span></span>
