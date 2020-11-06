---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: 3306bdeb37271072b5d7e1054286f5fd9d460403
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497543"
---
# <span data-ttu-id="99c71-101">New-AzureRmApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="99c71-101">New-AzureRmApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="99c71-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="99c71-102">SYNOPSIS</span></span>
<span data-ttu-id="99c71-103">A Health Probe által használt állapottanúsítvány-választ tartalmazó egyezést hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="99c71-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99c71-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="99c71-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeHealthResponseMatch [-Body <String>]
 [-StatusCode <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="99c71-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="99c71-105">DESCRIPTION</span></span>
<span data-ttu-id="99c71-106">**Az Add-AzureRmApplicationGatewayProbeHealthResponseMatch** parancsmag a Health Probe által használt, az alkalmazás-átjáróhoz használt állapottanúsítvány-választ tartalmazó találatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="99c71-106">**The Add-AzureRmApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="99c71-107">Példák</span><span class="sxs-lookup"><span data-stu-id="99c71-107">EXAMPLES</span></span>

### <span data-ttu-id="99c71-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="99c71-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzureRmApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="99c71-109">Ez a parancs olyan állapottanúsítvány-egyezést hoz létre, amelyet a ProbeConfig paraméterként továbbíthat a program.</span><span class="sxs-lookup"><span data-stu-id="99c71-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="99c71-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="99c71-110">PARAMETERS</span></span>

### <span data-ttu-id="99c71-111">-Body</span><span class="sxs-lookup"><span data-stu-id="99c71-111">-Body</span></span>
<span data-ttu-id="99c71-112">Az egészségvédelmi válaszban szerepelnie kell.</span><span class="sxs-lookup"><span data-stu-id="99c71-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="99c71-113">Az alapértelmezett érték üres</span><span class="sxs-lookup"><span data-stu-id="99c71-113">Default value is empty</span></span>

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

### <span data-ttu-id="99c71-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99c71-114">-DefaultProfile</span></span>
<span data-ttu-id="99c71-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="99c71-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99c71-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="99c71-116">-StatusCode</span></span>
<span data-ttu-id="99c71-117">Az egészséges állapotkódok megengedett tartományai. Az egészséges állapotkódok alapértelmezett köre a 200-399</span><span class="sxs-lookup"><span data-stu-id="99c71-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

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

### <span data-ttu-id="99c71-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99c71-118">CommonParameters</span></span>
<span data-ttu-id="99c71-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="99c71-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99c71-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99c71-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99c71-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="99c71-121">INPUTS</span></span>

### <span data-ttu-id="99c71-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="99c71-122">None</span></span>

## <span data-ttu-id="99c71-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99c71-123">OUTPUTS</span></span>

### <span data-ttu-id="99c71-124">Microsoft. Azure. commands. Network. models. PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="99c71-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="99c71-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="99c71-125">NOTES</span></span>

## <span data-ttu-id="99c71-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99c71-126">RELATED LINKS</span></span>

