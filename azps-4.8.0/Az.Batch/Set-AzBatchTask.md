---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
ms.openlocfilehash: 7c3e976e85e6754702f8288f5bb257086837fc36
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024874"
---
# <span data-ttu-id="8b0cc-101">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="8b0cc-101">Set-AzBatchTask</span></span>

## <span data-ttu-id="8b0cc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8b0cc-102">SYNOPSIS</span></span>
<span data-ttu-id="8b0cc-103">Frissíti a tevékenység tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="8b0cc-103">Updates the properties of a task.</span></span>

## <span data-ttu-id="8b0cc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8b0cc-104">SYNTAX</span></span>

```
Set-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b0cc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8b0cc-105">DESCRIPTION</span></span>
<span data-ttu-id="8b0cc-106">A **set-AzBatchTask** parancsmag frissíti egy tevékenység tulajdonságait az Azure kötegfájl-szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="8b0cc-106">The **Set-AzBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="8b0cc-107">A Get-AzBatchTask parancsmaggal **PSCloudTask** objektumot hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="8b0cc-107">Use the Get-AzBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="8b0cc-108">Módosítsa az objektum tulajdonságait, majd az aktuális parancsmag segítségével végezze el a módosításokat a köteg szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="8b0cc-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="8b0cc-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8b0cc-109">EXAMPLES</span></span>

### <span data-ttu-id="8b0cc-110">Példa 1: tevékenység frissítése</span><span class="sxs-lookup"><span data-stu-id="8b0cc-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="8b0cc-111">Az első parancs **beolvassa a feladatot a Get-AzBatchTask** függvénnyel, majd a $Task változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="8b0cc-111">The first command gets a task by using **Get-AzBatchTask** , and then stores it in the $Task variable.</span></span>
<span data-ttu-id="8b0cc-112">A következő két parancs módosítja a tevékenység korlátozásait a $Taskban.</span><span class="sxs-lookup"><span data-stu-id="8b0cc-112">The next two commands modify the constraints of the task in $Task.</span></span>
<span data-ttu-id="8b0cc-113">A végleges parancs frissíti a kötegfájlt a $Task helyi objektumának megfelelően.</span><span class="sxs-lookup"><span data-stu-id="8b0cc-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="8b0cc-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8b0cc-114">PARAMETERS</span></span>

### <span data-ttu-id="8b0cc-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8b0cc-115">-BatchContext</span></span>
<span data-ttu-id="8b0cc-116">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="8b0cc-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8b0cc-117">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="8b0cc-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8b0cc-118">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="8b0cc-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8b0cc-119">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="8b0cc-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8b0cc-120">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="8b0cc-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8b0cc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b0cc-121">-DefaultProfile</span></span>
<span data-ttu-id="8b0cc-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8b0cc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b0cc-123">-Tevékenység</span><span class="sxs-lookup"><span data-stu-id="8b0cc-123">-Task</span></span>
<span data-ttu-id="8b0cc-124">Azt a **PSCloudTask** adja meg, amelyre a parancsmag frissíti a köteg szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="8b0cc-124">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="8b0cc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b0cc-125">CommonParameters</span></span>
<span data-ttu-id="8b0cc-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8b0cc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b0cc-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8b0cc-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b0cc-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b0cc-128">INPUTS</span></span>

### <span data-ttu-id="8b0cc-129">Microsoft.Azure.Commands.BatCH. Modellek. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="8b0cc-129">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="8b0cc-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8b0cc-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8b0cc-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b0cc-131">OUTPUTS</span></span>

### <span data-ttu-id="8b0cc-132">System. Void</span><span class="sxs-lookup"><span data-stu-id="8b0cc-132">System.Void</span></span>

## <span data-ttu-id="8b0cc-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8b0cc-133">NOTES</span></span>

## <span data-ttu-id="8b0cc-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8b0cc-134">RELATED LINKS</span></span>

[<span data-ttu-id="8b0cc-135">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="8b0cc-135">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="8b0cc-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="8b0cc-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="8b0cc-137">Új – AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="8b0cc-137">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="8b0cc-138">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="8b0cc-138">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="8b0cc-139">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="8b0cc-139">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="8b0cc-140">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="8b0cc-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
