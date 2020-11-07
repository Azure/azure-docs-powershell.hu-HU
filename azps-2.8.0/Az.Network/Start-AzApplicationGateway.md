---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
ms.openlocfilehash: f90e35e0b8a88d7fa7b5089adf205bf6fe14e18f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838296"
---
# <span data-ttu-id="53a22-101">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="53a22-101">Start-AzApplicationGateway</span></span>

## <span data-ttu-id="53a22-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="53a22-102">SYNOPSIS</span></span>
<span data-ttu-id="53a22-103">Elindítja az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="53a22-103">Starts an application gateway.</span></span>

## <span data-ttu-id="53a22-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="53a22-104">SYNTAX</span></span>

```
Start-AzApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53a22-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="53a22-105">DESCRIPTION</span></span>
<span data-ttu-id="53a22-106">A **Start-AzApplicationGateway** parancsmag az Azure Application Gatewayt indítja el.</span><span class="sxs-lookup"><span data-stu-id="53a22-106">The **Start-AzApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="53a22-107">Példák</span><span class="sxs-lookup"><span data-stu-id="53a22-107">EXAMPLES</span></span>

### <span data-ttu-id="53a22-108">Example1: alkalmazás-átjáró indítása</span><span class="sxs-lookup"><span data-stu-id="53a22-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="53a22-109">Ez a parancs elindítja az $AppGw változóban tárolt alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="53a22-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="53a22-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="53a22-110">PARAMETERS</span></span>

### <span data-ttu-id="53a22-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="53a22-111">-ApplicationGateway</span></span>
<span data-ttu-id="53a22-112">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag elindul.</span><span class="sxs-lookup"><span data-stu-id="53a22-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="53a22-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53a22-113">-DefaultProfile</span></span>
<span data-ttu-id="53a22-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="53a22-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53a22-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53a22-115">CommonParameters</span></span>
<span data-ttu-id="53a22-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="53a22-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53a22-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53a22-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53a22-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="53a22-118">INPUTS</span></span>

### <span data-ttu-id="53a22-119">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="53a22-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="53a22-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53a22-120">OUTPUTS</span></span>

### <span data-ttu-id="53a22-121">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="53a22-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="53a22-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="53a22-122">NOTES</span></span>

## <span data-ttu-id="53a22-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53a22-123">RELATED LINKS</span></span>

[<span data-ttu-id="53a22-124">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="53a22-124">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


