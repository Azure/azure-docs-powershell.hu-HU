---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchLocationQuotas.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchLocationQuotas.md
ms.openlocfilehash: 208ba1055523a1dc76de88d665a7b1dbd097144e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497127"
---
# <span data-ttu-id="45b69-101">Get-AzureRmBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="45b69-101">Get-AzureRmBatchLocationQuotas</span></span>

## <span data-ttu-id="45b69-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="45b69-102">SYNOPSIS</span></span>
<span data-ttu-id="45b69-103">Az előfizetéshez tartozó kötegelt szolgáltatási kvótákat kapja meg az adott helyen.</span><span class="sxs-lookup"><span data-stu-id="45b69-103">Gets the Batch service quotas for your subscription at the given location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45b69-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="45b69-104">SYNTAX</span></span>

```
Get-AzureRmBatchLocationQuotas [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="45b69-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="45b69-105">DESCRIPTION</span></span>
<span data-ttu-id="45b69-106">A megadott előfizetéshez tartozó kötegelt szolgáltatási kvótákat kapja meg az adott helyen.</span><span class="sxs-lookup"><span data-stu-id="45b69-106">Gets the Batch service quotas for the specified subscription at the given location.</span></span>

## <span data-ttu-id="45b69-107">Példák</span><span class="sxs-lookup"><span data-stu-id="45b69-107">EXAMPLES</span></span>

### <span data-ttu-id="45b69-108">Példa 1: a kötegelt szolgáltatás kvótájának beszerzése az előfizetéshez a West US régióban</span><span class="sxs-lookup"><span data-stu-id="45b69-108">Example 1: Get the Batch service quotas for the subscription in the West US region</span></span>
```
PS C:\>Get-AzureRmBatchLocationQuotas -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

<span data-ttu-id="45b69-109">Ez a parancs az aktuális előfizetéshez tartozó kvótákat kapja meg a Nyugat-amerikai régióban.</span><span class="sxs-lookup"><span data-stu-id="45b69-109">This command gets the quotas for the current subscription in the West US region.</span></span>
<span data-ttu-id="45b69-110">A visszatérési érték azt jelzi, hogy ez az előfizetés csak egy köteg fiókot hozhat létre ebben a régióban.</span><span class="sxs-lookup"><span data-stu-id="45b69-110">The return value indicates that this subscription can create only one Batch account in that region.</span></span>

## <span data-ttu-id="45b69-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="45b69-111">PARAMETERS</span></span>

### <span data-ttu-id="45b69-112">-Hely</span><span class="sxs-lookup"><span data-stu-id="45b69-112">-Location</span></span>
<span data-ttu-id="45b69-113">Azt a régiót adja meg, amelyre a parancsmag ellenőrzi a kvótákat.</span><span class="sxs-lookup"><span data-stu-id="45b69-113">Specifies the region for which this cmdlet checks the quotas.</span></span>
<span data-ttu-id="45b69-114">További információ: Azure Regions ( https://azure.microsoft.com/regions) .</span><span class="sxs-lookup"><span data-stu-id="45b69-114">For more information, see Azure Regions (https://azure.microsoft.com/regions).</span></span>

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

### <span data-ttu-id="45b69-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45b69-115">-DefaultProfile</span></span>
<span data-ttu-id="45b69-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="45b69-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45b69-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45b69-117">CommonParameters</span></span>
<span data-ttu-id="45b69-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="45b69-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45b69-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45b69-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45b69-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="45b69-120">INPUTS</span></span>

## <span data-ttu-id="45b69-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45b69-121">OUTPUTS</span></span>

### <span data-ttu-id="45b69-122">Microsoft.Azure.Commands.BatCH. Modellek. PSBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="45b69-122">Microsoft.Azure.Commands.Batch.Models.PSBatchLocationQuotas</span></span>

## <span data-ttu-id="45b69-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="45b69-123">NOTES</span></span>

## <span data-ttu-id="45b69-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45b69-124">RELATED LINKS</span></span>

