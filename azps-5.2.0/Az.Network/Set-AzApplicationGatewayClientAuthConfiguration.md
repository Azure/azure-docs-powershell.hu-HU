---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 9512d2d2a51e70b2a0b5e7aa2e8240a8aeb1be1a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330245"
---
# <span data-ttu-id="202be-101">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="202be-101">Set-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="202be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="202be-102">SYNOPSIS</span></span>
<span data-ttu-id="202be-103">Módosítja egy ssl-profilobjektum ügyfél-hitelesítési konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="202be-103">Modifies the client auth configuration of a ssl profile object.</span></span>

## <span data-ttu-id="202be-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="202be-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-VerifyClientCertIssuerDN] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="202be-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="202be-105">DESCRIPTION</span></span>
<span data-ttu-id="202be-106">A **Set-AzApplicationGatewayClientAuthConfiguration** parancsmag módosítja egy ssl-profilobjektum ügyfél-hitelesítés konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="202be-106">The **Set-AzApplicationGatewayClientAuthConfiguration** cmdlet modifies the client auth configuration of a ssl profile object.</span></span>

## <span data-ttu-id="202be-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="202be-107">EXAMPLES</span></span>

### <span data-ttu-id="202be-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="202be-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayClientAuthConfiguration -SslProfile $profile -VerifyClientCertIssuerDN
```

<span data-ttu-id="202be-109">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót az ResourceGroup01 nevű erőforráscsoportban tárolja a $AppGw változóban.</span><span class="sxs-lookup"><span data-stu-id="202be-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="202be-110">A második parancs az SslProfile01 nevű ssl-profilt kapja $AppGw a beállításokat a $profile változóban.</span><span class="sxs-lookup"><span data-stu-id="202be-110">The second command gets the ssl profile named SslProfile01 for $AppGw and stores the settings in the $profile variable.</span></span> <span data-ttu-id="202be-111">Az utolsó parancs módosítja a fájlban tárolt ssl-profilobjektum ügyfél-hitelesítés-$profile.</span><span class="sxs-lookup"><span data-stu-id="202be-111">The last command modifies the client auth configuration of the ssl profile object stored in $profile.</span></span>

## <span data-ttu-id="202be-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="202be-112">PARAMETERS</span></span>

### <span data-ttu-id="202be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="202be-113">-DefaultProfile</span></span>
<span data-ttu-id="202be-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="202be-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="202be-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="202be-115">-SslProfile</span></span>
<span data-ttu-id="202be-116">Az ssl-profil</span><span class="sxs-lookup"><span data-stu-id="202be-116">The ssl profile</span></span>

```yaml
Type: PSApplicationGatewaySslProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="202be-117">-VerifyClientCertIssuerDN</span><span class="sxs-lookup"><span data-stu-id="202be-117">-VerifyClientCertIssuerDN</span></span>
<span data-ttu-id="202be-118">Ellenőrizze az ügyfél-tanúsítvány kibocsátójának nevét.</span><span class="sxs-lookup"><span data-stu-id="202be-118">Verify client certificate issuer name.</span></span>

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

### <span data-ttu-id="202be-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="202be-119">CommonParameters</span></span>
<span data-ttu-id="202be-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="202be-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="202be-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="202be-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="202be-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="202be-122">INPUTS</span></span>

### <span data-ttu-id="202be-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="202be-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="202be-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="202be-124">OUTPUTS</span></span>

### <span data-ttu-id="202be-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="202be-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="202be-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="202be-126">NOTES</span></span>

## <span data-ttu-id="202be-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="202be-127">RELATED LINKS</span></span>

[<span data-ttu-id="202be-128">Add-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="202be-128">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="202be-129">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="202be-129">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="202be-130">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="202be-130">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="202be-131">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="202be-131">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)