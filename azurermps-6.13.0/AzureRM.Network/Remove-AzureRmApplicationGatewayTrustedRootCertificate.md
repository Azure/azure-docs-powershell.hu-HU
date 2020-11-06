---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: eecce510632e7eef3fc61cf53127777b93c81e51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495022"
---
# <span data-ttu-id="3127f-101">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3127f-101">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="3127f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3127f-102">SYNOPSIS</span></span>
<span data-ttu-id="3127f-103">Egy megbízható főtanúsítvány eltávolítása egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="3127f-103">Removes a Trusted Root Certificate from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3127f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3127f-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayTrustedRootCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3127f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3127f-105">DESCRIPTION</span></span>
<span data-ttu-id="3127f-106">A **Remove-AzureRmApplicationGatewayTrustedRootCertificate** parancsmag egy meglévő alkalmazás-átjárótól eltávolítja a megbízható legfelső szintű tanúsítványokat.</span><span class="sxs-lookup"><span data-stu-id="3127f-106">The **Remove-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet removes a Trusted Root Certificate from an existing Application Gateway.</span></span>

## <span data-ttu-id="3127f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3127f-107">EXAMPLES</span></span>

### <span data-ttu-id="3127f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3127f-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name "myRootCA"
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="3127f-109">Az első parancs beolvassa az Application Gatewayt, és a $gw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="3127f-109">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="3127f-110">A második parancs eltávolítja a myRootCA nevű megbízható főtanúsítványt az $gw-ban tárolt alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="3127f-110">The second command removes the trusted root certificate named myRootCA from the application gateway stored in $gw.</span></span>
<span data-ttu-id="3127f-111">A harmadik parancs az Azure rendszerhez frissíti az Application Gatewayt.</span><span class="sxs-lookup"><span data-stu-id="3127f-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="3127f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3127f-112">PARAMETERS</span></span>

### <span data-ttu-id="3127f-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3127f-113">-ApplicationGateway</span></span>
<span data-ttu-id="3127f-114">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="3127f-114">The applicationGateway</span></span>

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

### <span data-ttu-id="3127f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3127f-115">-DefaultProfile</span></span>
<span data-ttu-id="3127f-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3127f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3127f-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3127f-117">-Name</span></span>
<span data-ttu-id="3127f-118">A TrustedRoot tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="3127f-118">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="3127f-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3127f-119">-Confirm</span></span>
<span data-ttu-id="3127f-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3127f-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3127f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3127f-121">-WhatIf</span></span>
<span data-ttu-id="3127f-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3127f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3127f-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3127f-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3127f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3127f-124">CommonParameters</span></span>
<span data-ttu-id="3127f-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3127f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3127f-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3127f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3127f-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3127f-127">INPUTS</span></span>

### <span data-ttu-id="3127f-128">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3127f-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3127f-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3127f-129">OUTPUTS</span></span>

### <span data-ttu-id="3127f-130">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3127f-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3127f-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3127f-131">NOTES</span></span>

## <span data-ttu-id="3127f-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3127f-132">RELATED LINKS</span></span>
