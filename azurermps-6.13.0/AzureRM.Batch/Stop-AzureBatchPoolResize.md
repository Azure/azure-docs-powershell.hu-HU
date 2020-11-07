---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
ms.openlocfilehash: 8db1f11cfd434beb52eb32e4b175b2dab67ecbdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673175"
---
# <span data-ttu-id="8120c-101">Stop-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="8120c-101">Stop-AzureBatchPoolResize</span></span>

## <span data-ttu-id="8120c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8120c-102">SYNOPSIS</span></span>
<span data-ttu-id="8120c-103">A készlet átméretezési műveletének leállítása</span><span class="sxs-lookup"><span data-stu-id="8120c-103">Stops a pool resize operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8120c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8120c-104">SYNTAX</span></span>

```
Stop-AzureBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8120c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8120c-105">DESCRIPTION</span></span>
<span data-ttu-id="8120c-106">A **stop-AzureBatchPoolResize** parancsmag az Azure-kötegek átméretezési műveletét egy készletre állítja.</span><span class="sxs-lookup"><span data-stu-id="8120c-106">The **Stop-AzureBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="8120c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8120c-107">EXAMPLES</span></span>

### <span data-ttu-id="8120c-108">1. példa: a készlet átméretezésének leállítása</span><span class="sxs-lookup"><span data-stu-id="8120c-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzureBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="8120c-109">Ez a parancs leállítja az átméretezési műveletet az azonosító ContosoPool06 tartalmazó készleten.</span><span class="sxs-lookup"><span data-stu-id="8120c-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="8120c-110">A Get-AzureRmBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="8120c-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="8120c-111">2. példa: a készlet átméretezésének leállítása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="8120c-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzureBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="8120c-112">Ez a parancs megszünteti a készlet átméretezését a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="8120c-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="8120c-113">A parancs a Get-AzureBatchPool parancsmag használatával az azonosító ContosoPool06 tartalmazó készletet kapja.</span><span class="sxs-lookup"><span data-stu-id="8120c-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="8120c-114">A parancs átadja a készlet objektumnak az aktuális parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8120c-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="8120c-115">A parancs ekkor leállítja az átméretezési műveletet a készleten.</span><span class="sxs-lookup"><span data-stu-id="8120c-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="8120c-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8120c-116">PARAMETERS</span></span>

### <span data-ttu-id="8120c-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8120c-117">-BatchContext</span></span>
<span data-ttu-id="8120c-118">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="8120c-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8120c-119">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="8120c-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8120c-120">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="8120c-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8120c-121">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="8120c-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8120c-122">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="8120c-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8120c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8120c-123">-DefaultProfile</span></span>
<span data-ttu-id="8120c-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8120c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8120c-125">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="8120c-125">-Id</span></span>
<span data-ttu-id="8120c-126">Annak a készletnek az AZONOSÍTÓját adja meg, amelyhez ez a parancsmag leállítja az átméretezési műveletet.</span><span class="sxs-lookup"><span data-stu-id="8120c-126">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

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

### <span data-ttu-id="8120c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8120c-127">CommonParameters</span></span>
<span data-ttu-id="8120c-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8120c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8120c-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8120c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8120c-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8120c-130">INPUTS</span></span>

### <span data-ttu-id="8120c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="8120c-131">System.String</span></span>

### <span data-ttu-id="8120c-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8120c-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="8120c-133">Paraméterek: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8120c-133">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="8120c-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8120c-134">OUTPUTS</span></span>

### <span data-ttu-id="8120c-135">System. Void</span><span class="sxs-lookup"><span data-stu-id="8120c-135">System.Void</span></span>

## <span data-ttu-id="8120c-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8120c-136">NOTES</span></span>

## <span data-ttu-id="8120c-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8120c-137">RELATED LINKS</span></span>

[<span data-ttu-id="8120c-138">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="8120c-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="8120c-139">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="8120c-139">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="8120c-140">Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="8120c-140">Start-AzureBatchPoolResize</span></span>](./Start-AzureBatchPoolResize.md)

[<span data-ttu-id="8120c-141">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="8120c-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


