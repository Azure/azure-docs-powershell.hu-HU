---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 5c3976ddeeaa856f956ecb785a9d35e62ba322fb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203133"
---
# <span data-ttu-id="12a0d-101">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="12a0d-101">Get-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="12a0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12a0d-102">SYNOPSIS</span></span>
<span data-ttu-id="12a0d-103">Bekéri a megbízható legfelső szintű tanúsítványt egy adott néven az alkalmazás átjáróból.</span><span class="sxs-lookup"><span data-stu-id="12a0d-103">Gets the Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="12a0d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="12a0d-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedRootCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12a0d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="12a0d-105">DESCRIPTION</span></span>
<span data-ttu-id="12a0d-106">A **Get-AzApplicationGatewayTrustedRootCertificate** parancsmag megbízható gyökértanúsítványt kap az alkalmazás átjáróból egy adott néven.</span><span class="sxs-lookup"><span data-stu-id="12a0d-106">The **Get-AzApplicationGatewayTrustedRootCertificate** cmdlet gets Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="12a0d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="12a0d-107">EXAMPLES</span></span>

### <span data-ttu-id="12a0d-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="12a0d-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedRootCert = Get-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
```

<span data-ttu-id="12a0d-109">Az első parancs lekérte az alkalmazás átjáróját, és egy változóban $gw tárolja.</span><span class="sxs-lookup"><span data-stu-id="12a0d-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="12a0d-110">A második parancs egy megadott nevű megbízható gyökértanúsítványt kap az alkalmazás átjáróból.</span><span class="sxs-lookup"><span data-stu-id="12a0d-110">The second command gets the Trusted Root Certificate with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="12a0d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12a0d-111">PARAMETERS</span></span>

### <span data-ttu-id="12a0d-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="12a0d-112">-ApplicationGateway</span></span>
<span data-ttu-id="12a0d-113">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="12a0d-113">The applicationGateway</span></span>

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

### <span data-ttu-id="12a0d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12a0d-114">-DefaultProfile</span></span>
<span data-ttu-id="12a0d-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="12a0d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12a0d-116">-Name</span><span class="sxs-lookup"><span data-stu-id="12a0d-116">-Name</span></span>
<span data-ttu-id="12a0d-117">A TrustedRoot tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="12a0d-117">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="12a0d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12a0d-118">CommonParameters</span></span>
<span data-ttu-id="12a0d-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12a0d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12a0d-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12a0d-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12a0d-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="12a0d-121">INPUTS</span></span>

### <span data-ttu-id="12a0d-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="12a0d-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="12a0d-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="12a0d-123">OUTPUTS</span></span>

### <span data-ttu-id="12a0d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="12a0d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="12a0d-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="12a0d-125">NOTES</span></span>

## <span data-ttu-id="12a0d-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="12a0d-126">RELATED LINKS</span></span>

[<span data-ttu-id="12a0d-127">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="12a0d-127">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="12a0d-128">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="12a0d-128">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="12a0d-129">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="12a0d-129">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="12a0d-130">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="12a0d-130">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
