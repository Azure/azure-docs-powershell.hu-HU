---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40198C86-A4EB-494A-86D5-DF632518EB95
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: e0ca615d856e7905127c488c17c039b23051cc0a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841878"
---
# <span data-ttu-id="fc755-101">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="fc755-101">Add-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="fc755-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fc755-102">SYNOPSIS</span></span>
<span data-ttu-id="fc755-103">Az előtér-portot hozzáadja az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="fc755-103">Adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="fc755-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fc755-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc755-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fc755-105">DESCRIPTION</span></span>
<span data-ttu-id="fc755-106">Az **Add-AzApplicationGatewayFrontendPort** parancsmag egy előtér-portot ad az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="fc755-106">The **Add-AzApplicationGatewayFrontendPort** cmdlet adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="fc755-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fc755-107">EXAMPLES</span></span>

### <span data-ttu-id="fc755-108">1. példa: előtér-végpont hozzáadása az alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="fc755-108">Example 1: Add a front-end port to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $ AppGw = Add-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="fc755-109">Az első parancs megkapja a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fc755-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="fc755-110">A második parancs hozzáadja a 80-as portot az $AppGw tárolt alkalmazási átjáróhoz, és megnevezi a port FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="fc755-110">The second command adds port 80 as a front-end port for the application gateway stored in $AppGw and names the port FrontEndPort01.</span></span>

## <span data-ttu-id="fc755-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fc755-111">PARAMETERS</span></span>

### <span data-ttu-id="fc755-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fc755-112">-ApplicationGateway</span></span>
<span data-ttu-id="fc755-113">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag az előtér-portot adja hozzá.</span><span class="sxs-lookup"><span data-stu-id="fc755-113">Specifies the application gateway to which this cmdlet adds a front-end port.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc755-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc755-114">-DefaultProfile</span></span>
<span data-ttu-id="fc755-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc755-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc755-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fc755-116">-Name</span></span>
<span data-ttu-id="fc755-117">Az előtér-port nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fc755-117">Specifies the name of the front-end port.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc755-118">-Port</span><span class="sxs-lookup"><span data-stu-id="fc755-118">-Port</span></span>
<span data-ttu-id="fc755-119">A portszámot adja meg.</span><span class="sxs-lookup"><span data-stu-id="fc755-119">Specifies the port number.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc755-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc755-120">CommonParameters</span></span>
<span data-ttu-id="fc755-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fc755-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc755-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc755-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc755-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc755-123">INPUTS</span></span>

### <span data-ttu-id="fc755-124">System. String</span><span class="sxs-lookup"><span data-stu-id="fc755-124">System.String</span></span>

## <span data-ttu-id="fc755-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc755-125">OUTPUTS</span></span>

### <span data-ttu-id="fc755-126">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fc755-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fc755-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fc755-127">NOTES</span></span>

## <span data-ttu-id="fc755-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc755-128">RELATED LINKS</span></span>

[<span data-ttu-id="fc755-129">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="fc755-129">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="fc755-130">Új – AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="fc755-130">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="fc755-131">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="fc755-131">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="fc755-132">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="fc755-132">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


