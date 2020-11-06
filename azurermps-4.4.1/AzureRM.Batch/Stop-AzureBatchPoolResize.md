---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
ms.openlocfilehash: d8ce1ec138decb5769aebba431db2accd671f100
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500100"
---
# <span data-ttu-id="9c52d-101">Stop-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="9c52d-101">Stop-AzureBatchPoolResize</span></span>

## <span data-ttu-id="9c52d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9c52d-102">SYNOPSIS</span></span>
<span data-ttu-id="9c52d-103">A készlet átméretezési műveletének leállítása</span><span class="sxs-lookup"><span data-stu-id="9c52d-103">Stops a pool resize operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c52d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9c52d-104">SYNTAX</span></span>

```
Stop-AzureBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c52d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9c52d-105">DESCRIPTION</span></span>
<span data-ttu-id="9c52d-106">A **stop-AzureBatchPoolResize** parancsmag az Azure-kötegek átméretezési műveletét egy készletre állítja.</span><span class="sxs-lookup"><span data-stu-id="9c52d-106">The **Stop-AzureBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="9c52d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9c52d-107">EXAMPLES</span></span>

### <span data-ttu-id="9c52d-108">1. példa: a készlet átméretezésének leállítása</span><span class="sxs-lookup"><span data-stu-id="9c52d-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzureBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="9c52d-109">Ez a parancs leállítja az átméretezési műveletet az azonosító ContosoPool06 tartalmazó készleten.</span><span class="sxs-lookup"><span data-stu-id="9c52d-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="9c52d-110">A Get-AzureRmBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="9c52d-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="9c52d-111">2. példa: a készlet átméretezésének leállítása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="9c52d-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzureBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="9c52d-112">Ez a parancs megszünteti a készlet átméretezését a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="9c52d-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="9c52d-113">A parancs a Get-AzureBatchPool parancsmag használatával az azonosító ContosoPool06 tartalmazó készletet kapja.</span><span class="sxs-lookup"><span data-stu-id="9c52d-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="9c52d-114">A parancs átadja a készlet objektumnak az aktuális parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="9c52d-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="9c52d-115">A parancs ekkor leállítja az átméretezési műveletet a készleten.</span><span class="sxs-lookup"><span data-stu-id="9c52d-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="9c52d-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9c52d-116">PARAMETERS</span></span>

### <span data-ttu-id="9c52d-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="9c52d-117">-BatchContext</span></span>
<span data-ttu-id="9c52d-118">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="9c52d-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9c52d-119">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="9c52d-119">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c52d-120">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="9c52d-120">-Id</span></span>
<span data-ttu-id="9c52d-121">Annak a készletnek az AZONOSÍTÓját adja meg, amelyhez ez a parancsmag leállítja az átméretezési műveletet.</span><span class="sxs-lookup"><span data-stu-id="9c52d-121">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c52d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c52d-122">-DefaultProfile</span></span>
<span data-ttu-id="9c52d-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9c52d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c52d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c52d-124">CommonParameters</span></span>
<span data-ttu-id="9c52d-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9c52d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c52d-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c52d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c52d-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c52d-127">INPUTS</span></span>

### <span data-ttu-id="9c52d-128">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9c52d-128">BatchAccountContext</span></span>
<span data-ttu-id="9c52d-129">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="9c52d-129">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="9c52d-130">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="9c52d-130">String</span></span>
<span data-ttu-id="9c52d-131">Az ' azonosító ' paraméter a pipeline "string" típusú értékét fogadja el.</span><span class="sxs-lookup"><span data-stu-id="9c52d-131">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="9c52d-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c52d-132">OUTPUTS</span></span>

## <span data-ttu-id="9c52d-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9c52d-133">NOTES</span></span>

## <span data-ttu-id="9c52d-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9c52d-134">RELATED LINKS</span></span>

[<span data-ttu-id="9c52d-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9c52d-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="9c52d-136">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="9c52d-136">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="9c52d-137">Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="9c52d-137">Start-AzureBatchPoolResize</span></span>](./Start-AzureBatchPoolResize.md)

[<span data-ttu-id="9c52d-138">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="9c52d-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


