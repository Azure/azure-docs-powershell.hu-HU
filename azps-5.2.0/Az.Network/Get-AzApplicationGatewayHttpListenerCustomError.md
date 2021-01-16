---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 34f92bfa7566679c4cee9f7a4281ac15c55676b4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326293"
---
# <span data-ttu-id="dd0fd-101">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="dd0fd-101">Get-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="dd0fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd0fd-102">SYNOPSIS</span></span>
<span data-ttu-id="dd0fd-103">Egyéni hiba(oka)t kap egy alkalmazásátjáró http-hallgatója által.</span><span class="sxs-lookup"><span data-stu-id="dd0fd-103">Gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="dd0fd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dd0fd-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListenerCustomError [-StatusCode <String>]
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd0fd-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dd0fd-105">DESCRIPTION</span></span>
<span data-ttu-id="dd0fd-106">A **Get-AzApplicationGatewayCustomError** parancsmag egyéni hiba(oka)t kap egy alkalmazásátjáró http-hallgatója által.</span><span class="sxs-lookup"><span data-stu-id="dd0fd-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="dd0fd-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dd0fd-107">EXAMPLES</span></span>

### <span data-ttu-id="dd0fd-108">1. példa: Egyéni hibát kap egy http-hallgatóban</span><span class="sxs-lookup"><span data-stu-id="dd0fd-108">Example 1: Gets a custom error in a http listener</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="dd0fd-109">Ez a parancs az 502-es http-állapotkód egyéni hibaüzenetét kapja és adja vissza a http-$listener 01-</span><span class="sxs-lookup"><span data-stu-id="dd0fd-109">This command gets and returns the custom error of http status code 502 from the http listener $listener01.</span></span>

### <span data-ttu-id="dd0fd-110">2. példa: Az összes egyéni hiba listájának lekérte egy http-hallgatóban</span><span class="sxs-lookup"><span data-stu-id="dd0fd-110">Example 2: Gets the list of all custom errors in a http listener</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -HttpListener $listener01
```

<span data-ttu-id="dd0fd-111">Ez a parancs be- és visszaadja az összes egyéni hiba listáját a http-hallgatótól $listener 01.</span><span class="sxs-lookup"><span data-stu-id="dd0fd-111">This command gets and returns the list of all custom errors from the http listener $listener01.</span></span>

## <span data-ttu-id="dd0fd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd0fd-112">PARAMETERS</span></span>

### <span data-ttu-id="dd0fd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd0fd-113">-DefaultProfile</span></span>
<span data-ttu-id="dd0fd-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dd0fd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd0fd-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="dd0fd-115">-HttpListener</span></span>
<span data-ttu-id="dd0fd-116">The Application Gateway Http Listener</span><span class="sxs-lookup"><span data-stu-id="dd0fd-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="dd0fd-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="dd0fd-117">-StatusCode</span></span>
<span data-ttu-id="dd0fd-118">Az alkalmazás-átjáró ügyfélhiba állapotkódja.</span><span class="sxs-lookup"><span data-stu-id="dd0fd-118">Status code of the application gateway customer error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd0fd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd0fd-119">CommonParameters</span></span>
<span data-ttu-id="dd0fd-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd0fd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd0fd-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd0fd-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd0fd-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dd0fd-122">INPUTS</span></span>

### <span data-ttu-id="dd0fd-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="dd0fd-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="dd0fd-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd0fd-124">OUTPUTS</span></span>

### <span data-ttu-id="dd0fd-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="dd0fd-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="dd0fd-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dd0fd-126">NOTES</span></span>

## <span data-ttu-id="dd0fd-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd0fd-127">RELATED LINKS</span></span>

[<span data-ttu-id="dd0fd-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="dd0fd-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="dd0fd-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="dd0fd-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="dd0fd-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="dd0fd-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
