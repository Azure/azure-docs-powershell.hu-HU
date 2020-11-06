---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: e44136d5fa9b0a6b0b979005c13faf6041d98f61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502039"
---
# <span data-ttu-id="539c1-101">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="539c1-101">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="539c1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="539c1-102">SYNOPSIS</span></span>
<span data-ttu-id="539c1-103">Egy megbízható főtanúsítvány felvétele az alkalmazás-átjáróba.</span><span class="sxs-lookup"><span data-stu-id="539c1-103">Adds a trusted root certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="539c1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="539c1-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="539c1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="539c1-105">DESCRIPTION</span></span>
<span data-ttu-id="539c1-106">Az **Add-AzureRmApplicationGatewayTrustedRootCertificate** parancsmag egy megbízható legfelső szintű tanúsítványt ad egy Azure Application Gateway-nek.</span><span class="sxs-lookup"><span data-stu-id="539c1-106">The **Add-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet adds a trusted root certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="539c1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="539c1-107">EXAMPLES</span></span>

### <span data-ttu-id="539c1-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="539c1-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Add-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
PS C:\> $gw = Add-AzureRmApplicationGatewayBackendHttpSetting -Name $poolSetting01Name -Port 443 -Protocol Https -CookieBasedAffinity Enabled -PickHostNameFromBackendAddress -TrustedRootCertificate $gw.TrustedRootCertificates[0]
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="539c1-109">Az első parancs beolvassa az Application Gatewayt, és az $gw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="539c1-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="539c1-110">A második parancs az hozzáadott új megbízható főtanúsítványát adja eredményül a főtanúsítvány elérési útjának.</span><span class="sxs-lookup"><span data-stu-id="539c1-110">The second command addes a new trusted root certificate to Application Gateway taking path of the root certificate as input.</span></span>
<span data-ttu-id="539c1-111">A harmadik parancs új backend http-beállítást hoz létre a megbízható főtanúsítvány használatával a backend-kiszolgáló tanúsítványának érvényesítéséhez.</span><span class="sxs-lookup"><span data-stu-id="539c1-111">The third command creates new backend http setting using trusted root certificate for validating the backend server certificate against.</span></span>
<span data-ttu-id="539c1-112">Az Fouth parancs frissíti az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="539c1-112">The fouth command updates the Application Gateway.</span></span>

## <span data-ttu-id="539c1-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="539c1-113">PARAMETERS</span></span>

### <span data-ttu-id="539c1-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="539c1-114">-ApplicationGateway</span></span>
<span data-ttu-id="539c1-115">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="539c1-115">The applicationGateway</span></span>

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

### <span data-ttu-id="539c1-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="539c1-116">-CertificateFile</span></span>
<span data-ttu-id="539c1-117">A bizonyítvány CER-fájljának elérési útja</span><span class="sxs-lookup"><span data-stu-id="539c1-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="539c1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="539c1-118">-DefaultProfile</span></span>
<span data-ttu-id="539c1-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="539c1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="539c1-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="539c1-120">-Name</span></span>
<span data-ttu-id="539c1-121">A TrustedRoot tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="539c1-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="539c1-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="539c1-122">-Confirm</span></span>
<span data-ttu-id="539c1-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="539c1-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="539c1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="539c1-124">-WhatIf</span></span>
<span data-ttu-id="539c1-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="539c1-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="539c1-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="539c1-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="539c1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="539c1-127">CommonParameters</span></span>
<span data-ttu-id="539c1-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="539c1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="539c1-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="539c1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="539c1-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="539c1-130">INPUTS</span></span>

### <span data-ttu-id="539c1-131">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="539c1-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="539c1-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="539c1-132">OUTPUTS</span></span>

### <span data-ttu-id="539c1-133">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="539c1-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="539c1-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="539c1-134">NOTES</span></span>

## <span data-ttu-id="539c1-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="539c1-135">RELATED LINKS</span></span>
