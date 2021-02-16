---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
ms.openlocfilehash: 229877db7a3077a4b1951a06914c842e63384ba6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162450"
---
# <span data-ttu-id="483af-101">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="483af-101">Stop-AzBatchPoolResize</span></span>

## <span data-ttu-id="483af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="483af-102">SYNOPSIS</span></span>
<span data-ttu-id="483af-103">Leállítja a készlet átméretezését.</span><span class="sxs-lookup"><span data-stu-id="483af-103">Stops a pool resize operation.</span></span>

## <span data-ttu-id="483af-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="483af-104">SYNTAX</span></span>

```
Stop-AzBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="483af-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="483af-105">DESCRIPTION</span></span>
<span data-ttu-id="483af-106">A **Stop-AzBatchPoolResize** parancsmag leállít egy Azure Batch-átméretezési műveletet egy készleten.</span><span class="sxs-lookup"><span data-stu-id="483af-106">The **Stop-AzBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="483af-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="483af-107">EXAMPLES</span></span>

### <span data-ttu-id="483af-108">1. példa: Készlet átméretezésének vége</span><span class="sxs-lookup"><span data-stu-id="483af-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="483af-109">Ez a parancs leállít egy átméretezési műveletet a ContosoPool06 azonosítójú készleten.</span><span class="sxs-lookup"><span data-stu-id="483af-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="483af-110">A Get-AzBatchAccountKey parancsmag használatával kontextust rendelhet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="483af-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="483af-111">2. példa: Készlet átméretezésének vége a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="483af-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="483af-112">Ez a parancs leállítja a készlet átméretezését a folyamat műveleti operátorával.</span><span class="sxs-lookup"><span data-stu-id="483af-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="483af-113">A parancs a ContosoPool06 azonosítót használó készletet a Get-AzBatchPool parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="483af-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="483af-114">A parancs átadja a készletobjektumot az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="483af-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="483af-115">A parancs leállítja az átméretezést a készleten.</span><span class="sxs-lookup"><span data-stu-id="483af-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="483af-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="483af-116">PARAMETERS</span></span>

### <span data-ttu-id="483af-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="483af-117">-BatchContext</span></span>
<span data-ttu-id="483af-118">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatással való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="483af-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="483af-119">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor az Azure Active Directory-hitelesítést fogja használni a Batch szolgáltatás használata során.</span><span class="sxs-lookup"><span data-stu-id="483af-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="483af-120">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="483af-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="483af-121">Megosztott kulcsú hitelesítés használata esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="483af-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="483af-122">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="483af-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="483af-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="483af-123">-DefaultProfile</span></span>
<span data-ttu-id="483af-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="483af-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="483af-125">-Id</span><span class="sxs-lookup"><span data-stu-id="483af-125">-Id</span></span>
<span data-ttu-id="483af-126">Annak a készletnek az azonosítója, amelynek a parancsmagja leállítja az átméretezést.</span><span class="sxs-lookup"><span data-stu-id="483af-126">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

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

### <span data-ttu-id="483af-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="483af-127">CommonParameters</span></span>
<span data-ttu-id="483af-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="483af-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="483af-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="483af-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="483af-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="483af-130">INPUTS</span></span>

### <span data-ttu-id="483af-131">System.String</span><span class="sxs-lookup"><span data-stu-id="483af-131">System.String</span></span>

### <span data-ttu-id="483af-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="483af-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="483af-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="483af-133">OUTPUTS</span></span>

### <span data-ttu-id="483af-134">System.Void</span><span class="sxs-lookup"><span data-stu-id="483af-134">System.Void</span></span>

## <span data-ttu-id="483af-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="483af-135">NOTES</span></span>

## <span data-ttu-id="483af-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="483af-136">RELATED LINKS</span></span>

[<span data-ttu-id="483af-137">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="483af-137">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="483af-138">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="483af-138">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="483af-139">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="483af-139">Start-AzBatchPoolResize</span></span>](./Start-AzBatchPoolResize.md)

[<span data-ttu-id="483af-140">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="483af-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
