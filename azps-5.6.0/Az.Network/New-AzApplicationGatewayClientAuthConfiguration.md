---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 002fdabfb01a0b12d36c69b0a8a75ddf91880012
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925442"
---
# <span data-ttu-id="761d4-101">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="761d4-101">New-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="761d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="761d4-102">SYNOPSIS</span></span>
<span data-ttu-id="761d4-103">Új ügyfél-hitelesítési konfigurációt hoz létre az SSL-profilhoz.</span><span class="sxs-lookup"><span data-stu-id="761d4-103">Creates a new client authentication configuration for SSL profile.</span></span>

## <span data-ttu-id="761d4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="761d4-104">SYNTAX</span></span>

```
New-AzApplicationGatewayClientAuthConfiguration [-VerifyClientCertIssuerDN]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="761d4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="761d4-105">DESCRIPTION</span></span>
<span data-ttu-id="761d4-106">A **New-AzApplicationGatewayClientAuthConfiguration** parancsmag létrehoz egy új ügyfél-hitelesítési konfigurációt az SSL-profilhoz.</span><span class="sxs-lookup"><span data-stu-id="761d4-106">The **New-AzApplicationGatewayClientAuthConfiguration** cmdlet creates a new client authentication configuration for SSL profile.</span></span>

## <span data-ttu-id="761d4-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="761d4-107">EXAMPLES</span></span>

### <span data-ttu-id="761d4-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="761d4-108">Example 1</span></span>
```powershell
PS C:\> $clientAuthConfig = New-AzApplicationGatewayClientAuthConfiguration -VerifyClientCertIssuerDN
```

<span data-ttu-id="761d4-109">A parancs létrehoz egy új ügyfél-hitelesítési konfigurációt, és azt egy $clientAuthConfig egy SSL-profilban használható változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="761d4-109">The command create a new client auth configuration and stores it in $clientAuthConfig variable to be used in a SSL profile.</span></span> 

## <span data-ttu-id="761d4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="761d4-110">PARAMETERS</span></span>

### <span data-ttu-id="761d4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="761d4-111">-DefaultProfile</span></span>
<span data-ttu-id="761d4-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="761d4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="761d4-113">-VerifyClientCertIssuerDN</span><span class="sxs-lookup"><span data-stu-id="761d4-113">-VerifyClientCertIssuerDN</span></span>
<span data-ttu-id="761d4-114">Ellenőrizze az ügyfél-tanúsítvány kibocsátójának nevét.</span><span class="sxs-lookup"><span data-stu-id="761d4-114">Verify client certificate issuer name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="761d4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="761d4-115">CommonParameters</span></span>
<span data-ttu-id="761d4-116">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="761d4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="761d4-117">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="761d4-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="761d4-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="761d4-118">INPUTS</span></span>

### <span data-ttu-id="761d4-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="761d4-119">None</span></span>

## <span data-ttu-id="761d4-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="761d4-120">OUTPUTS</span></span>

### <span data-ttu-id="761d4-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="761d4-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="761d4-122">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="761d4-122">NOTES</span></span>

## <span data-ttu-id="761d4-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="761d4-123">RELATED LINKS</span></span>

[<span data-ttu-id="761d4-124">Add-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="761d4-124">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="761d4-125">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="761d4-125">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="761d4-126">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="761d4-126">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="761d4-127">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="761d4-127">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)