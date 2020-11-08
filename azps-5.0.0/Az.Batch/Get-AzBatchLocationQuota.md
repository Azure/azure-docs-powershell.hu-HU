---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchlocationquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
ms.openlocfilehash: 5c20529e174e37bd4d9d5d3f60b56c448206d09e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194470"
---
# <span data-ttu-id="b7039-101">Get-AzBatchLocationQuota</span><span class="sxs-lookup"><span data-stu-id="b7039-101">Get-AzBatchLocationQuota</span></span>

## <span data-ttu-id="b7039-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b7039-102">SYNOPSIS</span></span>
<span data-ttu-id="b7039-103">Az előfizetéshez tartozó kötegelt szolgáltatási kvótákat kapja meg az adott helyen.</span><span class="sxs-lookup"><span data-stu-id="b7039-103">Gets the Batch service quotas for your subscription at the given location.</span></span>

## <span data-ttu-id="b7039-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b7039-104">SYNTAX</span></span>

```
Get-AzBatchLocationQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7039-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b7039-105">DESCRIPTION</span></span>
<span data-ttu-id="b7039-106">A megadott előfizetéshez tartozó kötegelt szolgáltatási kvótákat kapja meg az adott helyen.</span><span class="sxs-lookup"><span data-stu-id="b7039-106">Gets the Batch service quotas for the specified subscription at the given location.</span></span>

## <span data-ttu-id="b7039-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b7039-107">EXAMPLES</span></span>

### <span data-ttu-id="b7039-108">Példa 1: a kötegelt szolgáltatás kvótájának beszerzése az előfizetéshez a West US régióban</span><span class="sxs-lookup"><span data-stu-id="b7039-108">Example 1: Get the Batch service quotas for the subscription in the West US region</span></span>
```
PS C:\>Get-AzBatchLocationQuota -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

<span data-ttu-id="b7039-109">Ez a parancs az aktuális előfizetéshez tartozó kvótákat kapja meg a Nyugat-amerikai régióban.</span><span class="sxs-lookup"><span data-stu-id="b7039-109">This command gets the quotas for the current subscription in the West US region.</span></span>
<span data-ttu-id="b7039-110">A visszatérési érték azt jelzi, hogy ez az előfizetés csak egy köteg fiókot hozhat létre ebben a régióban.</span><span class="sxs-lookup"><span data-stu-id="b7039-110">The return value indicates that this subscription can create only one Batch account in that region.</span></span>

## <span data-ttu-id="b7039-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b7039-111">PARAMETERS</span></span>

### <span data-ttu-id="b7039-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7039-112">-DefaultProfile</span></span>
<span data-ttu-id="b7039-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b7039-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7039-114">-Hely</span><span class="sxs-lookup"><span data-stu-id="b7039-114">-Location</span></span>
<span data-ttu-id="b7039-115">Azt a régiót adja meg, amelyre a parancsmag ellenőrzi a kvótákat.</span><span class="sxs-lookup"><span data-stu-id="b7039-115">Specifies the region for which this cmdlet checks the quotas.</span></span>
<span data-ttu-id="b7039-116">További információ: Azure Regions ( https://azure.microsoft.com/regions) .</span><span class="sxs-lookup"><span data-stu-id="b7039-116">For more information, see Azure Regions (https://azure.microsoft.com/regions).</span></span>

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

### <span data-ttu-id="b7039-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7039-117">CommonParameters</span></span>
<span data-ttu-id="b7039-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b7039-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7039-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b7039-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7039-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7039-120">INPUTS</span></span>

### <span data-ttu-id="b7039-121">System. String</span><span class="sxs-lookup"><span data-stu-id="b7039-121">System.String</span></span>

## <span data-ttu-id="b7039-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7039-122">OUTPUTS</span></span>

### <span data-ttu-id="b7039-123">Microsoft.Azure.Commands.BatCH. Modellek. PSBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="b7039-123">Microsoft.Azure.Commands.Batch.Models.PSBatchLocationQuotas</span></span>

## <span data-ttu-id="b7039-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b7039-124">NOTES</span></span>

## <span data-ttu-id="b7039-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7039-125">RELATED LINKS</span></span>
