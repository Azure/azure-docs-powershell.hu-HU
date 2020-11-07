---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermcomputeresourcesku
schema: 2.0.0
ms.openlocfilehash: e7ebc6a8e6b59679757f559ff2d09ebaa8c5475f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850942"
---
# <span data-ttu-id="a944e-101">Get-AzureRmComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="a944e-101">Get-AzureRmComputeResourceSku</span></span>

## <span data-ttu-id="a944e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a944e-102">SYNOPSIS</span></span>
<span data-ttu-id="a944e-103">Az összes számítási erőforrás listázása</span><span class="sxs-lookup"><span data-stu-id="a944e-103">List all compute resource Skus</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a944e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a944e-104">SYNTAX</span></span>

```
Get-AzureRmComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a944e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a944e-105">DESCRIPTION</span></span>
<span data-ttu-id="a944e-106">Az összes számítási erőforrás listázása</span><span class="sxs-lookup"><span data-stu-id="a944e-106">List all compute resource Skus</span></span>

## <span data-ttu-id="a944e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a944e-107">EXAMPLES</span></span>

### <span data-ttu-id="a944e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a944e-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzureRmComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="a944e-109">Az összes számítási erőforrás listázása a Nyugat-amerikai régióban</span><span class="sxs-lookup"><span data-stu-id="a944e-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="a944e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a944e-110">PARAMETERS</span></span>

### <span data-ttu-id="a944e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a944e-111">-DefaultProfile</span></span>
<span data-ttu-id="a944e-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a944e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a944e-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a944e-113">CommonParameters</span></span>
<span data-ttu-id="a944e-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a944e-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a944e-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a944e-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a944e-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a944e-116">INPUTS</span></span>

### <span data-ttu-id="a944e-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="a944e-117">None</span></span>

## <span data-ttu-id="a944e-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a944e-118">OUTPUTS</span></span>

### <span data-ttu-id="a944e-119">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="a944e-119">System.Object</span></span>

## <span data-ttu-id="a944e-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a944e-120">NOTES</span></span>

## <span data-ttu-id="a944e-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a944e-121">RELATED LINKS</span></span>

