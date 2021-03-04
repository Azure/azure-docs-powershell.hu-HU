---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkUsage.md
ms.openlocfilehash: 7072d7a2c61f11433fbf75e99366769e4e86b277
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919889"
---
# <span data-ttu-id="72e88-101">Get-AzNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="72e88-101">Get-AzNetworkUsage</span></span>

## <span data-ttu-id="72e88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72e88-102">SYNOPSIS</span></span>
<span data-ttu-id="72e88-103">Az előfizetés hálózati használatának felsorolása</span><span class="sxs-lookup"><span data-stu-id="72e88-103">Lists network usages for a subscription</span></span>

## <span data-ttu-id="72e88-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="72e88-104">SYNTAX</span></span>

```
Get-AzNetworkUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72e88-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="72e88-105">DESCRIPTION</span></span>
<span data-ttu-id="72e88-106">A Get-AzNetworkUsage parancsmag korlátozza és aktuálisan kihasználja a hálózati erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="72e88-106">The Get-AzNetworkUsage cmdlet gets limits and current usage for Network resources.</span></span>

## <span data-ttu-id="72e88-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="72e88-107">EXAMPLES</span></span>

### <span data-ttu-id="72e88-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="72e88-108">Example 1</span></span>
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

<span data-ttu-id="72e88-109">Erőforrás-használati adatokat kap a westcentralusi régióban</span><span class="sxs-lookup"><span data-stu-id="72e88-109">Gets resources usage data in westcentralus region</span></span>

## <span data-ttu-id="72e88-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72e88-110">PARAMETERS</span></span>

### <span data-ttu-id="72e88-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72e88-111">-DefaultProfile</span></span>
<span data-ttu-id="72e88-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="72e88-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72e88-113">-Location</span><span class="sxs-lookup"><span data-stu-id="72e88-113">-Location</span></span>
<span data-ttu-id="72e88-114">Az a hely, ahol lekérdezi az erőforrás-használatot.</span><span class="sxs-lookup"><span data-stu-id="72e88-114">The location where resource usage is queried.</span></span>

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

### <span data-ttu-id="72e88-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72e88-115">CommonParameters</span></span>
<span data-ttu-id="72e88-116">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72e88-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72e88-117">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72e88-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72e88-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="72e88-118">INPUTS</span></span>

### <span data-ttu-id="72e88-119">System.String</span><span class="sxs-lookup"><span data-stu-id="72e88-119">System.String</span></span>

## <span data-ttu-id="72e88-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72e88-120">OUTPUTS</span></span>

### <span data-ttu-id="72e88-121">Microsoft.Azure.Commands.Network.Models.PSUsage</span><span class="sxs-lookup"><span data-stu-id="72e88-121">Microsoft.Azure.Commands.Network.Models.PSUsage</span></span>

## <span data-ttu-id="72e88-122">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="72e88-122">NOTES</span></span>

## <span data-ttu-id="72e88-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72e88-123">RELATED LINKS</span></span>
