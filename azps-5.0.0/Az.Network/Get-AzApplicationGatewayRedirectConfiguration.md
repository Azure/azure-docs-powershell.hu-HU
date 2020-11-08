---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 8a49bdeed095ee277d632559402c55ca3baf784c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195702"
---
# <span data-ttu-id="2fded-101">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fded-101">Get-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="2fded-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2fded-102">SYNOPSIS</span></span>
<span data-ttu-id="2fded-103">Meglévő átirányítási konfigurációt kap egy alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="2fded-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="2fded-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2fded-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fded-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2fded-105">DESCRIPTION</span></span>
<span data-ttu-id="2fded-106">A **Get-AzApplicationGatewayRedirectConfiguration** parancsmag egy meglévő átirányítási konfigurációt kap egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="2fded-106">The **Get-AzApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="2fded-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2fded-107">EXAMPLES</span></span>

### <span data-ttu-id="2fded-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2fded-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="2fded-109">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, és az eredményt az $AppGW nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2fded-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="2fded-110">A második parancs a Redirect01 nevű átirányítási konfigurációt a $AppGW nevű változóban tárolt alkalmazás-átjáróról kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2fded-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="2fded-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2fded-111">PARAMETERS</span></span>

### <span data-ttu-id="2fded-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2fded-112">-ApplicationGateway</span></span>
<span data-ttu-id="2fded-113">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="2fded-113">The applicationGateway</span></span>

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

### <span data-ttu-id="2fded-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fded-114">-DefaultProfile</span></span>
<span data-ttu-id="2fded-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2fded-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fded-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2fded-116">-Name</span></span>
<span data-ttu-id="2fded-117">A kérés útválasztási szabályának neve</span><span class="sxs-lookup"><span data-stu-id="2fded-117">The name of the request routing rule</span></span>

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

### <span data-ttu-id="2fded-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fded-118">CommonParameters</span></span>
<span data-ttu-id="2fded-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2fded-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fded-120">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2fded-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fded-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2fded-121">INPUTS</span></span>

### <span data-ttu-id="2fded-122">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2fded-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2fded-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2fded-123">OUTPUTS</span></span>

### <span data-ttu-id="2fded-124">Microsoft. Azure. commands. Network. models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fded-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="2fded-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2fded-125">NOTES</span></span>

## <span data-ttu-id="2fded-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2fded-126">RELATED LINKS</span></span>

[<span data-ttu-id="2fded-127">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fded-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="2fded-128">Új – AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fded-128">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="2fded-129">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fded-129">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="2fded-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fded-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)