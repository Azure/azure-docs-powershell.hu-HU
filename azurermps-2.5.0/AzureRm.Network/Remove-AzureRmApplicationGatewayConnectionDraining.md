---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayconnectiondraining
schema: 2.0.0
ms.openlocfilehash: 751e27600d81a24005ea0a9200d3efa1d1647597
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850650"
---
# <span data-ttu-id="08cf4-101">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="08cf4-101">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="08cf4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="08cf4-102">SYNOPSIS</span></span>
<span data-ttu-id="08cf4-103">Eltávolítja a back-end HTTP Settings objektum kapcsolat-kiürítési konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="08cf4-103">Removes the connection draining configuration of a back-end HTTP settings object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08cf4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="08cf4-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayConnectionDraining
 -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="08cf4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="08cf4-105">DESCRIPTION</span></span>
<span data-ttu-id="08cf4-106">A **Remove-AzureRmApplicationGatewayConnectionDraining** parancsmag eltávolítja a back-end http Settings objektum kapcsolat-kiürítési konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="08cf4-106">The **Remove-AzureRmApplicationGatewayConnectionDraining** cmdlet removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="08cf4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="08cf4-107">EXAMPLES</span></span>

### <span data-ttu-id="08cf4-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="08cf4-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Remove-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="08cf4-109">Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="08cf4-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="08cf4-110">A második parancs megkapja a Settings01 $AppGw nevű back-end HTTP-beállításokat, és a $Settings változó beállításait tárolja.</span><span class="sxs-lookup"><span data-stu-id="08cf4-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="08cf4-111">Az utolsó parancs eltávolítja a $Settings-on tárolt back-end HTTP-beállítások kapcsolat-kiürítési konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="08cf4-111">The last command removes the connection draining configuration of the back-end HTTP settings stored in $Settings.</span></span>

## <span data-ttu-id="08cf4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="08cf4-112">PARAMETERS</span></span>

### <span data-ttu-id="08cf4-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="08cf4-113">-BackendHttpSettings</span></span>
<span data-ttu-id="08cf4-114">A backend http-beállításai</span><span class="sxs-lookup"><span data-stu-id="08cf4-114">The backend http settings</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08cf4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08cf4-115">-DefaultProfile</span></span>
<span data-ttu-id="08cf4-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="08cf4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08cf4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08cf4-117">CommonParameters</span></span>
<span data-ttu-id="08cf4-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="08cf4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08cf4-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08cf4-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08cf4-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="08cf4-120">INPUTS</span></span>

### <span data-ttu-id="08cf4-121">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="08cf4-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="08cf4-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="08cf4-122">OUTPUTS</span></span>

### <span data-ttu-id="08cf4-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="08cf4-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="08cf4-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="08cf4-124">NOTES</span></span>

## <span data-ttu-id="08cf4-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="08cf4-125">RELATED LINKS</span></span>

[<span data-ttu-id="08cf4-126">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="08cf4-126">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="08cf4-127">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="08cf4-127">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./Get-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="08cf4-128">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="08cf4-128">Get-AzureRmApplicationGatewayConnectionDraining</span></span>](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="08cf4-129">Új – AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="08cf4-129">New-AzureRmApplicationGatewayConnectionDraining</span></span>](./New-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="08cf4-130">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="08cf4-130">Set-AzureRmApplicationGatewayConnectionDraining</span></span>](./Set-AzureRmApplicationGatewayConnectionDraining.md)

