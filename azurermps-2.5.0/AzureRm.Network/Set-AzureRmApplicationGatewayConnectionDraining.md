---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayconnectiondraining
schema: 2.0.0
ms.openlocfilehash: ab876b5bc0ea63a2299ec17168b56125c9dbcdba
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849094"
---
# <span data-ttu-id="de625-101">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="de625-101">Set-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="de625-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="de625-102">SYNOPSIS</span></span>
<span data-ttu-id="de625-103">Egy back-end HTTP Settings objektum kapcsolat-kiürítési konfigurációjának módosítása.</span><span class="sxs-lookup"><span data-stu-id="de625-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de625-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="de625-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de625-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="de625-105">DESCRIPTION</span></span>
<span data-ttu-id="de625-106">A **set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** parancsmag a back-end http Settings objektum kapcsolat-kiürítési konfigurációját módosítja.</span><span class="sxs-lookup"><span data-stu-id="de625-106">The **Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="de625-107">Példák</span><span class="sxs-lookup"><span data-stu-id="de625-107">EXAMPLES</span></span>

### <span data-ttu-id="de625-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="de625-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="de625-109">Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="de625-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="de625-110">A második parancs megkapja a Settings01 $AppGw nevű back-end HTTP-beállításokat, és a $Settings változó beállításait tárolja.</span><span class="sxs-lookup"><span data-stu-id="de625-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="de625-111">A legutóbbi parancs módosította a $Settingsban tárolt back-end HTTP Settings objektum kapcsolat-ürítési konfigurációját, a False értékre és a DrainTimeoutInSec az 3600-be való engedélyezésével.</span><span class="sxs-lookup"><span data-stu-id="de625-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="de625-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="de625-112">PARAMETERS</span></span>

### <span data-ttu-id="de625-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="de625-113">-BackendHttpSettings</span></span>
<span data-ttu-id="de625-114">A backend http-beállításai</span><span class="sxs-lookup"><span data-stu-id="de625-114">The backend http settings</span></span>

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

### <span data-ttu-id="de625-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de625-115">-DefaultProfile</span></span>
<span data-ttu-id="de625-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="de625-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de625-117">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="de625-117">-DrainTimeoutInSec</span></span>
<span data-ttu-id="de625-118">A kapcsolat ürítésének száma másodpercben.</span><span class="sxs-lookup"><span data-stu-id="de625-118">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="de625-119">Az elfogadható értékek 1 másodpercről 3600 másodpercre.</span><span class="sxs-lookup"><span data-stu-id="de625-119">Acceptable values are from 1 second to 3600 seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de625-120">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="de625-120">-Enabled</span></span>
<span data-ttu-id="de625-121">Engedélyezve van-e a kapcsolat kiürítése?</span><span class="sxs-lookup"><span data-stu-id="de625-121">Whether connection draining is enabled or not.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de625-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de625-122">CommonParameters</span></span>
<span data-ttu-id="de625-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="de625-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de625-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de625-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de625-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="de625-125">INPUTS</span></span>

### <span data-ttu-id="de625-126">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="de625-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="de625-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de625-127">OUTPUTS</span></span>

### <span data-ttu-id="de625-128">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="de625-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="de625-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="de625-129">NOTES</span></span>

## <span data-ttu-id="de625-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de625-130">RELATED LINKS</span></span>

[<span data-ttu-id="de625-131">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="de625-131">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="de625-132">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="de625-132">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./Get-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="de625-133">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="de625-133">Get-AzureRmApplicationGatewayConnectionDraining</span></span>](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="de625-134">Új – AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="de625-134">New-AzureRmApplicationGatewayConnectionDraining</span></span>](./New-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="de625-135">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="de625-135">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

