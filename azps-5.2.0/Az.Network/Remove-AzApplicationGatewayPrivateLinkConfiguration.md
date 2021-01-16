---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 8d222f4eaaa9d37a4f87f5f19604bdef9cff9e39
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333929"
---
# <span data-ttu-id="c4593-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4593-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="c4593-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4593-102">SYNOPSIS</span></span>
<span data-ttu-id="c4593-103">Eltávolít egy privateLink-konfigurációt egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="c4593-103">Removes a privateLink configuration from an application gateway.</span></span>

## <span data-ttu-id="c4593-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c4593-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayPrivateLinkConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4593-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c4593-105">DESCRIPTION</span></span>
<span data-ttu-id="c4593-106">A **Remove-AzApplicationGatewayPrivateLinkConfiguration** parancsmag eltávolít egy privátLink-konfigurációt egy Azure-alkalmazásátjáróból.</span><span class="sxs-lookup"><span data-stu-id="c4593-106">The **Remove-AzApplicationGatewayPrivateLinkConfiguration** cmdlet removes an privateLink configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="c4593-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c4593-107">EXAMPLES</span></span>

### <span data-ttu-id="c4593-108">1. példa: Alkalmazás átjárójának eltávolítása – PrivateLink-konfiguráció</span><span class="sxs-lookup"><span data-stu-id="c4593-108">Example 1: Remove an application gateway PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01"
```

<span data-ttu-id="c4593-109">Az első parancs egy alkalmazás-átjárót kap, és a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="c4593-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c4593-110">A második parancs eltávolítja a privateLinkConfig01 nevű privátLink-konfigurációt a $AppGw.</span><span class="sxs-lookup"><span data-stu-id="c4593-110">The second command removes the privateLink configuration named privateLinkConfig01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="c4593-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4593-111">PARAMETERS</span></span>

### <span data-ttu-id="c4593-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c4593-112">-ApplicationGateway</span></span>
<span data-ttu-id="c4593-113">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="c4593-113">The applicationGateway</span></span>

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

### <span data-ttu-id="c4593-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4593-114">-DefaultProfile</span></span>
<span data-ttu-id="c4593-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c4593-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4593-116">-Name</span><span class="sxs-lookup"><span data-stu-id="c4593-116">-Name</span></span>
<span data-ttu-id="c4593-117">Az alkalmazás átjárójának privateLink-konfigurációjának neve</span><span class="sxs-lookup"><span data-stu-id="c4593-117">The name of the application gateway privateLink configuration</span></span>

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

### <span data-ttu-id="c4593-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4593-118">CommonParameters</span></span>
<span data-ttu-id="c4593-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4593-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4593-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4593-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4593-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c4593-121">INPUTS</span></span>

### <span data-ttu-id="c4593-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c4593-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c4593-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4593-123">OUTPUTS</span></span>

### <span data-ttu-id="c4593-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c4593-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c4593-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c4593-125">NOTES</span></span>

## <span data-ttu-id="c4593-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4593-126">RELATED LINKS</span></span>

[<span data-ttu-id="c4593-127">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4593-127">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="c4593-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4593-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="c4593-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4593-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="c4593-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4593-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)