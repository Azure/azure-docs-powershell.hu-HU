---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 85C0A1C3-FC6D-496A-B6B5-8DC2A73B8032
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: e134fafb8f7089b803b09a0202d3c43b0948f7ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920994"
---
# <span data-ttu-id="b591f-101">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b591f-101">Set-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="b591f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b591f-102">SYNOPSIS</span></span>
<span data-ttu-id="b591f-103">Módosítja egy alkalmazás átjárójának előlapi portját.</span><span class="sxs-lookup"><span data-stu-id="b591f-103">Modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="b591f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b591f-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b591f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b591f-105">DESCRIPTION</span></span>
<span data-ttu-id="b591f-106">A **Set-AzApplicationGatewayFrontendPort** parancsmag módosítja az alkalmazás-átjárók előtér-portját.</span><span class="sxs-lookup"><span data-stu-id="b591f-106">The **Set-AzApplicationGatewayFrontendPort** cmdlet modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="b591f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b591f-107">EXAMPLES</span></span>

### <span data-ttu-id="b591f-108">1. példa: Egy alkalmazás átjárójának előlapi portjának beállítása 80-ra</span><span class="sxs-lookup"><span data-stu-id="b591f-108">Example 1: Set an application gateway front-end port to 80</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="b591f-109">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót kapja meg, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="b591f-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b591f-110">A második parancs módosítja az átjárót a $AppGw és a 80-as portot használja a FrontEndPort01 nevű előlapi porthoz.</span><span class="sxs-lookup"><span data-stu-id="b591f-110">The second command modifies the gateway in $AppGw to use port 80 for the front-end port named FrontEndPort01.</span></span>

## <span data-ttu-id="b591f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b591f-111">PARAMETERS</span></span>

### <span data-ttu-id="b591f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b591f-112">-ApplicationGateway</span></span>
<span data-ttu-id="b591f-113">Azt az alkalmazás-átjáróobjektumot adja meg, amellyel ez a parancsmag társítja az előlapi portot.</span><span class="sxs-lookup"><span data-stu-id="b591f-113">Specifies the application gateway object with which this cmdlet associates the front-end port.</span></span>

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

### <span data-ttu-id="b591f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b591f-114">-DefaultProfile</span></span>
<span data-ttu-id="b591f-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b591f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b591f-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b591f-116">-Name</span></span>
<span data-ttu-id="b591f-117">A módosítani szükséges előlapi port nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b591f-117">Specifies the name of the front-end port to modify.</span></span>

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

### <span data-ttu-id="b591f-118">-Port</span><span class="sxs-lookup"><span data-stu-id="b591f-118">-Port</span></span>
<span data-ttu-id="b591f-119">Az előlapi port portszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b591f-119">Specifies the port number to use for the front-end port.</span></span>

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

### <span data-ttu-id="b591f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b591f-120">CommonParameters</span></span>
<span data-ttu-id="b591f-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b591f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b591f-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b591f-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b591f-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b591f-123">INPUTS</span></span>

### <span data-ttu-id="b591f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b591f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b591f-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b591f-125">OUTPUTS</span></span>

### <span data-ttu-id="b591f-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b591f-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b591f-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b591f-127">NOTES</span></span>

## <span data-ttu-id="b591f-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b591f-128">RELATED LINKS</span></span>

[<span data-ttu-id="b591f-129">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b591f-129">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="b591f-130">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b591f-130">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="b591f-131">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b591f-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="b591f-132">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b591f-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)
