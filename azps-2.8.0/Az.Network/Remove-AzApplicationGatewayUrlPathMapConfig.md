---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 27561ec3592633e1e7c668a4d901ba1e7d39c050
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837118"
---
# <span data-ttu-id="a4e5a-101">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a4e5a-101">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="a4e5a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a4e5a-102">SYNOPSIS</span></span>
<span data-ttu-id="a4e5a-103">Eltávolítja az URL-címek elérési útját a backend-kiszolgálók készletéből.</span><span class="sxs-lookup"><span data-stu-id="a4e5a-103">Removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="a4e5a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a4e5a-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4e5a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a4e5a-105">DESCRIPTION</span></span>
<span data-ttu-id="a4e5a-106">A **Remove-AzApplicationGatewayUrlPathMapConfig** parancsmag eltávolítja az URL-elérési utakat a backend-kiszolgálók készletéből.</span><span class="sxs-lookup"><span data-stu-id="a4e5a-106">The **Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="a4e5a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a4e5a-107">EXAMPLES</span></span>

### <span data-ttu-id="a4e5a-108">1. példa: az URL-elérési út megfeleltetésének eltávolítása egy alkalmazás-átjáróról</span><span class="sxs-lookup"><span data-stu-id="a4e5a-108">Example 1: Remove an URL path mapping from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="a4e5a-109">Az első parancs beolvassa a appGwName nevű alkalmazás-átjárót, és az eredményt az $appgw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a4e5a-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="a4e5a-110">A második parancs eltávolítja az map01 nevű URL-elérési út megfeleltetését az Application Gateway-ből.</span><span class="sxs-lookup"><span data-stu-id="a4e5a-110">The second command removes the URL path mapping named map01 from the application gateway.</span></span>
<span data-ttu-id="a4e5a-111">A harmadik parancs frissíti az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="a4e5a-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="a4e5a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a4e5a-112">PARAMETERS</span></span>

### <span data-ttu-id="a4e5a-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a4e5a-113">-ApplicationGateway</span></span>
<span data-ttu-id="a4e5a-114">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag eltávolítja az URL Path Map-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="a4e5a-114">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="a4e5a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4e5a-115">-DefaultProfile</span></span>
<span data-ttu-id="a4e5a-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a4e5a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4e5a-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a4e5a-117">-Name</span></span>
<span data-ttu-id="a4e5a-118">Itt adhatja meg az URL-cím elérési útjának nevét, amelyet a parancsmag a backend-kiszolgálóról távolít el.</span><span class="sxs-lookup"><span data-stu-id="a4e5a-118">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="a4e5a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4e5a-119">CommonParameters</span></span>
<span data-ttu-id="a4e5a-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a4e5a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4e5a-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4e5a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4e5a-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4e5a-122">INPUTS</span></span>

### <span data-ttu-id="a4e5a-123">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a4e5a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a4e5a-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4e5a-124">OUTPUTS</span></span>

### <span data-ttu-id="a4e5a-125">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a4e5a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a4e5a-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a4e5a-126">NOTES</span></span>

## <span data-ttu-id="a4e5a-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4e5a-127">RELATED LINKS</span></span>

[<span data-ttu-id="a4e5a-128">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a4e5a-128">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="a4e5a-129">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a4e5a-129">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="a4e5a-130">Új – AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a4e5a-130">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="a4e5a-131">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a4e5a-131">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


