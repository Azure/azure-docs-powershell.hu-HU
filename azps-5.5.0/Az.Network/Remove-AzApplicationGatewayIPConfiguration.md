---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 87f6f441220f1f8ab47fee5356bddca8d02b96c0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206630"
---
# <span data-ttu-id="9f400-101">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f400-101">Remove-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="9f400-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f400-102">SYNOPSIS</span></span>
<span data-ttu-id="9f400-103">Eltávolít egy IP-konfigurációt egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="9f400-103">Removes an IP configuration from an application gateway.</span></span>

## <span data-ttu-id="9f400-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9f400-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f400-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9f400-105">DESCRIPTION</span></span>
<span data-ttu-id="9f400-106">A **Remove-AzApplicationGatewayIPConfiguration** parancsmag eltávolít egy IP-konfigurációt egy Azure-alkalmazás átjáróból.</span><span class="sxs-lookup"><span data-stu-id="9f400-106">The **Remove-AzApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="9f400-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9f400-107">EXAMPLES</span></span>

### <span data-ttu-id="9f400-108">1. példa: IP-konfiguráció eltávolítása Azure-alkalmazásátjáróból</span><span class="sxs-lookup"><span data-stu-id="9f400-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="9f400-109">Az első parancs egy alkalmazás-átjárót kap, és a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="9f400-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="9f400-110">A második parancs eltávolítja az Alhálózat02 IP-konfigurációt a $AppGw.</span><span class="sxs-lookup"><span data-stu-id="9f400-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="9f400-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f400-111">PARAMETERS</span></span>

### <span data-ttu-id="9f400-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9f400-112">-ApplicationGateway</span></span>
<span data-ttu-id="9f400-113">Azt az alkalmazás-átjárót adja meg, amelyről el szeretné távolítani az IP-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="9f400-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="9f400-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f400-114">-DefaultProfile</span></span>
<span data-ttu-id="9f400-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9f400-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f400-116">-Name</span><span class="sxs-lookup"><span data-stu-id="9f400-116">-Name</span></span>
<span data-ttu-id="9f400-117">Az eltávolítható IP-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="9f400-117">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="9f400-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f400-118">CommonParameters</span></span>
<span data-ttu-id="9f400-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f400-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f400-120">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f400-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f400-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f400-121">INPUTS</span></span>

### <span data-ttu-id="9f400-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9f400-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9f400-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f400-123">OUTPUTS</span></span>

### <span data-ttu-id="9f400-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9f400-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9f400-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9f400-125">NOTES</span></span>

## <span data-ttu-id="9f400-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f400-126">RELATED LINKS</span></span>

[<span data-ttu-id="9f400-127">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f400-127">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="9f400-128">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f400-128">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="9f400-129">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f400-129">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="9f400-130">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f400-130">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


