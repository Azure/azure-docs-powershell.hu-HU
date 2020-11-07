---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJob.md
ms.openlocfilehash: fa7dede61cd19ec0ea0a4ccd59f2eca3e0cc8f41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672804"
---
# <span data-ttu-id="3ec9d-101">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="3ec9d-101">Remove-AzureBatchJob</span></span>

## <span data-ttu-id="3ec9d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3ec9d-102">SYNOPSIS</span></span>
<span data-ttu-id="3ec9d-103">Töröl egy kötegelt feladatot.</span><span class="sxs-lookup"><span data-stu-id="3ec9d-103">Deletes a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ec9d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3ec9d-104">SYNTAX</span></span>

```
Remove-AzureBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ec9d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3ec9d-105">DESCRIPTION</span></span>
<span data-ttu-id="3ec9d-106">A **Remove-AzureBatchJob** parancsmag egy Azure kötegelt feladatot töröl.</span><span class="sxs-lookup"><span data-stu-id="3ec9d-106">The **Remove-AzureBatchJob** cmdlet deletes an Azure Batch job.</span></span>
<span data-ttu-id="3ec9d-107">Ez a parancsmag arra kéri, hogy erősítse meg a feladat eltávolítását, hacsak nem adja meg az *erő* paramétert.</span><span class="sxs-lookup"><span data-stu-id="3ec9d-107">This cmdlet prompts you for confirmation before it removes a job, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="3ec9d-108">Példák</span><span class="sxs-lookup"><span data-stu-id="3ec9d-108">EXAMPLES</span></span>

### <span data-ttu-id="3ec9d-109">Példa 1: kötegelt feladat törlése</span><span class="sxs-lookup"><span data-stu-id="3ec9d-109">Example 1: Delete a Batch job</span></span>
```
PS C:\>Remove-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="3ec9d-110">Ez a parancs törli azt a feladatot, amely a 000001 AZONOSÍTÓval rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="3ec9d-110">This command deletes the job that has the ID Job-000001.</span></span>
<span data-ttu-id="3ec9d-111">A parancs a feladat törlése előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3ec9d-111">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="3ec9d-112">A Get-AzureRmBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="3ec9d-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="3ec9d-113">2. példa: kötegelt feladat törlése megerősítés nélkül a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="3ec9d-113">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzureBatchJob -Force -BatchContext $Context
```

<span data-ttu-id="3ec9d-114">Ez a parancs a Get-AzureBatchJob parancsmaggal a 000002 AZONOSÍTÓJÚ feladatot kapja.</span><span class="sxs-lookup"><span data-stu-id="3ec9d-114">This command gets the job that has the ID Job-000002 by using the Get-AzureBatchJob cmdlet.</span></span>
<span data-ttu-id="3ec9d-115">A parancs a munkafolyamatot a csővezeték-kezelő használatával továbbítja az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="3ec9d-115">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3ec9d-116">A parancs törli azt a feladatot.</span><span class="sxs-lookup"><span data-stu-id="3ec9d-116">The command deletes that job.</span></span>
<span data-ttu-id="3ec9d-117">Mivel a parancs az *erő* paramétert tartalmazza, nem kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3ec9d-117">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="3ec9d-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3ec9d-118">PARAMETERS</span></span>

### <span data-ttu-id="3ec9d-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3ec9d-119">-BatchContext</span></span>
<span data-ttu-id="3ec9d-120">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="3ec9d-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3ec9d-121">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="3ec9d-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="3ec9d-122">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="3ec9d-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="3ec9d-123">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="3ec9d-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="3ec9d-124">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="3ec9d-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="3ec9d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ec9d-125">-DefaultProfile</span></span>
<span data-ttu-id="3ec9d-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3ec9d-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ec9d-127">-Force</span><span class="sxs-lookup"><span data-stu-id="3ec9d-127">-Force</span></span>
<span data-ttu-id="3ec9d-128">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="3ec9d-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3ec9d-129">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="3ec9d-129">-Id</span></span>
<span data-ttu-id="3ec9d-130">Annak a feladatnak az AZONOSÍTÓját adja meg, amelyre a parancsmag törlődik.</span><span class="sxs-lookup"><span data-stu-id="3ec9d-130">Specifies the ID of the job that this cmdlet deletes.</span></span>
<span data-ttu-id="3ec9d-131">A helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="3ec9d-131">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="3ec9d-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3ec9d-132">-Confirm</span></span>
<span data-ttu-id="3ec9d-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3ec9d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ec9d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ec9d-134">-WhatIf</span></span>
<span data-ttu-id="3ec9d-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3ec9d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ec9d-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3ec9d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ec9d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ec9d-137">CommonParameters</span></span>
<span data-ttu-id="3ec9d-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3ec9d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ec9d-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ec9d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ec9d-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ec9d-140">INPUTS</span></span>

### <span data-ttu-id="3ec9d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3ec9d-141">System.String</span></span>

### <span data-ttu-id="3ec9d-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3ec9d-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="3ec9d-143">Paraméterek: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3ec9d-143">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="3ec9d-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ec9d-144">OUTPUTS</span></span>

### <span data-ttu-id="3ec9d-145">System. Void</span><span class="sxs-lookup"><span data-stu-id="3ec9d-145">System.Void</span></span>

## <span data-ttu-id="3ec9d-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3ec9d-146">NOTES</span></span>

## <span data-ttu-id="3ec9d-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ec9d-147">RELATED LINKS</span></span>

[<span data-ttu-id="3ec9d-148">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="3ec9d-148">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="3ec9d-149">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="3ec9d-149">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="3ec9d-150">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="3ec9d-150">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="3ec9d-151">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="3ec9d-151">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="3ec9d-152">Új – AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="3ec9d-152">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="3ec9d-153">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="3ec9d-153">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="3ec9d-154">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="3ec9d-154">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


