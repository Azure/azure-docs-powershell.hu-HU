---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40198C86-A4EB-494A-86D5-DF632518EB95
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 9cd7cd0b859ff806b084ebfe1c76e07aed3a7c43
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161227"
---
# <span data-ttu-id="5a7ad-101">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5a7ad-101">Add-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="5a7ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a7ad-102">SYNOPSIS</span></span>
<span data-ttu-id="5a7ad-103">Előlapi portot ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="5a7ad-103">Adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="5a7ad-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5a7ad-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a7ad-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5a7ad-105">DESCRIPTION</span></span>
<span data-ttu-id="5a7ad-106">Az **Add-AzApplicationGatewayFrontendPort** parancsmag előtér-portot ad egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="5a7ad-106">The **Add-AzApplicationGatewayFrontendPort** cmdlet adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="5a7ad-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5a7ad-107">EXAMPLES</span></span>

### <span data-ttu-id="5a7ad-108">1. példa: Előlapi port hozzáadása egy alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="5a7ad-108">Example 1: Add a front-end port to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="5a7ad-109">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót kapja meg, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="5a7ad-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="5a7ad-110">A második parancs hozzáadja a 80-as portot előlapi portként a $AppGw és a port FrontEndPort01 nevet ad.</span><span class="sxs-lookup"><span data-stu-id="5a7ad-110">The second command adds port 80 as a front-end port for the application gateway stored in $AppGw and names the port FrontEndPort01.</span></span>

## <span data-ttu-id="5a7ad-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a7ad-111">PARAMETERS</span></span>

### <span data-ttu-id="5a7ad-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5a7ad-112">-ApplicationGateway</span></span>
<span data-ttu-id="5a7ad-113">Azt az alkalmazás-átjárót adja meg, amelyhez ez a parancsmag előtűnő portot ad.</span><span class="sxs-lookup"><span data-stu-id="5a7ad-113">Specifies the application gateway to which this cmdlet adds a front-end port.</span></span>

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

### <span data-ttu-id="5a7ad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a7ad-114">-DefaultProfile</span></span>
<span data-ttu-id="5a7ad-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5a7ad-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a7ad-116">-Name</span><span class="sxs-lookup"><span data-stu-id="5a7ad-116">-Name</span></span>
<span data-ttu-id="5a7ad-117">Az előlapi port nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a7ad-117">Specifies the name of the front-end port.</span></span>

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

### <span data-ttu-id="5a7ad-118">-Port</span><span class="sxs-lookup"><span data-stu-id="5a7ad-118">-Port</span></span>
<span data-ttu-id="5a7ad-119">A portszámot adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a7ad-119">Specifies the port number.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a7ad-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a7ad-120">CommonParameters</span></span>
<span data-ttu-id="5a7ad-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a7ad-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a7ad-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a7ad-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a7ad-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a7ad-123">INPUTS</span></span>

### <span data-ttu-id="5a7ad-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5a7ad-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5a7ad-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a7ad-125">OUTPUTS</span></span>

### <span data-ttu-id="5a7ad-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5a7ad-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5a7ad-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5a7ad-127">NOTES</span></span>

## <span data-ttu-id="5a7ad-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a7ad-128">RELATED LINKS</span></span>

[<span data-ttu-id="5a7ad-129">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5a7ad-129">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="5a7ad-130">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5a7ad-130">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="5a7ad-131">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5a7ad-131">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="5a7ad-132">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5a7ad-132">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


