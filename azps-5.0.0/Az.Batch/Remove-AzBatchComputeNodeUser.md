---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
ms.openlocfilehash: 52fea755708645173a5f0f3429591a384ec63b01
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187071"
---
# <span data-ttu-id="ba8f3-101">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="ba8f3-101">Remove-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="ba8f3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ba8f3-102">SYNOPSIS</span></span>
<span data-ttu-id="ba8f3-103">Felhasználói fiók törlése kötegelt számítási csomópontból.</span><span class="sxs-lookup"><span data-stu-id="ba8f3-103">Deletes a user account from a Batch compute node.</span></span>

## <span data-ttu-id="ba8f3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ba8f3-104">SYNTAX</span></span>

```
Remove-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ba8f3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ba8f3-105">DESCRIPTION</span></span>
<span data-ttu-id="ba8f3-106">A **Remove-AzBatchComputeNodeUser** parancsmag az Azure batch számítási csomópontból törli a felhasználói fiókokat.</span><span class="sxs-lookup"><span data-stu-id="ba8f3-106">The **Remove-AzBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="ba8f3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ba8f3-107">EXAMPLES</span></span>

### <span data-ttu-id="ba8f3-108">Példa 1: felhasználó törlése egy számítási csomópontról megerősítés nélkül</span><span class="sxs-lookup"><span data-stu-id="ba8f3-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="ba8f3-109">Ez a parancs törli a User14 nevű felhasználót a ComputeNode01 nevű számítási csomópontból.</span><span class="sxs-lookup"><span data-stu-id="ba8f3-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="ba8f3-110">A számítási csomópont a Pool01 nevű készletben található.</span><span class="sxs-lookup"><span data-stu-id="ba8f3-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="ba8f3-111">Ez a parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba8f3-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="ba8f3-112">Ezért a parancs nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ba8f3-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="ba8f3-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ba8f3-113">PARAMETERS</span></span>

### <span data-ttu-id="ba8f3-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ba8f3-114">-BatchContext</span></span>
<span data-ttu-id="ba8f3-115">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="ba8f3-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ba8f3-116">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="ba8f3-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ba8f3-117">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="ba8f3-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ba8f3-118">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="ba8f3-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ba8f3-119">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="ba8f3-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ba8f3-120">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="ba8f3-120">-ComputeNodeId</span></span>
<span data-ttu-id="ba8f3-121">Annak a számítási csomópontnak az AZONOSÍTÓját adja meg, amelyen a parancsmag törli a felhasználói fiókot.</span><span class="sxs-lookup"><span data-stu-id="ba8f3-121">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

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

### <span data-ttu-id="ba8f3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba8f3-122">-DefaultProfile</span></span>
<span data-ttu-id="ba8f3-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ba8f3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba8f3-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ba8f3-124">-Name</span></span>
<span data-ttu-id="ba8f3-125">A törlendő felhasználói fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba8f3-125">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="ba8f3-126">A helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="ba8f3-126">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="ba8f3-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="ba8f3-127">-PoolId</span></span>
<span data-ttu-id="ba8f3-128">Annak a készletnek az AZONOSÍTÓját adja meg, amely a felhasználói fiók törlésére szolgáló számítási csomópontot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ba8f3-128">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

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

### <span data-ttu-id="ba8f3-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ba8f3-129">-Confirm</span></span>
<span data-ttu-id="ba8f3-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ba8f3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba8f3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba8f3-131">-WhatIf</span></span>
<span data-ttu-id="ba8f3-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ba8f3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba8f3-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ba8f3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba8f3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba8f3-134">CommonParameters</span></span>
<span data-ttu-id="ba8f3-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ba8f3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba8f3-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ba8f3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba8f3-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba8f3-137">INPUTS</span></span>

### <span data-ttu-id="ba8f3-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ba8f3-138">System.String</span></span>

### <span data-ttu-id="ba8f3-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ba8f3-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ba8f3-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba8f3-140">OUTPUTS</span></span>

### <span data-ttu-id="ba8f3-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="ba8f3-141">System.Void</span></span>

## <span data-ttu-id="ba8f3-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ba8f3-142">NOTES</span></span>

## <span data-ttu-id="ba8f3-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba8f3-143">RELATED LINKS</span></span>

[<span data-ttu-id="ba8f3-144">Új – AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="ba8f3-144">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="ba8f3-145">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ba8f3-145">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ba8f3-146">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="ba8f3-146">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
