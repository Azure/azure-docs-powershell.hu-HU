---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 85C0A1C3-FC6D-496A-B6B5-8DC2A73B8032
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 08637412afafe9220107e95dd3cb7dcc5154ba26
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011353"
---
# <span data-ttu-id="4eef4-101">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="4eef4-101">Set-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="4eef4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4eef4-102">SYNOPSIS</span></span>
<span data-ttu-id="4eef4-103">Az alkalmazás-átjáró előtér-portjának módosítása.</span><span class="sxs-lookup"><span data-stu-id="4eef4-103">Modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="4eef4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4eef4-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4eef4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4eef4-105">DESCRIPTION</span></span>
<span data-ttu-id="4eef4-106">A **set-AzApplicationGatewayFrontendPort** parancsmag az alkalmazás-átjárók előtér-portját módosítja.</span><span class="sxs-lookup"><span data-stu-id="4eef4-106">The **Set-AzApplicationGatewayFrontendPort** cmdlet modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="4eef4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4eef4-107">EXAMPLES</span></span>

### <span data-ttu-id="4eef4-108">1. példa: az alkalmazás-átjáró előtér-Port beállítása az 80-hoz</span><span class="sxs-lookup"><span data-stu-id="4eef4-108">Example 1: Set an application gateway front-end port to 80</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="4eef4-109">Az első parancs megkapja a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4eef4-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4eef4-110">A második parancs módosítja az átjárót a $AppGw-ban, hogy a 80-ös portot használja a FrontEndPort01 nevű előtér-porthoz.</span><span class="sxs-lookup"><span data-stu-id="4eef4-110">The second command modifies the gateway in $AppGw to use port 80 for the front-end port named FrontEndPort01.</span></span>

## <span data-ttu-id="4eef4-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4eef4-111">PARAMETERS</span></span>

### <span data-ttu-id="4eef4-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4eef4-112">-ApplicationGateway</span></span>
<span data-ttu-id="4eef4-113">Azt az Application Gateway-objektumot adja meg, amelyhez a parancsmag az előtér-portot társítja.</span><span class="sxs-lookup"><span data-stu-id="4eef4-113">Specifies the application gateway object with which this cmdlet associates the front-end port.</span></span>

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

### <span data-ttu-id="4eef4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eef4-114">-DefaultProfile</span></span>
<span data-ttu-id="4eef4-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4eef4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4eef4-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4eef4-116">-Name</span></span>
<span data-ttu-id="4eef4-117">A módosítani kívánt előtér-végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4eef4-117">Specifies the name of the front-end port to modify.</span></span>

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

### <span data-ttu-id="4eef4-118">-Port</span><span class="sxs-lookup"><span data-stu-id="4eef4-118">-Port</span></span>
<span data-ttu-id="4eef4-119">Az előtér-porthoz használni kívánt portszámot adja meg.</span><span class="sxs-lookup"><span data-stu-id="4eef4-119">Specifies the port number to use for the front-end port.</span></span>

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

### <span data-ttu-id="4eef4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eef4-120">CommonParameters</span></span>
<span data-ttu-id="4eef4-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4eef4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eef4-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4eef4-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eef4-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4eef4-123">INPUTS</span></span>

### <span data-ttu-id="4eef4-124">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4eef4-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4eef4-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4eef4-125">OUTPUTS</span></span>

### <span data-ttu-id="4eef4-126">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4eef4-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4eef4-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4eef4-127">NOTES</span></span>

## <span data-ttu-id="4eef4-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4eef4-128">RELATED LINKS</span></span>

[<span data-ttu-id="4eef4-129">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="4eef4-129">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="4eef4-130">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="4eef4-130">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="4eef4-131">Új – AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="4eef4-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="4eef4-132">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="4eef4-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)
