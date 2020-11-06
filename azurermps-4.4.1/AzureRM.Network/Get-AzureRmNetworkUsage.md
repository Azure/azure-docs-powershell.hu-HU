---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkUsage.md
ms.openlocfilehash: c5bb92ad330b49ff015f21ae14fab42d6583305c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504851"
---
# <span data-ttu-id="b45a8-101">Get-AzureRmNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="b45a8-101">Get-AzureRmNetworkUsage</span></span>

## <span data-ttu-id="b45a8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b45a8-102">SYNOPSIS</span></span>
<span data-ttu-id="b45a8-103">Előfizetéshez tartozó hálózati használatot listáz</span><span class="sxs-lookup"><span data-stu-id="b45a8-103">Lists network usages for a subscription</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b45a8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b45a8-104">SYNTAX</span></span>

```
Get-AzureRmNetworkUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b45a8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b45a8-105">DESCRIPTION</span></span>
<span data-ttu-id="b45a8-106">A Get-AzureRmNetworkUsage parancsmag korlátozásokat és a hálózati erőforrások jelenlegi használatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b45a8-106">The Get-AzureRmNetworkUsage cmdlet gets limits and current usage for Network resources.</span></span>

## <span data-ttu-id="b45a8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b45a8-107">EXAMPLES</span></span>

### <span data-ttu-id="b45a8-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b45a8-108">Example 1</span></span>
```
PS C:\> Get-AzureRmNetworkUsage -Location westcentralus

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

<span data-ttu-id="b45a8-109">Erőforrások használati adatainak beolvasása a westcentralus-régióban</span><span class="sxs-lookup"><span data-stu-id="b45a8-109">Gets resources usage data in westcentralus region</span></span>

## <span data-ttu-id="b45a8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b45a8-110">PARAMETERS</span></span>

### <span data-ttu-id="b45a8-111">-Hely</span><span class="sxs-lookup"><span data-stu-id="b45a8-111">-Location</span></span>
<span data-ttu-id="b45a8-112">Az erőforrás-kihasználtság lekérdezésének helye.</span><span class="sxs-lookup"><span data-stu-id="b45a8-112">The location where resource usage is queried.</span></span>

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

### <span data-ttu-id="b45a8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b45a8-113">-DefaultProfile</span></span>
<span data-ttu-id="b45a8-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b45a8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b45a8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b45a8-115">CommonParameters</span></span>
<span data-ttu-id="b45a8-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b45a8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b45a8-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b45a8-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b45a8-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b45a8-118">INPUTS</span></span>

### <span data-ttu-id="b45a8-119">System. String</span><span class="sxs-lookup"><span data-stu-id="b45a8-119">System.String</span></span>

## <span data-ttu-id="b45a8-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b45a8-120">OUTPUTS</span></span>

### <span data-ttu-id="b45a8-121">Microsoft. Azure. commands. Network. models. PSUs</span><span class="sxs-lookup"><span data-stu-id="b45a8-121">Microsoft.Azure.Commands.Network.Models.PSUsage</span></span>

## <span data-ttu-id="b45a8-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b45a8-122">NOTES</span></span>

## <span data-ttu-id="b45a8-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b45a8-123">RELATED LINKS</span></span>

