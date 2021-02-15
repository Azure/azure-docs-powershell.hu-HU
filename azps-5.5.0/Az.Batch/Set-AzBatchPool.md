---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
ms.openlocfilehash: 423f249a7971883cbe47d8f499fdd780980362f3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164242"
---
# <span data-ttu-id="94d24-101">Set-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="94d24-101">Set-AzBatchPool</span></span>

## <span data-ttu-id="94d24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94d24-102">SYNOPSIS</span></span>
<span data-ttu-id="94d24-103">Frissíti egy készlet tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="94d24-103">Updates the properties of a pool.</span></span>

## <span data-ttu-id="94d24-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="94d24-104">SYNTAX</span></span>

```
Set-AzBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94d24-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="94d24-105">DESCRIPTION</span></span>
<span data-ttu-id="94d24-106">A **Set-AzBatchPool** parancsmag frissíti egy készlet tulajdonságait az Azure Batch szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="94d24-106">The **Set-AzBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="94d24-107">A Get-AzBatchPool parancsmagot használva szerezze be a **PSCloudPool-objektumot.**</span><span class="sxs-lookup"><span data-stu-id="94d24-107">Use the Get-AzBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="94d24-108">Módosítsa az objektum tulajdonságait, majd az aktuális parancsmagot használva végleges kövesse a módosításokat a Batch szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="94d24-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="94d24-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="94d24-109">EXAMPLES</span></span>

### <span data-ttu-id="94d24-110">1. példa: Készlet frissítése</span><span class="sxs-lookup"><span data-stu-id="94d24-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="94d24-111">Az első parancs a **Get-AzBatchPool** segítségével kap egy készletet, majd azt a $Pool tárolja.</span><span class="sxs-lookup"><span data-stu-id="94d24-111">The first command gets a pool by using **Get-AzBatchPool**, and then stores it in the $Pool variable.</span></span>
<span data-ttu-id="94d24-112">A következő három parancs módosítja a feladat indítási specifikációját a $Pool objektumon.</span><span class="sxs-lookup"><span data-stu-id="94d24-112">The next three commands modify the start task specification on the $Pool object.</span></span>
<span data-ttu-id="94d24-113">Az utolsó parancs frissíti a Batch szolgáltatást úgy, hogy megfeleljen a helyi objektumnak a $Pool.</span><span class="sxs-lookup"><span data-stu-id="94d24-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="94d24-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94d24-114">PARAMETERS</span></span>

### <span data-ttu-id="94d24-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="94d24-115">-BatchContext</span></span>
<span data-ttu-id="94d24-116">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="94d24-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="94d24-117">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor az Azure Active Directory-hitelesítést fogja használni a Batch szolgáltatás használata során.</span><span class="sxs-lookup"><span data-stu-id="94d24-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="94d24-118">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse le a BatchAccountContext objektumot, és töltse ki a hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="94d24-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="94d24-119">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="94d24-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="94d24-120">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="94d24-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="94d24-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94d24-121">-DefaultProfile</span></span>
<span data-ttu-id="94d24-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94d24-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94d24-123">-Pool</span><span class="sxs-lookup"><span data-stu-id="94d24-123">-Pool</span></span>
<span data-ttu-id="94d24-124">Azt a **PSCloudPoolt adja** meg, amelyhez ez a parancsmag frissíti a Batch szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="94d24-124">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94d24-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94d24-125">CommonParameters</span></span>
<span data-ttu-id="94d24-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94d24-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94d24-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94d24-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94d24-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94d24-128">INPUTS</span></span>

### <span data-ttu-id="94d24-129">Microsoft.Azure.Commands.Bat. Models.PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="94d24-129">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="94d24-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="94d24-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="94d24-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94d24-131">OUTPUTS</span></span>

### <span data-ttu-id="94d24-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="94d24-132">System.Void</span></span>

## <span data-ttu-id="94d24-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="94d24-133">NOTES</span></span>

## <span data-ttu-id="94d24-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94d24-134">RELATED LINKS</span></span>

[<span data-ttu-id="94d24-135">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="94d24-135">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="94d24-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="94d24-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="94d24-137">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="94d24-137">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="94d24-138">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="94d24-138">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="94d24-139">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="94d24-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
