---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: eee7040dab93a4f73bacdf440c6450a525fab9a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326350"
---
# <span data-ttu-id="2cd7c-101">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="2cd7c-101">Get-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="2cd7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cd7c-102">SYNOPSIS</span></span>
<span data-ttu-id="2cd7c-103">Ssl-profilobjektum ügyfél-hitelesítési konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2cd7c-103">Gets the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="2cd7c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2cd7c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cd7c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2cd7c-105">DESCRIPTION</span></span>
<span data-ttu-id="2cd7c-106">A **Get-AzApplicationGatewayClientAuthConfiguration parancsmag** egy SSL-profilobjektum ügyfél-hitelesítési konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2cd7c-106">The **Get-AzApplicationGatewayClientAuthConfiguration** cmdlet gets the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="2cd7c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2cd7c-107">EXAMPLES</span></span>

### <span data-ttu-id="2cd7c-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="2cd7c-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SslProfile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $ClientAuthConfig = Get-AzApplicationGatewayClientAuthConfiguration -SslProfile $SslProfile
```

<span data-ttu-id="2cd7c-109">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót az ResourceGroup01 nevű erőforráscsoportban tárolja a $AppGw változóban.</span><span class="sxs-lookup"><span data-stu-id="2cd7c-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="2cd7c-110">A második parancs az SslProfile01 nevű SSL-profilt kapja meg a $AppGw, és azt $SslProfile tárolja.</span><span class="sxs-lookup"><span data-stu-id="2cd7c-110">The second command gets the SSL profile named SslProfile01 for $AppGw and stores it $SslProfile variable.</span></span> <span data-ttu-id="2cd7c-111">Az utolsó parancs az SSL-profilból kapja meg az ügyfélhitelesítési $SslProfile és tárolja azt a $ClientAuthConfig változóban.</span><span class="sxs-lookup"><span data-stu-id="2cd7c-111">The last command gets the client authentication configuration from the SSL profile $SslProfile and stores it in the $ClientAuthConfig variable.</span></span>

## <span data-ttu-id="2cd7c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2cd7c-112">PARAMETERS</span></span>

### <span data-ttu-id="2cd7c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cd7c-113">-DefaultProfile</span></span>
<span data-ttu-id="2cd7c-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2cd7c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cd7c-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="2cd7c-115">-SslProfile</span></span>
<span data-ttu-id="2cd7c-116">Az ssl-profil</span><span class="sxs-lookup"><span data-stu-id="2cd7c-116">The ssl profile</span></span>

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

### <span data-ttu-id="2cd7c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cd7c-117">CommonParameters</span></span>
<span data-ttu-id="2cd7c-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cd7c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cd7c-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2cd7c-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cd7c-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2cd7c-120">INPUTS</span></span>

### <span data-ttu-id="2cd7c-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="2cd7c-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="2cd7c-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2cd7c-122">OUTPUTS</span></span>

### <span data-ttu-id="2cd7c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="2cd7c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="2cd7c-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2cd7c-124">NOTES</span></span>

## <span data-ttu-id="2cd7c-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2cd7c-125">RELATED LINKS</span></span>

[<span data-ttu-id="2cd7c-126">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="2cd7c-126">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="2cd7c-127">Add-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="2cd7c-127">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="2cd7c-128">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="2cd7c-128">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="2cd7c-129">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="2cd7c-129">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)