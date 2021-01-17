---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
ms.openlocfilehash: 8b84028bc9da854b5aa749867a8759b71d9f7b63
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478157"
---
# <span data-ttu-id="48cbb-101">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="48cbb-101">Stop-AzBatchTask</span></span>

## <span data-ttu-id="48cbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48cbb-102">SYNOPSIS</span></span>
<span data-ttu-id="48cbb-103">Egy kötegfeladat leállítja.</span><span class="sxs-lookup"><span data-stu-id="48cbb-103">Stops a Batch task.</span></span>

## <span data-ttu-id="48cbb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="48cbb-104">SYNTAX</span></span>

### <span data-ttu-id="48cbb-105">Azonosító</span><span class="sxs-lookup"><span data-stu-id="48cbb-105">Id</span></span>
```
Stop-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48cbb-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="48cbb-106">InputObject</span></span>
```
Stop-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48cbb-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="48cbb-107">DESCRIPTION</span></span>
<span data-ttu-id="48cbb-108">A **Stop-AzBatchTask** parancsmag leállít egy Azure Batch-feladatot.</span><span class="sxs-lookup"><span data-stu-id="48cbb-108">The **Stop-AzBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="48cbb-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="48cbb-109">EXAMPLES</span></span>

### <span data-ttu-id="48cbb-110">1. példa: Batch-feladat törlése azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="48cbb-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="48cbb-111">Ez a parancs leállítja a 23-as azonosítójú tevékenységet a 000001 azonosítójú feladat alatt.</span><span class="sxs-lookup"><span data-stu-id="48cbb-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="48cbb-112">A parancs megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="48cbb-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="48cbb-113">A Get-AzBatchAccountKey parancsmag használatával kontextust rendelhet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="48cbb-113">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="48cbb-114">2. példa: Kötegfeladat leállítása a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="48cbb-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="48cbb-115">Ez a parancs a 000001-es azonosítójú feladathoz az azonosító feladat26 azonosítóját használó kötegfeladatot kapja a Get-AzBatchTask parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="48cbb-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="48cbb-116">A parancs a folyamat műveleti operátorával átadja a feladatot az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="48cbb-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="48cbb-117">A parancs leállítja ezt a feladatot.</span><span class="sxs-lookup"><span data-stu-id="48cbb-117">The command stops that task.</span></span>

## <span data-ttu-id="48cbb-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48cbb-118">PARAMETERS</span></span>

### <span data-ttu-id="48cbb-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="48cbb-119">-BatchContext</span></span>
<span data-ttu-id="48cbb-120">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="48cbb-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="48cbb-121">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="48cbb-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="48cbb-122">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="48cbb-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="48cbb-123">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="48cbb-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="48cbb-124">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="48cbb-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="48cbb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48cbb-125">-DefaultProfile</span></span>
<span data-ttu-id="48cbb-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="48cbb-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48cbb-127">-Id</span><span class="sxs-lookup"><span data-stu-id="48cbb-127">-Id</span></span>
<span data-ttu-id="48cbb-128">A parancsmag által leállítható feladat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="48cbb-128">Specifies the ID of the task that this cmdlet stops.</span></span>

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

### <span data-ttu-id="48cbb-129">-JobId</span><span class="sxs-lookup"><span data-stu-id="48cbb-129">-JobId</span></span>
<span data-ttu-id="48cbb-130">A tevékenységet tartalmazó feladat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="48cbb-130">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="48cbb-131">-Task</span><span class="sxs-lookup"><span data-stu-id="48cbb-131">-Task</span></span>
<span data-ttu-id="48cbb-132">A parancsmag által leállítható feladat.</span><span class="sxs-lookup"><span data-stu-id="48cbb-132">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="48cbb-133">**PSCloudTask-objektum** beszerzéséhez használja a Get-AzBatchTask parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="48cbb-133">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="48cbb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48cbb-134">CommonParameters</span></span>
<span data-ttu-id="48cbb-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48cbb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48cbb-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48cbb-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48cbb-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="48cbb-137">INPUTS</span></span>

### <span data-ttu-id="48cbb-138">System.String</span><span class="sxs-lookup"><span data-stu-id="48cbb-138">System.String</span></span>

### <span data-ttu-id="48cbb-139">Microsoft.Azure.Commands.Bat. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="48cbb-139">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="48cbb-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="48cbb-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="48cbb-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48cbb-141">OUTPUTS</span></span>

### <span data-ttu-id="48cbb-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="48cbb-142">System.Void</span></span>

## <span data-ttu-id="48cbb-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="48cbb-143">NOTES</span></span>

## <span data-ttu-id="48cbb-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48cbb-144">RELATED LINKS</span></span>

[<span data-ttu-id="48cbb-145">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="48cbb-145">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="48cbb-146">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="48cbb-146">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="48cbb-147">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="48cbb-147">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="48cbb-148">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="48cbb-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
