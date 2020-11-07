---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
ms.openlocfilehash: a57707b10fc103e860fe579e75d7d4ad09cfd0e3
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847838"
---
# <span data-ttu-id="ab550-101">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="ab550-101">Remove-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="ab550-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ab550-102">SYNOPSIS</span></span>
<span data-ttu-id="ab550-103">Felhasználói fiók törlése kötegelt számítási csomópontból.</span><span class="sxs-lookup"><span data-stu-id="ab550-103">Deletes a user account from a Batch compute node.</span></span>

## <span data-ttu-id="ab550-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ab550-104">SYNTAX</span></span>

```
Remove-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ab550-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ab550-105">DESCRIPTION</span></span>
<span data-ttu-id="ab550-106">A **Remove-AzBatchComputeNodeUser** parancsmag az Azure batch számítási csomópontból törli a felhasználói fiókokat.</span><span class="sxs-lookup"><span data-stu-id="ab550-106">The **Remove-AzBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="ab550-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ab550-107">EXAMPLES</span></span>

### <span data-ttu-id="ab550-108">Példa 1: felhasználó törlése egy számítási csomópontról megerősítés nélkül</span><span class="sxs-lookup"><span data-stu-id="ab550-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="ab550-109">Ez a parancs törli a User14 nevű felhasználót a ComputeNode01 nevű számítási csomópontból.</span><span class="sxs-lookup"><span data-stu-id="ab550-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="ab550-110">A számítási csomópont a Pool01 nevű készletben található.</span><span class="sxs-lookup"><span data-stu-id="ab550-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="ab550-111">Ez a parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab550-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="ab550-112">Ezért a parancs nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ab550-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="ab550-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ab550-113">PARAMETERS</span></span>

### <span data-ttu-id="ab550-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ab550-114">-BatchContext</span></span>
<span data-ttu-id="ab550-115">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="ab550-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ab550-116">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="ab550-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ab550-117">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="ab550-117">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ab550-118">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="ab550-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ab550-119">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="ab550-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ab550-120">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="ab550-120">-ComputeNodeId</span></span>
<span data-ttu-id="ab550-121">Annak a számítási csomópontnak az AZONOSÍTÓját adja meg, amelyen a parancsmag törli a felhasználói fiókot.</span><span class="sxs-lookup"><span data-stu-id="ab550-121">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

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

### <span data-ttu-id="ab550-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab550-122">-DefaultProfile</span></span>
<span data-ttu-id="ab550-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ab550-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab550-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ab550-124">-Name</span></span>
<span data-ttu-id="ab550-125">A törlendő felhasználói fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab550-125">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="ab550-126">A helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="ab550-126">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="ab550-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="ab550-127">-PoolId</span></span>
<span data-ttu-id="ab550-128">Annak a készletnek az AZONOSÍTÓját adja meg, amely a felhasználói fiók törlésére szolgáló számítási csomópontot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ab550-128">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

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

### <span data-ttu-id="ab550-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ab550-129">-Confirm</span></span>
<span data-ttu-id="ab550-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ab550-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab550-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab550-131">-WhatIf</span></span>
<span data-ttu-id="ab550-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ab550-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab550-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ab550-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab550-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab550-134">CommonParameters</span></span>
<span data-ttu-id="ab550-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ab550-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab550-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab550-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab550-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab550-137">INPUTS</span></span>

### <span data-ttu-id="ab550-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ab550-138">System.String</span></span>

### <span data-ttu-id="ab550-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ab550-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ab550-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab550-140">OUTPUTS</span></span>

### <span data-ttu-id="ab550-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="ab550-141">System.Void</span></span>

## <span data-ttu-id="ab550-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ab550-142">NOTES</span></span>

## <span data-ttu-id="ab550-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab550-143">RELATED LINKS</span></span>

[<span data-ttu-id="ab550-144">Új – AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="ab550-144">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="ab550-145">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ab550-145">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ab550-146">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="ab550-146">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


