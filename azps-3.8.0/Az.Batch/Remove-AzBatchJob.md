---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
ms.openlocfilehash: 348924c4243245200666dae6f4e54061783182ce
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "94017206"
---
# <span data-ttu-id="74049-101">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="74049-101">Remove-AzBatchJob</span></span>

## <span data-ttu-id="74049-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="74049-102">SYNOPSIS</span></span>
<span data-ttu-id="74049-103">Töröl egy kötegelt feladatot.</span><span class="sxs-lookup"><span data-stu-id="74049-103">Deletes a Batch job.</span></span>

## <span data-ttu-id="74049-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="74049-104">SYNTAX</span></span>

```
Remove-AzBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74049-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="74049-105">DESCRIPTION</span></span>
<span data-ttu-id="74049-106">A **Remove-AzBatchJob** parancsmag egy Azure kötegelt feladatot töröl.</span><span class="sxs-lookup"><span data-stu-id="74049-106">The **Remove-AzBatchJob** cmdlet deletes an Azure Batch job.</span></span>
<span data-ttu-id="74049-107">Ez a parancsmag arra kéri, hogy erősítse meg a feladat eltávolítását, hacsak nem adja meg az *erő* paramétert.</span><span class="sxs-lookup"><span data-stu-id="74049-107">This cmdlet prompts you for confirmation before it removes a job, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="74049-108">Példák</span><span class="sxs-lookup"><span data-stu-id="74049-108">EXAMPLES</span></span>

### <span data-ttu-id="74049-109">Példa 1: kötegelt feladat törlése</span><span class="sxs-lookup"><span data-stu-id="74049-109">Example 1: Delete a Batch job</span></span>
```
PS C:\>Remove-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="74049-110">Ez a parancs törli azt a feladatot, amely a 000001 AZONOSÍTÓval rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="74049-110">This command deletes the job that has the ID Job-000001.</span></span>
<span data-ttu-id="74049-111">A parancs a feladat törlése előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="74049-111">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="74049-112">A Get-AzBatchAccountKey parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="74049-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="74049-113">2. példa: kötegelt feladat törlése megerősítés nélkül a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="74049-113">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzBatchJob -Force -BatchContext $Context
```

<span data-ttu-id="74049-114">Ez a parancs a Get-AzBatchJob parancsmaggal a 000002 AZONOSÍTÓJÚ feladatot kapja.</span><span class="sxs-lookup"><span data-stu-id="74049-114">This command gets the job that has the ID Job-000002 by using the Get-AzBatchJob cmdlet.</span></span>
<span data-ttu-id="74049-115">A parancs a munkafolyamatot a csővezeték-kezelő használatával továbbítja az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="74049-115">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="74049-116">A parancs törli azt a feladatot.</span><span class="sxs-lookup"><span data-stu-id="74049-116">The command deletes that job.</span></span>
<span data-ttu-id="74049-117">Mivel a parancs az *erő* paramétert tartalmazza, nem kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="74049-117">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="74049-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="74049-118">PARAMETERS</span></span>

### <span data-ttu-id="74049-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="74049-119">-BatchContext</span></span>
<span data-ttu-id="74049-120">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="74049-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="74049-121">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="74049-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="74049-122">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="74049-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="74049-123">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="74049-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="74049-124">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="74049-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="74049-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74049-125">-DefaultProfile</span></span>
<span data-ttu-id="74049-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="74049-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74049-127">-Force</span><span class="sxs-lookup"><span data-stu-id="74049-127">-Force</span></span>
<span data-ttu-id="74049-128">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="74049-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="74049-129">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="74049-129">-Id</span></span>
<span data-ttu-id="74049-130">Annak a feladatnak az AZONOSÍTÓját adja meg, amelyre a parancsmag törlődik.</span><span class="sxs-lookup"><span data-stu-id="74049-130">Specifies the ID of the job that this cmdlet deletes.</span></span>
<span data-ttu-id="74049-131">A helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="74049-131">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="74049-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="74049-132">-Confirm</span></span>
<span data-ttu-id="74049-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="74049-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74049-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74049-134">-WhatIf</span></span>
<span data-ttu-id="74049-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="74049-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74049-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="74049-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74049-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74049-137">CommonParameters</span></span>
<span data-ttu-id="74049-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="74049-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74049-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="74049-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74049-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="74049-140">INPUTS</span></span>

### <span data-ttu-id="74049-141">System. String</span><span class="sxs-lookup"><span data-stu-id="74049-141">System.String</span></span>

### <span data-ttu-id="74049-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="74049-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="74049-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="74049-143">OUTPUTS</span></span>

### <span data-ttu-id="74049-144">System. Void</span><span class="sxs-lookup"><span data-stu-id="74049-144">System.Void</span></span>

## <span data-ttu-id="74049-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="74049-145">NOTES</span></span>

## <span data-ttu-id="74049-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="74049-146">RELATED LINKS</span></span>

[<span data-ttu-id="74049-147">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="74049-147">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="74049-148">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="74049-148">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="74049-149">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="74049-149">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="74049-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="74049-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="74049-151">Új – AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="74049-151">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="74049-152">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="74049-152">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="74049-153">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="74049-153">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


