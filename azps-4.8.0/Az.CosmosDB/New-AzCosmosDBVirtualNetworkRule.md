---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
ms.openlocfilehash: d60284cec84c1b0a023f06a77acfe794d8d5315f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182379"
---
# <span data-ttu-id="a27b6-101">New-AzCosmosDBVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a27b6-101">New-AzCosmosDBVirtualNetworkRule</span></span>

## <span data-ttu-id="a27b6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a27b6-102">SYNOPSIS</span></span>
<span data-ttu-id="a27b6-103">Hozzon létre egy új CosmosDB-VirtualNetworkRule objektumot (PSVirtualNetworkRule).</span><span class="sxs-lookup"><span data-stu-id="a27b6-103">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="a27b6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a27b6-104">SYNTAX</span></span>

```
New-AzCosmosDBVirtualNetworkRule -Id <String> [-IgnoreMissingVNetServiceEndpoint <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a27b6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a27b6-105">DESCRIPTION</span></span>
<span data-ttu-id="a27b6-106">Hozzon létre egy új CosmosDB-VirtualNetworkRule objektumot (PSVirtualNetworkRule).</span><span class="sxs-lookup"><span data-stu-id="a27b6-106">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="a27b6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a27b6-107">EXAMPLES</span></span>

### <span data-ttu-id="a27b6-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a27b6-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBVirtualNetworkRule -Id {id} -IgnoreMissingVNetServiceEndpoint 0
Id  IgnoreMissingVNetServiceEndpoint
--   --------------------------------
{id}                            False
```

## <span data-ttu-id="a27b6-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a27b6-109">PARAMETERS</span></span>

### <span data-ttu-id="a27b6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a27b6-110">-DefaultProfile</span></span>
<span data-ttu-id="a27b6-111">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a27b6-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a27b6-112">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="a27b6-112">-Id</span></span>
<span data-ttu-id="a27b6-113">Egy alhálózat erőforrás-azonosítója, például:/subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span><span class="sxs-lookup"><span data-stu-id="a27b6-113">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a27b6-114">-IgnoreMissingVNetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="a27b6-114">-IgnoreMissingVNetServiceEndpoint</span></span>
<span data-ttu-id="a27b6-115">Logikai érték, amely azt jelzi, hogy a virtuális hálózat vnet-szolgáltatás végpontja engedélyezve van-e a tűzfalszabályok létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="a27b6-115">Boolean to indicate if to create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a27b6-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a27b6-116">CommonParameters</span></span>
<span data-ttu-id="a27b6-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a27b6-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a27b6-118">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a27b6-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a27b6-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a27b6-119">INPUTS</span></span>

### <span data-ttu-id="a27b6-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="a27b6-120">None</span></span>

## <span data-ttu-id="a27b6-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a27b6-121">OUTPUTS</span></span>

### <span data-ttu-id="a27b6-122">Microsoft. Azure. Command. CosmosDB. models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a27b6-122">Microsoft.Azure.Commands.CosmosDB.Models.PSVirtualNetworkRule</span></span>

## <span data-ttu-id="a27b6-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a27b6-123">NOTES</span></span>

## <span data-ttu-id="a27b6-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a27b6-124">RELATED LINKS</span></span>
