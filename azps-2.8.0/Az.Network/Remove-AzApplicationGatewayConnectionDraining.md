---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 5357b8a0a59fade3e9ff7439da9ac1eeb63f6035
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837890"
---
# <span data-ttu-id="2aee7-101">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="2aee7-101">Remove-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="2aee7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2aee7-102">SYNOPSIS</span></span>
<span data-ttu-id="2aee7-103">Eltávolítja a back-end HTTP Settings objektum kapcsolat-kiürítési konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="2aee7-103">Removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="2aee7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2aee7-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2aee7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2aee7-105">DESCRIPTION</span></span>
<span data-ttu-id="2aee7-106">A **Remove-AzApplicationGatewayConnectionDraining** parancsmag eltávolítja a back-end http Settings objektum kapcsolat-kiürítési konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="2aee7-106">The **Remove-AzApplicationGatewayConnectionDraining** cmdlet removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="2aee7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2aee7-107">EXAMPLES</span></span>

### <span data-ttu-id="2aee7-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2aee7-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="2aee7-109">Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2aee7-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="2aee7-110">A második parancs megkapja a Settings01 $AppGw nevű back-end HTTP-beállításokat, és a $Settings változó beállításait tárolja.</span><span class="sxs-lookup"><span data-stu-id="2aee7-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="2aee7-111">Az utolsó parancs eltávolítja a $Settings-on tárolt back-end HTTP-beállítások kapcsolat-kiürítési konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="2aee7-111">The last command removes the connection draining configuration of the back-end HTTP settings stored in $Settings.</span></span>

## <span data-ttu-id="2aee7-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2aee7-112">PARAMETERS</span></span>

### <span data-ttu-id="2aee7-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2aee7-113">-BackendHttpSettings</span></span>
<span data-ttu-id="2aee7-114">A backend http-beállításai</span><span class="sxs-lookup"><span data-stu-id="2aee7-114">The backend http settings</span></span>

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

### <span data-ttu-id="2aee7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aee7-115">-DefaultProfile</span></span>
<span data-ttu-id="2aee7-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2aee7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2aee7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aee7-117">CommonParameters</span></span>
<span data-ttu-id="2aee7-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2aee7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aee7-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2aee7-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aee7-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2aee7-120">INPUTS</span></span>

### <span data-ttu-id="2aee7-121">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2aee7-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="2aee7-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2aee7-122">OUTPUTS</span></span>

### <span data-ttu-id="2aee7-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2aee7-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="2aee7-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2aee7-124">NOTES</span></span>

## <span data-ttu-id="2aee7-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2aee7-125">RELATED LINKS</span></span>

[<span data-ttu-id="2aee7-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2aee7-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="2aee7-127">Get-AzApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2aee7-127">Get-AzApplicationGatewayBackendHttpSettings</span></span>](./Get-AzApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="2aee7-128">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="2aee7-128">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="2aee7-129">Új – AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="2aee7-129">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="2aee7-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="2aee7-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

