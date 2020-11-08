---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: ec2c73be940e887b4cd1ca96da1442f8ae007ab6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185962"
---
# <span data-ttu-id="dcac9-101">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="dcac9-101">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="dcac9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dcac9-102">SYNOPSIS</span></span>
<span data-ttu-id="dcac9-103">Eltávolítja az URL-címek elérési útját a backend-kiszolgálók készletéből.</span><span class="sxs-lookup"><span data-stu-id="dcac9-103">Removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="dcac9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dcac9-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcac9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dcac9-105">DESCRIPTION</span></span>
<span data-ttu-id="dcac9-106">A **Remove-AzApplicationGatewayUrlPathMapConfig** parancsmag eltávolítja az URL-elérési utakat a backend-kiszolgálók készletéből.</span><span class="sxs-lookup"><span data-stu-id="dcac9-106">The **Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="dcac9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dcac9-107">EXAMPLES</span></span>

### <span data-ttu-id="dcac9-108">1. példa: az URL-elérési út megfeleltetésének eltávolítása egy alkalmazás-átjáróról</span><span class="sxs-lookup"><span data-stu-id="dcac9-108">Example 1: Remove an URL path mapping from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="dcac9-109">Az első parancs beolvassa a appGwName nevű alkalmazás-átjárót, és az eredményt az $appgw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="dcac9-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="dcac9-110">A második parancs eltávolítja az map01 nevű URL-elérési út megfeleltetését az Application Gateway-ből.</span><span class="sxs-lookup"><span data-stu-id="dcac9-110">The second command removes the URL path mapping named map01 from the application gateway.</span></span>
<span data-ttu-id="dcac9-111">A harmadik parancs frissíti az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="dcac9-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="dcac9-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dcac9-112">PARAMETERS</span></span>

### <span data-ttu-id="dcac9-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dcac9-113">-ApplicationGateway</span></span>
<span data-ttu-id="dcac9-114">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag eltávolítja az URL Path Map-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="dcac9-114">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="dcac9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcac9-115">-DefaultProfile</span></span>
<span data-ttu-id="dcac9-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dcac9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcac9-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dcac9-117">-Name</span></span>
<span data-ttu-id="dcac9-118">Itt adhatja meg az URL-cím elérési útjának nevét, amelyet a parancsmag a backend-kiszolgálóról távolít el.</span><span class="sxs-lookup"><span data-stu-id="dcac9-118">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="dcac9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcac9-119">CommonParameters</span></span>
<span data-ttu-id="dcac9-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dcac9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcac9-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcac9-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcac9-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dcac9-122">INPUTS</span></span>

### <span data-ttu-id="dcac9-123">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dcac9-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dcac9-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dcac9-124">OUTPUTS</span></span>

### <span data-ttu-id="dcac9-125">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dcac9-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dcac9-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dcac9-126">NOTES</span></span>

## <span data-ttu-id="dcac9-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dcac9-127">RELATED LINKS</span></span>

[<span data-ttu-id="dcac9-128">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="dcac9-128">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="dcac9-129">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="dcac9-129">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="dcac9-130">Új – AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="dcac9-130">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="dcac9-131">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="dcac9-131">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)

