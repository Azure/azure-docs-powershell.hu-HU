---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNodeUser.md
ms.openlocfilehash: 668abe661eebfe600625ea85d5694838ef0e12f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679745"
---
# <span data-ttu-id="2082d-101">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="2082d-101">Remove-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="2082d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2082d-102">SYNOPSIS</span></span>
<span data-ttu-id="2082d-103">Felhasználói fiók törlése kötegelt számítási csomópontból.</span><span class="sxs-lookup"><span data-stu-id="2082d-103">Deletes a user account from a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2082d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2082d-104">SYNTAX</span></span>

```
Remove-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2082d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2082d-105">DESCRIPTION</span></span>
<span data-ttu-id="2082d-106">A **Remove-AzureBatchComputeNodeUser** parancsmag az Azure batch számítási csomópontból törli a felhasználói fiókokat.</span><span class="sxs-lookup"><span data-stu-id="2082d-106">The **Remove-AzureBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="2082d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2082d-107">EXAMPLES</span></span>

### <span data-ttu-id="2082d-108">Példa 1: felhasználó törlése egy számítási csomópontról megerősítés nélkül</span><span class="sxs-lookup"><span data-stu-id="2082d-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzureBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="2082d-109">Ez a parancs törli a User14 nevű felhasználót a ComputeNode01 nevű számítási csomópontból.</span><span class="sxs-lookup"><span data-stu-id="2082d-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="2082d-110">A számítási csomópont a Pool01 nevű készletben található.</span><span class="sxs-lookup"><span data-stu-id="2082d-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="2082d-111">Ez a parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="2082d-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="2082d-112">Ezért a parancs nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2082d-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="2082d-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2082d-113">PARAMETERS</span></span>

### <span data-ttu-id="2082d-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2082d-114">-BatchContext</span></span>
<span data-ttu-id="2082d-115">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="2082d-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2082d-116">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="2082d-116">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2082d-117">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="2082d-117">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2082d-118">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="2082d-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2082d-119">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="2082d-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2082d-120">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="2082d-120">-ComputeNodeId</span></span>
<span data-ttu-id="2082d-121">Annak a számítási csomópontnak az AZONOSÍTÓját adja meg, amelyen a parancsmag törli a felhasználói fiókot.</span><span class="sxs-lookup"><span data-stu-id="2082d-121">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2082d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2082d-122">-DefaultProfile</span></span>
<span data-ttu-id="2082d-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2082d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2082d-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2082d-124">-Name</span></span>
<span data-ttu-id="2082d-125">A törlendő felhasználói fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2082d-125">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="2082d-126">A helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="2082d-126">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2082d-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="2082d-127">-PoolId</span></span>
<span data-ttu-id="2082d-128">Annak a készletnek az AZONOSÍTÓját adja meg, amely a felhasználói fiók törlésére szolgáló számítási csomópontot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="2082d-128">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2082d-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2082d-129">-Confirm</span></span>
<span data-ttu-id="2082d-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2082d-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2082d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2082d-131">-WhatIf</span></span>
<span data-ttu-id="2082d-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2082d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2082d-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2082d-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2082d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2082d-134">CommonParameters</span></span>
<span data-ttu-id="2082d-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2082d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2082d-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2082d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2082d-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2082d-137">INPUTS</span></span>

### <span data-ttu-id="2082d-138">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2082d-138">BatchAccountContext</span></span>
<span data-ttu-id="2082d-139">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="2082d-139">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="2082d-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2082d-140">OUTPUTS</span></span>

## <span data-ttu-id="2082d-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2082d-141">NOTES</span></span>

## <span data-ttu-id="2082d-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2082d-142">RELATED LINKS</span></span>

[<span data-ttu-id="2082d-143">Új – AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="2082d-143">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="2082d-144">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="2082d-144">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="2082d-145">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="2082d-145">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


