---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 82675befb6a900bacdead036f323959e1e7a72a9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342257"
---
# <span data-ttu-id="ac735-101">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="ac735-101">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="ac735-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac735-102">SYNOPSIS</span></span>
<span data-ttu-id="ac735-103">Eltávolít egy egyéni hibát egy alkalmazásátjáró http-hallgatója elől.</span><span class="sxs-lookup"><span data-stu-id="ac735-103">Removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="ac735-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ac735-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ac735-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ac735-105">DESCRIPTION</span></span>
<span data-ttu-id="ac735-106">A **Remove-AzApplicationGatewayCustomError** parancsmag eltávolít egy egyéni hibát egy alkalmazásátjáró http-hallgatója elől.</span><span class="sxs-lookup"><span data-stu-id="ac735-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="ac735-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ac735-107">EXAMPLES</span></span>

### <span data-ttu-id="ac735-108">1. példa: Egyéni hiba eltávolítása a http-hallgatótól</span><span class="sxs-lookup"><span data-stu-id="ac735-108">Example 1: Removes custom error from a http listener</span></span>
```powershell
PS C:\> $updatedlistener = Remove-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="ac735-109">Ez a parancs eltávolítja az 502-es http-állapotkódot a http$listener 01-es állapotkódból, és visszaadja a frissített hallgatót.</span><span class="sxs-lookup"><span data-stu-id="ac735-109">This command removes the custom error of http status code 502 from the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="ac735-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac735-110">PARAMETERS</span></span>

### <span data-ttu-id="ac735-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac735-111">-DefaultProfile</span></span>
<span data-ttu-id="ac735-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ac735-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac735-113">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="ac735-113">-HttpListener</span></span>
<span data-ttu-id="ac735-114">The Application Gateway Http Listener</span><span class="sxs-lookup"><span data-stu-id="ac735-114">The Application Gateway Http Listener</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac735-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="ac735-115">-StatusCode</span></span>
<span data-ttu-id="ac735-116">Az alkalmazás-átjáró ügyfélhiba állapotkódja.</span><span class="sxs-lookup"><span data-stu-id="ac735-116">Status code of the application gateway customer error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac735-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac735-117">CommonParameters</span></span>
<span data-ttu-id="ac735-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac735-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac735-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac735-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac735-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ac735-120">INPUTS</span></span>

### <span data-ttu-id="ac735-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ac735-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="ac735-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac735-122">OUTPUTS</span></span>

### <span data-ttu-id="ac735-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ac735-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="ac735-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ac735-124">NOTES</span></span>

## <span data-ttu-id="ac735-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ac735-125">RELATED LINKS</span></span>

[<span data-ttu-id="ac735-126">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="ac735-126">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="ac735-127">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="ac735-127">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="ac735-128">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="ac735-128">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
