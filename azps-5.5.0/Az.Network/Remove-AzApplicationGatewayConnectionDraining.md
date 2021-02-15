---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 98b097e0be8d4b08ba16d5af06fbec1a2f3d66de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151571"
---
# <span data-ttu-id="80446-101">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="80446-101">Remove-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="80446-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80446-102">SYNOPSIS</span></span>
<span data-ttu-id="80446-103">Eltávolítja a háttér HTTP-beállítások objektum kapcsolatelvezetési konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="80446-103">Removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="80446-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="80446-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80446-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="80446-105">DESCRIPTION</span></span>
<span data-ttu-id="80446-106">A **Remove-AzApplicationGatewayConnectionDraining** parancsmag eltávolítja a háttér HTTP-beállításobjektum kapcsolatleerítési konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="80446-106">The **Remove-AzApplicationGatewayConnectionDraining** cmdlet removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="80446-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="80446-107">EXAMPLES</span></span>

### <span data-ttu-id="80446-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="80446-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="80446-109">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót az ResourceGroup01 nevű erőforráscsoportban tárolja a $AppGw változóban.</span><span class="sxs-lookup"><span data-stu-id="80446-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="80446-110">A második parancs a Beállítások01 nevű háttér-HTTP-beállításokat kapja $AppGw és a beállításokat a $Settings változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="80446-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="80446-111">Az utolsó parancs eltávolítja a háttér HTTP-beállítások kapcsolatelvezetési konfigurációját, amely a $Settings.</span><span class="sxs-lookup"><span data-stu-id="80446-111">The last command removes the connection draining configuration of the back-end HTTP settings stored in $Settings.</span></span>

## <span data-ttu-id="80446-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80446-112">PARAMETERS</span></span>

### <span data-ttu-id="80446-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="80446-113">-BackendHttpSettings</span></span>
<span data-ttu-id="80446-114">A háttér http-beállításai</span><span class="sxs-lookup"><span data-stu-id="80446-114">The backend http settings</span></span>

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

### <span data-ttu-id="80446-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80446-115">-DefaultProfile</span></span>
<span data-ttu-id="80446-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="80446-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80446-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80446-117">CommonParameters</span></span>
<span data-ttu-id="80446-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80446-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80446-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80446-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80446-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="80446-120">INPUTS</span></span>

### <span data-ttu-id="80446-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="80446-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="80446-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="80446-122">OUTPUTS</span></span>

### <span data-ttu-id="80446-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="80446-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="80446-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="80446-124">NOTES</span></span>

## <span data-ttu-id="80446-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="80446-125">RELATED LINKS</span></span>

[<span data-ttu-id="80446-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="80446-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="80446-127">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="80446-127">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="80446-128">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="80446-128">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="80446-129">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="80446-129">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="80446-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="80446-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

