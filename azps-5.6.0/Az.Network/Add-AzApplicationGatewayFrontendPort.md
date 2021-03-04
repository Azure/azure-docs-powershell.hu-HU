---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40198C86-A4EB-494A-86D5-DF632518EB95
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 5926b2fb4b97d42ff8743ad227fdfb1b32326a20
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926601"
---
# <span data-ttu-id="dc68f-101">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="dc68f-101">Add-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="dc68f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc68f-102">SYNOPSIS</span></span>
<span data-ttu-id="dc68f-103">Előlapi portot ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="dc68f-103">Adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="dc68f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dc68f-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc68f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dc68f-105">DESCRIPTION</span></span>
<span data-ttu-id="dc68f-106">Az **Add-AzApplicationGatewayFrontendPort** parancsmag előtér-portot ad egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="dc68f-106">The **Add-AzApplicationGatewayFrontendPort** cmdlet adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="dc68f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dc68f-107">EXAMPLES</span></span>

### <span data-ttu-id="dc68f-108">1. példa: Előlapi port hozzáadása egy alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="dc68f-108">Example 1: Add a front-end port to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="dc68f-109">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót kapja meg, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="dc68f-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="dc68f-110">A második parancs hozzáadja a 80-as portot előlapi portként a $AppGw és a port FrontEndPort01 nevet ad.</span><span class="sxs-lookup"><span data-stu-id="dc68f-110">The second command adds port 80 as a front-end port for the application gateway stored in $AppGw and names the port FrontEndPort01.</span></span>

## <span data-ttu-id="dc68f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc68f-111">PARAMETERS</span></span>

### <span data-ttu-id="dc68f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dc68f-112">-ApplicationGateway</span></span>
<span data-ttu-id="dc68f-113">Azt az alkalmazás-átjárót adja meg, amelyhez ez a parancsmag előtűnő portot ad.</span><span class="sxs-lookup"><span data-stu-id="dc68f-113">Specifies the application gateway to which this cmdlet adds a front-end port.</span></span>

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

### <span data-ttu-id="dc68f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc68f-114">-DefaultProfile</span></span>
<span data-ttu-id="dc68f-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dc68f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc68f-116">-Name</span><span class="sxs-lookup"><span data-stu-id="dc68f-116">-Name</span></span>
<span data-ttu-id="dc68f-117">Az előlapi port nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc68f-117">Specifies the name of the front-end port.</span></span>

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

### <span data-ttu-id="dc68f-118">-Port</span><span class="sxs-lookup"><span data-stu-id="dc68f-118">-Port</span></span>
<span data-ttu-id="dc68f-119">A portszámot adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc68f-119">Specifies the port number.</span></span>

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

### <span data-ttu-id="dc68f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc68f-120">CommonParameters</span></span>
<span data-ttu-id="dc68f-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc68f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc68f-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc68f-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc68f-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dc68f-123">INPUTS</span></span>

### <span data-ttu-id="dc68f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dc68f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dc68f-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc68f-125">OUTPUTS</span></span>

### <span data-ttu-id="dc68f-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dc68f-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dc68f-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dc68f-127">NOTES</span></span>

## <span data-ttu-id="dc68f-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dc68f-128">RELATED LINKS</span></span>

[<span data-ttu-id="dc68f-129">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="dc68f-129">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="dc68f-130">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="dc68f-130">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="dc68f-131">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="dc68f-131">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="dc68f-132">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="dc68f-132">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


