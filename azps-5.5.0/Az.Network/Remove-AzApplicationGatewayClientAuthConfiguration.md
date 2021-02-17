---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 64dc67a59b739ac7cab51c9c4a02fd7a73f8b4cc
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407590"
---
# <span data-ttu-id="89969-101">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="89969-101">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="89969-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89969-102">SYNOPSIS</span></span>
<span data-ttu-id="89969-103">Eltávolítja egy SSL-profilobjektum ügyfélhitelesítési konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="89969-103">Removes the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="89969-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="89969-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89969-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="89969-105">DESCRIPTION</span></span>
<span data-ttu-id="89969-106">A **Remove-AzApplicationGatewayClientAuthConfiguration** parancsmag eltávolítja az SSL-profilobjektumok ügyfél-hitelesítési konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="89969-106">The **Remove-AzApplicationGatewayClientAuthConfiguration** cmdlet removes the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="89969-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="89969-107">EXAMPLES</span></span>

### <span data-ttu-id="89969-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="89969-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "Profile01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayClientAuthConfiguration -SslProfile $profile
```

<span data-ttu-id="89969-109">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót az ResourceGroup01 nevű erőforráscsoportban tárolja a $AppGw változóban.</span><span class="sxs-lookup"><span data-stu-id="89969-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="89969-110">A második parancs a Profil01 nevű SSL-profilt kapja $AppGw és tárolja a $profile változóban.</span><span class="sxs-lookup"><span data-stu-id="89969-110">The second command gets the SSL profile named Profile01 for $AppGw and stores it in the $profile variable.</span></span> <span data-ttu-id="89969-111">Az utolsó parancs eltávolítja a fájlban tárolt ssl-profil ügyfélhitelesítési $profile.</span><span class="sxs-lookup"><span data-stu-id="89969-111">The last command removes the client authentication configuration of the ssl profile stored in $profile.</span></span>

## <span data-ttu-id="89969-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89969-112">PARAMETERS</span></span>

### <span data-ttu-id="89969-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89969-113">-DefaultProfile</span></span>
<span data-ttu-id="89969-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="89969-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89969-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="89969-115">-SslProfile</span></span>
<span data-ttu-id="89969-116">Az ssl-profil</span><span class="sxs-lookup"><span data-stu-id="89969-116">The ssl profile</span></span>

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

### <span data-ttu-id="89969-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89969-117">CommonParameters</span></span>
<span data-ttu-id="89969-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89969-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89969-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89969-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89969-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="89969-120">INPUTS</span></span>

### <span data-ttu-id="89969-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="89969-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="89969-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89969-122">OUTPUTS</span></span>

### <span data-ttu-id="89969-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="89969-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="89969-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="89969-124">NOTES</span></span>

## <span data-ttu-id="89969-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89969-125">RELATED LINKS</span></span>

[<span data-ttu-id="89969-126">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="89969-126">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)


[<span data-ttu-id="89969-127">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="89969-127">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="89969-128">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="89969-128">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)
