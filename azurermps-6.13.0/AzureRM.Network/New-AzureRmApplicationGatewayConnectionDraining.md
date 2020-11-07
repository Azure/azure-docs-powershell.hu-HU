---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: b0f459d6884c9588036668743edc58333ecc1275
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680647"
---
# <span data-ttu-id="01af5-101">New-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="01af5-101">New-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="01af5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="01af5-102">SYNOPSIS</span></span>
<span data-ttu-id="01af5-103">Új kapcsolat-kiürítési konfigurációt hoz létre a back-end HTTP-beállításokhoz.</span><span class="sxs-lookup"><span data-stu-id="01af5-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01af5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="01af5-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01af5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="01af5-105">DESCRIPTION</span></span>
<span data-ttu-id="01af5-106">A **New-AzureRmApplicationGatewayConnectionDraining** parancsmag új kapcsolat-elvezetési konfigurációt hoz létre a back-end http-beállításokhoz.</span><span class="sxs-lookup"><span data-stu-id="01af5-106">The **New-AzureRmApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="01af5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="01af5-107">EXAMPLES</span></span>

### <span data-ttu-id="01af5-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="01af5-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzureRmApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="01af5-109">A parancs létrehoz egy új kapcsolat-elvezetési konfigurációt, melyen engedélyezve van a set to True és a DrainTimeoutInSec értéke 42 másodpercre, és a $connectionDraining-ban tárolja.</span><span class="sxs-lookup"><span data-stu-id="01af5-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="01af5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="01af5-110">PARAMETERS</span></span>

### <span data-ttu-id="01af5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01af5-111">-DefaultProfile</span></span>
<span data-ttu-id="01af5-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="01af5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01af5-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="01af5-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="01af5-114">A kapcsolat ürítésének száma másodpercben.</span><span class="sxs-lookup"><span data-stu-id="01af5-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="01af5-115">Az elfogadható értékek 1 másodpercről 3600 másodpercre.</span><span class="sxs-lookup"><span data-stu-id="01af5-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="01af5-116">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="01af5-116">-Enabled</span></span>
<span data-ttu-id="01af5-117">Engedélyezve van-e a kapcsolat kiürítése?</span><span class="sxs-lookup"><span data-stu-id="01af5-117">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="01af5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01af5-118">CommonParameters</span></span>
<span data-ttu-id="01af5-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="01af5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01af5-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01af5-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01af5-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="01af5-121">INPUTS</span></span>

### <span data-ttu-id="01af5-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="01af5-122">None</span></span>

## <span data-ttu-id="01af5-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01af5-123">OUTPUTS</span></span>

### <span data-ttu-id="01af5-124">Microsoft. Azure. commands. Network. models. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="01af5-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="01af5-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="01af5-125">NOTES</span></span>

## <span data-ttu-id="01af5-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01af5-126">RELATED LINKS</span></span>

[<span data-ttu-id="01af5-127">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="01af5-127">Get-AzureRmApplicationGatewayConnectionDraining</span></span>](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="01af5-128">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="01af5-128">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="01af5-129">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="01af5-129">Set-AzureRmApplicationGatewayConnectionDraining</span></span>](./Set-AzureRmApplicationGatewayConnectionDraining.md)

