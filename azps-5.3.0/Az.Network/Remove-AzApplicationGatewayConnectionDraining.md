---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 98b097e0be8d4b08ba16d5af06fbec1a2f3d66de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378809"
---
# <span data-ttu-id="18509-101">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="18509-101">Remove-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="18509-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18509-102">SYNOPSIS</span></span>
<span data-ttu-id="18509-103">A háttér HTTP-beállításobjektum kapcsolatelvezetési konfigurációjának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="18509-103">Removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="18509-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="18509-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18509-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="18509-105">DESCRIPTION</span></span>
<span data-ttu-id="18509-106">A **Remove-AzApplicationGatewayConnectionDraining** parancsmag eltávolítja a háttér HTTP-beállításobjektum kapcsolatleerítési konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="18509-106">The **Remove-AzApplicationGatewayConnectionDraining** cmdlet removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="18509-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="18509-107">EXAMPLES</span></span>

### <span data-ttu-id="18509-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="18509-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="18509-109">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót az ResourceGroup01 nevű erőforráscsoportban tárolja a $AppGw változóban.</span><span class="sxs-lookup"><span data-stu-id="18509-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="18509-110">A második parancs a Beállítások01 nevű háttér-HTTP-beállításokat kapja $AppGw és a beállításokat a $Settings változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="18509-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="18509-111">Az utolsó parancs eltávolítja a háttér HTTP-beállítások kapcsolatelvezetési konfigurációját, amely a $Settings.</span><span class="sxs-lookup"><span data-stu-id="18509-111">The last command removes the connection draining configuration of the back-end HTTP settings stored in $Settings.</span></span>

## <span data-ttu-id="18509-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18509-112">PARAMETERS</span></span>

### <span data-ttu-id="18509-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="18509-113">-BackendHttpSettings</span></span>
<span data-ttu-id="18509-114">A háttér http-beállításai</span><span class="sxs-lookup"><span data-stu-id="18509-114">The backend http settings</span></span>

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

### <span data-ttu-id="18509-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18509-115">-DefaultProfile</span></span>
<span data-ttu-id="18509-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="18509-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18509-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18509-117">CommonParameters</span></span>
<span data-ttu-id="18509-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18509-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18509-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18509-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18509-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="18509-120">INPUTS</span></span>

### <span data-ttu-id="18509-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="18509-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="18509-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18509-122">OUTPUTS</span></span>

### <span data-ttu-id="18509-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="18509-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="18509-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="18509-124">NOTES</span></span>

## <span data-ttu-id="18509-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18509-125">RELATED LINKS</span></span>

[<span data-ttu-id="18509-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="18509-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="18509-127">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="18509-127">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="18509-128">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="18509-128">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="18509-129">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="18509-129">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="18509-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="18509-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

