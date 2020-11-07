---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchlocationquotas
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchLocationQuotas.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchLocationQuotas.md
ms.openlocfilehash: dea724c77b0574e8235c58a2a696987c94ca586d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679620"
---
# <span data-ttu-id="bf31c-101">Get-AzureRmBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="bf31c-101">Get-AzureRmBatchLocationQuotas</span></span>

## <span data-ttu-id="bf31c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bf31c-102">SYNOPSIS</span></span>
<span data-ttu-id="bf31c-103">Az előfizetéshez tartozó kötegelt szolgáltatási kvótákat kapja meg az adott helyen.</span><span class="sxs-lookup"><span data-stu-id="bf31c-103">Gets the Batch service quotas for your subscription at the given location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf31c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bf31c-104">SYNTAX</span></span>

```
Get-AzureRmBatchLocationQuotas [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bf31c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bf31c-105">DESCRIPTION</span></span>
<span data-ttu-id="bf31c-106">A megadott előfizetéshez tartozó kötegelt szolgáltatási kvótákat kapja meg az adott helyen.</span><span class="sxs-lookup"><span data-stu-id="bf31c-106">Gets the Batch service quotas for the specified subscription at the given location.</span></span>

## <span data-ttu-id="bf31c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bf31c-107">EXAMPLES</span></span>

### <span data-ttu-id="bf31c-108">Példa 1: a kötegelt szolgáltatás kvótájának beszerzése az előfizetéshez a West US régióban</span><span class="sxs-lookup"><span data-stu-id="bf31c-108">Example 1: Get the Batch service quotas for the subscription in the West US region</span></span>
```
PS C:\>Get-AzureRmBatchLocationQuotas -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

<span data-ttu-id="bf31c-109">Ez a parancs az aktuális előfizetéshez tartozó kvótákat kapja meg a Nyugat-amerikai régióban.</span><span class="sxs-lookup"><span data-stu-id="bf31c-109">This command gets the quotas for the current subscription in the West US region.</span></span>
<span data-ttu-id="bf31c-110">A visszatérési érték azt jelzi, hogy ez az előfizetés csak egy köteg fiókot hozhat létre ebben a régióban.</span><span class="sxs-lookup"><span data-stu-id="bf31c-110">The return value indicates that this subscription can create only one Batch account in that region.</span></span>

## <span data-ttu-id="bf31c-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bf31c-111">PARAMETERS</span></span>

### <span data-ttu-id="bf31c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf31c-112">-DefaultProfile</span></span>
<span data-ttu-id="bf31c-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bf31c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf31c-114">-Hely</span><span class="sxs-lookup"><span data-stu-id="bf31c-114">-Location</span></span>
<span data-ttu-id="bf31c-115">Azt a régiót adja meg, amelyre a parancsmag ellenőrzi a kvótákat.</span><span class="sxs-lookup"><span data-stu-id="bf31c-115">Specifies the region for which this cmdlet checks the quotas.</span></span>
<span data-ttu-id="bf31c-116">További információ: Azure Regions ( https://azure.microsoft.com/regions) .</span><span class="sxs-lookup"><span data-stu-id="bf31c-116">For more information, see Azure Regions (https://azure.microsoft.com/regions).</span></span>

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

### <span data-ttu-id="bf31c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf31c-117">CommonParameters</span></span>
<span data-ttu-id="bf31c-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bf31c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf31c-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf31c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf31c-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf31c-120">INPUTS</span></span>

### <span data-ttu-id="bf31c-121">System. String</span><span class="sxs-lookup"><span data-stu-id="bf31c-121">System.String</span></span>

## <span data-ttu-id="bf31c-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf31c-122">OUTPUTS</span></span>

### <span data-ttu-id="bf31c-123">Microsoft.Azure.Commands.BatCH. Modellek. PSBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="bf31c-123">Microsoft.Azure.Commands.Batch.Models.PSBatchLocationQuotas</span></span>

## <span data-ttu-id="bf31c-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bf31c-124">NOTES</span></span>

## <span data-ttu-id="bf31c-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf31c-125">RELATED LINKS</span></span>
