---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 84a9ccb86f9fd1d4995ad52e913059181c0b887e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926506"
---
# <span data-ttu-id="8f531-101">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="8f531-101">Set-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="8f531-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f531-102">SYNOPSIS</span></span>
<span data-ttu-id="8f531-103">Módosítja a háttér HTTP-beállítások objektum kapcsolatelvezetési konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="8f531-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="8f531-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8f531-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f531-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8f531-105">DESCRIPTION</span></span>
<span data-ttu-id="8f531-106">A **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** parancsmag módosítja egy háttér-HTTP-beállítási objektum kapcsolat-ürítési konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="8f531-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="8f531-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8f531-107">EXAMPLES</span></span>

### <span data-ttu-id="8f531-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="8f531-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="8f531-109">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót az ResourceGroup01 nevű erőforráscsoportban tárolja a $AppGw változóban.</span><span class="sxs-lookup"><span data-stu-id="8f531-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="8f531-110">A második parancs a Beállítások01 nevű háttér-HTTP-beállításokat kapja $AppGw és a beállításokat a $Settings változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="8f531-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="8f531-111">Az utolsó parancs módosítja az $Settings-ben tárolt háttér HTTP-beállítások objektum kapcsolatelvezetési konfigurációját úgy, hogy az Engedélyezve a Hamis, az DrainTimeoutInSec beállítást pedig 3600-ra módosítja.</span><span class="sxs-lookup"><span data-stu-id="8f531-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="8f531-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f531-112">PARAMETERS</span></span>

### <span data-ttu-id="8f531-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="8f531-113">-BackendHttpSettings</span></span>
<span data-ttu-id="8f531-114">A háttér http-beállításai</span><span class="sxs-lookup"><span data-stu-id="8f531-114">The backend http settings</span></span>

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

### <span data-ttu-id="8f531-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f531-115">-DefaultProfile</span></span>
<span data-ttu-id="8f531-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8f531-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f531-117">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="8f531-117">-DrainTimeoutInSec</span></span>
<span data-ttu-id="8f531-118">Aktív a kapcsolatelvezetés másodpercek alatt lefolyatva.</span><span class="sxs-lookup"><span data-stu-id="8f531-118">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="8f531-119">Az elfogadható értékek 1 másodperctől 3600 másodpercig esnek.</span><span class="sxs-lookup"><span data-stu-id="8f531-119">Acceptable values are from 1 second to 3600 seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f531-120">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="8f531-120">-Enabled</span></span>
<span data-ttu-id="8f531-121">Hogy engedélyezve van-e a kapcsolat lemerülése.</span><span class="sxs-lookup"><span data-stu-id="8f531-121">Whether connection draining is enabled or not.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f531-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f531-122">CommonParameters</span></span>
<span data-ttu-id="8f531-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f531-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f531-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f531-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f531-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8f531-125">INPUTS</span></span>

### <span data-ttu-id="8f531-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="8f531-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="8f531-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f531-127">OUTPUTS</span></span>

### <span data-ttu-id="8f531-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="8f531-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="8f531-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8f531-129">NOTES</span></span>

## <span data-ttu-id="8f531-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f531-130">RELATED LINKS</span></span>

[<span data-ttu-id="8f531-131">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8f531-131">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="8f531-132">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="8f531-132">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="8f531-133">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="8f531-133">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="8f531-134">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="8f531-134">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="8f531-135">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="8f531-135">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

