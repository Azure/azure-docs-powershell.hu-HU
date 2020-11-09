---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
ms.openlocfilehash: 9979a0fa16b8cfbe59eb8412a76cbbebcb2fca4a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303797"
---
# <span data-ttu-id="a4fd1-101">Enable-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="a4fd1-101">Enable-AzBatchTask</span></span>

## <span data-ttu-id="a4fd1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a4fd1-102">SYNOPSIS</span></span>
<span data-ttu-id="a4fd1-103">Tevékenység újraaktiválása</span><span class="sxs-lookup"><span data-stu-id="a4fd1-103">Reactivates a task.</span></span>

## <span data-ttu-id="a4fd1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a4fd1-104">SYNTAX</span></span>

### <span data-ttu-id="a4fd1-105">Azonosító</span><span class="sxs-lookup"><span data-stu-id="a4fd1-105">Id</span></span>
```
Enable-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4fd1-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a4fd1-106">InputObject</span></span>
```
Enable-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4fd1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a4fd1-107">DESCRIPTION</span></span>
<span data-ttu-id="a4fd1-108">Az **enable-AzBatchTask** parancsmag újraaktiválja a feladatot.</span><span class="sxs-lookup"><span data-stu-id="a4fd1-108">The **Enable-AzBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="a4fd1-109">Ha egy tevékenység kimerítette az újrapróbálkozások számát, ez a parancsmag mégis lehetővé teszi a futtatását.</span><span class="sxs-lookup"><span data-stu-id="a4fd1-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="a4fd1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a4fd1-110">EXAMPLES</span></span>

### <span data-ttu-id="a4fd1-111">1. példa: tevékenység újraaktiválása</span><span class="sxs-lookup"><span data-stu-id="a4fd1-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="a4fd1-112">Ez a parancs újra aktiválja a tevékenység Task2 a munkahelyi Job7.</span><span class="sxs-lookup"><span data-stu-id="a4fd1-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="a4fd1-113">2. példa: tevékenység újraaktiválása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="a4fd1-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="a4fd1-114">Ez a parancs azt a kötegelt feladatot kapja meg, amely a Task3 azonosítóval rendelkezik, és az Get-AzBatchTask parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="a4fd1-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="a4fd1-115">A parancs a tevékenységet a pipeline operátorral továbbítja az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="a4fd1-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a4fd1-116">A parancs újra aktiválja ezt a feladatot.</span><span class="sxs-lookup"><span data-stu-id="a4fd1-116">The command reactivates that task.</span></span>

## <span data-ttu-id="a4fd1-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a4fd1-117">PARAMETERS</span></span>

### <span data-ttu-id="a4fd1-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a4fd1-118">-BatchContext</span></span>
<span data-ttu-id="a4fd1-119">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="a4fd1-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a4fd1-120">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="a4fd1-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a4fd1-121">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="a4fd1-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a4fd1-122">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="a4fd1-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a4fd1-123">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="a4fd1-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a4fd1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4fd1-124">-DefaultProfile</span></span>
<span data-ttu-id="a4fd1-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a4fd1-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4fd1-126">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="a4fd1-126">-Id</span></span>
<span data-ttu-id="a4fd1-127">Az újraaktiválni kívánt tevékenység AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4fd1-127">Specifies the ID of the task to reactivate.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4fd1-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="a4fd1-128">-JobId</span></span>
<span data-ttu-id="a4fd1-129">A tevékenységet tartalmazó feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4fd1-129">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4fd1-130">-Tevékenység</span><span class="sxs-lookup"><span data-stu-id="a4fd1-130">-Task</span></span>
<span data-ttu-id="a4fd1-131">A parancsmag által újraaktivált feladatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4fd1-131">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="a4fd1-132">**PSCloudTask** objektum beolvasásához használja az Get-AzBatchTask parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a4fd1-132">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4fd1-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a4fd1-133">-Confirm</span></span>
<span data-ttu-id="a4fd1-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a4fd1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4fd1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4fd1-135">-WhatIf</span></span>
<span data-ttu-id="a4fd1-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a4fd1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4fd1-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a4fd1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4fd1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4fd1-138">CommonParameters</span></span>
<span data-ttu-id="a4fd1-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a4fd1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4fd1-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a4fd1-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4fd1-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4fd1-141">INPUTS</span></span>

### <span data-ttu-id="a4fd1-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a4fd1-142">System.String</span></span>

### <span data-ttu-id="a4fd1-143">Microsoft.Azure.Commands.BatCH. Modellek. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="a4fd1-143">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="a4fd1-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a4fd1-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a4fd1-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4fd1-145">OUTPUTS</span></span>

### <span data-ttu-id="a4fd1-146">System. Void</span><span class="sxs-lookup"><span data-stu-id="a4fd1-146">System.Void</span></span>

## <span data-ttu-id="a4fd1-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a4fd1-147">NOTES</span></span>

## <span data-ttu-id="a4fd1-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4fd1-148">RELATED LINKS</span></span>

[<span data-ttu-id="a4fd1-149">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="a4fd1-149">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="a4fd1-150">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="a4fd1-150">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="a4fd1-151">Új – AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="a4fd1-151">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="a4fd1-152">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="a4fd1-152">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="a4fd1-153">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="a4fd1-153">Set-AzBatchTask</span></span>](./Set-AzBatchTask.md)

[<span data-ttu-id="a4fd1-154">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="a4fd1-154">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)


