---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: edc0309b5e1a0c8b17d400e965074d38ca02bb80
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341345"
---
# <span data-ttu-id="ecd8c-101">New-AzApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="ecd8c-101">New-AzApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="ecd8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecd8c-102">SYNOPSIS</span></span>
<span data-ttu-id="ecd8c-103">Egy alkalmazás-átjáró Állapotvetítója által használt állapotválasz-egyezést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ecd8c-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="ecd8c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ecd8c-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeHealthResponseMatch [-Body <String>] [-StatusCode <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecd8c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ecd8c-105">DESCRIPTION</span></span>
<span data-ttu-id="ecd8c-106">**Az Add-AzApplicationGatewayProbealthResponseMatch** parancsmag létrehoz egy állapotlejárat-válasz egyezést, amelyet az Állapotvetítő egy alkalmazás-átjáróhoz használ.</span><span class="sxs-lookup"><span data-stu-id="ecd8c-106">**The Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="ecd8c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ecd8c-107">EXAMPLES</span></span>

### <span data-ttu-id="ecd8c-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="ecd8c-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="ecd8c-109">Ez a parancs egy olyan állapot-egyezést hoz létre, amely paraméterként át lehet adva a ÉssokConfignek.</span><span class="sxs-lookup"><span data-stu-id="ecd8c-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="ecd8c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ecd8c-110">PARAMETERS</span></span>

### <span data-ttu-id="ecd8c-111">-Body</span><span class="sxs-lookup"><span data-stu-id="ecd8c-111">-Body</span></span>
<span data-ttu-id="ecd8c-112">Az állapotra adott válaszban szereplő törzs.</span><span class="sxs-lookup"><span data-stu-id="ecd8c-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="ecd8c-113">Az alapértelmezett érték üres</span><span class="sxs-lookup"><span data-stu-id="ecd8c-113">Default value is empty</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecd8c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecd8c-114">-DefaultProfile</span></span>
<span data-ttu-id="ecd8c-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ecd8c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecd8c-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="ecd8c-116">-StatusCode</span></span>
<span data-ttu-id="ecd8c-117">Engedélyezett állapotkódok tartományai. Az egészséges állapotkódok alapértelmezett tartománya 200–399</span><span class="sxs-lookup"><span data-stu-id="ecd8c-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecd8c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecd8c-118">CommonParameters</span></span>
<span data-ttu-id="ecd8c-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecd8c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecd8c-120">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecd8c-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecd8c-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ecd8c-121">INPUTS</span></span>

### <span data-ttu-id="ecd8c-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="ecd8c-122">None</span></span>

## <span data-ttu-id="ecd8c-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ecd8c-123">OUTPUTS</span></span>

### <span data-ttu-id="ecd8c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="ecd8c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="ecd8c-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ecd8c-125">NOTES</span></span>

## <span data-ttu-id="ecd8c-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ecd8c-126">RELATED LINKS</span></span>
