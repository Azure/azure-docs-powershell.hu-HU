---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 99d56b837b67fe8b816c4f27c8658932a74452e7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337865"
---
# <span data-ttu-id="31a81-101">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="31a81-101">Get-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="31a81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31a81-102">SYNOPSIS</span></span>
<span data-ttu-id="31a81-103">Beolvassa a megbízható ügyfél-hitelesítésszolgáltató tanúsítványláncát egy adott névvel az alkalmazás átjáróból.</span><span class="sxs-lookup"><span data-stu-id="31a81-103">Gets the trusted client CA certificate chain with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="31a81-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="31a81-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedClientCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31a81-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="31a81-105">DESCRIPTION</span></span>
<span data-ttu-id="31a81-106">A Get-AzApplicationGatewayTrustedClientCertificate parancsmag lekéri a megbízható ügyfél-hitelesítésszolgáltató tanúsítványláncát, és egy konkrét nevet kap az alkalmazás átjárótól.</span><span class="sxs-lookup"><span data-stu-id="31a81-106">The Get-AzApplicationGatewayTrustedClientCertificate cmdlet gets the trusted client CA certificate chain with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="31a81-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="31a81-107">EXAMPLES</span></span>

### <span data-ttu-id="31a81-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="31a81-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedClientCert = Get-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name $certName
```

<span data-ttu-id="31a81-109">Az első parancs lekérte az alkalmazás átjáróját, és egy változóban $gw tárolja.</span><span class="sxs-lookup"><span data-stu-id="31a81-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span> <span data-ttu-id="31a81-110">A második parancs egy megadott nevű megbízható ügyfél-hitelesítésszolgáltatói tanúsítványláncot kap az alkalmazás átjáróból.</span><span class="sxs-lookup"><span data-stu-id="31a81-110">The second command gets the trusted client CA certificate chain with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="31a81-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31a81-111">PARAMETERS</span></span>

### <span data-ttu-id="31a81-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="31a81-112">-ApplicationGateway</span></span>
<span data-ttu-id="31a81-113">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="31a81-113">The applicationGateway</span></span>

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

### <span data-ttu-id="31a81-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31a81-114">-DefaultProfile</span></span>
<span data-ttu-id="31a81-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="31a81-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31a81-116">-Name</span><span class="sxs-lookup"><span data-stu-id="31a81-116">-Name</span></span>
<span data-ttu-id="31a81-117">A megbízható ügyfél-hitelesítésszolgáltató tanúsítványláncának neve</span><span class="sxs-lookup"><span data-stu-id="31a81-117">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="31a81-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31a81-118">CommonParameters</span></span>
<span data-ttu-id="31a81-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31a81-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31a81-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="31a81-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31a81-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="31a81-121">INPUTS</span></span>

### <span data-ttu-id="31a81-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="31a81-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="31a81-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="31a81-123">OUTPUTS</span></span>

### <span data-ttu-id="31a81-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="31a81-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="31a81-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="31a81-125">NOTES</span></span>

## <span data-ttu-id="31a81-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="31a81-126">RELATED LINKS</span></span>

[<span data-ttu-id="31a81-127">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="31a81-127">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="31a81-128">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="31a81-128">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="31a81-129">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="31a81-129">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="31a81-130">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="31a81-130">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)