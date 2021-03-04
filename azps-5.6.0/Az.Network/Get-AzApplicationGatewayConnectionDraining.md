---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 3d1df3262fa9cee55d5aa49c026b7b1e681b5c00
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941778"
---
# <span data-ttu-id="593b4-101">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="593b4-101">Get-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="593b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="593b4-102">SYNOPSIS</span></span>
<span data-ttu-id="593b4-103">Egy háttér-HTTP-beállításobjektum kapcsolatelvezetési konfigurációját használja.</span><span class="sxs-lookup"><span data-stu-id="593b4-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="593b4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="593b4-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="593b4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="593b4-105">DESCRIPTION</span></span>
<span data-ttu-id="593b4-106">A **Get-AzApplicationGatewayConnectionDraining** parancsmag lecsökkenti a háttér-HTTP-beállítások objektum kapcsolatlepárolási konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="593b4-106">The **Get-AzApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="593b4-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="593b4-107">EXAMPLES</span></span>

### <span data-ttu-id="593b4-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="593b4-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="593b4-109">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót az ResourceGroup01 nevű erőforráscsoportban tárolja a $AppGw változóban.</span><span class="sxs-lookup"><span data-stu-id="593b4-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="593b4-110">A második parancs a Beállítások01 nevű háttér-HTTP-beállításokat kapja $AppGw és a beállításokat a $Settings változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="593b4-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="593b4-111">Az utolsó parancs lecsökkenti a kapcsolat konfigurációját a háttér-HTTP-beállításokból$Settings és tárolja a $ConnectionDraining változóban.</span><span class="sxs-lookup"><span data-stu-id="593b4-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="593b4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="593b4-112">PARAMETERS</span></span>

### <span data-ttu-id="593b4-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="593b4-113">-BackendHttpSettings</span></span>
<span data-ttu-id="593b4-114">A háttér http-beállításai</span><span class="sxs-lookup"><span data-stu-id="593b4-114">The backend http settings</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="593b4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="593b4-115">-DefaultProfile</span></span>
<span data-ttu-id="593b4-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="593b4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="593b4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="593b4-117">CommonParameters</span></span>
<span data-ttu-id="593b4-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="593b4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="593b4-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="593b4-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="593b4-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="593b4-120">INPUTS</span></span>

### <span data-ttu-id="593b4-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="593b4-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="593b4-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="593b4-122">OUTPUTS</span></span>

### <span data-ttu-id="593b4-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="593b4-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="593b4-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="593b4-124">NOTES</span></span>

## <span data-ttu-id="593b4-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="593b4-125">RELATED LINKS</span></span>

[<span data-ttu-id="593b4-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="593b4-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="593b4-127">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="593b4-127">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="593b4-128">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="593b4-128">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="593b4-129">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="593b4-129">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="593b4-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="593b4-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)
