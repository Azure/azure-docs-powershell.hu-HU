---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
ms.openlocfilehash: ffaac0bdd4a144cc3979da052c0c40cb824862f4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025543"
---
# <span data-ttu-id="77bea-101">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="77bea-101">Stop-AzBatchJob</span></span>

## <span data-ttu-id="77bea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="77bea-102">SYNOPSIS</span></span>
<span data-ttu-id="77bea-103">Leállít egy kötegelt feladatot.</span><span class="sxs-lookup"><span data-stu-id="77bea-103">Stops a Batch job.</span></span>

## <span data-ttu-id="77bea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="77bea-104">SYNTAX</span></span>

```
Stop-AzBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77bea-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="77bea-105">DESCRIPTION</span></span>
<span data-ttu-id="77bea-106">A **stop-AzBatchJob** parancsmag leállítja az Azure kötegelt feladatot.</span><span class="sxs-lookup"><span data-stu-id="77bea-106">The **Stop-AzBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="77bea-107">Ez a parancs befejezettként jelöli meg a feladatot.</span><span class="sxs-lookup"><span data-stu-id="77bea-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="77bea-108">Példák</span><span class="sxs-lookup"><span data-stu-id="77bea-108">EXAMPLES</span></span>

### <span data-ttu-id="77bea-109">Példa 1: kötegelt feladat leállítása</span><span class="sxs-lookup"><span data-stu-id="77bea-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="77bea-110">Ez a parancs leállítja a 000001 AZONOSÍTÓJÚ munkát.</span><span class="sxs-lookup"><span data-stu-id="77bea-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="77bea-111">A parancs azt a lehetőséget adja meg, amely a feladat leállítását választotta.</span><span class="sxs-lookup"><span data-stu-id="77bea-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="77bea-112">A Get-AzBatchAccountKey parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="77bea-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="77bea-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="77bea-113">PARAMETERS</span></span>

### <span data-ttu-id="77bea-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="77bea-114">-BatchContext</span></span>
<span data-ttu-id="77bea-115">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="77bea-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="77bea-116">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="77bea-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="77bea-117">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="77bea-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="77bea-118">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="77bea-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="77bea-119">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="77bea-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="77bea-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77bea-120">-DefaultProfile</span></span>
<span data-ttu-id="77bea-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="77bea-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77bea-122">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="77bea-122">-Id</span></span>
<span data-ttu-id="77bea-123">Annak a projektnek az AZONOSÍTÓját adja meg, amelyre a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="77bea-123">Specifies the ID of the job that this cmdlet stops.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77bea-124">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="77bea-124">-TerminateReason</span></span>
<span data-ttu-id="77bea-125">Itt adhatja meg, hogy miért döntött a feladat leállítására.</span><span class="sxs-lookup"><span data-stu-id="77bea-125">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="77bea-126">Ez a parancsmag a következő szöveget tárolja a projekt **TerminateReason** tulajdonságával.</span><span class="sxs-lookup"><span data-stu-id="77bea-126">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77bea-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77bea-127">CommonParameters</span></span>
<span data-ttu-id="77bea-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="77bea-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77bea-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="77bea-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77bea-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="77bea-130">INPUTS</span></span>

### <span data-ttu-id="77bea-131">System. String</span><span class="sxs-lookup"><span data-stu-id="77bea-131">System.String</span></span>

### <span data-ttu-id="77bea-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="77bea-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="77bea-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="77bea-133">OUTPUTS</span></span>

### <span data-ttu-id="77bea-134">System. Void</span><span class="sxs-lookup"><span data-stu-id="77bea-134">System.Void</span></span>

## <span data-ttu-id="77bea-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="77bea-135">NOTES</span></span>

## <span data-ttu-id="77bea-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="77bea-136">RELATED LINKS</span></span>

[<span data-ttu-id="77bea-137">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="77bea-137">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="77bea-138">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="77bea-138">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="77bea-139">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="77bea-139">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="77bea-140">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="77bea-140">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="77bea-141">Új – AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="77bea-141">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="77bea-142">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="77bea-142">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="77bea-143">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="77bea-143">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
