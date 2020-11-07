---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmApplicationGateway.md
ms.openlocfilehash: 88ca18eca50f1e68eab8599ad79f902ff1fd2551
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672790"
---
# <span data-ttu-id="9c90a-101">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c90a-101">Start-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="9c90a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9c90a-102">SYNOPSIS</span></span>
<span data-ttu-id="9c90a-103">Elindítja az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="9c90a-103">Starts an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c90a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9c90a-104">SYNTAX</span></span>

```
Start-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c90a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9c90a-105">DESCRIPTION</span></span>
<span data-ttu-id="9c90a-106">A **Start-AzureRmApplicationGateway** parancsmag az Azure Application Gatewayt indítja el.</span><span class="sxs-lookup"><span data-stu-id="9c90a-106">The **Start-AzureRmApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="9c90a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9c90a-107">EXAMPLES</span></span>

### <span data-ttu-id="9c90a-108">Example1: alkalmazás-átjáró indítása</span><span class="sxs-lookup"><span data-stu-id="9c90a-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="9c90a-109">Ez a parancs elindítja az $AppGw változóban tárolt alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="9c90a-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="9c90a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9c90a-110">PARAMETERS</span></span>

### <span data-ttu-id="9c90a-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c90a-111">-ApplicationGateway</span></span>
<span data-ttu-id="9c90a-112">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag elindul.</span><span class="sxs-lookup"><span data-stu-id="9c90a-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="9c90a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c90a-113">-DefaultProfile</span></span>
<span data-ttu-id="9c90a-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9c90a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c90a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c90a-115">CommonParameters</span></span>
<span data-ttu-id="9c90a-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9c90a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c90a-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c90a-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c90a-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c90a-118">INPUTS</span></span>

### <span data-ttu-id="9c90a-119">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c90a-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="9c90a-120">Paraméterek: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9c90a-120">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="9c90a-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c90a-121">OUTPUTS</span></span>

### <span data-ttu-id="9c90a-122">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c90a-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9c90a-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9c90a-123">NOTES</span></span>

## <span data-ttu-id="9c90a-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9c90a-124">RELATED LINKS</span></span>

[<span data-ttu-id="9c90a-125">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c90a-125">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


