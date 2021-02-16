---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 99d56b837b67fe8b816c4f27c8658932a74452e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161147"
---
# <span data-ttu-id="ae4fa-101">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ae4fa-101">Get-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="ae4fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae4fa-102">SYNOPSIS</span></span>
<span data-ttu-id="ae4fa-103">Beolvassa a megbízható ügyfél-hitelesítésszolgáltató tanúsítványláncát egy adott névvel az alkalmazás átjáróból.</span><span class="sxs-lookup"><span data-stu-id="ae4fa-103">Gets the trusted client CA certificate chain with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="ae4fa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ae4fa-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedClientCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae4fa-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ae4fa-105">DESCRIPTION</span></span>
<span data-ttu-id="ae4fa-106">A Get-AzApplicationGatewayTrustedClientCertificate parancsmag lekéri a megbízható ügyfél-hitelesítésszolgáltató tanúsítványláncát, és egy konkrét nevet kap az alkalmazás átjárótól.</span><span class="sxs-lookup"><span data-stu-id="ae4fa-106">The Get-AzApplicationGatewayTrustedClientCertificate cmdlet gets the trusted client CA certificate chain with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="ae4fa-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ae4fa-107">EXAMPLES</span></span>

### <span data-ttu-id="ae4fa-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="ae4fa-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedClientCert = Get-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name $certName
```

<span data-ttu-id="ae4fa-109">Az első parancs lekérte az alkalmazás átjáróját, és egy változóban $gw tárolja.</span><span class="sxs-lookup"><span data-stu-id="ae4fa-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span> <span data-ttu-id="ae4fa-110">A második parancs egy megadott nevű megbízható ügyfél-hitelesítésszolgáltatói tanúsítványláncot kap az alkalmazás átjáróból.</span><span class="sxs-lookup"><span data-stu-id="ae4fa-110">The second command gets the trusted client CA certificate chain with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="ae4fa-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae4fa-111">PARAMETERS</span></span>

### <span data-ttu-id="ae4fa-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ae4fa-112">-ApplicationGateway</span></span>
<span data-ttu-id="ae4fa-113">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="ae4fa-113">The applicationGateway</span></span>

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

### <span data-ttu-id="ae4fa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae4fa-114">-DefaultProfile</span></span>
<span data-ttu-id="ae4fa-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ae4fa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae4fa-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ae4fa-116">-Name</span></span>
<span data-ttu-id="ae4fa-117">A megbízható ügyfél-hitelesítésszolgáltató tanúsítványláncának neve</span><span class="sxs-lookup"><span data-stu-id="ae4fa-117">The name of the trusted client CA certificate chain</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae4fa-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae4fa-118">CommonParameters</span></span>
<span data-ttu-id="ae4fa-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae4fa-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae4fa-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae4fa-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae4fa-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ae4fa-121">INPUTS</span></span>

### <span data-ttu-id="ae4fa-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ae4fa-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ae4fa-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae4fa-123">OUTPUTS</span></span>

### <span data-ttu-id="ae4fa-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ae4fa-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="ae4fa-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ae4fa-125">NOTES</span></span>

## <span data-ttu-id="ae4fa-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ae4fa-126">RELATED LINKS</span></span>

[<span data-ttu-id="ae4fa-127">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ae4fa-127">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="ae4fa-128">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ae4fa-128">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="ae4fa-129">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ae4fa-129">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="ae4fa-130">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ae4fa-130">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)