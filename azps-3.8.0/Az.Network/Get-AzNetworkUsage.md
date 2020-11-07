---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkUsage.md
ms.openlocfilehash: e02527c0f206607ae778d6447e65a1c93c620b02
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845942"
---
# <span data-ttu-id="d462c-101">Get-AzNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="d462c-101">Get-AzNetworkUsage</span></span>

## <span data-ttu-id="d462c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d462c-102">SYNOPSIS</span></span>
<span data-ttu-id="d462c-103">Előfizetéshez tartozó hálózati használatot listáz</span><span class="sxs-lookup"><span data-stu-id="d462c-103">Lists network usages for a subscription</span></span>

## <span data-ttu-id="d462c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d462c-104">SYNTAX</span></span>

```
Get-AzNetworkUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d462c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d462c-105">DESCRIPTION</span></span>
<span data-ttu-id="d462c-106">A Get-AzNetworkUsage parancsmag korlátozásokat és a hálózati erőforrások jelenlegi használatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d462c-106">The Get-AzNetworkUsage cmdlet gets limits and current usage for Network resources.</span></span>

## <span data-ttu-id="d462c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d462c-107">EXAMPLES</span></span>

### <span data-ttu-id="d462c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d462c-108">Example 1</span></span>
```
PS C:\> Get-AzNetworkUsage -Location westcentralus

ResourceType : Virtual Networks
CurrentValue : 6
Limit        : 50

ResourceType : Static Public IP Addresses
CurrentValue : 1
Limit        : 20

ResourceType : Network Security Groups
CurrentValue : 2
Limit        : 100

ResourceType : Public IP Addresses
CurrentValue : 6
Limit        : 60

ResourceType : Network Interfaces
CurrentValue : 1
Limit        : 300

ResourceType : Load Balancers
CurrentValue : 1
Limit        : 100

ResourceType : Application Gateways
CurrentValue : 1
Limit        : 50

ResourceType : Route Tables
CurrentValue : 0
Limit        : 100

ResourceType : Route Filters
CurrentValue : 0
Limit        : 1000

ResourceType : Network Watchers
CurrentValue : 1
Limit        : 1

ResourceType : Packet Captures
CurrentValue : 0
Limit        : 10
```

<span data-ttu-id="d462c-109">Erőforrások használati adatainak beolvasása a westcentralus-régióban</span><span class="sxs-lookup"><span data-stu-id="d462c-109">Gets resources usage data in westcentralus region</span></span>

## <span data-ttu-id="d462c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d462c-110">PARAMETERS</span></span>

### <span data-ttu-id="d462c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d462c-111">-DefaultProfile</span></span>
<span data-ttu-id="d462c-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d462c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d462c-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="d462c-113">-Location</span></span>
<span data-ttu-id="d462c-114">Az erőforrás-kihasználtság lekérdezésének helye.</span><span class="sxs-lookup"><span data-stu-id="d462c-114">The location where resource usage is queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d462c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d462c-115">CommonParameters</span></span>
<span data-ttu-id="d462c-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d462c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d462c-117">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d462c-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d462c-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d462c-118">INPUTS</span></span>

### <span data-ttu-id="d462c-119">System. String</span><span class="sxs-lookup"><span data-stu-id="d462c-119">System.String</span></span>

## <span data-ttu-id="d462c-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d462c-120">OUTPUTS</span></span>

### <span data-ttu-id="d462c-121">Microsoft. Azure. commands. Network. models. PSUs</span><span class="sxs-lookup"><span data-stu-id="d462c-121">Microsoft.Azure.Commands.Network.Models.PSUsage</span></span>

## <span data-ttu-id="d462c-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d462c-122">NOTES</span></span>

## <span data-ttu-id="d462c-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d462c-123">RELATED LINKS</span></span>
