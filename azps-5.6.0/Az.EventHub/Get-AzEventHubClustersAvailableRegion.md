---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubclustersavailableregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
ms.openlocfilehash: 633881b298059c35a54591bb1ff93d4e93a267d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919970"
---
# <span data-ttu-id="18f5e-101">Get-AzEventHubClustersAvailableRegion</span><span class="sxs-lookup"><span data-stu-id="18f5e-101">Get-AzEventHubClustersAvailableRegion</span></span>

## <span data-ttu-id="18f5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18f5e-102">SYNOPSIS</span></span>
<span data-ttu-id="18f5e-103">Egyetlen Eventhub-fürt vagy a megadott erőforráscsoportban található fürtök listájának részletei</span><span class="sxs-lookup"><span data-stu-id="18f5e-103">Gets the details of single Eventhub cluster or the list of clusters in the given Resource Group</span></span>

## <span data-ttu-id="18f5e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="18f5e-104">SYNTAX</span></span>

```
Get-AzEventHubClustersAvailableRegion [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18f5e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="18f5e-105">DESCRIPTION</span></span>
<span data-ttu-id="18f5e-106">A Get-AzEventHubClustersAvailableRegion azon régiók teljes listája, amelyekhez külön parancsmagot lehet létrehozni.</span><span class="sxs-lookup"><span data-stu-id="18f5e-106">The Get-AzEventHubClustersAvailableRegion cmdlet list of regions where dedicated are available to create.</span></span>

## <span data-ttu-id="18f5e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="18f5e-107">EXAMPLES</span></span>

### <span data-ttu-id="18f5e-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="18f5e-108">Example 1</span></span>
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

<span data-ttu-id="18f5e-109">A visszaadott régiók listája</span><span class="sxs-lookup"><span data-stu-id="18f5e-109">List of regions is returned where</span></span>

## <span data-ttu-id="18f5e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18f5e-110">PARAMETERS</span></span>

### <span data-ttu-id="18f5e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18f5e-111">-DefaultProfile</span></span>
<span data-ttu-id="18f5e-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="18f5e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18f5e-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18f5e-113">CommonParameters</span></span>
<span data-ttu-id="18f5e-114">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18f5e-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18f5e-115">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="18f5e-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18f5e-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="18f5e-116">INPUTS</span></span>

### <span data-ttu-id="18f5e-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="18f5e-117">None</span></span>

## <span data-ttu-id="18f5e-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18f5e-118">OUTPUTS</span></span>

### <span data-ttu-id="18f5e-119">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubsAvailableCluster, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.5.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="18f5e-119">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubsAvailableCluster, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="18f5e-120">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="18f5e-120">NOTES</span></span>

## <span data-ttu-id="18f5e-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18f5e-121">RELATED LINKS</span></span>
