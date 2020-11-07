---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: e94ca1bbed8e37643b301e5a5cb2ca3acc78d264
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837034"
---
# <span data-ttu-id="7ab58-101">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7ab58-101">Set-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="7ab58-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7ab58-102">SYNOPSIS</span></span>
<span data-ttu-id="7ab58-103">Egy alkalmazás-átjáró megbízható főtanúsítványát frissíti.</span><span class="sxs-lookup"><span data-stu-id="7ab58-103">Updates a Trusted Root Certificate of an application gateway.</span></span>

## <span data-ttu-id="7ab58-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7ab58-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ab58-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7ab58-105">DESCRIPTION</span></span>
<span data-ttu-id="7ab58-106">A **set-AzApplicationGatewayTrustedRootCertificate** parancsmag módosította az alkalmazás-átjárók meglévő megbízható főtanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="7ab58-106">The **Set-AzApplicationGatewayTrustedRootCertificate** cmdlet modifies the existing trusted root certificate of an Application Gateway.</span></span>

## <span data-ttu-id="7ab58-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7ab58-107">EXAMPLES</span></span>

### <span data-ttu-id="7ab58-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7ab58-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="7ab58-109">A fenti példa szerint az esetek azt mutatják be, hogy miként frissíthet egy meglévő megbízható főtanúsítványt a főtanúsítvány bedobásakor.</span><span class="sxs-lookup"><span data-stu-id="7ab58-109">Above example scenarios shows how to update an existing trusted root certificate when a root certificate is rolled.</span></span>
<span data-ttu-id="7ab58-110">Az első parancs beolvassa az Application Gatewayt, és a $gw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7ab58-110">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="7ab58-111">A második parancs módosította a meglévő megbízható főtanúsítványot egy új főtanúsítványsal.</span><span class="sxs-lookup"><span data-stu-id="7ab58-111">The second command modifies the existing trusted root certificate with a new root certificate.</span></span>
<span data-ttu-id="7ab58-112">A harmadik parancs az Azure rendszerhez frissíti az Application Gatewayt.</span><span class="sxs-lookup"><span data-stu-id="7ab58-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="7ab58-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7ab58-113">PARAMETERS</span></span>

### <span data-ttu-id="7ab58-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ab58-114">-ApplicationGateway</span></span>
<span data-ttu-id="7ab58-115">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ab58-115">The applicationGateway</span></span>

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

### <span data-ttu-id="7ab58-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="7ab58-116">-CertificateFile</span></span>
<span data-ttu-id="7ab58-117">A bizonyítvány CER-fájljának elérési útja</span><span class="sxs-lookup"><span data-stu-id="7ab58-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="7ab58-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ab58-118">-DefaultProfile</span></span>
<span data-ttu-id="7ab58-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7ab58-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ab58-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7ab58-120">-Name</span></span>
<span data-ttu-id="7ab58-121">A TrustedRoot tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="7ab58-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="7ab58-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7ab58-122">-Confirm</span></span>
<span data-ttu-id="7ab58-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7ab58-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ab58-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ab58-124">-WhatIf</span></span>
<span data-ttu-id="7ab58-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7ab58-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ab58-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7ab58-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ab58-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ab58-127">CommonParameters</span></span>
<span data-ttu-id="7ab58-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7ab58-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ab58-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ab58-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ab58-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ab58-130">INPUTS</span></span>

### <span data-ttu-id="7ab58-131">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ab58-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7ab58-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ab58-132">OUTPUTS</span></span>

### <span data-ttu-id="7ab58-133">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ab58-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7ab58-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7ab58-134">NOTES</span></span>

## <span data-ttu-id="7ab58-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ab58-135">RELATED LINKS</span></span>

[<span data-ttu-id="7ab58-136">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7ab58-136">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="7ab58-137">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7ab58-137">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="7ab58-138">Új – AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7ab58-138">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="7ab58-139">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7ab58-139">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)
