---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 367e54036d7665cf59ebcc6f1a10b3060b97580d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938601"
---
# <span data-ttu-id="70ab7-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="70ab7-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="70ab7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70ab7-102">SYNOPSIS</span></span>
<span data-ttu-id="70ab7-103">Eltávolítja a privateLink-konfigurációt egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="70ab7-103">Removes a privateLink configuration from an application gateway.</span></span>

## <span data-ttu-id="70ab7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="70ab7-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayPrivateLinkConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70ab7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="70ab7-105">DESCRIPTION</span></span>
<span data-ttu-id="70ab7-106">A **Remove-AzApplicationGatewayPrivateLinkConfiguration** parancsmag eltávolít egy privátLink-konfigurációt egy Azure-alkalmazásátjáróból.</span><span class="sxs-lookup"><span data-stu-id="70ab7-106">The **Remove-AzApplicationGatewayPrivateLinkConfiguration** cmdlet removes an privateLink configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="70ab7-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="70ab7-107">EXAMPLES</span></span>

### <span data-ttu-id="70ab7-108">1. példa: Alkalmazás átjárójának eltávolítása – PrivateLink-konfiguráció</span><span class="sxs-lookup"><span data-stu-id="70ab7-108">Example 1: Remove an application gateway PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01"
```

<span data-ttu-id="70ab7-109">Az első parancs egy alkalmazás-átjárót kap, és a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="70ab7-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="70ab7-110">A második parancs eltávolítja a privateLinkConfig01 nevű privátLink-konfigurációt a $AppGw.</span><span class="sxs-lookup"><span data-stu-id="70ab7-110">The second command removes the privateLink configuration named privateLinkConfig01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="70ab7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70ab7-111">PARAMETERS</span></span>

### <span data-ttu-id="70ab7-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="70ab7-112">-ApplicationGateway</span></span>
<span data-ttu-id="70ab7-113">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="70ab7-113">The applicationGateway</span></span>

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

### <span data-ttu-id="70ab7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70ab7-114">-DefaultProfile</span></span>
<span data-ttu-id="70ab7-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="70ab7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70ab7-116">-Name</span><span class="sxs-lookup"><span data-stu-id="70ab7-116">-Name</span></span>
<span data-ttu-id="70ab7-117">Az alkalmazás átjárójának privateLink-konfigurációjának neve</span><span class="sxs-lookup"><span data-stu-id="70ab7-117">The name of the application gateway privateLink configuration</span></span>

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

### <span data-ttu-id="70ab7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70ab7-118">CommonParameters</span></span>
<span data-ttu-id="70ab7-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70ab7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70ab7-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70ab7-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70ab7-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="70ab7-121">INPUTS</span></span>

### <span data-ttu-id="70ab7-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="70ab7-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="70ab7-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70ab7-123">OUTPUTS</span></span>

### <span data-ttu-id="70ab7-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="70ab7-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="70ab7-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="70ab7-125">NOTES</span></span>

## <span data-ttu-id="70ab7-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70ab7-126">RELATED LINKS</span></span>

[<span data-ttu-id="70ab7-127">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="70ab7-127">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="70ab7-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="70ab7-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="70ab7-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="70ab7-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="70ab7-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="70ab7-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)