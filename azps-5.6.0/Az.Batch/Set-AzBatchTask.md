---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: https://docs.microsoft.com/powershell/module/az.batch/set-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
ms.openlocfilehash: 80fc0c530904717561aa34ca98844fede75e747e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939705"
---
# <span data-ttu-id="27242-101">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="27242-101">Set-AzBatchTask</span></span>

## <span data-ttu-id="27242-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27242-102">SYNOPSIS</span></span>
<span data-ttu-id="27242-103">Frissíti egy feladat tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="27242-103">Updates the properties of a task.</span></span>

## <span data-ttu-id="27242-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="27242-104">SYNTAX</span></span>

```
Set-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27242-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="27242-105">DESCRIPTION</span></span>
<span data-ttu-id="27242-106">A **Set-AzBatchTask** parancsmag frissíti egy feladat tulajdonságait az Azure Batch szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="27242-106">The **Set-AzBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="27242-107">A Get-AzBatchTask parancsmagot használva szerezze be a **PSCloudTask-objektumot.**</span><span class="sxs-lookup"><span data-stu-id="27242-107">Use the Get-AzBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="27242-108">Módosítsa az objektum tulajdonságait, majd az aktuális parancsmagot használva végleges kövesse a módosításokat a Batch szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="27242-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="27242-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="27242-109">EXAMPLES</span></span>

### <span data-ttu-id="27242-110">1. példa: Tevékenység frissítése</span><span class="sxs-lookup"><span data-stu-id="27242-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="27242-111">Az első parancs a **Get-AzBatchTask** használatával kap feladatot, majd azt a $Task tárolja.</span><span class="sxs-lookup"><span data-stu-id="27242-111">The first command gets a task by using **Get-AzBatchTask**, and then stores it in the $Task variable.</span></span>
<span data-ttu-id="27242-112">A következő két parancs módosítja a tevékenység kényszerét a $Task.</span><span class="sxs-lookup"><span data-stu-id="27242-112">The next two commands modify the constraints of the task in $Task.</span></span>
<span data-ttu-id="27242-113">Az utolsó parancs frissíti a Batch szolgáltatást úgy, hogy megfeleljen a helyi objektumnak a $Task.</span><span class="sxs-lookup"><span data-stu-id="27242-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="27242-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27242-114">PARAMETERS</span></span>

### <span data-ttu-id="27242-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="27242-115">-BatchContext</span></span>
<span data-ttu-id="27242-116">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="27242-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="27242-117">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="27242-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="27242-118">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse le a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="27242-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="27242-119">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="27242-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="27242-120">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="27242-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="27242-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27242-121">-DefaultProfile</span></span>
<span data-ttu-id="27242-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="27242-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27242-123">-Task</span><span class="sxs-lookup"><span data-stu-id="27242-123">-Task</span></span>
<span data-ttu-id="27242-124">Azt a **PSCloudTaskot adja** meg, amelyhez ez a parancsmag frissíti a Batch szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="27242-124">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27242-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27242-125">CommonParameters</span></span>
<span data-ttu-id="27242-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27242-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27242-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27242-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27242-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="27242-128">INPUTS</span></span>

### <span data-ttu-id="27242-129">Microsoft.Azure.Commands.Bat. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="27242-129">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="27242-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="27242-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="27242-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27242-131">OUTPUTS</span></span>

### <span data-ttu-id="27242-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="27242-132">System.Void</span></span>

## <span data-ttu-id="27242-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="27242-133">NOTES</span></span>

## <span data-ttu-id="27242-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27242-134">RELATED LINKS</span></span>

[<span data-ttu-id="27242-135">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="27242-135">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="27242-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="27242-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="27242-137">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="27242-137">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="27242-138">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="27242-138">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="27242-139">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="27242-139">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="27242-140">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="27242-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
