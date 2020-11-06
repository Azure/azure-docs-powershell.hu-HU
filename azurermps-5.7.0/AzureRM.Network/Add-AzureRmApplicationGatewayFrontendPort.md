---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 40198C86-A4EB-494A-86D5-DF632518EB95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: c9be5f69fc210f68ceb90cfe2e21f5afab164b6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500536"
---
# <span data-ttu-id="831ea-101">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="831ea-101">Add-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="831ea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="831ea-102">SYNOPSIS</span></span>
<span data-ttu-id="831ea-103">Az előtér-portot hozzáadja az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="831ea-103">Adds a front-end port to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="831ea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="831ea-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="831ea-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="831ea-105">DESCRIPTION</span></span>
<span data-ttu-id="831ea-106">Az **Add-AzureRmApplicationGatewayFrontendPort** parancsmag egy előtér-portot ad az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="831ea-106">The **Add-AzureRmApplicationGatewayFrontendPort** cmdlet adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="831ea-107">Példák</span><span class="sxs-lookup"><span data-stu-id="831ea-107">EXAMPLES</span></span>

### <span data-ttu-id="831ea-108">1. példa: előtér-végpont hozzáadása az alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="831ea-108">Example 1: Add a front-end port to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $ AppGw = Add-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="831ea-109">Az első parancs megkapja a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="831ea-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="831ea-110">A második parancs hozzáadja a 80-as portot az $AppGw tárolt alkalmazási átjáróhoz, és megnevezi a port FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="831ea-110">The second command adds port 80 as a front-end port for the application gateway stored in $AppGw and names the port FrontEndPort01.</span></span>

## <span data-ttu-id="831ea-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="831ea-111">PARAMETERS</span></span>

### <span data-ttu-id="831ea-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="831ea-112">-ApplicationGateway</span></span>
<span data-ttu-id="831ea-113">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag az előtér-portot adja hozzá.</span><span class="sxs-lookup"><span data-stu-id="831ea-113">Specifies the application gateway to which this cmdlet adds a front-end port.</span></span>

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

### <span data-ttu-id="831ea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="831ea-114">-DefaultProfile</span></span>
<span data-ttu-id="831ea-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="831ea-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="831ea-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="831ea-116">-Name</span></span>
<span data-ttu-id="831ea-117">Az előtér-port nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="831ea-117">Specifies the name of the front-end port.</span></span>

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

### <span data-ttu-id="831ea-118">-Port</span><span class="sxs-lookup"><span data-stu-id="831ea-118">-Port</span></span>
<span data-ttu-id="831ea-119">A portszámot adja meg.</span><span class="sxs-lookup"><span data-stu-id="831ea-119">Specifies the port number.</span></span>

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

### <span data-ttu-id="831ea-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="831ea-120">CommonParameters</span></span>
<span data-ttu-id="831ea-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="831ea-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="831ea-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="831ea-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="831ea-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="831ea-123">INPUTS</span></span>

### <span data-ttu-id="831ea-124">System. String</span><span class="sxs-lookup"><span data-stu-id="831ea-124">System.String</span></span>

## <span data-ttu-id="831ea-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="831ea-125">OUTPUTS</span></span>

### <span data-ttu-id="831ea-126">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="831ea-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="831ea-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="831ea-127">NOTES</span></span>

## <span data-ttu-id="831ea-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="831ea-128">RELATED LINKS</span></span>

[<span data-ttu-id="831ea-129">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="831ea-129">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="831ea-130">Új – AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="831ea-130">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="831ea-131">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="831ea-131">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="831ea-132">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="831ea-132">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


