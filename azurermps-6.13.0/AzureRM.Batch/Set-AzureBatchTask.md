---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
ms.openlocfilehash: bae5f2b075f8d4f2fa579b38bdccf160cd46caad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672122"
---
# <span data-ttu-id="6b9aa-101">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="6b9aa-101">Set-AzureBatchTask</span></span>

## <span data-ttu-id="6b9aa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6b9aa-102">SYNOPSIS</span></span>
<span data-ttu-id="6b9aa-103">Frissíti a tevékenység tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="6b9aa-103">Updates the properties of a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b9aa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6b9aa-104">SYNTAX</span></span>

```
Set-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b9aa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6b9aa-105">DESCRIPTION</span></span>
<span data-ttu-id="6b9aa-106">A **set-AzureBatchTask** parancsmag frissíti egy tevékenység tulajdonságait az Azure kötegfájl-szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="6b9aa-106">The **Set-AzureBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="6b9aa-107">A Get-AzureBatchTask parancsmaggal **PSCloudTask** objektumot hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="6b9aa-107">Use the Get-AzureBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="6b9aa-108">Módosítsa az objektum tulajdonságait, majd az aktuális parancsmag segítségével végezze el a módosításokat a köteg szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="6b9aa-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="6b9aa-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6b9aa-109">EXAMPLES</span></span>

### <span data-ttu-id="6b9aa-110">Példa 1: tevékenység frissítése</span><span class="sxs-lookup"><span data-stu-id="6b9aa-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzureBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzureBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="6b9aa-111">Az első parancs **beolvassa a feladatot a Get-AzureBatchTask** függvénnyel, majd a $Task változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="6b9aa-111">The first command gets a task by using **Get-AzureBatchTask** , and then stores it in the $Task variable.</span></span>
<span data-ttu-id="6b9aa-112">A következő két parancs módosítja a tevékenység korlátozásait a $Taskban.</span><span class="sxs-lookup"><span data-stu-id="6b9aa-112">The next two commands modify the constraints of the task in $Task.</span></span>
<span data-ttu-id="6b9aa-113">A végleges parancs frissíti a kötegfájlt a $Task helyi objektumának megfelelően.</span><span class="sxs-lookup"><span data-stu-id="6b9aa-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="6b9aa-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6b9aa-114">PARAMETERS</span></span>

### <span data-ttu-id="6b9aa-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6b9aa-115">-BatchContext</span></span>
<span data-ttu-id="6b9aa-116">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="6b9aa-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6b9aa-117">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="6b9aa-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6b9aa-118">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="6b9aa-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6b9aa-119">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="6b9aa-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6b9aa-120">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="6b9aa-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6b9aa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b9aa-121">-DefaultProfile</span></span>
<span data-ttu-id="6b9aa-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b9aa-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b9aa-123">-Tevékenység</span><span class="sxs-lookup"><span data-stu-id="6b9aa-123">-Task</span></span>
<span data-ttu-id="6b9aa-124">Azt a **PSCloudTask** adja meg, amelyre a parancsmag frissíti a köteg szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="6b9aa-124">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="6b9aa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b9aa-125">CommonParameters</span></span>
<span data-ttu-id="6b9aa-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6b9aa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b9aa-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b9aa-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b9aa-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b9aa-128">INPUTS</span></span>

### <span data-ttu-id="6b9aa-129">Microsoft.Azure.Commands.BatCH. Modellek. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="6b9aa-129">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>
<span data-ttu-id="6b9aa-130">Paraméterek: tevékenység (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6b9aa-130">Parameters: Task (ByValue)</span></span>

### <span data-ttu-id="6b9aa-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6b9aa-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="6b9aa-132">Paraméterek: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6b9aa-132">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="6b9aa-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b9aa-133">OUTPUTS</span></span>

### <span data-ttu-id="6b9aa-134">System. Void</span><span class="sxs-lookup"><span data-stu-id="6b9aa-134">System.Void</span></span>

## <span data-ttu-id="6b9aa-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6b9aa-135">NOTES</span></span>

## <span data-ttu-id="6b9aa-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b9aa-136">RELATED LINKS</span></span>

[<span data-ttu-id="6b9aa-137">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="6b9aa-137">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="6b9aa-138">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6b9aa-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="6b9aa-139">Új – AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="6b9aa-139">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="6b9aa-140">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="6b9aa-140">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="6b9aa-141">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="6b9aa-141">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="6b9aa-142">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="6b9aa-142">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


