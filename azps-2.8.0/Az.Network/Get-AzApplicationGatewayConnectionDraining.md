---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 1630b0177efbccbf4d1cba674f0cf11ab457307e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100397917"
---
# <span data-ttu-id="2936f-101">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="2936f-101">Get-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="2936f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2936f-102">SYNOPSIS</span></span>
<span data-ttu-id="2936f-103">Egy háttér-HTTP-beállításobjektum kapcsolatelvezetési konfigurációját használja.</span><span class="sxs-lookup"><span data-stu-id="2936f-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="2936f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2936f-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2936f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2936f-105">DESCRIPTION</span></span>
<span data-ttu-id="2936f-106">A **Get-AzApplicationGatewayConnectionDraining** parancsmag lecsökkenti a háttér HTTP-beállítások objektumának csatlakozás-ürítési konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="2936f-106">The **Get-AzApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="2936f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2936f-107">EXAMPLES</span></span>

### <span data-ttu-id="2936f-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="2936f-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="2936f-109">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót az ResourceGroup01 nevű erőforráscsoportban tárolja a $AppGw változóban.</span><span class="sxs-lookup"><span data-stu-id="2936f-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="2936f-110">A második parancs a Beállítások01 nevű háttér-HTTP-beállításokat kapja $AppGw és a beállításokat a $Settings változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2936f-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="2936f-111">Az utolsó parancs lecsökkenti a kapcsolat konfigurációját a háttér-HTTP-beállításokból$Settings és tárolja a $ConnectionDraining változóban.</span><span class="sxs-lookup"><span data-stu-id="2936f-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="2936f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2936f-112">PARAMETERS</span></span>

### <span data-ttu-id="2936f-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2936f-113">-BackendHttpSettings</span></span>
<span data-ttu-id="2936f-114">A háttér http-beállításai</span><span class="sxs-lookup"><span data-stu-id="2936f-114">The backend http settings</span></span>

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

### <span data-ttu-id="2936f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2936f-115">-DefaultProfile</span></span>
<span data-ttu-id="2936f-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2936f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2936f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2936f-117">CommonParameters</span></span>
<span data-ttu-id="2936f-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2936f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2936f-119">További információt a [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2936f-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2936f-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2936f-120">INPUTS</span></span>

### <span data-ttu-id="2936f-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2936f-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="2936f-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2936f-122">OUTPUTS</span></span>

### <span data-ttu-id="2936f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="2936f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="2936f-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2936f-124">NOTES</span></span>

## <span data-ttu-id="2936f-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2936f-125">RELATED LINKS</span></span>

[<span data-ttu-id="2936f-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2936f-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)


[<span data-ttu-id="2936f-127">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="2936f-127">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="2936f-128">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="2936f-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="2936f-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="2936f-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)
