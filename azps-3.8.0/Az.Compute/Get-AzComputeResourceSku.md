---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: ab57e922a7ef63d14a36bbd91ed268822e2c61e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013691"
---
# <span data-ttu-id="69746-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="69746-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="69746-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="69746-102">SYNOPSIS</span></span>
<span data-ttu-id="69746-103">Az összes számítási erőforrás listázása</span><span class="sxs-lookup"><span data-stu-id="69746-103">List all compute resource Skus</span></span>

## <span data-ttu-id="69746-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="69746-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69746-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="69746-105">DESCRIPTION</span></span>
<span data-ttu-id="69746-106">Az összes számítási erőforrás listázása</span><span class="sxs-lookup"><span data-stu-id="69746-106">List all compute resource Skus</span></span>

## <span data-ttu-id="69746-107">Példák</span><span class="sxs-lookup"><span data-stu-id="69746-107">EXAMPLES</span></span>

### <span data-ttu-id="69746-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="69746-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="69746-109">Az összes számítási erőforrás listázása a Nyugat-amerikai régióban</span><span class="sxs-lookup"><span data-stu-id="69746-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="69746-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="69746-110">PARAMETERS</span></span>

### <span data-ttu-id="69746-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69746-111">-DefaultProfile</span></span>
<span data-ttu-id="69746-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69746-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69746-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69746-113">CommonParameters</span></span>
<span data-ttu-id="69746-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="69746-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69746-115">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="69746-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69746-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="69746-116">INPUTS</span></span>

### <span data-ttu-id="69746-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="69746-117">None</span></span>

## <span data-ttu-id="69746-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69746-118">OUTPUTS</span></span>

### <span data-ttu-id="69746-119">Microsoft. Azure. commands. számítási. Automation. models. PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="69746-119">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="69746-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="69746-120">NOTES</span></span>

## <span data-ttu-id="69746-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69746-121">RELATED LINKS</span></span>
