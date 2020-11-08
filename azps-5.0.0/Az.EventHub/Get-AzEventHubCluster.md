---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubCluster.md
ms.openlocfilehash: 4e2657d6a4af26b96a2e7a97a56b735838610005
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194408"
---
# <span data-ttu-id="88ed3-101">Get-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="88ed3-101">Get-AzEventHubCluster</span></span>

## <span data-ttu-id="88ed3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="88ed3-102">SYNOPSIS</span></span>
<span data-ttu-id="88ed3-103">Egyetlen esemény központi fürtjén kapja meg a részleteket, vagy az esemény-hub-fürtök listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="88ed3-103">Gets the details of a single Event Hub Cluster , or gets a list of Event Hub Clusters.</span></span>

## <span data-ttu-id="88ed3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="88ed3-104">SYNTAX</span></span>

```
Get-AzEventHubCluster [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88ed3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="88ed3-105">DESCRIPTION</span></span>
<span data-ttu-id="88ed3-106">A Get-AzEventHubCluster parancsmag az esemény központi fürtjének részleteit vagy az adott erőforráscsoport összes esemény-központi fürtjének listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="88ed3-106">The Get-AzEventHubCluster cmdlet returns either the details of an Event Hub Cluster, or a list of all Event Hub Clusters in given resource group.</span></span>
<span data-ttu-id="88ed3-107">Ha a fürt neve meg van határozva, akkor egy egyetlen fürt adatait adja vissza a rendszer.</span><span class="sxs-lookup"><span data-stu-id="88ed3-107">If the cluster name is provided, the details of a single cluster are returned.</span></span>
<span data-ttu-id="88ed3-108">Ha a fürt neve nincs megadva, a megadott erőforráscsoport összes szektorcsoportjának listáját a program visszaadja.</span><span class="sxs-lookup"><span data-stu-id="88ed3-108">If an cluster name is not provided, a list of all clusters in the specified resource group is returned.</span></span>

## <span data-ttu-id="88ed3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="88ed3-109">EXAMPLES</span></span>

### <span data-ttu-id="88ed3-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="88ed3-110">Example 1</span></span>
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

<span data-ttu-id="88ed3-111">A "Eventhub-cluster-5557" DETIALS számítja ki a ' RSG-Cluster27651 ' erőforráscsoport-csoportból.</span><span class="sxs-lookup"><span data-stu-id="88ed3-111">Returns the detials of cluster 'Eventhub-Cluster-5557' from the resource group 'RSG-Cluster27651'</span></span>

## <span data-ttu-id="88ed3-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="88ed3-112">PARAMETERS</span></span>

### <span data-ttu-id="88ed3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88ed3-113">-DefaultProfile</span></span>
<span data-ttu-id="88ed3-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="88ed3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88ed3-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="88ed3-115">-Name</span></span>
<span data-ttu-id="88ed3-116">Fürt neve</span><span class="sxs-lookup"><span data-stu-id="88ed3-116">Cluster Name</span></span>

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

### <span data-ttu-id="88ed3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88ed3-117">-ResourceGroupName</span></span>
<span data-ttu-id="88ed3-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="88ed3-118">Resource Group Name</span></span>

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

### <span data-ttu-id="88ed3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88ed3-119">CommonParameters</span></span>
<span data-ttu-id="88ed3-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="88ed3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88ed3-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="88ed3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88ed3-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="88ed3-122">INPUTS</span></span>

### <span data-ttu-id="88ed3-123">System. String</span><span class="sxs-lookup"><span data-stu-id="88ed3-123">System.String</span></span>

## <span data-ttu-id="88ed3-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="88ed3-124">OUTPUTS</span></span>

### <span data-ttu-id="88ed3-125">Microsoft. Azure. Command. EventHub. models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="88ed3-125">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="88ed3-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="88ed3-126">NOTES</span></span>

## <span data-ttu-id="88ed3-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="88ed3-127">RELATED LINKS</span></span>
