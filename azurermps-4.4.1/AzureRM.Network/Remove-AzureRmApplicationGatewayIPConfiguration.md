---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 4ef644fb92bf3f872a9e80aef2674a3ffb56747b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497071"
---
# <span data-ttu-id="c9ca7-101">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9ca7-101">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="c9ca7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c9ca7-102">SYNOPSIS</span></span>
<span data-ttu-id="c9ca7-103">IP-konfiguráció eltávolítása egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="c9ca7-103">Removes an IP configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9ca7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c9ca7-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9ca7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c9ca7-105">DESCRIPTION</span></span>
<span data-ttu-id="c9ca7-106">A **Remove-AzureRmApplicationGatewayIPConfiguration** parancsmag az Azure Application Gateway-ből távolítja el az IP-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="c9ca7-106">The **Remove-AzureRmApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="c9ca7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c9ca7-107">EXAMPLES</span></span>

### <span data-ttu-id="c9ca7-108">Példa 1: IP-konfiguráció eltávolítása Azure Application Gateway-ből</span><span class="sxs-lookup"><span data-stu-id="c9ca7-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="c9ca7-109">Az első parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c9ca7-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="c9ca7-110">A második parancs eltávolítja a Subnet02 nevű IP-konfigurációt az $AppGw-ban tárolt alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="c9ca7-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="c9ca7-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c9ca7-111">PARAMETERS</span></span>

### <span data-ttu-id="c9ca7-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c9ca7-112">-ApplicationGateway</span></span>
<span data-ttu-id="c9ca7-113">Annak az alkalmazásnak az átjáróját adja meg, amelyből el szeretné távolítani az IP-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="c9ca7-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="c9ca7-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c9ca7-114">-Name</span></span>
<span data-ttu-id="c9ca7-115">Az eltávolítandó IP-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c9ca7-115">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="c9ca7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9ca7-116">-DefaultProfile</span></span>
<span data-ttu-id="c9ca7-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c9ca7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9ca7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9ca7-118">CommonParameters</span></span>
<span data-ttu-id="c9ca7-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c9ca7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9ca7-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9ca7-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9ca7-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9ca7-121">INPUTS</span></span>

### <span data-ttu-id="c9ca7-122">System. String</span><span class="sxs-lookup"><span data-stu-id="c9ca7-122">System.String</span></span>

## <span data-ttu-id="c9ca7-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9ca7-123">OUTPUTS</span></span>

### <span data-ttu-id="c9ca7-124">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c9ca7-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c9ca7-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c9ca7-125">NOTES</span></span>

## <span data-ttu-id="c9ca7-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9ca7-126">RELATED LINKS</span></span>

[<span data-ttu-id="c9ca7-127">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9ca7-127">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="c9ca7-128">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9ca7-128">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="c9ca7-129">Új – AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9ca7-129">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="c9ca7-130">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9ca7-130">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


