---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
ms.openlocfilehash: 4c7001bf69e6dc8f418f1bc56867154bf9d769ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845390"
---
# <span data-ttu-id="0a749-101">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0a749-101">Stop-AzApplicationGateway</span></span>

## <span data-ttu-id="0a749-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0a749-102">SYNOPSIS</span></span>
<span data-ttu-id="0a749-103">Az alkalmazás-átjáró leállítása</span><span class="sxs-lookup"><span data-stu-id="0a749-103">Stops an application gateway</span></span>

## <span data-ttu-id="0a749-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0a749-104">SYNTAX</span></span>

```
Stop-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a749-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0a749-105">DESCRIPTION</span></span>
<span data-ttu-id="0a749-106">A **stop-AzApplicationGateway** parancsmag leállítja az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="0a749-106">The **Stop-AzApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="0a749-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0a749-107">EXAMPLES</span></span>

### <span data-ttu-id="0a749-108">1. példa: az alkalmazás-átjáró leállítása</span><span class="sxs-lookup"><span data-stu-id="0a749-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="0a749-109">Ez a parancs leállítja a $AppGw változóban tárolt alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="0a749-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="0a749-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0a749-110">PARAMETERS</span></span>

### <span data-ttu-id="0a749-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0a749-111">-ApplicationGateway</span></span>
<span data-ttu-id="0a749-112">Annak az alkalmazásnak az átjáróját adja meg, amely a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="0a749-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="0a749-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a749-113">-AsJob</span></span>
<span data-ttu-id="0a749-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0a749-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a749-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a749-115">-DefaultProfile</span></span>
<span data-ttu-id="0a749-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0a749-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a749-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a749-117">CommonParameters</span></span>
<span data-ttu-id="0a749-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0a749-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a749-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a749-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a749-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a749-120">INPUTS</span></span>

### <span data-ttu-id="0a749-121">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0a749-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0a749-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a749-122">OUTPUTS</span></span>

### <span data-ttu-id="0a749-123">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0a749-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0a749-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0a749-124">NOTES</span></span>

## <span data-ttu-id="0a749-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a749-125">RELATED LINKS</span></span>

[<span data-ttu-id="0a749-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0a749-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="0a749-127">Új – AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0a749-127">New-AzApplicationGateway</span></span>](./New-AzApplicationGateway.md)

[<span data-ttu-id="0a749-128">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0a749-128">Remove-AzApplicationGateway</span></span>](./Remove-AzApplicationGateway.md)

[<span data-ttu-id="0a749-129">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0a749-129">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)

[<span data-ttu-id="0a749-130">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0a749-130">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


