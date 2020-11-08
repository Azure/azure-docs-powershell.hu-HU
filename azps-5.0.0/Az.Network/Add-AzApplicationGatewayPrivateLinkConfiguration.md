---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 2083dd00c5163a67492ff9973fdf7399d67d7cb6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186573"
---
# <span data-ttu-id="7fb7d-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="7fb7d-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="7fb7d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7fb7d-102">SYNOPSIS</span></span>
<span data-ttu-id="7fb7d-103">Privát hivatkozás-konfiguráció felvétele az alkalmazás-átjáróba.</span><span class="sxs-lookup"><span data-stu-id="7fb7d-103">Adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="7fb7d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7fb7d-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7fb7d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7fb7d-105">DESCRIPTION</span></span>
<span data-ttu-id="7fb7d-106">Az **Add-AzApplicationGatewayPrivateLinkConfiguration** parancsmag egy privát hivatkozás-konfigurációt ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="7fb7d-106">The **Add-AzApplicationGatewayPrivateLinkConfiguration** cmdlet adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="7fb7d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7fb7d-107">EXAMPLES</span></span>

### <span data-ttu-id="7fb7d-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7fb7d-108">Example 1</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $PrivateLinkIpConfiguration
```

<span data-ttu-id="7fb7d-109">Az első parancs létrehoz egy privateLinkIpConfiguration, és a $PrivateLinkIpConfiguration változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7fb7d-109">The first command creates a privateLinkIpConfiguration and stores it in the $PrivateLinkIpConfiguration variable.</span></span>
<span data-ttu-id="7fb7d-110">A második parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7fb7d-110">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7fb7d-111">A harmadik parancs hozzáadja a privateLinkConfig01 nevű privát hivatkozás-konfigurációt az $AppGw átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="7fb7d-111">The third command adds the private link configuration named privateLinkConfig01, for the gateway in $AppGw</span></span>

## <span data-ttu-id="7fb7d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7fb7d-112">PARAMETERS</span></span>

### <span data-ttu-id="7fb7d-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7fb7d-113">-ApplicationGateway</span></span>
<span data-ttu-id="7fb7d-114">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="7fb7d-114">The applicationGateway</span></span>

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

### <span data-ttu-id="7fb7d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fb7d-115">-DefaultProfile</span></span>
<span data-ttu-id="7fb7d-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7fb7d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fb7d-117">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="7fb7d-117">-IpConfiguration</span></span>
<span data-ttu-id="7fb7d-118">A ipConfiguration listája</span><span class="sxs-lookup"><span data-stu-id="7fb7d-118">The list of ipConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fb7d-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7fb7d-119">-Name</span></span>
<span data-ttu-id="7fb7d-120">A privateLink konfigurációjának neve</span><span class="sxs-lookup"><span data-stu-id="7fb7d-120">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="7fb7d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fb7d-121">CommonParameters</span></span>
<span data-ttu-id="7fb7d-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7fb7d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fb7d-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7fb7d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fb7d-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7fb7d-124">INPUTS</span></span>

### <span data-ttu-id="7fb7d-125">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7fb7d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="7fb7d-126">Microsoft. Azure. commands. Network. models. PSApplicationGatewayPrivateLinkIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="7fb7d-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="7fb7d-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7fb7d-127">OUTPUTS</span></span>

### <span data-ttu-id="7fb7d-128">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7fb7d-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7fb7d-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7fb7d-129">NOTES</span></span>

## <span data-ttu-id="7fb7d-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7fb7d-130">RELATED LINKS</span></span>

[<span data-ttu-id="7fb7d-131">Új – AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="7fb7d-131">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="7fb7d-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="7fb7d-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="7fb7d-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="7fb7d-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="7fb7d-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="7fb7d-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)