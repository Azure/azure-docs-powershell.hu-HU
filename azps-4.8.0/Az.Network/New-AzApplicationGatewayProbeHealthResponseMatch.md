---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: edc0309b5e1a0c8b17d400e965074d38ca02bb80
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184390"
---
# <span data-ttu-id="6a11b-101">New-AzApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="6a11b-101">New-AzApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="6a11b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6a11b-102">SYNOPSIS</span></span>
<span data-ttu-id="6a11b-103">A Health Probe által használt állapottanúsítvány-választ tartalmazó egyezést hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="6a11b-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="6a11b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6a11b-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeHealthResponseMatch [-Body <String>] [-StatusCode <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a11b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6a11b-105">DESCRIPTION</span></span>
<span data-ttu-id="6a11b-106">**Az Add-AzApplicationGatewayProbeHealthResponseMatch** parancsmag a Health Probe által használt, az alkalmazás-átjáróhoz használt állapottanúsítvány-választ tartalmazó találatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6a11b-106">**The Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="6a11b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6a11b-107">EXAMPLES</span></span>

### <span data-ttu-id="6a11b-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6a11b-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="6a11b-109">Ez a parancs olyan állapottanúsítvány-egyezést hoz létre, amelyet a ProbeConfig paraméterként továbbíthat a program.</span><span class="sxs-lookup"><span data-stu-id="6a11b-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="6a11b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6a11b-110">PARAMETERS</span></span>

### <span data-ttu-id="6a11b-111">-Body</span><span class="sxs-lookup"><span data-stu-id="6a11b-111">-Body</span></span>
<span data-ttu-id="6a11b-112">Az egészségvédelmi válaszban szerepelnie kell.</span><span class="sxs-lookup"><span data-stu-id="6a11b-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="6a11b-113">Az alapértelmezett érték üres</span><span class="sxs-lookup"><span data-stu-id="6a11b-113">Default value is empty</span></span>

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

### <span data-ttu-id="6a11b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a11b-114">-DefaultProfile</span></span>
<span data-ttu-id="6a11b-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6a11b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a11b-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="6a11b-116">-StatusCode</span></span>
<span data-ttu-id="6a11b-117">Az egészséges állapotkódok megengedett tartományai. Az egészséges állapotkódok alapértelmezett köre a 200-399</span><span class="sxs-lookup"><span data-stu-id="6a11b-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

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

### <span data-ttu-id="6a11b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a11b-118">CommonParameters</span></span>
<span data-ttu-id="6a11b-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6a11b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a11b-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a11b-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a11b-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a11b-121">INPUTS</span></span>

### <span data-ttu-id="6a11b-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="6a11b-122">None</span></span>

## <span data-ttu-id="6a11b-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a11b-123">OUTPUTS</span></span>

### <span data-ttu-id="6a11b-124">Microsoft. Azure. commands. Network. models. PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="6a11b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="6a11b-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6a11b-125">NOTES</span></span>

## <span data-ttu-id="6a11b-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a11b-126">RELATED LINKS</span></span>
