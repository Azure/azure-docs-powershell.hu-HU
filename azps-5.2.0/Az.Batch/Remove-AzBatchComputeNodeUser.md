---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
ms.openlocfilehash: 52fea755708645173a5f0f3429591a384ec63b01
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370466"
---
# <span data-ttu-id="e7531-101">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="e7531-101">Remove-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="e7531-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7531-102">SYNOPSIS</span></span>
<span data-ttu-id="e7531-103">Felhasználói fiókot töröl egy batch számítási csomópontból.</span><span class="sxs-lookup"><span data-stu-id="e7531-103">Deletes a user account from a Batch compute node.</span></span>

## <span data-ttu-id="e7531-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e7531-104">SYNTAX</span></span>

```
Remove-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e7531-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e7531-105">DESCRIPTION</span></span>
<span data-ttu-id="e7531-106">A **Remove-AzBatchComputeNodeUser** parancsmag töröl egy felhasználói fiókot egy Azure Batch-számítási csomópontból.</span><span class="sxs-lookup"><span data-stu-id="e7531-106">The **Remove-AzBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="e7531-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e7531-107">EXAMPLES</span></span>

### <span data-ttu-id="e7531-108">1. példa: Felhasználó törlése egy számítási csomópontból megerősítés nélkül</span><span class="sxs-lookup"><span data-stu-id="e7531-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="e7531-109">Ez a parancs törli a User14 nevű felhasználót a ComputeNode01 nevű számítási csomópontból.</span><span class="sxs-lookup"><span data-stu-id="e7531-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="e7531-110">A számítási csomópont a Pool01 nevű készletben található.</span><span class="sxs-lookup"><span data-stu-id="e7531-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="e7531-111">Ez a parancs a *Force paramétert* adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7531-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="e7531-112">Ezért a parancs nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e7531-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="e7531-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7531-113">PARAMETERS</span></span>

### <span data-ttu-id="e7531-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e7531-114">-BatchContext</span></span>
<span data-ttu-id="e7531-115">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="e7531-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e7531-116">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="e7531-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e7531-117">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="e7531-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e7531-118">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="e7531-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e7531-119">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="e7531-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e7531-120">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="e7531-120">-ComputeNodeId</span></span>
<span data-ttu-id="e7531-121">Annak a számítási csomópontnak az azonosítója, amelyen ez a parancsmag törli a felhasználói fiókot.</span><span class="sxs-lookup"><span data-stu-id="e7531-121">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7531-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7531-122">-DefaultProfile</span></span>
<span data-ttu-id="e7531-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e7531-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7531-124">-Name</span><span class="sxs-lookup"><span data-stu-id="e7531-124">-Name</span></span>
<span data-ttu-id="e7531-125">A törölni kívánt felhasználói fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7531-125">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="e7531-126">Helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="e7531-126">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7531-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="e7531-127">-PoolId</span></span>
<span data-ttu-id="e7531-128">Annak a készletnek az azonosítója, amely azt a számítási csomópontot tartalmazza, amelyen törölni szeretné a felhasználói fiókot.</span><span class="sxs-lookup"><span data-stu-id="e7531-128">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

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

### <span data-ttu-id="e7531-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7531-129">-Confirm</span></span>
<span data-ttu-id="e7531-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e7531-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7531-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7531-131">-WhatIf</span></span>
<span data-ttu-id="e7531-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e7531-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7531-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e7531-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7531-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7531-134">CommonParameters</span></span>
<span data-ttu-id="e7531-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7531-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7531-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7531-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7531-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e7531-137">INPUTS</span></span>

### <span data-ttu-id="e7531-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e7531-138">System.String</span></span>

### <span data-ttu-id="e7531-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e7531-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e7531-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7531-140">OUTPUTS</span></span>

### <span data-ttu-id="e7531-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="e7531-141">System.Void</span></span>

## <span data-ttu-id="e7531-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e7531-142">NOTES</span></span>

## <span data-ttu-id="e7531-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e7531-143">RELATED LINKS</span></span>

[<span data-ttu-id="e7531-144">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="e7531-144">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="e7531-145">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="e7531-145">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="e7531-146">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="e7531-146">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
