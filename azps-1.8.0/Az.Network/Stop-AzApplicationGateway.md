---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
ms.openlocfilehash: 921c770cce5d1f597fa0af96dd30014f9dacb2fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669941"
---
# <span data-ttu-id="48c68-101">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48c68-101">Stop-AzApplicationGateway</span></span>

## <span data-ttu-id="48c68-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="48c68-102">SYNOPSIS</span></span>
<span data-ttu-id="48c68-103">Az alkalmazás-átjáró leállítása</span><span class="sxs-lookup"><span data-stu-id="48c68-103">Stops an application gateway</span></span>

## <span data-ttu-id="48c68-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="48c68-104">SYNTAX</span></span>

```
Stop-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48c68-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="48c68-105">DESCRIPTION</span></span>
<span data-ttu-id="48c68-106">A **stop-AzApplicationGateway** parancsmag leállítja az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="48c68-106">The **Stop-AzApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="48c68-107">Példák</span><span class="sxs-lookup"><span data-stu-id="48c68-107">EXAMPLES</span></span>

### <span data-ttu-id="48c68-108">1. példa: az alkalmazás-átjáró leállítása</span><span class="sxs-lookup"><span data-stu-id="48c68-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="48c68-109">Ez a parancs leállítja a $AppGw változóban tárolt alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="48c68-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="48c68-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="48c68-110">PARAMETERS</span></span>

### <span data-ttu-id="48c68-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48c68-111">-ApplicationGateway</span></span>
<span data-ttu-id="48c68-112">Annak az alkalmazásnak az átjáróját adja meg, amely a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="48c68-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="48c68-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48c68-113">-AsJob</span></span>
<span data-ttu-id="48c68-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="48c68-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="48c68-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48c68-115">-DefaultProfile</span></span>
<span data-ttu-id="48c68-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="48c68-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48c68-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48c68-117">CommonParameters</span></span>
<span data-ttu-id="48c68-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="48c68-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48c68-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48c68-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48c68-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="48c68-120">INPUTS</span></span>

### <span data-ttu-id="48c68-121">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48c68-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="48c68-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48c68-122">OUTPUTS</span></span>

### <span data-ttu-id="48c68-123">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48c68-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="48c68-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="48c68-124">NOTES</span></span>

## <span data-ttu-id="48c68-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48c68-125">RELATED LINKS</span></span>

[<span data-ttu-id="48c68-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48c68-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="48c68-127">Új – AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48c68-127">New-AzApplicationGateway</span></span>](./New-AzApplicationGateway.md)

[<span data-ttu-id="48c68-128">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48c68-128">Remove-AzApplicationGateway</span></span>](./Remove-AzApplicationGateway.md)

[<span data-ttu-id="48c68-129">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48c68-129">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)

[<span data-ttu-id="48c68-130">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48c68-130">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


