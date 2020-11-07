---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 382c4cd1b189e0dc95edd4824dec58a280dbb889
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849918"
---
# <span data-ttu-id="4b557-101">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4b557-101">Start-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="4b557-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4b557-102">SYNOPSIS</span></span>
<span data-ttu-id="4b557-103">Elindítja az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="4b557-103">Starts an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b557-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4b557-104">SYNTAX</span></span>

```
Start-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b557-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4b557-105">DESCRIPTION</span></span>
<span data-ttu-id="4b557-106">A **Start-AzureRmApplicationGateway** parancsmag az Azure Application Gatewayt indítja el.</span><span class="sxs-lookup"><span data-stu-id="4b557-106">The **Start-AzureRmApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="4b557-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4b557-107">EXAMPLES</span></span>

### <span data-ttu-id="4b557-108">Example1: alkalmazás-átjáró indítása</span><span class="sxs-lookup"><span data-stu-id="4b557-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="4b557-109">Ez a parancs elindítja az $AppGw változóban tárolt alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="4b557-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="4b557-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4b557-110">PARAMETERS</span></span>

### <span data-ttu-id="4b557-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4b557-111">-ApplicationGateway</span></span>
<span data-ttu-id="4b557-112">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag elindul.</span><span class="sxs-lookup"><span data-stu-id="4b557-112">Specifies the application gateway that this cmdlet starts.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b557-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b557-113">-DefaultProfile</span></span>
<span data-ttu-id="4b557-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4b557-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b557-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b557-115">CommonParameters</span></span>
<span data-ttu-id="4b557-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4b557-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b557-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b557-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b557-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b557-118">INPUTS</span></span>

### <span data-ttu-id="4b557-119">System. String</span><span class="sxs-lookup"><span data-stu-id="4b557-119">System.String</span></span>

## <span data-ttu-id="4b557-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b557-120">OUTPUTS</span></span>

### <span data-ttu-id="4b557-121">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4b557-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4b557-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4b557-122">NOTES</span></span>

## <span data-ttu-id="4b557-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4b557-123">RELATED LINKS</span></span>

[<span data-ttu-id="4b557-124">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4b557-124">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


