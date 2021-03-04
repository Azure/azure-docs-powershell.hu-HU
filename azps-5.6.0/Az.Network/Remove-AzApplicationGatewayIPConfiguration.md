---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 610fe3f2ba4867dc1145488dfe789dba051b23bb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936730"
---
# <span data-ttu-id="f2955-101">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f2955-101">Remove-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="f2955-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2955-102">SYNOPSIS</span></span>
<span data-ttu-id="f2955-103">Eltávolít egy IP-konfigurációt egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="f2955-103">Removes an IP configuration from an application gateway.</span></span>

## <span data-ttu-id="f2955-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f2955-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2955-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f2955-105">DESCRIPTION</span></span>
<span data-ttu-id="f2955-106">A **Remove-AzApplicationGatewayIPConfiguration** parancsmag eltávolít egy IP-konfigurációt egy Azure-alkalmazás átjáróból.</span><span class="sxs-lookup"><span data-stu-id="f2955-106">The **Remove-AzApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="f2955-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f2955-107">EXAMPLES</span></span>

### <span data-ttu-id="f2955-108">1. példa: IP-konfiguráció eltávolítása Azure-alkalmazásátjáróból</span><span class="sxs-lookup"><span data-stu-id="f2955-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="f2955-109">Az első parancs egy alkalmazás-átjárót kap, és a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="f2955-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f2955-110">A második parancs eltávolítja az Alhálózat02 IP-konfigurációt a $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f2955-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="f2955-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2955-111">PARAMETERS</span></span>

### <span data-ttu-id="f2955-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f2955-112">-ApplicationGateway</span></span>
<span data-ttu-id="f2955-113">Azt az alkalmazás-átjárót adja meg, amelyről el szeretné távolítani az IP-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="f2955-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="f2955-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2955-114">-DefaultProfile</span></span>
<span data-ttu-id="f2955-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f2955-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2955-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f2955-116">-Name</span></span>
<span data-ttu-id="f2955-117">Az eltávolítható IP-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="f2955-117">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="f2955-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2955-118">CommonParameters</span></span>
<span data-ttu-id="f2955-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2955-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2955-120">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2955-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2955-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2955-121">INPUTS</span></span>

### <span data-ttu-id="f2955-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f2955-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f2955-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2955-123">OUTPUTS</span></span>

### <span data-ttu-id="f2955-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f2955-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f2955-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f2955-125">NOTES</span></span>

## <span data-ttu-id="f2955-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2955-126">RELATED LINKS</span></span>

[<span data-ttu-id="f2955-127">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f2955-127">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="f2955-128">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f2955-128">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="f2955-129">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f2955-129">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="f2955-130">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f2955-130">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


