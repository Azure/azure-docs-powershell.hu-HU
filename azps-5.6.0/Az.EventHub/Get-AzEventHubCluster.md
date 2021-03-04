---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubCluster.md
ms.openlocfilehash: 22bbbb79f8662f1e1e70785489187e68e5b38813
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934178"
---
# <span data-ttu-id="bbd38-101">Get-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="bbd38-101">Get-AzEventHubCluster</span></span>

## <span data-ttu-id="bbd38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbd38-102">SYNOPSIS</span></span>
<span data-ttu-id="bbd38-103">Lekérte egyetlen eseményközpont-fürt adatait, vagy lekérte az Eseményközpont-fürtök listáját.</span><span class="sxs-lookup"><span data-stu-id="bbd38-103">Gets the details of a single Event Hub Cluster , or gets a list of Event Hub Clusters.</span></span>

## <span data-ttu-id="bbd38-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bbd38-104">SYNTAX</span></span>

```
Get-AzEventHubCluster [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bbd38-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bbd38-105">DESCRIPTION</span></span>
<span data-ttu-id="bbd38-106">A Get-AzEventHubCluster parancsmag vagy az Eseményközpont-fürt adatait, vagy az eseményközpont-fürtök listáját adja vissza az adott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="bbd38-106">The Get-AzEventHubCluster cmdlet returns either the details of an Event Hub Cluster, or a list of all Event Hub Clusters in given resource group.</span></span>
<span data-ttu-id="bbd38-107">Ha meg van téve a fürt neve, a visszaadott érték egyetlen fürt részletei.</span><span class="sxs-lookup"><span data-stu-id="bbd38-107">If the cluster name is provided, the details of a single cluster are returned.</span></span>
<span data-ttu-id="bbd38-108">Ha nem adja meg a fürt nevét, a megadott erőforráscsoport összes fürtének listáját adja vissza a visszaadott érték.</span><span class="sxs-lookup"><span data-stu-id="bbd38-108">If an cluster name is not provided, a list of all clusters in the specified resource group is returned.</span></span>

## <span data-ttu-id="bbd38-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bbd38-109">EXAMPLES</span></span>

### <span data-ttu-id="bbd38-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="bbd38-110">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557

Id        : /subscriptions/326100e2-f69d-4268-8503-075374f62b6e/resourceGroups/RSG-Cluster27651/providers/Microsoft.Eve
            ntHub/clusters/Eventhub-Cluster-5557
Name      : Eventhub-Cluster-5557
Location  : southcentralus
CreatedAt : 09/10/2020 22:09:57
UpdatedAt : 09/10/2020 23:02:48
MetricId  :
Status    :
Sku       : Microsoft.Azure.Commands.EventHub.Models.PSEventHubsClusterSkuAttributes
Tags      : {[ClusterTag2, Tag4], [ClusterTag1, Tag3]}

```

<span data-ttu-id="bbd38-111">Az "RSG-Cluster27651" erőforráscsoport "Eventhub-Cluster-5557" fürtének detialsát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="bbd38-111">Returns the detials of cluster 'Eventhub-Cluster-5557' from the resource group 'RSG-Cluster27651'</span></span>

## <span data-ttu-id="bbd38-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bbd38-112">PARAMETERS</span></span>

### <span data-ttu-id="bbd38-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbd38-113">-DefaultProfile</span></span>
<span data-ttu-id="bbd38-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bbd38-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbd38-115">-Name</span><span class="sxs-lookup"><span data-stu-id="bbd38-115">-Name</span></span>
<span data-ttu-id="bbd38-116">Fürt neve</span><span class="sxs-lookup"><span data-stu-id="bbd38-116">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbd38-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbd38-117">-ResourceGroupName</span></span>
<span data-ttu-id="bbd38-118">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="bbd38-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbd38-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbd38-119">CommonParameters</span></span>
<span data-ttu-id="bbd38-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbd38-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbd38-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bbd38-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbd38-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bbd38-122">INPUTS</span></span>

### <span data-ttu-id="bbd38-123">System.String</span><span class="sxs-lookup"><span data-stu-id="bbd38-123">System.String</span></span>

## <span data-ttu-id="bbd38-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bbd38-124">OUTPUTS</span></span>

### <span data-ttu-id="bbd38-125">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="bbd38-125">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="bbd38-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bbd38-126">NOTES</span></span>

## <span data-ttu-id="bbd38-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bbd38-127">RELATED LINKS</span></span>
