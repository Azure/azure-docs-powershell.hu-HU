---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmApplicationGateway.md
ms.openlocfilehash: 8d6f52401544d723f7f5303aa45722d828a6ac59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493407"
---
# <span data-ttu-id="cdec7-101">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cdec7-101">Start-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="cdec7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cdec7-102">SYNOPSIS</span></span>
<span data-ttu-id="cdec7-103">Elindítja az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="cdec7-103">Starts an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdec7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cdec7-104">SYNTAX</span></span>

```
Start-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdec7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cdec7-105">DESCRIPTION</span></span>
<span data-ttu-id="cdec7-106">A **Start-AzureRmApplicationGateway** parancsmag az Azure Application Gatewayt indítja el.</span><span class="sxs-lookup"><span data-stu-id="cdec7-106">The **Start-AzureRmApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="cdec7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cdec7-107">EXAMPLES</span></span>

### <span data-ttu-id="cdec7-108">Example1: alkalmazás-átjáró indítása</span><span class="sxs-lookup"><span data-stu-id="cdec7-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="cdec7-109">Ez a parancs elindítja az $AppGw változóban tárolt alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="cdec7-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="cdec7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cdec7-110">PARAMETERS</span></span>

### <span data-ttu-id="cdec7-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cdec7-111">-ApplicationGateway</span></span>
<span data-ttu-id="cdec7-112">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag elindul.</span><span class="sxs-lookup"><span data-stu-id="cdec7-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="cdec7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdec7-113">-DefaultProfile</span></span>
<span data-ttu-id="cdec7-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cdec7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cdec7-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdec7-115">CommonParameters</span></span>
<span data-ttu-id="cdec7-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cdec7-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdec7-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdec7-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdec7-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cdec7-118">INPUTS</span></span>

### <span data-ttu-id="cdec7-119">System. String</span><span class="sxs-lookup"><span data-stu-id="cdec7-119">System.String</span></span>

## <span data-ttu-id="cdec7-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cdec7-120">OUTPUTS</span></span>

### <span data-ttu-id="cdec7-121">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cdec7-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cdec7-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cdec7-122">NOTES</span></span>

## <span data-ttu-id="cdec7-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cdec7-123">RELATED LINKS</span></span>

[<span data-ttu-id="cdec7-124">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cdec7-124">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


