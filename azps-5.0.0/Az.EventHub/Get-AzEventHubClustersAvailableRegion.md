---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubclustersavailableregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
ms.openlocfilehash: 712e9274eabe27bbe5f4a8acce704926e1e895fe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194405"
---
# <span data-ttu-id="7df07-101">Get-AzEventHubClustersAvailableRegion</span><span class="sxs-lookup"><span data-stu-id="7df07-101">Get-AzEventHubClustersAvailableRegion</span></span>

## <span data-ttu-id="7df07-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7df07-102">SYNOPSIS</span></span>
<span data-ttu-id="7df07-103">Egy Eventhub-fürt vagy a szektorcsoportok listájának lekérdezése az adott erőforráscsoport számára</span><span class="sxs-lookup"><span data-stu-id="7df07-103">Gets the details of single Eventhub cluster or the list of clusters in the given Resource Group</span></span>

## <span data-ttu-id="7df07-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7df07-104">SYNTAX</span></span>

```
Get-AzEventHubClustersAvailableRegion [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7df07-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7df07-105">DESCRIPTION</span></span>
<span data-ttu-id="7df07-106">Azoknak a régióknak a Get-AzEventHubClustersAvailableRegion parancsmag listája, amelyekhez dedikáltak.</span><span class="sxs-lookup"><span data-stu-id="7df07-106">The Get-AzEventHubClustersAvailableRegion cmdlet list of regions where dedicated are available to create.</span></span>

## <span data-ttu-id="7df07-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7df07-107">EXAMPLES</span></span>

### <span data-ttu-id="7df07-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7df07-108">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubClustersAvailableRegion

Location
--------
northcentralus
westeurope
uksouth
westcentralus
australiasoutheast
ukwest
brazilsouth
centralus
australiaeast
eastus
southcentralus
japaneast
northeurope
eastus2
southeastasia
eastasia
westus
westus2
```

<span data-ttu-id="7df07-109">A régiókat visszaadó lista</span><span class="sxs-lookup"><span data-stu-id="7df07-109">List of regions is returned where</span></span>

## <span data-ttu-id="7df07-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7df07-110">PARAMETERS</span></span>

### <span data-ttu-id="7df07-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7df07-111">-DefaultProfile</span></span>
<span data-ttu-id="7df07-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7df07-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7df07-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7df07-113">CommonParameters</span></span>
<span data-ttu-id="7df07-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7df07-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7df07-115">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7df07-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7df07-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7df07-116">INPUTS</span></span>

### <span data-ttu-id="7df07-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="7df07-117">None</span></span>

## <span data-ttu-id="7df07-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7df07-118">OUTPUTS</span></span>

### <span data-ttu-id="7df07-119">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. EventHub. models. PSEventHubsAvailableCluster, Microsoft. Azure. PowerShell. parancsmagok. EventHub, Version = 1.5.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7df07-119">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubsAvailableCluster, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7df07-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7df07-120">NOTES</span></span>

## <span data-ttu-id="7df07-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7df07-121">RELATED LINKS</span></span>
