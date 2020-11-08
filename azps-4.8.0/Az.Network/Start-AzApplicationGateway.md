---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
ms.openlocfilehash: 974e30d9a287d18293515c019b0032bf36f15b51
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94172871"
---
# <span data-ttu-id="2200b-101">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2200b-101">Start-AzApplicationGateway</span></span>

## <span data-ttu-id="2200b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2200b-102">SYNOPSIS</span></span>
<span data-ttu-id="2200b-103">Elindítja az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="2200b-103">Starts an application gateway.</span></span>

## <span data-ttu-id="2200b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2200b-104">SYNTAX</span></span>

```
Start-AzApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2200b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2200b-105">DESCRIPTION</span></span>
<span data-ttu-id="2200b-106">A **Start-AzApplicationGateway** parancsmag az Azure Application Gatewayt indítja el.</span><span class="sxs-lookup"><span data-stu-id="2200b-106">The **Start-AzApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="2200b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2200b-107">EXAMPLES</span></span>

### <span data-ttu-id="2200b-108">Example1: alkalmazás-átjáró indítása</span><span class="sxs-lookup"><span data-stu-id="2200b-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="2200b-109">Ez a parancs elindítja az $AppGw változóban tárolt alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="2200b-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="2200b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2200b-110">PARAMETERS</span></span>

### <span data-ttu-id="2200b-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2200b-111">-ApplicationGateway</span></span>
<span data-ttu-id="2200b-112">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag elindul.</span><span class="sxs-lookup"><span data-stu-id="2200b-112">Specifies the application gateway that this cmdlet starts.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2200b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2200b-113">-DefaultProfile</span></span>
<span data-ttu-id="2200b-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2200b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2200b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2200b-115">CommonParameters</span></span>
<span data-ttu-id="2200b-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2200b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2200b-117">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2200b-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2200b-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2200b-118">INPUTS</span></span>

### <span data-ttu-id="2200b-119">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2200b-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2200b-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2200b-120">OUTPUTS</span></span>

### <span data-ttu-id="2200b-121">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2200b-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2200b-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2200b-122">NOTES</span></span>

## <span data-ttu-id="2200b-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2200b-123">RELATED LINKS</span></span>

[<span data-ttu-id="2200b-124">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2200b-124">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


