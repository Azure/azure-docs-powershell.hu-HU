---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 404a9ff22f6b6af480e167c5a4f958b9ac4b5d52
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025203"
---
# <span data-ttu-id="86b49-101">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="86b49-101">Get-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="86b49-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="86b49-102">SYNOPSIS</span></span>
<span data-ttu-id="86b49-103">Beilleszti az alkalmazás átjárójának előtér-végpontját.</span><span class="sxs-lookup"><span data-stu-id="86b49-103">Gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="86b49-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="86b49-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86b49-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="86b49-105">DESCRIPTION</span></span>
<span data-ttu-id="86b49-106">A **Get-AzApplicationGatewayFrontendPort** parancsmag az alkalmazás-átjárók előtér-végpontját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="86b49-106">The **Get-AzApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="86b49-107">Példák</span><span class="sxs-lookup"><span data-stu-id="86b49-107">EXAMPLES</span></span>

### <span data-ttu-id="86b49-108">Példa 1: meghatározott előtér-port beszerzése</span><span class="sxs-lookup"><span data-stu-id="86b49-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="86b49-109">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót a ResourceGroup01 nevű erőforráscsoport nevéből, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="86b49-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="86b49-110">A második parancs a FrontEndPort01 nevű előtér-portot kapja $AppGw és a $FrontEndPort változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="86b49-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="86b49-111">2. példa: az előtér-portok listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="86b49-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzApplicationGatewayFrontendPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="86b49-112">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót a ResourceGroup01 nevű erőforráscsoport nevéből, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="86b49-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="86b49-113">A második parancs beolvassa az előtér-portok listáját a $AppGwból, és a $FrontEndPorts változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="86b49-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="86b49-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="86b49-114">PARAMETERS</span></span>

### <span data-ttu-id="86b49-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="86b49-115">-ApplicationGateway</span></span>
<span data-ttu-id="86b49-116">Megadja az előtér-portot tartalmazó Application Gateway-objektumot.</span><span class="sxs-lookup"><span data-stu-id="86b49-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="86b49-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86b49-117">-DefaultProfile</span></span>
<span data-ttu-id="86b49-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="86b49-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86b49-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="86b49-119">-Name</span></span>
<span data-ttu-id="86b49-120">A beolvasott előtér-port nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="86b49-120">Specifies the name of the front-end port to get.</span></span>

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

### <span data-ttu-id="86b49-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86b49-121">CommonParameters</span></span>
<span data-ttu-id="86b49-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="86b49-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86b49-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="86b49-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86b49-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="86b49-124">INPUTS</span></span>

### <span data-ttu-id="86b49-125">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="86b49-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="86b49-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86b49-126">OUTPUTS</span></span>

### <span data-ttu-id="86b49-127">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="86b49-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="86b49-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="86b49-128">NOTES</span></span>

## <span data-ttu-id="86b49-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86b49-129">RELATED LINKS</span></span>

[<span data-ttu-id="86b49-130">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="86b49-130">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="86b49-131">Új – AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="86b49-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="86b49-132">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="86b49-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="86b49-133">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="86b49-133">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


