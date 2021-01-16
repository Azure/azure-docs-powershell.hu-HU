---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
ms.openlocfilehash: c8bd4a0070aa0e5635fad7cb20a627a7d23f5922
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468181"
---
# <span data-ttu-id="cb9ea-101">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="cb9ea-101">Get-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="cb9ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb9ea-102">SYNOPSIS</span></span>
<span data-ttu-id="cb9ea-103">Egy alkalmazás-átjáró termékváltozatát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cb9ea-103">Gets the SKU of an application gateway.</span></span>

## <span data-ttu-id="cb9ea-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cb9ea-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb9ea-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cb9ea-105">DESCRIPTION</span></span>
<span data-ttu-id="cb9ea-106">A **Get-AzApplicationGatewaySku** parancsmag egy alkalmazás-átjáró készlet-készletegységét (SKU) kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cb9ea-106">The **Get-AzApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="cb9ea-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cb9ea-107">EXAMPLES</span></span>

### <span data-ttu-id="cb9ea-108">1. példa: Alkalmazás-átjáró termékváltozatának lekérte</span><span class="sxs-lookup"><span data-stu-id="cb9ea-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="cb9ea-109">Az első parancs az ApplicationGateway01 nevű Alkalmazás-átjárót kapja meg, és az eredményt a következő nevű változóban $AppGW.</span><span class="sxs-lookup"><span data-stu-id="cb9ea-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="cb9ea-110">A második parancs egy ApplicationGateway01 nevű alkalmazás-átjáró termékváltozatát kapja meg, és az eredményt a következő nevű változóban $SKU.</span><span class="sxs-lookup"><span data-stu-id="cb9ea-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="cb9ea-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb9ea-111">PARAMETERS</span></span>

### <span data-ttu-id="cb9ea-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb9ea-112">-ApplicationGateway</span></span>
<span data-ttu-id="cb9ea-113">Az alkalmazás átjáróobjektumát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="cb9ea-113">Specifies the application gateway object.</span></span>

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

### <span data-ttu-id="cb9ea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb9ea-114">-DefaultProfile</span></span>
<span data-ttu-id="cb9ea-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cb9ea-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb9ea-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb9ea-116">CommonParameters</span></span>
<span data-ttu-id="cb9ea-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb9ea-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb9ea-118">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb9ea-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb9ea-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cb9ea-119">INPUTS</span></span>

### <span data-ttu-id="cb9ea-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb9ea-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cb9ea-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb9ea-121">OUTPUTS</span></span>

### <span data-ttu-id="cb9ea-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="cb9ea-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="cb9ea-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cb9ea-123">NOTES</span></span>

## <span data-ttu-id="cb9ea-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb9ea-124">RELATED LINKS</span></span>

[<span data-ttu-id="cb9ea-125">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="cb9ea-125">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="cb9ea-126">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="cb9ea-126">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


