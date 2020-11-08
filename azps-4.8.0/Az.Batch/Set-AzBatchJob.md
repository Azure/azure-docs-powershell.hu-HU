---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
ms.openlocfilehash: 1104eed4d60405226cdc6dad351ae418b84142e2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024887"
---
# <span data-ttu-id="22e89-101">Set-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="22e89-101">Set-AzBatchJob</span></span>

## <span data-ttu-id="22e89-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="22e89-102">SYNOPSIS</span></span>
<span data-ttu-id="22e89-103">Kötegelt feladatot frissít.</span><span class="sxs-lookup"><span data-stu-id="22e89-103">Updates a Batch job.</span></span>

## <span data-ttu-id="22e89-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="22e89-104">SYNTAX</span></span>

```
Set-AzBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22e89-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="22e89-105">DESCRIPTION</span></span>
<span data-ttu-id="22e89-106">A **set-AzBatchJob** parancsmag egy Azure-köteg-feladatot frissít.</span><span class="sxs-lookup"><span data-stu-id="22e89-106">The **Set-AzBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="22e89-107">A Get-AzBatchJob parancsmaggal **PSCloudJob** objektumot hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="22e89-107">Use the Get-AzBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="22e89-108">Módosítsa az objektum tulajdonságait, majd az aktuális parancsmag segítségével végezze el a módosításokat a köteg szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="22e89-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="22e89-109">Példák</span><span class="sxs-lookup"><span data-stu-id="22e89-109">EXAMPLES</span></span>

### <span data-ttu-id="22e89-110">Példa 1: feladat frissítése</span><span class="sxs-lookup"><span data-stu-id="22e89-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="22e89-111">Az első parancs a **Get-AzBatchJob** használatával kap munkát, majd a $Job változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="22e89-111">The first command gets a job by using **Get-AzBatchJob** , and then stores it in the $Job variable.</span></span>
<span data-ttu-id="22e89-112">A második parancs módosítja a $Job objektum prioritási specifikációját.</span><span class="sxs-lookup"><span data-stu-id="22e89-112">The second command modifies the priority specification on the $Job object.</span></span>
<span data-ttu-id="22e89-113">A végleges parancs frissíti a kötegfájlt a $Job helyi objektumának megfelelően.</span><span class="sxs-lookup"><span data-stu-id="22e89-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="22e89-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="22e89-114">PARAMETERS</span></span>

### <span data-ttu-id="22e89-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="22e89-115">-BatchContext</span></span>
<span data-ttu-id="22e89-116">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="22e89-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="22e89-117">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="22e89-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="22e89-118">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="22e89-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="22e89-119">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="22e89-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="22e89-120">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="22e89-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="22e89-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22e89-121">-DefaultProfile</span></span>
<span data-ttu-id="22e89-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="22e89-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22e89-123">-Job</span><span class="sxs-lookup"><span data-stu-id="22e89-123">-Job</span></span>
<span data-ttu-id="22e89-124">Itt adhatja meg azt a **PSCloudJob** , amelyre a parancsmag frissíti a köteg szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="22e89-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22e89-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22e89-125">CommonParameters</span></span>
<span data-ttu-id="22e89-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="22e89-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22e89-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="22e89-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22e89-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="22e89-128">INPUTS</span></span>

### <span data-ttu-id="22e89-129">Microsoft.Azure.Commands.BatCH. Modellek. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="22e89-129">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="22e89-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="22e89-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="22e89-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22e89-131">OUTPUTS</span></span>

### <span data-ttu-id="22e89-132">System. Void</span><span class="sxs-lookup"><span data-stu-id="22e89-132">System.Void</span></span>

## <span data-ttu-id="22e89-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="22e89-133">NOTES</span></span>

## <span data-ttu-id="22e89-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22e89-134">RELATED LINKS</span></span>

[<span data-ttu-id="22e89-135">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="22e89-135">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="22e89-136">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="22e89-136">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="22e89-137">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="22e89-137">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="22e89-138">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="22e89-138">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="22e89-139">Új – AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="22e89-139">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="22e89-140">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="22e89-140">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="22e89-141">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="22e89-141">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="22e89-142">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="22e89-142">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
