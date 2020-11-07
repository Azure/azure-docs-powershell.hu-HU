---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: d04dc0c3d9d446941870f30578f50d5ecd795009
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670065"
---
# <span data-ttu-id="42dbe-101">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="42dbe-101">Set-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="42dbe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="42dbe-102">SYNOPSIS</span></span>
<span data-ttu-id="42dbe-103">Egy back-end HTTP Settings objektum kapcsolat-kiürítési konfigurációjának módosítása.</span><span class="sxs-lookup"><span data-stu-id="42dbe-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="42dbe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="42dbe-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42dbe-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="42dbe-105">DESCRIPTION</span></span>
<span data-ttu-id="42dbe-106">A **set-AzApplicationGatewayWebApplicationFirewallConfiguration** parancsmag a back-end http Settings objektum kapcsolat-kiürítési konfigurációját módosítja.</span><span class="sxs-lookup"><span data-stu-id="42dbe-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="42dbe-107">Példák</span><span class="sxs-lookup"><span data-stu-id="42dbe-107">EXAMPLES</span></span>

### <span data-ttu-id="42dbe-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="42dbe-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="42dbe-109">Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="42dbe-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="42dbe-110">A második parancs megkapja a Settings01 $AppGw nevű back-end HTTP-beállításokat, és a $Settings változó beállításait tárolja.</span><span class="sxs-lookup"><span data-stu-id="42dbe-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="42dbe-111">A legutóbbi parancs módosította a $Settingsban tárolt back-end HTTP Settings objektum kapcsolat-ürítési konfigurációját, a False értékre és a DrainTimeoutInSec az 3600-be való engedélyezésével.</span><span class="sxs-lookup"><span data-stu-id="42dbe-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="42dbe-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="42dbe-112">PARAMETERS</span></span>

### <span data-ttu-id="42dbe-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="42dbe-113">-BackendHttpSettings</span></span>
<span data-ttu-id="42dbe-114">A backend http-beállításai</span><span class="sxs-lookup"><span data-stu-id="42dbe-114">The backend http settings</span></span>

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

### <span data-ttu-id="42dbe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42dbe-115">-DefaultProfile</span></span>
<span data-ttu-id="42dbe-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="42dbe-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42dbe-117">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="42dbe-117">-DrainTimeoutInSec</span></span>
<span data-ttu-id="42dbe-118">A kapcsolat ürítésének száma másodpercben.</span><span class="sxs-lookup"><span data-stu-id="42dbe-118">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="42dbe-119">Az elfogadható értékek 1 másodpercről 3600 másodpercre.</span><span class="sxs-lookup"><span data-stu-id="42dbe-119">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="42dbe-120">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="42dbe-120">-Enabled</span></span>
<span data-ttu-id="42dbe-121">Engedélyezve van-e a kapcsolat kiürítése?</span><span class="sxs-lookup"><span data-stu-id="42dbe-121">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="42dbe-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42dbe-122">CommonParameters</span></span>
<span data-ttu-id="42dbe-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="42dbe-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42dbe-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42dbe-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42dbe-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="42dbe-125">INPUTS</span></span>

### <span data-ttu-id="42dbe-126">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="42dbe-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="42dbe-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="42dbe-127">OUTPUTS</span></span>

### <span data-ttu-id="42dbe-128">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="42dbe-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="42dbe-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="42dbe-129">NOTES</span></span>

## <span data-ttu-id="42dbe-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="42dbe-130">RELATED LINKS</span></span>

[<span data-ttu-id="42dbe-131">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="42dbe-131">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="42dbe-132">Get-AzApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="42dbe-132">Get-AzApplicationGatewayBackendHttpSettings</span></span>](./Get-AzApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="42dbe-133">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="42dbe-133">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="42dbe-134">Új – AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="42dbe-134">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="42dbe-135">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="42dbe-135">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

