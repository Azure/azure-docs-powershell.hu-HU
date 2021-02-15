---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: def44c0925239aed345eed84b4f34690d2db8746
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100395690"
---
# <span data-ttu-id="36536-101">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="36536-101">Set-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="36536-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36536-102">SYNOPSIS</span></span>
<span data-ttu-id="36536-103">Módosítja egy ssl-profilobjektum ügyfél-hitelesítési konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="36536-103">Modifies the client auth configuration of a ssl profile object.</span></span>

## <span data-ttu-id="36536-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="36536-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-VerifyClientCertIssuerDN] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36536-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="36536-105">DESCRIPTION</span></span>
<span data-ttu-id="36536-106">A **Set-AzApplicationGatewayClientAuthConfiguration** parancsmag módosítja egy ssl-profilobjektum ügyfél-hitelesítés konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="36536-106">The **Set-AzApplicationGatewayClientAuthConfiguration** cmdlet modifies the client auth configuration of a ssl profile object.</span></span>

## <span data-ttu-id="36536-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="36536-107">EXAMPLES</span></span>

### <span data-ttu-id="36536-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="36536-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayClientAuthConfiguration -SslProfile $profile -VerifyClientCertIssuerDN
```

<span data-ttu-id="36536-109">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót az ResourceGroup01 nevű erőforráscsoportban tárolja a $AppGw változóban.</span><span class="sxs-lookup"><span data-stu-id="36536-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="36536-110">A második parancs az SslProfile01 nevű ssl-profilt kapja $AppGw a beállításokat a $profile változóban.</span><span class="sxs-lookup"><span data-stu-id="36536-110">The second command gets the ssl profile named SslProfile01 for $AppGw and stores the settings in the $profile variable.</span></span> <span data-ttu-id="36536-111">Az utolsó parancs módosítja a fájlban tárolt ssl-profilobjektum ügyfél-hitelesítés-$profile.</span><span class="sxs-lookup"><span data-stu-id="36536-111">The last command modifies the client auth configuration of the ssl profile object stored in $profile.</span></span>

## <span data-ttu-id="36536-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36536-112">PARAMETERS</span></span>

### <span data-ttu-id="36536-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36536-113">-DefaultProfile</span></span>
<span data-ttu-id="36536-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="36536-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36536-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="36536-115">-SslProfile</span></span>
<span data-ttu-id="36536-116">Az ssl-profil</span><span class="sxs-lookup"><span data-stu-id="36536-116">The ssl profile</span></span>

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

### <span data-ttu-id="36536-117">-VerifyClientCertIssuerDN</span><span class="sxs-lookup"><span data-stu-id="36536-117">-VerifyClientCertIssuerDN</span></span>
<span data-ttu-id="36536-118">Ellenőrizze az ügyfél-tanúsítvány kibocsátójának nevét.</span><span class="sxs-lookup"><span data-stu-id="36536-118">Verify client certificate issuer name.</span></span>

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

### <span data-ttu-id="36536-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36536-119">CommonParameters</span></span>
<span data-ttu-id="36536-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36536-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36536-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36536-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36536-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36536-122">INPUTS</span></span>

### <span data-ttu-id="36536-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="36536-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="36536-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36536-124">OUTPUTS</span></span>

### <span data-ttu-id="36536-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="36536-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="36536-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="36536-126">NOTES</span></span>

## <span data-ttu-id="36536-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36536-127">RELATED LINKS</span></span>


[<span data-ttu-id="36536-128">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="36536-128">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="36536-129">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="36536-129">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="36536-130">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="36536-130">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)
