---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: d810afe9f5fcf2a1377f55ffe0822d3e71ee409f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359784"
---
# <span data-ttu-id="0559d-101">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="0559d-101">Add-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="0559d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0559d-102">SYNOPSIS</span></span>
<span data-ttu-id="0559d-103">Egyéni hibát ad hozzá egy alkalmazás-átjáró http-hallgatója számára.</span><span class="sxs-lookup"><span data-stu-id="0559d-103">Adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="0559d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0559d-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0559d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0559d-105">DESCRIPTION</span></span>
<span data-ttu-id="0559d-106">Az **Add-AzApplicationGatewayCustomError** parancsmag egyéni hibát ad hozzá egy alkalmazás-átjáró http-hallgatója számára.</span><span class="sxs-lookup"><span data-stu-id="0559d-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="0559d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0559d-107">EXAMPLES</span></span>

### <span data-ttu-id="0559d-108">1. példa: Egyéni hiba hozzáadása a http-hallgatói szinthez</span><span class="sxs-lookup"><span data-stu-id="0559d-108">Example 1: Adds custom error to http listener level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="0559d-109">Ez a parancs hozzáadja az 502-es http-állapotkódot a http$listener 01-es állapotkódhoz, és visszaadja a frissített hallgatót.</span><span class="sxs-lookup"><span data-stu-id="0559d-109">This command adds a custom error of http status code 502 to the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="0559d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0559d-110">PARAMETERS</span></span>

### <span data-ttu-id="0559d-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="0559d-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="0559d-112">Hibalap URL-címe az alkalmazás-átjáró ügyfélalkalmazásának hibaüzenetéhez.</span><span class="sxs-lookup"><span data-stu-id="0559d-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="0559d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0559d-113">-DefaultProfile</span></span>
<span data-ttu-id="0559d-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0559d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0559d-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="0559d-115">-HttpListener</span></span>
<span data-ttu-id="0559d-116">The Application Gateway Http Listener</span><span class="sxs-lookup"><span data-stu-id="0559d-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="0559d-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="0559d-117">-StatusCode</span></span>
<span data-ttu-id="0559d-118">Az alkalmazás-átjáró ügyfélhiba állapotkódja.</span><span class="sxs-lookup"><span data-stu-id="0559d-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="0559d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0559d-119">CommonParameters</span></span>
<span data-ttu-id="0559d-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0559d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0559d-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0559d-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0559d-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0559d-122">INPUTS</span></span>

### <span data-ttu-id="0559d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="0559d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="0559d-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0559d-124">OUTPUTS</span></span>

### <span data-ttu-id="0559d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="0559d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="0559d-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0559d-126">NOTES</span></span>

## <span data-ttu-id="0559d-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0559d-127">RELATED LINKS</span></span>

[<span data-ttu-id="0559d-128">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="0559d-128">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="0559d-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="0559d-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="0559d-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="0559d-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
