---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 364C41D0-A5DB-4AEF-853A-FE5A11AD9155
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 2e90ce87e5ab8e33cf1653dd1dbc4cf48ffaf455
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013555"
---
# <span data-ttu-id="f2980-101">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f2980-101">Get-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="f2980-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f2980-102">SYNOPSIS</span></span>
<span data-ttu-id="f2980-103">Beilleszti az alkalmazás átjárójának előtér IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="f2980-103">Gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="f2980-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f2980-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendIPConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2980-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f2980-105">DESCRIPTION</span></span>
<span data-ttu-id="f2980-106">A **Get-AzApplicationGatewayFrontendIPConfig** parancsmag az alkalmazás-átjárók ELŐTÉR IP-konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f2980-106">The **Get-AzApplicationGatewayFrontendIPConfig** cmdlet gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="f2980-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f2980-107">EXAMPLES</span></span>

### <span data-ttu-id="f2980-108">Példa 1: meghatározott előtér-IP-konfiguráció beszerzése</span><span class="sxs-lookup"><span data-stu-id="f2980-108">Example 1: Get a specified front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIP= Get-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -ApplicationGateway $AppGw
```

<span data-ttu-id="f2980-109">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót a ResourceGroup01 nevű erőforráscsoport nevéből, és a $AppGw változóban tárolja. A második parancs beilleszti a FrontEndIP01 nevű előtér IP-konfigurációját a $AppGw, és a $FrontEndIP változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f2980-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the front-end IP configuration named FrontEndIP01 from $AppGw and stores it in the $FrontEndIP variable.</span></span>

### <span data-ttu-id="f2980-110">2. példa: az előtér-IP-konfigurációk listáját tartalmazó lista beszerzése</span><span class="sxs-lookup"><span data-stu-id="f2980-110">Example 2: Get a list of front-end IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIPs= Get-AzApplicationGatewayFrontendIPConfig  -ApplicationGateway $AppGw
```

<span data-ttu-id="f2980-111">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót a ResourceGroup01 nevű erőforráscsoport nevéből, és a $AppGw változóban tárolja. A második parancs beolvassa a $AppGwból az előtér IP-konfigurációjának listáját, és a $FrontEndIPs változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f2980-111">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets a list of the front-end IP configurations from $AppGw and stores it in the $FrontEndIPs variable.</span></span>

## <span data-ttu-id="f2980-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f2980-112">PARAMETERS</span></span>

### <span data-ttu-id="f2980-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f2980-113">-ApplicationGateway</span></span>
<span data-ttu-id="f2980-114">Azt az Application Gateway-objektumot adja meg, amely az előtér IP-konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="f2980-114">Specifies the application gateway object that contains the front-end IP configuration.</span></span>

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

### <span data-ttu-id="f2980-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2980-115">-DefaultProfile</span></span>
<span data-ttu-id="f2980-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f2980-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2980-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f2980-117">-Name</span></span>
<span data-ttu-id="f2980-118">Annak az előtér-IP-konfigurációnak a nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="f2980-118">Specifies the name of the front-end IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f2980-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2980-119">CommonParameters</span></span>
<span data-ttu-id="f2980-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f2980-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2980-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f2980-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2980-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2980-122">INPUTS</span></span>

### <span data-ttu-id="f2980-123">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f2980-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f2980-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2980-124">OUTPUTS</span></span>

### <span data-ttu-id="f2980-125">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f2980-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="f2980-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f2980-126">NOTES</span></span>

## <span data-ttu-id="f2980-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2980-127">RELATED LINKS</span></span>

[<span data-ttu-id="f2980-128">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f2980-128">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="f2980-129">Új – AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f2980-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="f2980-130">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f2980-130">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="f2980-131">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f2980-131">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


