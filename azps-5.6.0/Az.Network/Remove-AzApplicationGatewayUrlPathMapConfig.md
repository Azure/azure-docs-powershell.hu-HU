---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 1d9caf3c95d7f8a508a41b8c047684b86c66227a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941697"
---
# <span data-ttu-id="bdede-101">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="bdede-101">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="bdede-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdede-102">SYNOPSIS</span></span>
<span data-ttu-id="bdede-103">Eltávolítja egy háttérkiszolgáló-készlet URL-útvonal-megfeleltetését.</span><span class="sxs-lookup"><span data-stu-id="bdede-103">Removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="bdede-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bdede-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdede-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bdede-105">DESCRIPTION</span></span>
<span data-ttu-id="bdede-106">A **Remove-AzApplicationGatewayUrlPathMapConfig** parancsmag eltávolítja a háttérkiszolgáló-készlet URL-útvonal-megfeleltetését.</span><span class="sxs-lookup"><span data-stu-id="bdede-106">The **Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="bdede-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bdede-107">EXAMPLES</span></span>

### <span data-ttu-id="bdede-108">1. példa: URL-útvonal-megfeleltetés eltávolítása egy alkalmazás-átjáróból</span><span class="sxs-lookup"><span data-stu-id="bdede-108">Example 1: Remove an URL path mapping from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="bdede-109">Az első parancs az appGwName nevű alkalmazás-átjárót kapja meg, és az eredményt a $appgw tárolja.</span><span class="sxs-lookup"><span data-stu-id="bdede-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="bdede-110">A második parancs eltávolítja a map01 nevű URL-útvonal-megfeleltetést az alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="bdede-110">The second command removes the URL path mapping named map01 from the application gateway.</span></span>
<span data-ttu-id="bdede-111">A harmadik parancs frissíti az alkalmazás átjáróját.</span><span class="sxs-lookup"><span data-stu-id="bdede-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="bdede-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bdede-112">PARAMETERS</span></span>

### <span data-ttu-id="bdede-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bdede-113">-ApplicationGateway</span></span>
<span data-ttu-id="bdede-114">Megadja azt az alkalmazás átjárót, amelyhez ez a parancsmag eltávolítja az URL-útvonal-leképezés konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="bdede-114">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="bdede-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdede-115">-DefaultProfile</span></span>
<span data-ttu-id="bdede-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bdede-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdede-117">-Name</span><span class="sxs-lookup"><span data-stu-id="bdede-117">-Name</span></span>
<span data-ttu-id="bdede-118">Megadja a parancsmag által a háttérkiszolgálóról eltávolított URL-útvonal-leképezés nevét.</span><span class="sxs-lookup"><span data-stu-id="bdede-118">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="bdede-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdede-119">CommonParameters</span></span>
<span data-ttu-id="bdede-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdede-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdede-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdede-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdede-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bdede-122">INPUTS</span></span>

### <span data-ttu-id="bdede-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bdede-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bdede-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bdede-124">OUTPUTS</span></span>

### <span data-ttu-id="bdede-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bdede-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bdede-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bdede-126">NOTES</span></span>

## <span data-ttu-id="bdede-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bdede-127">RELATED LINKS</span></span>

[<span data-ttu-id="bdede-128">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="bdede-128">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="bdede-129">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="bdede-129">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="bdede-130">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="bdede-130">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="bdede-131">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="bdede-131">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


