---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
ms.openlocfilehash: 8b84028bc9da854b5aa749867a8759b71d9f7b63
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182595"
---
# <span data-ttu-id="f23a7-101">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="f23a7-101">Stop-AzBatchTask</span></span>

## <span data-ttu-id="f23a7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f23a7-102">SYNOPSIS</span></span>
<span data-ttu-id="f23a7-103">Leállít egy kötegelt feladatot.</span><span class="sxs-lookup"><span data-stu-id="f23a7-103">Stops a Batch task.</span></span>

## <span data-ttu-id="f23a7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f23a7-104">SYNTAX</span></span>

### <span data-ttu-id="f23a7-105">Azonosító</span><span class="sxs-lookup"><span data-stu-id="f23a7-105">Id</span></span>
```
Stop-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f23a7-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f23a7-106">InputObject</span></span>
```
Stop-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f23a7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f23a7-107">DESCRIPTION</span></span>
<span data-ttu-id="f23a7-108">A **stop-AzBatchTask** parancsmag egy Azure-köteg-feladatot leáll.</span><span class="sxs-lookup"><span data-stu-id="f23a7-108">The **Stop-AzBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="f23a7-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f23a7-109">EXAMPLES</span></span>

### <span data-ttu-id="f23a7-110">1. példa: egy köteg tevékenységének törlése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="f23a7-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="f23a7-111">Ez a parancs leállítja azt a feladatot, amely a Task23 AZONOSÍTÓval rendelkezik a 000001 azonosítójú projektben.</span><span class="sxs-lookup"><span data-stu-id="f23a7-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="f23a7-112">A parancs a megerősítést kéri.</span><span class="sxs-lookup"><span data-stu-id="f23a7-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="f23a7-113">A Get-AzBatchAccountKey parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="f23a7-113">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="f23a7-114">2. példa: a kötegelt feladat leállítása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="f23a7-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="f23a7-115">Ez a parancs azt a kötegelt feladatot kapja meg, amely a Task26 azonosító 000001 tartalmazó projekt azonosítóját tartalmazza a Get-AzBatchTask parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="f23a7-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="f23a7-116">A parancs a tevékenységet a pipeline operátorral továbbítja az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="f23a7-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f23a7-117">A parancs leállítja a feladatot.</span><span class="sxs-lookup"><span data-stu-id="f23a7-117">The command stops that task.</span></span>

## <span data-ttu-id="f23a7-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f23a7-118">PARAMETERS</span></span>

### <span data-ttu-id="f23a7-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f23a7-119">-BatchContext</span></span>
<span data-ttu-id="f23a7-120">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="f23a7-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f23a7-121">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="f23a7-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f23a7-122">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="f23a7-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f23a7-123">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="f23a7-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f23a7-124">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="f23a7-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f23a7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f23a7-125">-DefaultProfile</span></span>
<span data-ttu-id="f23a7-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f23a7-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f23a7-127">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="f23a7-127">-Id</span></span>
<span data-ttu-id="f23a7-128">Annak a tevékenységnek az AZONOSÍTÓját adja meg, amelyre a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="f23a7-128">Specifies the ID of the task that this cmdlet stops.</span></span>

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

### <span data-ttu-id="f23a7-129">-JobId</span><span class="sxs-lookup"><span data-stu-id="f23a7-129">-JobId</span></span>
<span data-ttu-id="f23a7-130">A tevékenységet tartalmazó feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f23a7-130">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="f23a7-131">-Tevékenység</span><span class="sxs-lookup"><span data-stu-id="f23a7-131">-Task</span></span>
<span data-ttu-id="f23a7-132">Azt a feladatot adja meg, amelyre a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="f23a7-132">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="f23a7-133">**PSCloudTask** objektum beolvasásához használja az Get-AzBatchTask parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f23a7-133">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="f23a7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f23a7-134">CommonParameters</span></span>
<span data-ttu-id="f23a7-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f23a7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f23a7-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f23a7-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f23a7-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f23a7-137">INPUTS</span></span>

### <span data-ttu-id="f23a7-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f23a7-138">System.String</span></span>

### <span data-ttu-id="f23a7-139">Microsoft.Azure.Commands.BatCH. Modellek. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="f23a7-139">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="f23a7-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f23a7-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f23a7-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f23a7-141">OUTPUTS</span></span>

### <span data-ttu-id="f23a7-142">System. Void</span><span class="sxs-lookup"><span data-stu-id="f23a7-142">System.Void</span></span>

## <span data-ttu-id="f23a7-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f23a7-143">NOTES</span></span>

## <span data-ttu-id="f23a7-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f23a7-144">RELATED LINKS</span></span>

[<span data-ttu-id="f23a7-145">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="f23a7-145">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="f23a7-146">Új – AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="f23a7-146">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="f23a7-147">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="f23a7-147">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="f23a7-148">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f23a7-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
