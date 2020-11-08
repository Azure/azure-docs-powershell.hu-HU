---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 679a1311526f7fa5028c83e6571001d14b2ff3f5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014836"
---
# <span data-ttu-id="cba20-101">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="cba20-101">New-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="cba20-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cba20-102">SYNOPSIS</span></span>
<span data-ttu-id="cba20-103">Új kapcsolat-kiürítési konfigurációt hoz létre a back-end HTTP-beállításokhoz.</span><span class="sxs-lookup"><span data-stu-id="cba20-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="cba20-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cba20-104">SYNTAX</span></span>

```
New-AzApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cba20-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cba20-105">DESCRIPTION</span></span>
<span data-ttu-id="cba20-106">A **New-AzApplicationGatewayConnectionDraining** parancsmag új kapcsolat-elvezetési konfigurációt hoz létre a back-end http-beállításokhoz.</span><span class="sxs-lookup"><span data-stu-id="cba20-106">The **New-AzApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="cba20-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cba20-107">EXAMPLES</span></span>

### <span data-ttu-id="cba20-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cba20-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="cba20-109">A parancs létrehoz egy új kapcsolat-elvezetési konfigurációt, melyen engedélyezve van a set to True és a DrainTimeoutInSec értéke 42 másodpercre, és a $connectionDraining-ban tárolja.</span><span class="sxs-lookup"><span data-stu-id="cba20-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="cba20-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cba20-110">PARAMETERS</span></span>

### <span data-ttu-id="cba20-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cba20-111">-DefaultProfile</span></span>
<span data-ttu-id="cba20-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cba20-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cba20-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="cba20-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="cba20-114">A kapcsolat ürítésének száma másodpercben.</span><span class="sxs-lookup"><span data-stu-id="cba20-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="cba20-115">Az elfogadható értékek 1 másodpercről 3600 másodpercre.</span><span class="sxs-lookup"><span data-stu-id="cba20-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="cba20-116">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="cba20-116">-Enabled</span></span>
<span data-ttu-id="cba20-117">Engedélyezve van-e a kapcsolat kiürítése?</span><span class="sxs-lookup"><span data-stu-id="cba20-117">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="cba20-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cba20-118">CommonParameters</span></span>
<span data-ttu-id="cba20-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cba20-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cba20-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cba20-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cba20-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cba20-121">INPUTS</span></span>

### <span data-ttu-id="cba20-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="cba20-122">None</span></span>

## <span data-ttu-id="cba20-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cba20-123">OUTPUTS</span></span>

### <span data-ttu-id="cba20-124">Microsoft. Azure. commands. Network. models. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="cba20-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="cba20-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cba20-125">NOTES</span></span>

## <span data-ttu-id="cba20-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cba20-126">RELATED LINKS</span></span>

[<span data-ttu-id="cba20-127">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="cba20-127">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="cba20-128">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="cba20-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="cba20-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="cba20-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

