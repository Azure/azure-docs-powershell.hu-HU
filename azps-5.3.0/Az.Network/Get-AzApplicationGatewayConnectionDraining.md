---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: b6fe7d8be92e2d82762557a05bf88ef053e0d407
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468210"
---
# <span data-ttu-id="f5ca2-101">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f5ca2-101">Get-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="f5ca2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5ca2-102">SYNOPSIS</span></span>
<span data-ttu-id="f5ca2-103">Egy háttér-HTTP-beállításobjektum kapcsolatelvezetési konfigurációját használja.</span><span class="sxs-lookup"><span data-stu-id="f5ca2-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="f5ca2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f5ca2-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5ca2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f5ca2-105">DESCRIPTION</span></span>
<span data-ttu-id="f5ca2-106">A **Get-AzApplicationGatewayConnectionDraining** parancsmag lecsökkenti a háttér HTTP-beállítások objektumának csatlakozás-ürítési konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="f5ca2-106">The **Get-AzApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="f5ca2-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f5ca2-107">EXAMPLES</span></span>

### <span data-ttu-id="f5ca2-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="f5ca2-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="f5ca2-109">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót az ResourceGroup01 nevű erőforráscsoportban tárolja a $AppGw változóban.</span><span class="sxs-lookup"><span data-stu-id="f5ca2-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f5ca2-110">A második parancs a Beállítások01 nevű háttér-HTTP-beállításokat kapja $AppGw és a beállításokat a $Settings változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f5ca2-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="f5ca2-111">Az utolsó parancs lecsökkenti a kapcsolat konfigurációját a háttér-HTTP-beállításokból$Settings és tárolja a $ConnectionDraining változóban.</span><span class="sxs-lookup"><span data-stu-id="f5ca2-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="f5ca2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5ca2-112">PARAMETERS</span></span>

### <span data-ttu-id="f5ca2-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f5ca2-113">-BackendHttpSettings</span></span>
<span data-ttu-id="f5ca2-114">A háttér http-beállításai</span><span class="sxs-lookup"><span data-stu-id="f5ca2-114">The backend http settings</span></span>

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

### <span data-ttu-id="f5ca2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5ca2-115">-DefaultProfile</span></span>
<span data-ttu-id="f5ca2-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f5ca2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5ca2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5ca2-117">CommonParameters</span></span>
<span data-ttu-id="f5ca2-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5ca2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5ca2-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5ca2-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5ca2-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f5ca2-120">INPUTS</span></span>

### <span data-ttu-id="f5ca2-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f5ca2-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="f5ca2-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5ca2-122">OUTPUTS</span></span>

### <span data-ttu-id="f5ca2-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f5ca2-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="f5ca2-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f5ca2-124">NOTES</span></span>

## <span data-ttu-id="f5ca2-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f5ca2-125">RELATED LINKS</span></span>

[<span data-ttu-id="f5ca2-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f5ca2-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="f5ca2-127">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="f5ca2-127">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="f5ca2-128">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f5ca2-128">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="f5ca2-129">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f5ca2-129">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="f5ca2-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f5ca2-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)
