---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchlocationquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
ms.openlocfilehash: 5c20529e174e37bd4d9d5d3f60b56c448206d09e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478350"
---
# <span data-ttu-id="d244f-101">Get-AzBatchLocationQuota</span><span class="sxs-lookup"><span data-stu-id="d244f-101">Get-AzBatchLocationQuota</span></span>

## <span data-ttu-id="d244f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d244f-102">SYNOPSIS</span></span>
<span data-ttu-id="d244f-103">Az adott helyen megkapja az előfizetés kötegszolgáltatásra vonatkozó kvótáját.</span><span class="sxs-lookup"><span data-stu-id="d244f-103">Gets the Batch service quotas for your subscription at the given location.</span></span>

## <span data-ttu-id="d244f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d244f-104">SYNTAX</span></span>

```
Get-AzBatchLocationQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d244f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d244f-105">DESCRIPTION</span></span>
<span data-ttu-id="d244f-106">A megadott előfizetés kötegszolgáltatáskvótáját kapja meg a megadott helyen.</span><span class="sxs-lookup"><span data-stu-id="d244f-106">Gets the Batch service quotas for the specified subscription at the given location.</span></span>

## <span data-ttu-id="d244f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d244f-107">EXAMPLES</span></span>

### <span data-ttu-id="d244f-108">1. példa: Az előfizetés kötegszolgáltatásra vonatkozó kvótáinak lekérte a nyugat-amerikai régiót</span><span class="sxs-lookup"><span data-stu-id="d244f-108">Example 1: Get the Batch service quotas for the subscription in the West US region</span></span>
```
PS C:\>Get-AzBatchLocationQuota -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

<span data-ttu-id="d244f-109">Ez a parancs a nyugat-amerikai régió aktuális előfizetésének kvótáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d244f-109">This command gets the quotas for the current subscription in the West US region.</span></span>
<span data-ttu-id="d244f-110">A visszatérési érték azt jelzi, hogy ez az előfizetés csak egy Batch-fiókot hozhat létre az adott régióban.</span><span class="sxs-lookup"><span data-stu-id="d244f-110">The return value indicates that this subscription can create only one Batch account in that region.</span></span>

## <span data-ttu-id="d244f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d244f-111">PARAMETERS</span></span>

### <span data-ttu-id="d244f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d244f-112">-DefaultProfile</span></span>
<span data-ttu-id="d244f-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d244f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d244f-114">-Location</span><span class="sxs-lookup"><span data-stu-id="d244f-114">-Location</span></span>
<span data-ttu-id="d244f-115">Azt a régiót adja meg, amelyhez a parancsmag a kvótát ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="d244f-115">Specifies the region for which this cmdlet checks the quotas.</span></span>
<span data-ttu-id="d244f-116">További információt az Azure Régiók https://azure.microsoft.com/regions) ( .</span><span class="sxs-lookup"><span data-stu-id="d244f-116">For more information, see Azure Regions (https://azure.microsoft.com/regions).</span></span>

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

### <span data-ttu-id="d244f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d244f-117">CommonParameters</span></span>
<span data-ttu-id="d244f-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d244f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d244f-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d244f-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d244f-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d244f-120">INPUTS</span></span>

### <span data-ttu-id="d244f-121">System.String</span><span class="sxs-lookup"><span data-stu-id="d244f-121">System.String</span></span>

## <span data-ttu-id="d244f-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d244f-122">OUTPUTS</span></span>

### <span data-ttu-id="d244f-123">Microsoft.Azure.Commands.Bat. Models.PSBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="d244f-123">Microsoft.Azure.Commands.Batch.Models.PSBatchLocationQuotas</span></span>

## <span data-ttu-id="d244f-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d244f-124">NOTES</span></span>

## <span data-ttu-id="d244f-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d244f-125">RELATED LINKS</span></span>
