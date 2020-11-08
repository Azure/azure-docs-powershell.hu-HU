---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
ms.openlocfilehash: dc5267f93845c6e373b5a6b623df710bd19671ba
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "94017232"
---
# <span data-ttu-id="5ab7e-101">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="5ab7e-101">Stop-AzBatchPoolResize</span></span>

## <span data-ttu-id="5ab7e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5ab7e-102">SYNOPSIS</span></span>
<span data-ttu-id="5ab7e-103">A készlet átméretezési műveletének leállítása</span><span class="sxs-lookup"><span data-stu-id="5ab7e-103">Stops a pool resize operation.</span></span>

## <span data-ttu-id="5ab7e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5ab7e-104">SYNTAX</span></span>

```
Stop-AzBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ab7e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5ab7e-105">DESCRIPTION</span></span>
<span data-ttu-id="5ab7e-106">A **stop-AzBatchPoolResize** parancsmag az Azure-kötegek átméretezési műveletét egy készletre állítja.</span><span class="sxs-lookup"><span data-stu-id="5ab7e-106">The **Stop-AzBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="5ab7e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5ab7e-107">EXAMPLES</span></span>

### <span data-ttu-id="5ab7e-108">1. példa: a készlet átméretezésének leállítása</span><span class="sxs-lookup"><span data-stu-id="5ab7e-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="5ab7e-109">Ez a parancs leállítja az átméretezési műveletet az azonosító ContosoPool06 tartalmazó készleten.</span><span class="sxs-lookup"><span data-stu-id="5ab7e-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="5ab7e-110">A Get-AzBatchAccountKey parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="5ab7e-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="5ab7e-111">2. példa: a készlet átméretezésének leállítása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="5ab7e-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="5ab7e-112">Ez a parancs megszünteti a készlet átméretezését a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="5ab7e-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="5ab7e-113">A parancs a Get-AzBatchPool parancsmag használatával az azonosító ContosoPool06 tartalmazó készletet kapja.</span><span class="sxs-lookup"><span data-stu-id="5ab7e-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="5ab7e-114">A parancs átadja a készlet objektumnak az aktuális parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5ab7e-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="5ab7e-115">A parancs ekkor leállítja az átméretezési műveletet a készleten.</span><span class="sxs-lookup"><span data-stu-id="5ab7e-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="5ab7e-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5ab7e-116">PARAMETERS</span></span>

### <span data-ttu-id="5ab7e-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5ab7e-117">-BatchContext</span></span>
<span data-ttu-id="5ab7e-118">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="5ab7e-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5ab7e-119">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="5ab7e-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5ab7e-120">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="5ab7e-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5ab7e-121">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="5ab7e-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5ab7e-122">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="5ab7e-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5ab7e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ab7e-123">-DefaultProfile</span></span>
<span data-ttu-id="5ab7e-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5ab7e-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ab7e-125">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="5ab7e-125">-Id</span></span>
<span data-ttu-id="5ab7e-126">Annak a készletnek az AZONOSÍTÓját adja meg, amelyhez ez a parancsmag leállítja az átméretezési műveletet.</span><span class="sxs-lookup"><span data-stu-id="5ab7e-126">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

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

### <span data-ttu-id="5ab7e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ab7e-127">CommonParameters</span></span>
<span data-ttu-id="5ab7e-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5ab7e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ab7e-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5ab7e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ab7e-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ab7e-130">INPUTS</span></span>

### <span data-ttu-id="5ab7e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5ab7e-131">System.String</span></span>

### <span data-ttu-id="5ab7e-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5ab7e-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="5ab7e-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ab7e-133">OUTPUTS</span></span>

### <span data-ttu-id="5ab7e-134">System. Void</span><span class="sxs-lookup"><span data-stu-id="5ab7e-134">System.Void</span></span>

## <span data-ttu-id="5ab7e-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5ab7e-135">NOTES</span></span>

## <span data-ttu-id="5ab7e-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ab7e-136">RELATED LINKS</span></span>

[<span data-ttu-id="5ab7e-137">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="5ab7e-137">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="5ab7e-138">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="5ab7e-138">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="5ab7e-139">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="5ab7e-139">Start-AzBatchPoolResize</span></span>](./Start-AzBatchPoolResize.md)

[<span data-ttu-id="5ab7e-140">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="5ab7e-140">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


