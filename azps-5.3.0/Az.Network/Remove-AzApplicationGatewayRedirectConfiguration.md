---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: fdd461ea2908e59ba824b09a49bed3b6b8f4d38f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470146"
---
# <span data-ttu-id="7f950-101">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7f950-101">Remove-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="7f950-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f950-102">SYNOPSIS</span></span>
<span data-ttu-id="7f950-103">Eltávolít egy átirányítási konfigurációt egy meglévő alkalmazásátjáróból.</span><span class="sxs-lookup"><span data-stu-id="7f950-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="7f950-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7f950-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f950-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7f950-105">DESCRIPTION</span></span>
<span data-ttu-id="7f950-106">A **Remove-AzApplicationGatewayRedirectConfiguration** parancsmag eltávolít egy átirányítási konfigurációt egy meglévő alkalmazás átjáróból.</span><span class="sxs-lookup"><span data-stu-id="7f950-106">The **Remove-AzApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="7f950-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7f950-107">EXAMPLES</span></span>

### <span data-ttu-id="7f950-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="7f950-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="7f950-109">Az első parancs egy alkalmazás-átjárót kap, és a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="7f950-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7f950-110">A második parancs eltávolítja az Átirányítás01 nevű átirányítási konfigurációt a $AppGw.</span><span class="sxs-lookup"><span data-stu-id="7f950-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="7f950-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f950-111">PARAMETERS</span></span>

### <span data-ttu-id="7f950-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7f950-112">-ApplicationGateway</span></span>
<span data-ttu-id="7f950-113">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="7f950-113">The applicationGateway</span></span>

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

### <span data-ttu-id="7f950-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f950-114">-DefaultProfile</span></span>
<span data-ttu-id="7f950-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7f950-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f950-116">-Name</span><span class="sxs-lookup"><span data-stu-id="7f950-116">-Name</span></span>
<span data-ttu-id="7f950-117">Az átirányítási konfiguráció neve</span><span class="sxs-lookup"><span data-stu-id="7f950-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="7f950-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f950-118">CommonParameters</span></span>
<span data-ttu-id="7f950-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f950-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f950-120">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f950-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f950-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7f950-121">INPUTS</span></span>

### <span data-ttu-id="7f950-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7f950-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7f950-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f950-123">OUTPUTS</span></span>

### <span data-ttu-id="7f950-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7f950-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7f950-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7f950-125">NOTES</span></span>

## <span data-ttu-id="7f950-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7f950-126">RELATED LINKS</span></span>

[<span data-ttu-id="7f950-127">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7f950-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="7f950-128">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7f950-128">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="7f950-129">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7f950-129">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="7f950-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7f950-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
