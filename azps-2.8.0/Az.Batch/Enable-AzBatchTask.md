---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
ms.openlocfilehash: 1eef03db73e6b1afcb2c9ca92f507e8b0f3ff0ae
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847866"
---
# <span data-ttu-id="9a954-101">Enable-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="9a954-101">Enable-AzBatchTask</span></span>

## <span data-ttu-id="9a954-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9a954-102">SYNOPSIS</span></span>
<span data-ttu-id="9a954-103">Tevékenység újraaktiválása</span><span class="sxs-lookup"><span data-stu-id="9a954-103">Reactivates a task.</span></span>

## <span data-ttu-id="9a954-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9a954-104">SYNTAX</span></span>

### <span data-ttu-id="9a954-105">Azonosító</span><span class="sxs-lookup"><span data-stu-id="9a954-105">Id</span></span>
```
Enable-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a954-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="9a954-106">InputObject</span></span>
```
Enable-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a954-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9a954-107">DESCRIPTION</span></span>
<span data-ttu-id="9a954-108">Az **enable-AzBatchTask** parancsmag újraaktiválja a feladatot.</span><span class="sxs-lookup"><span data-stu-id="9a954-108">The **Enable-AzBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="9a954-109">Ha egy tevékenység kimerítette az újrapróbálkozások számát, ez a parancsmag mégis lehetővé teszi a futtatását.</span><span class="sxs-lookup"><span data-stu-id="9a954-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="9a954-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9a954-110">EXAMPLES</span></span>

### <span data-ttu-id="9a954-111">1. példa: tevékenység újraaktiválása</span><span class="sxs-lookup"><span data-stu-id="9a954-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="9a954-112">Ez a parancs újra aktiválja a tevékenység Task2 a munkahelyi Job7.</span><span class="sxs-lookup"><span data-stu-id="9a954-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="9a954-113">2. példa: tevékenység újraaktiválása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="9a954-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="9a954-114">Ez a parancs azt a kötegelt feladatot kapja meg, amely a Task3 azonosítóval rendelkezik, és az Get-AzBatchTask parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="9a954-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="9a954-115">A parancs a tevékenységet a pipeline operátorral továbbítja az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="9a954-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9a954-116">A parancs újra aktiválja ezt a feladatot.</span><span class="sxs-lookup"><span data-stu-id="9a954-116">The command reactivates that task.</span></span>

## <span data-ttu-id="9a954-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9a954-117">PARAMETERS</span></span>

### <span data-ttu-id="9a954-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="9a954-118">-BatchContext</span></span>
<span data-ttu-id="9a954-119">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="9a954-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9a954-120">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="9a954-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="9a954-121">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="9a954-121">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="9a954-122">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="9a954-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="9a954-123">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="9a954-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="9a954-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a954-124">-DefaultProfile</span></span>
<span data-ttu-id="9a954-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9a954-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a954-126">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="9a954-126">-Id</span></span>
<span data-ttu-id="9a954-127">Az újraaktiválni kívánt tevékenység AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9a954-127">Specifies the ID of the task to reactivate.</span></span>

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

### <span data-ttu-id="9a954-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="9a954-128">-JobId</span></span>
<span data-ttu-id="9a954-129">A tevékenységet tartalmazó feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9a954-129">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="9a954-130">-Tevékenység</span><span class="sxs-lookup"><span data-stu-id="9a954-130">-Task</span></span>
<span data-ttu-id="9a954-131">A parancsmag által újraaktivált feladatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="9a954-131">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="9a954-132">**PSCloudTask** objektum beolvasásához használja az Get-AzBatchTask parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="9a954-132">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="9a954-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9a954-133">-Confirm</span></span>
<span data-ttu-id="9a954-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9a954-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a954-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a954-135">-WhatIf</span></span>
<span data-ttu-id="9a954-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9a954-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a954-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9a954-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a954-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a954-138">CommonParameters</span></span>
<span data-ttu-id="9a954-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9a954-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a954-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a954-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a954-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a954-141">INPUTS</span></span>

### <span data-ttu-id="9a954-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9a954-142">System.String</span></span>

### <span data-ttu-id="9a954-143">Microsoft.Azure.Commands.BatCH. Modellek. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="9a954-143">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="9a954-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9a954-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="9a954-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a954-145">OUTPUTS</span></span>

### <span data-ttu-id="9a954-146">System. Void</span><span class="sxs-lookup"><span data-stu-id="9a954-146">System.Void</span></span>

## <span data-ttu-id="9a954-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9a954-147">NOTES</span></span>

## <span data-ttu-id="9a954-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9a954-148">RELATED LINKS</span></span>

[<span data-ttu-id="9a954-149">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9a954-149">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="9a954-150">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="9a954-150">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="9a954-151">Új – AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="9a954-151">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="9a954-152">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="9a954-152">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="9a954-153">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="9a954-153">Set-AzBatchTask</span></span>](./Set-AzBatchTask.md)

[<span data-ttu-id="9a954-154">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="9a954-154">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)


