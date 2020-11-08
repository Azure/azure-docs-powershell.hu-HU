---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: b6fe7d8be92e2d82762557a05bf88ef053e0d407
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025210"
---
# <span data-ttu-id="622e3-101">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="622e3-101">Get-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="622e3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="622e3-102">SYNOPSIS</span></span>
<span data-ttu-id="622e3-103">A back-end HTTP Settings objektum kapcsolat-ürítési konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="622e3-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="622e3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="622e3-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="622e3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="622e3-105">DESCRIPTION</span></span>
<span data-ttu-id="622e3-106">A **Get-AzApplicationGatewayConnectionDraining** parancsmag a back-end http Settings objektum kapcsolat-kiürítési konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="622e3-106">The **Get-AzApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="622e3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="622e3-107">EXAMPLES</span></span>

### <span data-ttu-id="622e3-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="622e3-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="622e3-109">Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="622e3-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="622e3-110">A második parancs megkapja a Settings01 $AppGw nevű back-end HTTP-beállításokat, és a $Settings változó beállításait tárolja.</span><span class="sxs-lookup"><span data-stu-id="622e3-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="622e3-111">Az utolsó parancs a kapcsolat-levezetési konfigurációt kapja a back-end HTTP-beállításokból $Settings és a $ConnectionDraining változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="622e3-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="622e3-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="622e3-112">PARAMETERS</span></span>

### <span data-ttu-id="622e3-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="622e3-113">-BackendHttpSettings</span></span>
<span data-ttu-id="622e3-114">A backend http-beállításai</span><span class="sxs-lookup"><span data-stu-id="622e3-114">The backend http settings</span></span>

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

### <span data-ttu-id="622e3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="622e3-115">-DefaultProfile</span></span>
<span data-ttu-id="622e3-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="622e3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="622e3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="622e3-117">CommonParameters</span></span>
<span data-ttu-id="622e3-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="622e3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="622e3-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="622e3-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="622e3-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="622e3-120">INPUTS</span></span>

### <span data-ttu-id="622e3-121">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="622e3-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="622e3-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="622e3-122">OUTPUTS</span></span>

### <span data-ttu-id="622e3-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="622e3-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="622e3-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="622e3-124">NOTES</span></span>

## <span data-ttu-id="622e3-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="622e3-125">RELATED LINKS</span></span>

[<span data-ttu-id="622e3-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="622e3-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="622e3-127">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="622e3-127">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="622e3-128">Új – AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="622e3-128">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="622e3-129">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="622e3-129">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="622e3-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="622e3-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)
