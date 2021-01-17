---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 8d222f4eaaa9d37a4f87f5f19604bdef9cff9e39
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479970"
---
# <span data-ttu-id="cd9bc-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd9bc-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="cd9bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd9bc-102">SYNOPSIS</span></span>
<span data-ttu-id="cd9bc-103">Eltávolít egy privateLink-konfigurációt egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="cd9bc-103">Removes a privateLink configuration from an application gateway.</span></span>

## <span data-ttu-id="cd9bc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cd9bc-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayPrivateLinkConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd9bc-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cd9bc-105">DESCRIPTION</span></span>
<span data-ttu-id="cd9bc-106">A **Remove-AzApplicationGatewayPrivateLinkConfiguration** parancsmag eltávolít egy privátLink-konfigurációt egy Azure-alkalmazásátjáróból.</span><span class="sxs-lookup"><span data-stu-id="cd9bc-106">The **Remove-AzApplicationGatewayPrivateLinkConfiguration** cmdlet removes an privateLink configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="cd9bc-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cd9bc-107">EXAMPLES</span></span>

### <span data-ttu-id="cd9bc-108">1. példa: Alkalmazás átjárójának eltávolítása – PrivateLink-konfiguráció</span><span class="sxs-lookup"><span data-stu-id="cd9bc-108">Example 1: Remove an application gateway PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01"
```

<span data-ttu-id="cd9bc-109">Az első parancs egy alkalmazás-átjárót kap, és a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="cd9bc-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="cd9bc-110">A második parancs eltávolítja a privateLinkConfig01 nevű privátLink-konfigurációt a $AppGw.</span><span class="sxs-lookup"><span data-stu-id="cd9bc-110">The second command removes the privateLink configuration named privateLinkConfig01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="cd9bc-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd9bc-111">PARAMETERS</span></span>

### <span data-ttu-id="cd9bc-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cd9bc-112">-ApplicationGateway</span></span>
<span data-ttu-id="cd9bc-113">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="cd9bc-113">The applicationGateway</span></span>

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

### <span data-ttu-id="cd9bc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd9bc-114">-DefaultProfile</span></span>
<span data-ttu-id="cd9bc-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cd9bc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd9bc-116">-Name</span><span class="sxs-lookup"><span data-stu-id="cd9bc-116">-Name</span></span>
<span data-ttu-id="cd9bc-117">Az alkalmazás átjárójának privateLink-konfigurációjának neve</span><span class="sxs-lookup"><span data-stu-id="cd9bc-117">The name of the application gateway privateLink configuration</span></span>

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

### <span data-ttu-id="cd9bc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd9bc-118">CommonParameters</span></span>
<span data-ttu-id="cd9bc-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd9bc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd9bc-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd9bc-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd9bc-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cd9bc-121">INPUTS</span></span>

### <span data-ttu-id="cd9bc-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cd9bc-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cd9bc-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd9bc-123">OUTPUTS</span></span>

### <span data-ttu-id="cd9bc-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cd9bc-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cd9bc-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cd9bc-125">NOTES</span></span>

## <span data-ttu-id="cd9bc-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd9bc-126">RELATED LINKS</span></span>

[<span data-ttu-id="cd9bc-127">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd9bc-127">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="cd9bc-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd9bc-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="cd9bc-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd9bc-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="cd9bc-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd9bc-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)