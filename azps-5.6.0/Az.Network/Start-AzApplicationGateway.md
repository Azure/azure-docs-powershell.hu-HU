---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/powershell/module/az.network/start-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
ms.openlocfilehash: 4d2f3f225e185678dd1e3b0047810a5e68d4273f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918617"
---
# <span data-ttu-id="1895f-101">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1895f-101">Start-AzApplicationGateway</span></span>

## <span data-ttu-id="1895f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1895f-102">SYNOPSIS</span></span>
<span data-ttu-id="1895f-103">Elindít egy alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="1895f-103">Starts an application gateway.</span></span>

## <span data-ttu-id="1895f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1895f-104">SYNTAX</span></span>

```
Start-AzApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1895f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1895f-105">DESCRIPTION</span></span>
<span data-ttu-id="1895f-106">A **Start-AzApplicationGateway** parancsmag elindít egy Azure-alkalmazás-átjárót</span><span class="sxs-lookup"><span data-stu-id="1895f-106">The **Start-AzApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="1895f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1895f-107">EXAMPLES</span></span>

### <span data-ttu-id="1895f-108">Példa1: Alkalmazás-átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="1895f-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="1895f-109">Ez a parancs elindítja a változóban tárolt $AppGw.</span><span class="sxs-lookup"><span data-stu-id="1895f-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="1895f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1895f-110">PARAMETERS</span></span>

### <span data-ttu-id="1895f-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1895f-111">-ApplicationGateway</span></span>
<span data-ttu-id="1895f-112">A parancsmag által elindított alkalmazás-átjáró.</span><span class="sxs-lookup"><span data-stu-id="1895f-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="1895f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1895f-113">-DefaultProfile</span></span>
<span data-ttu-id="1895f-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1895f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1895f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1895f-115">CommonParameters</span></span>
<span data-ttu-id="1895f-116">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1895f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1895f-117">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1895f-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1895f-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1895f-118">INPUTS</span></span>

### <span data-ttu-id="1895f-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1895f-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1895f-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1895f-120">OUTPUTS</span></span>

### <span data-ttu-id="1895f-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1895f-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1895f-122">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1895f-122">NOTES</span></span>

## <span data-ttu-id="1895f-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1895f-123">RELATED LINKS</span></span>

[<span data-ttu-id="1895f-124">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1895f-124">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


