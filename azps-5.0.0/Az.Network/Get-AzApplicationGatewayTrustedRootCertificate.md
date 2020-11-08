---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 5c3976ddeeaa856f956ecb785a9d35e62ba322fb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195686"
---
# <span data-ttu-id="f71a5-101">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f71a5-101">Get-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="f71a5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f71a5-102">SYNOPSIS</span></span>
<span data-ttu-id="f71a5-103">A megbízható főtanúsítvány beolvasása az alkalmazás-átjáró konkrét nevével</span><span class="sxs-lookup"><span data-stu-id="f71a5-103">Gets the Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="f71a5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f71a5-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedRootCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f71a5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f71a5-105">DESCRIPTION</span></span>
<span data-ttu-id="f71a5-106">A **Get-AzApplicationGatewayTrustedRootCertificate** parancsmag megbízható főtanúsítványokat kap, az alkalmazás-átjáróban megadott névvel.</span><span class="sxs-lookup"><span data-stu-id="f71a5-106">The **Get-AzApplicationGatewayTrustedRootCertificate** cmdlet gets Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="f71a5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f71a5-107">EXAMPLES</span></span>

### <span data-ttu-id="f71a5-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f71a5-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedRootCert = Get-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
```

<span data-ttu-id="f71a5-109">Az első parancs beolvassa az Application Gatewayt, és az $gw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f71a5-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="f71a5-110">A második parancs a megbízható főtanúsítványt az alkalmazás-átjáró megadott nevével kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f71a5-110">The second command gets the Trusted Root Certificate with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="f71a5-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f71a5-111">PARAMETERS</span></span>

### <span data-ttu-id="f71a5-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f71a5-112">-ApplicationGateway</span></span>
<span data-ttu-id="f71a5-113">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="f71a5-113">The applicationGateway</span></span>

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

### <span data-ttu-id="f71a5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f71a5-114">-DefaultProfile</span></span>
<span data-ttu-id="f71a5-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f71a5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f71a5-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f71a5-116">-Name</span></span>
<span data-ttu-id="f71a5-117">A TrustedRoot tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="f71a5-117">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="f71a5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f71a5-118">CommonParameters</span></span>
<span data-ttu-id="f71a5-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f71a5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f71a5-120">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f71a5-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f71a5-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f71a5-121">INPUTS</span></span>

### <span data-ttu-id="f71a5-122">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f71a5-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f71a5-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f71a5-123">OUTPUTS</span></span>

### <span data-ttu-id="f71a5-124">Microsoft. Azure. commands. Network. models. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f71a5-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="f71a5-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f71a5-125">NOTES</span></span>

## <span data-ttu-id="f71a5-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f71a5-126">RELATED LINKS</span></span>

[<span data-ttu-id="f71a5-127">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f71a5-127">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="f71a5-128">Új – AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f71a5-128">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="f71a5-129">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f71a5-129">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="f71a5-130">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f71a5-130">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
