---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
ms.openlocfilehash: c0a0f0a11b4caf18b12c21d37dd18ef153220a97
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478426"
---
# <span data-ttu-id="80fd0-101">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="80fd0-101">Disable-AzBatchAutoScale</span></span>

## <span data-ttu-id="80fd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80fd0-102">SYNOPSIS</span></span>
<span data-ttu-id="80fd0-103">Letiltja a készlet automatikus méretezését.</span><span class="sxs-lookup"><span data-stu-id="80fd0-103">Disables automatic scaling of a pool.</span></span>

## <span data-ttu-id="80fd0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="80fd0-104">SYNTAX</span></span>

```
Disable-AzBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80fd0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="80fd0-105">DESCRIPTION</span></span>
<span data-ttu-id="80fd0-106">A **Disable-AzBatchAutoScale** parancsmag letiltja a megadott készlet automatikus méretezését.</span><span class="sxs-lookup"><span data-stu-id="80fd0-106">The **Disable-AzBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="80fd0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="80fd0-107">EXAMPLES</span></span>

### <span data-ttu-id="80fd0-108">1. példa: A készlet automatikus méretezésének letiltása</span><span class="sxs-lookup"><span data-stu-id="80fd0-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="80fd0-109">Ez a parancs letiltja az automatikus méretezést a MyPool nevű készletben.</span><span class="sxs-lookup"><span data-stu-id="80fd0-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="80fd0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80fd0-110">PARAMETERS</span></span>

### <span data-ttu-id="80fd0-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="80fd0-111">-BatchContext</span></span>
<span data-ttu-id="80fd0-112">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="80fd0-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="80fd0-113">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="80fd0-113">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="80fd0-114">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="80fd0-114">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="80fd0-115">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="80fd0-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="80fd0-116">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="80fd0-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="80fd0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80fd0-117">-DefaultProfile</span></span>
<span data-ttu-id="80fd0-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="80fd0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80fd0-119">-Id</span><span class="sxs-lookup"><span data-stu-id="80fd0-119">-Id</span></span>
<span data-ttu-id="80fd0-120">A készlet objektumazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="80fd0-120">Specifies the object ID of the pool.</span></span>

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

### <span data-ttu-id="80fd0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80fd0-121">CommonParameters</span></span>
<span data-ttu-id="80fd0-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80fd0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80fd0-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80fd0-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80fd0-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="80fd0-124">INPUTS</span></span>

### <span data-ttu-id="80fd0-125">System.String</span><span class="sxs-lookup"><span data-stu-id="80fd0-125">System.String</span></span>

### <span data-ttu-id="80fd0-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="80fd0-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="80fd0-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="80fd0-127">OUTPUTS</span></span>

### <span data-ttu-id="80fd0-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="80fd0-128">System.Void</span></span>

## <span data-ttu-id="80fd0-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="80fd0-129">NOTES</span></span>

## <span data-ttu-id="80fd0-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="80fd0-130">RELATED LINKS</span></span>

[<span data-ttu-id="80fd0-131">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="80fd0-131">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="80fd0-132">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="80fd0-132">Test-AzBatchAutoScale</span></span>](./Test-AzBatchAutoScale.md)

[<span data-ttu-id="80fd0-133">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="80fd0-133">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)


