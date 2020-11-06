---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
ms.openlocfilehash: 6e6bb12aeb5b5d319b0997578991c87e91c81003
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496648"
---
# <span data-ttu-id="e6e30-101">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="e6e30-101">Set-AzureBatchTask</span></span>

## <span data-ttu-id="e6e30-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e6e30-102">SYNOPSIS</span></span>
<span data-ttu-id="e6e30-103">Frissíti a tevékenység tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="e6e30-103">Updates the properties of a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6e30-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e6e30-104">SYNTAX</span></span>

```
Set-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6e30-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e6e30-105">DESCRIPTION</span></span>
<span data-ttu-id="e6e30-106">A **set-AzureBatchTask** parancsmag frissíti egy tevékenység tulajdonságait az Azure kötegfájl-szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="e6e30-106">The **Set-AzureBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="e6e30-107">A Get-AzureBatchTask parancsmaggal **PSCloudTask** objektumot hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="e6e30-107">Use the Get-AzureBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="e6e30-108">Módosítsa az objektum tulajdonságait, majd az aktuális parancsmag segítségével végezze el a módosításokat a köteg szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="e6e30-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="e6e30-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e6e30-109">EXAMPLES</span></span>

### <span data-ttu-id="e6e30-110">Példa 1: tevékenység frissítése</span><span class="sxs-lookup"><span data-stu-id="e6e30-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzureBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzureBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="e6e30-111">Az első parancs **beolvassa a feladatot a Get-AzureBatchTask** függvénnyel, majd a $Task változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e6e30-111">The first command gets a task by using **Get-AzureBatchTask** , and then stores it in the $Task variable.</span></span>

<span data-ttu-id="e6e30-112">A következő két parancs módosítja a tevékenység korlátozásait a $Taskban.</span><span class="sxs-lookup"><span data-stu-id="e6e30-112">The next two commands modify the constraints of the task in $Task.</span></span>

<span data-ttu-id="e6e30-113">A végleges parancs frissíti a kötegfájlt a $Task helyi objektumának megfelelően.</span><span class="sxs-lookup"><span data-stu-id="e6e30-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="e6e30-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e6e30-114">PARAMETERS</span></span>

### <span data-ttu-id="e6e30-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e6e30-115">-BatchContext</span></span>
<span data-ttu-id="e6e30-116">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="e6e30-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e6e30-117">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="e6e30-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e6e30-118">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="e6e30-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e6e30-119">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="e6e30-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e6e30-120">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="e6e30-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e6e30-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6e30-121">-DefaultProfile</span></span>
<span data-ttu-id="e6e30-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6e30-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6e30-123">-Tevékenység</span><span class="sxs-lookup"><span data-stu-id="e6e30-123">-Task</span></span>
<span data-ttu-id="e6e30-124">Azt a **PSCloudTask** adja meg, amelyre a parancsmag frissíti a köteg szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="e6e30-124">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: PSCloudTask
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6e30-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6e30-125">CommonParameters</span></span>
<span data-ttu-id="e6e30-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e6e30-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6e30-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6e30-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6e30-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6e30-128">INPUTS</span></span>

### <span data-ttu-id="e6e30-129">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e6e30-129">BatchAccountContext</span></span>
<span data-ttu-id="e6e30-130">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="e6e30-130">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="e6e30-131">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="e6e30-131">PSCloudTask</span></span>
<span data-ttu-id="e6e30-132">A "tevékenység" paraméter elfogadja a "PSCloudTask" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="e6e30-132">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="e6e30-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6e30-133">OUTPUTS</span></span>

## <span data-ttu-id="e6e30-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e6e30-134">NOTES</span></span>

## <span data-ttu-id="e6e30-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6e30-135">RELATED LINKS</span></span>

[<span data-ttu-id="e6e30-136">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="e6e30-136">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="e6e30-137">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e6e30-137">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="e6e30-138">Új – AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="e6e30-138">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="e6e30-139">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="e6e30-139">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="e6e30-140">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="e6e30-140">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="e6e30-141">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="e6e30-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


