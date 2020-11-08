---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
ms.openlocfilehash: 247b2494e002ae6340f38aa626b9661dbf7722ac
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186814"
---
# <span data-ttu-id="c0594-101">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c0594-101">Remove-AzBatchJobSchedule</span></span>

## <span data-ttu-id="c0594-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c0594-102">SYNOPSIS</span></span>
<span data-ttu-id="c0594-103">A kötegelt feladat ütemezése törlődik.</span><span class="sxs-lookup"><span data-stu-id="c0594-103">Removes a Batch job schedule.</span></span>

## <span data-ttu-id="c0594-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c0594-104">SYNTAX</span></span>

```
Remove-AzBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0594-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c0594-105">DESCRIPTION</span></span>
<span data-ttu-id="c0594-106">A **Remove-AzBatchJobSchedule** parancsmag az Azure-kötegek ütemtervét távolítja el.</span><span class="sxs-lookup"><span data-stu-id="c0594-106">The **Remove-AzBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="c0594-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c0594-107">EXAMPLES</span></span>

### <span data-ttu-id="c0594-108">1. példa: kötegelt feladat ütemezéseinak törlése</span><span class="sxs-lookup"><span data-stu-id="c0594-108">Example 1: Delete a Batch job schedule</span></span>
```
PS C:\>Remove-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
```

<span data-ttu-id="c0594-109">Ez a parancs törli az azonosító MyJobSchedule tartalmazó ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="c0594-109">This command deletes the job schedule that has the ID MyJobSchedule.</span></span>
<span data-ttu-id="c0594-110">A parancs a feladat törlése előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c0594-110">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="c0594-111">A Get-AzBatchAccountKey parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="c0594-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="c0594-112">2. példa: kötegelt feladat törlése megerősítés nélkül a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="c0594-112">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context | Remove-AzBatchJobSchedule -Force -BatchContext $Context
```

<span data-ttu-id="c0594-113">Ez a parancs azt a munkabeosztást kapja, amely az azonosító MyJobSchedule az Get-AzBatchJobSchedule parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="c0594-113">This command gets the job schedule that has the ID MyJobSchedule by using the Get-AzBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="c0594-114">A parancs a munkabeosztást átadja az aktuális parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="c0594-114">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c0594-115">A parancs törli a munkabeosztást.</span><span class="sxs-lookup"><span data-stu-id="c0594-115">The command deletes that job schedule.</span></span>
<span data-ttu-id="c0594-116">Mivel a parancs az *erő* paramétert tartalmazza, nem kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c0594-116">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="c0594-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c0594-117">PARAMETERS</span></span>

### <span data-ttu-id="c0594-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c0594-118">-BatchContext</span></span>
<span data-ttu-id="c0594-119">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="c0594-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c0594-120">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="c0594-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c0594-121">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="c0594-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c0594-122">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="c0594-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c0594-123">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="c0594-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c0594-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0594-124">-DefaultProfile</span></span>
<span data-ttu-id="c0594-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c0594-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0594-126">-Force</span><span class="sxs-lookup"><span data-stu-id="c0594-126">-Force</span></span>
<span data-ttu-id="c0594-127">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="c0594-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c0594-128">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="c0594-128">-Id</span></span>
<span data-ttu-id="c0594-129">Az eltávolítandó munkaütemezés AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0594-129">Specifies the ID of the job schedule to remove.</span></span>

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

### <span data-ttu-id="c0594-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c0594-130">-Confirm</span></span>
<span data-ttu-id="c0594-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c0594-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0594-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0594-132">-WhatIf</span></span>
<span data-ttu-id="c0594-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c0594-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0594-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c0594-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0594-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0594-135">CommonParameters</span></span>
<span data-ttu-id="c0594-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c0594-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0594-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c0594-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0594-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0594-138">INPUTS</span></span>

### <span data-ttu-id="c0594-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c0594-139">System.String</span></span>

### <span data-ttu-id="c0594-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c0594-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c0594-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0594-141">OUTPUTS</span></span>

### <span data-ttu-id="c0594-142">System. Void</span><span class="sxs-lookup"><span data-stu-id="c0594-142">System.Void</span></span>

## <span data-ttu-id="c0594-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c0594-143">NOTES</span></span>

## <span data-ttu-id="c0594-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0594-144">RELATED LINKS</span></span>

[<span data-ttu-id="c0594-145">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c0594-145">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="c0594-146">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c0594-146">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="c0594-147">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c0594-147">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="c0594-148">Új – AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c0594-148">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="c0594-149">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c0594-149">Set-AzBatchJobSchedule</span></span>](./Set-AzBatchJobSchedule.md)

[<span data-ttu-id="c0594-150">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c0594-150">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


