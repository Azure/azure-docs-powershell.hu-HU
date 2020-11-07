---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: 41693da553178bdd45d19da498a5774ef8d2fa60
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841405"
---
# <span data-ttu-id="06353-101">New-AzApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="06353-101">New-AzApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="06353-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="06353-102">SYNOPSIS</span></span>
<span data-ttu-id="06353-103">A Health Probe által használt állapottanúsítvány-választ tartalmazó egyezést hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="06353-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="06353-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="06353-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeHealthResponseMatch [-Body <String>]
 [-StatusCode <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="06353-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="06353-105">DESCRIPTION</span></span>
<span data-ttu-id="06353-106">**Az Add-AzApplicationGatewayProbeHealthResponseMatch** parancsmag a Health Probe által használt, az alkalmazás-átjáróhoz használt állapottanúsítvány-választ tartalmazó találatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="06353-106">**The Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="06353-107">Példák</span><span class="sxs-lookup"><span data-stu-id="06353-107">EXAMPLES</span></span>

### <span data-ttu-id="06353-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="06353-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="06353-109">Ez a parancs olyan állapottanúsítvány-egyezést hoz létre, amelyet a ProbeConfig paraméterként továbbíthat a program.</span><span class="sxs-lookup"><span data-stu-id="06353-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="06353-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="06353-110">PARAMETERS</span></span>

### <span data-ttu-id="06353-111">-Body</span><span class="sxs-lookup"><span data-stu-id="06353-111">-Body</span></span>
<span data-ttu-id="06353-112">Az egészségvédelmi válaszban szerepelnie kell.</span><span class="sxs-lookup"><span data-stu-id="06353-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="06353-113">Az alapértelmezett érték üres</span><span class="sxs-lookup"><span data-stu-id="06353-113">Default value is empty</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06353-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06353-114">-DefaultProfile</span></span>
<span data-ttu-id="06353-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="06353-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06353-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="06353-116">-StatusCode</span></span>
<span data-ttu-id="06353-117">Az egészséges állapotkódok megengedett tartományai. Az egészséges állapotkódok alapértelmezett köre a 200-399</span><span class="sxs-lookup"><span data-stu-id="06353-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06353-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06353-118">CommonParameters</span></span>
<span data-ttu-id="06353-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="06353-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06353-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06353-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06353-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="06353-121">INPUTS</span></span>

### <span data-ttu-id="06353-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="06353-122">None</span></span>

## <span data-ttu-id="06353-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06353-123">OUTPUTS</span></span>

### <span data-ttu-id="06353-124">Microsoft. Azure. commands. Network. models. PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="06353-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="06353-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="06353-125">NOTES</span></span>

## <span data-ttu-id="06353-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06353-126">RELATED LINKS</span></span>

