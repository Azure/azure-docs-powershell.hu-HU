---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 78c3a151f066d8ff05e92798ebad822943816af8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493447"
---
# <span data-ttu-id="f04c9-101">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f04c9-101">Get-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="f04c9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f04c9-102">SYNOPSIS</span></span>
<span data-ttu-id="f04c9-103">A back-end HTTP Settings objektum kapcsolat-ürítési konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f04c9-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f04c9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f04c9-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f04c9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f04c9-105">DESCRIPTION</span></span>
<span data-ttu-id="f04c9-106">A **Get-AzureRmApplicationGatewayConnectionDraining** parancsmag a back-end http Settings objektum kapcsolat-kiürítési konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f04c9-106">The **Get-AzureRmApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="f04c9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f04c9-107">EXAMPLES</span></span>

### <span data-ttu-id="f04c9-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f04c9-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="f04c9-109">Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f04c9-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f04c9-110">A második parancs megkapja a Settings01 $AppGw nevű back-end HTTP-beállításokat, és a $Settings változó beállításait tárolja.</span><span class="sxs-lookup"><span data-stu-id="f04c9-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="f04c9-111">Az utolsó parancs a kapcsolat-levezetési konfigurációt kapja a back-end HTTP-beállításokból $Settings és a $ConnectionDraining változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f04c9-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="f04c9-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f04c9-112">PARAMETERS</span></span>

### <span data-ttu-id="f04c9-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f04c9-113">-BackendHttpSettings</span></span>
<span data-ttu-id="f04c9-114">A backend http-beállításai</span><span class="sxs-lookup"><span data-stu-id="f04c9-114">The backend http settings</span></span>

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

### <span data-ttu-id="f04c9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f04c9-115">-DefaultProfile</span></span>
<span data-ttu-id="f04c9-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f04c9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f04c9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f04c9-117">CommonParameters</span></span>
<span data-ttu-id="f04c9-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f04c9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f04c9-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f04c9-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f04c9-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f04c9-120">INPUTS</span></span>

### <span data-ttu-id="f04c9-121">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f04c9-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="f04c9-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f04c9-122">OUTPUTS</span></span>

### <span data-ttu-id="f04c9-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f04c9-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="f04c9-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f04c9-124">NOTES</span></span>

## <span data-ttu-id="f04c9-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f04c9-125">RELATED LINKS</span></span>

[<span data-ttu-id="f04c9-126">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f04c9-126">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="f04c9-127">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f04c9-127">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./Get-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="f04c9-128">Új – AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f04c9-128">New-AzureRmApplicationGatewayConnectionDraining</span></span>](./New-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="f04c9-129">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f04c9-129">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="f04c9-130">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f04c9-130">Set-AzureRmApplicationGatewayConnectionDraining</span></span>](./Set-AzureRmApplicationGatewayConnectionDraining.md)
