---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
ms.openlocfilehash: 6c2de883a797c445105edddfc562bc2d494fd234
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493406"
---
# <span data-ttu-id="e1a50-101">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1a50-101">Stop-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="e1a50-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e1a50-102">SYNOPSIS</span></span>
<span data-ttu-id="e1a50-103">Az alkalmazás-átjáró leállítása</span><span class="sxs-lookup"><span data-stu-id="e1a50-103">Stops an application gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1a50-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e1a50-104">SYNTAX</span></span>

```
Stop-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1a50-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e1a50-105">DESCRIPTION</span></span>
<span data-ttu-id="e1a50-106">A **stop-AzureRmApplicationGateway** parancsmag leállítja az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="e1a50-106">The **Stop-AzureRmApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="e1a50-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e1a50-107">EXAMPLES</span></span>

### <span data-ttu-id="e1a50-108">1. példa: az alkalmazás-átjáró leállítása</span><span class="sxs-lookup"><span data-stu-id="e1a50-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="e1a50-109">Ez a parancs leállítja a $AppGw változóban tárolt alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="e1a50-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="e1a50-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e1a50-110">PARAMETERS</span></span>

### <span data-ttu-id="e1a50-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1a50-111">-ApplicationGateway</span></span>
<span data-ttu-id="e1a50-112">Annak az alkalmazásnak az átjáróját adja meg, amely a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="e1a50-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="e1a50-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1a50-113">-DefaultProfile</span></span>
<span data-ttu-id="e1a50-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e1a50-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1a50-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1a50-115">CommonParameters</span></span>
<span data-ttu-id="e1a50-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e1a50-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1a50-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1a50-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1a50-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1a50-118">INPUTS</span></span>

### <span data-ttu-id="e1a50-119">System. String</span><span class="sxs-lookup"><span data-stu-id="e1a50-119">System.String</span></span>

## <span data-ttu-id="e1a50-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1a50-120">OUTPUTS</span></span>

### <span data-ttu-id="e1a50-121">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1a50-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e1a50-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e1a50-122">NOTES</span></span>

## <span data-ttu-id="e1a50-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1a50-123">RELATED LINKS</span></span>

[<span data-ttu-id="e1a50-124">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1a50-124">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="e1a50-125">Új – AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1a50-125">New-AzureRmApplicationGateway</span></span>](./New-AzureRmApplicationGateway.md)

[<span data-ttu-id="e1a50-126">Remove-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1a50-126">Remove-AzureRmApplicationGateway</span></span>](./Remove-AzureRmApplicationGateway.md)

[<span data-ttu-id="e1a50-127">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1a50-127">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)

[<span data-ttu-id="e1a50-128">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1a50-128">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


