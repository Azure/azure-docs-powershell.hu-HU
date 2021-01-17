---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
ms.openlocfilehash: 575c2e8a7e510f3c8b3808b4ed6ce9169cd4f21f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345606"
---
# <span data-ttu-id="f3197-101">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="f3197-101">Remove-AzBatchPool</span></span>

## <span data-ttu-id="f3197-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3197-102">SYNOPSIS</span></span>
<span data-ttu-id="f3197-103">Törli a megadott kötegkészletet.</span><span class="sxs-lookup"><span data-stu-id="f3197-103">Deletes the specified Batch pool.</span></span>

## <span data-ttu-id="f3197-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f3197-104">SYNTAX</span></span>

```
Remove-AzBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3197-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f3197-105">DESCRIPTION</span></span>
<span data-ttu-id="f3197-106">A **Remove-AzBatchPool** parancsmag törli a megadott Azure Batch-készletet.</span><span class="sxs-lookup"><span data-stu-id="f3197-106">The **Remove-AzBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="f3197-107">A rendszer megerősítést kér, hacsak nem használja a *Force paramétert.*</span><span class="sxs-lookup"><span data-stu-id="f3197-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="f3197-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f3197-108">EXAMPLES</span></span>

### <span data-ttu-id="f3197-109">1. példa: Kötegkészlet törlése készletazonosító szerint</span><span class="sxs-lookup"><span data-stu-id="f3197-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="f3197-110">Ez a parancs törli a készletet az Id MyPool azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="f3197-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="f3197-111">A törlési művelet előtt a felhasználó megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f3197-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="f3197-112">2. példa: Az összes kötegkészlet törlése kényszerítve</span><span class="sxs-lookup"><span data-stu-id="f3197-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzBatchPool -BatchContext $Context | Remove-AzBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="f3197-113">Ez a parancs törli az összes kötegkészletet.</span><span class="sxs-lookup"><span data-stu-id="f3197-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="f3197-114">Mivel a *Force* paraméter jelen van, a megerősítést kérő üzenet nem lesz megadva.</span><span class="sxs-lookup"><span data-stu-id="f3197-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="f3197-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3197-115">PARAMETERS</span></span>

### <span data-ttu-id="f3197-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f3197-116">-BatchContext</span></span>
<span data-ttu-id="f3197-117">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="f3197-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f3197-118">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="f3197-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f3197-119">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="f3197-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f3197-120">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="f3197-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f3197-121">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="f3197-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f3197-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3197-122">-DefaultProfile</span></span>
<span data-ttu-id="f3197-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3197-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3197-124">-Force</span><span class="sxs-lookup"><span data-stu-id="f3197-124">-Force</span></span>
<span data-ttu-id="f3197-125">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="f3197-125">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3197-126">-Id</span><span class="sxs-lookup"><span data-stu-id="f3197-126">-Id</span></span>
<span data-ttu-id="f3197-127">A törölni kívánt készlet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f3197-127">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="f3197-128">Helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="f3197-128">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="f3197-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3197-129">-Confirm</span></span>
<span data-ttu-id="f3197-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f3197-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3197-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3197-131">-WhatIf</span></span>
<span data-ttu-id="f3197-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f3197-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3197-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f3197-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3197-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3197-134">CommonParameters</span></span>
<span data-ttu-id="f3197-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3197-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3197-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3197-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3197-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f3197-137">INPUTS</span></span>

### <span data-ttu-id="f3197-138">System.String</span><span class="sxs-lookup"><span data-stu-id="f3197-138">System.String</span></span>

### <span data-ttu-id="f3197-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f3197-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f3197-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3197-140">OUTPUTS</span></span>

### <span data-ttu-id="f3197-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="f3197-141">System.Void</span></span>

## <span data-ttu-id="f3197-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f3197-142">NOTES</span></span>

## <span data-ttu-id="f3197-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3197-143">RELATED LINKS</span></span>

[<span data-ttu-id="f3197-144">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="f3197-144">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="f3197-145">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="f3197-145">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="f3197-146">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="f3197-146">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="f3197-147">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f3197-147">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
