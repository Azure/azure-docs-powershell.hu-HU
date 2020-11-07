---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: e3c33fb3d61479531303389defb0d7ebdbb3fb64
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836803"
---
# <span data-ttu-id="223e1-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="223e1-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="223e1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="223e1-102">SYNOPSIS</span></span>
<span data-ttu-id="223e1-103">Az összes számítási erőforrás listázása</span><span class="sxs-lookup"><span data-stu-id="223e1-103">List all compute resource Skus</span></span>

## <span data-ttu-id="223e1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="223e1-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="223e1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="223e1-105">DESCRIPTION</span></span>
<span data-ttu-id="223e1-106">Az összes számítási erőforrás listázása</span><span class="sxs-lookup"><span data-stu-id="223e1-106">List all compute resource Skus</span></span>

## <span data-ttu-id="223e1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="223e1-107">EXAMPLES</span></span>

### <span data-ttu-id="223e1-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="223e1-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="223e1-109">Az összes számítási erőforrás listázása a Nyugat-amerikai régióban</span><span class="sxs-lookup"><span data-stu-id="223e1-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="223e1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="223e1-110">PARAMETERS</span></span>

### <span data-ttu-id="223e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="223e1-111">-DefaultProfile</span></span>
<span data-ttu-id="223e1-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="223e1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="223e1-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="223e1-113">CommonParameters</span></span>
<span data-ttu-id="223e1-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="223e1-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="223e1-115">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="223e1-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="223e1-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="223e1-116">INPUTS</span></span>

### <span data-ttu-id="223e1-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="223e1-117">None</span></span>

## <span data-ttu-id="223e1-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="223e1-118">OUTPUTS</span></span>

### <span data-ttu-id="223e1-119">Microsoft. Azure. commands. számítási. Automation. models. PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="223e1-119">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="223e1-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="223e1-120">NOTES</span></span>

## <span data-ttu-id="223e1-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="223e1-121">RELATED LINKS</span></span>
