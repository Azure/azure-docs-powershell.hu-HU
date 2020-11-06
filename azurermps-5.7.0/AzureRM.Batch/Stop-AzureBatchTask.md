---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
ms.openlocfilehash: 979c136f1bdbd216cebe367060ebdc5d8360ea24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493247"
---
# <span data-ttu-id="01a36-101">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="01a36-101">Stop-AzureBatchTask</span></span>

## <span data-ttu-id="01a36-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="01a36-102">SYNOPSIS</span></span>
<span data-ttu-id="01a36-103">Leállít egy kötegelt feladatot.</span><span class="sxs-lookup"><span data-stu-id="01a36-103">Stops a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01a36-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="01a36-104">SYNTAX</span></span>

### <span data-ttu-id="01a36-105">Azonosító</span><span class="sxs-lookup"><span data-stu-id="01a36-105">Id</span></span>
```
Stop-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01a36-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="01a36-106">InputObject</span></span>
```
Stop-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01a36-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="01a36-107">DESCRIPTION</span></span>
<span data-ttu-id="01a36-108">A **stop-AzureBatchTask** parancsmag egy Azure-köteg-feladatot leáll.</span><span class="sxs-lookup"><span data-stu-id="01a36-108">The **Stop-AzureBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="01a36-109">Példák</span><span class="sxs-lookup"><span data-stu-id="01a36-109">EXAMPLES</span></span>

### <span data-ttu-id="01a36-110">1. példa: egy köteg tevékenységének törlése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="01a36-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="01a36-111">Ez a parancs leállítja azt a feladatot, amely a Task23 AZONOSÍTÓval rendelkezik a 000001 azonosítójú projektben.</span><span class="sxs-lookup"><span data-stu-id="01a36-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="01a36-112">A parancs a megerősítést kéri.</span><span class="sxs-lookup"><span data-stu-id="01a36-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="01a36-113">A Get-AzureRmBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="01a36-113">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="01a36-114">2. példa: a kötegelt feladat leállítása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="01a36-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="01a36-115">Ez a parancs azt a kötegelt feladatot kapja meg, amely a Task26 azonosító 000001 tartalmazó projekt azonosítóját tartalmazza a Get-AzureBatchTask parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="01a36-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="01a36-116">A parancs a tevékenységet a pipeline operátorral továbbítja az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="01a36-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="01a36-117">A parancs leállítja a feladatot.</span><span class="sxs-lookup"><span data-stu-id="01a36-117">The command stops that task.</span></span>

## <span data-ttu-id="01a36-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="01a36-118">PARAMETERS</span></span>

### <span data-ttu-id="01a36-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="01a36-119">-BatchContext</span></span>
<span data-ttu-id="01a36-120">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="01a36-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="01a36-121">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="01a36-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="01a36-122">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="01a36-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="01a36-123">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="01a36-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="01a36-124">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="01a36-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="01a36-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01a36-125">-DefaultProfile</span></span>
<span data-ttu-id="01a36-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="01a36-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01a36-127">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="01a36-127">-Id</span></span>
<span data-ttu-id="01a36-128">Annak a tevékenységnek az AZONOSÍTÓját adja meg, amelyre a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="01a36-128">Specifies the ID of the task that this cmdlet stops.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a36-129">-JobId</span><span class="sxs-lookup"><span data-stu-id="01a36-129">-JobId</span></span>
<span data-ttu-id="01a36-130">A tevékenységet tartalmazó feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="01a36-130">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a36-131">-Tevékenység</span><span class="sxs-lookup"><span data-stu-id="01a36-131">-Task</span></span>
<span data-ttu-id="01a36-132">Azt a feladatot adja meg, amelyre a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="01a36-132">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="01a36-133">**PSCloudTask** objektum beolvasásához használja az Get-AzureBatchTask parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="01a36-133">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: PSCloudTask
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01a36-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01a36-134">CommonParameters</span></span>
<span data-ttu-id="01a36-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="01a36-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01a36-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01a36-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01a36-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="01a36-137">INPUTS</span></span>

### <span data-ttu-id="01a36-138">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="01a36-138">BatchAccountContext</span></span>
<span data-ttu-id="01a36-139">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="01a36-139">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="01a36-140">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="01a36-140">PSCloudTask</span></span>
<span data-ttu-id="01a36-141">A "tevékenység" paraméter elfogadja a "PSCloudTask" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="01a36-141">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="01a36-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01a36-142">OUTPUTS</span></span>

## <span data-ttu-id="01a36-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="01a36-143">NOTES</span></span>

## <span data-ttu-id="01a36-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01a36-144">RELATED LINKS</span></span>

[<span data-ttu-id="01a36-145">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="01a36-145">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="01a36-146">Új – AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="01a36-146">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="01a36-147">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="01a36-147">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="01a36-148">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="01a36-148">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


