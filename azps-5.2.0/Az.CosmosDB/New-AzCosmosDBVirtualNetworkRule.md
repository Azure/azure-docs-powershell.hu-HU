---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
ms.openlocfilehash: d60284cec84c1b0a023f06a77acfe794d8d5315f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357781"
---
# <span data-ttu-id="468a8-101">New-AzCosmosDBVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="468a8-101">New-AzCosmosDBVirtualNetworkRule</span></span>

## <span data-ttu-id="468a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="468a8-102">SYNOPSIS</span></span>
<span data-ttu-id="468a8-103">Hozzon létre egy új TárolóDB VirtualNetworkRule objektumot (PSVirtualNetworkRule).</span><span class="sxs-lookup"><span data-stu-id="468a8-103">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="468a8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="468a8-104">SYNTAX</span></span>

```
New-AzCosmosDBVirtualNetworkRule -Id <String> [-IgnoreMissingVNetServiceEndpoint <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="468a8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="468a8-105">DESCRIPTION</span></span>
<span data-ttu-id="468a8-106">Hozzon létre egy új TárolóDB VirtualNetworkRule objektumot (PSVirtualNetworkRule).</span><span class="sxs-lookup"><span data-stu-id="468a8-106">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="468a8-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="468a8-107">EXAMPLES</span></span>

### <span data-ttu-id="468a8-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="468a8-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBVirtualNetworkRule -Id {id} -IgnoreMissingVNetServiceEndpoint 0
Id  IgnoreMissingVNetServiceEndpoint
--   --------------------------------
{id}                            False
```

## <span data-ttu-id="468a8-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="468a8-109">PARAMETERS</span></span>

### <span data-ttu-id="468a8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="468a8-110">-DefaultProfile</span></span>
<span data-ttu-id="468a8-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="468a8-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="468a8-112">-Id</span><span class="sxs-lookup"><span data-stu-id="468a8-112">-Id</span></span>
<span data-ttu-id="468a8-113">Egy alhálózat erőforrás-azonosítója, például: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/alhálózatok/{alnetName}</span><span class="sxs-lookup"><span data-stu-id="468a8-113">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span></span>

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

### <span data-ttu-id="468a8-114">-IgnoreMissingVNetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="468a8-114">-IgnoreMissingVNetServiceEndpoint</span></span>
<span data-ttu-id="468a8-115">Logikai érték, amely azt jelzi, hogy létre kell-e hozni tűzfalszabályt, mielőtt a virtuális hálózat engedélyezné a virtuális hálózat szolgáltatás végpontját.</span><span class="sxs-lookup"><span data-stu-id="468a8-115">Boolean to indicate if to create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="468a8-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="468a8-116">CommonParameters</span></span>
<span data-ttu-id="468a8-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="468a8-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="468a8-118">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="468a8-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="468a8-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="468a8-119">INPUTS</span></span>

### <span data-ttu-id="468a8-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="468a8-120">None</span></span>

## <span data-ttu-id="468a8-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="468a8-121">OUTPUTS</span></span>

### <span data-ttu-id="468a8-122">Microsoft.Azure.Commands.FogsDB.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="468a8-122">Microsoft.Azure.Commands.CosmosDB.Models.PSVirtualNetworkRule</span></span>

## <span data-ttu-id="468a8-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="468a8-123">NOTES</span></span>

## <span data-ttu-id="468a8-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="468a8-124">RELATED LINKS</span></span>
