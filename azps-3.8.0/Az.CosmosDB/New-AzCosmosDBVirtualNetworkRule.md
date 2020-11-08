---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
ms.openlocfilehash: d60284cec84c1b0a023f06a77acfe794d8d5315f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013628"
---
# <span data-ttu-id="5bf7f-101">New-AzCosmosDBVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5bf7f-101">New-AzCosmosDBVirtualNetworkRule</span></span>

## <span data-ttu-id="5bf7f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5bf7f-102">SYNOPSIS</span></span>
<span data-ttu-id="5bf7f-103">Hozzon létre egy új CosmosDB-VirtualNetworkRule objektumot (PSVirtualNetworkRule).</span><span class="sxs-lookup"><span data-stu-id="5bf7f-103">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="5bf7f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5bf7f-104">SYNTAX</span></span>

```
New-AzCosmosDBVirtualNetworkRule -Id <String> [-IgnoreMissingVNetServiceEndpoint <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bf7f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5bf7f-105">DESCRIPTION</span></span>
<span data-ttu-id="5bf7f-106">Hozzon létre egy új CosmosDB-VirtualNetworkRule objektumot (PSVirtualNetworkRule).</span><span class="sxs-lookup"><span data-stu-id="5bf7f-106">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="5bf7f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5bf7f-107">EXAMPLES</span></span>

### <span data-ttu-id="5bf7f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5bf7f-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBVirtualNetworkRule -Id {id} -IgnoreMissingVNetServiceEndpoint 0
Id  IgnoreMissingVNetServiceEndpoint
--   --------------------------------
{id}                            False
```

## <span data-ttu-id="5bf7f-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5bf7f-109">PARAMETERS</span></span>

### <span data-ttu-id="5bf7f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bf7f-110">-DefaultProfile</span></span>
<span data-ttu-id="5bf7f-111">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5bf7f-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bf7f-112">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="5bf7f-112">-Id</span></span>
<span data-ttu-id="5bf7f-113">Egy alhálózat erőforrás-azonosítója, például:/subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span><span class="sxs-lookup"><span data-stu-id="5bf7f-113">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span></span>

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

### <span data-ttu-id="5bf7f-114">-IgnoreMissingVNetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="5bf7f-114">-IgnoreMissingVNetServiceEndpoint</span></span>
<span data-ttu-id="5bf7f-115">Logikai érték, amely azt jelzi, hogy a virtuális hálózat vnet-szolgáltatás végpontja engedélyezve van-e a tűzfalszabályok létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="5bf7f-115">Boolean to indicate if to create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="5bf7f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bf7f-116">CommonParameters</span></span>
<span data-ttu-id="5bf7f-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5bf7f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bf7f-118">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5bf7f-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bf7f-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5bf7f-119">INPUTS</span></span>

### <span data-ttu-id="5bf7f-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="5bf7f-120">None</span></span>

## <span data-ttu-id="5bf7f-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5bf7f-121">OUTPUTS</span></span>

### <span data-ttu-id="5bf7f-122">Microsoft. Azure. Command. CosmosDB. models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5bf7f-122">Microsoft.Azure.Commands.CosmosDB.Models.PSVirtualNetworkRule</span></span>

## <span data-ttu-id="5bf7f-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5bf7f-123">NOTES</span></span>

## <span data-ttu-id="5bf7f-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5bf7f-124">RELATED LINKS</span></span>
