---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
ms.openlocfilehash: 3baaa7296ab0fdd2c1dcab606b2896b11e5773f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492860"
---
# <span data-ttu-id="43c75-101">Set-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="43c75-101">Set-AzureBatchJob</span></span>

## <span data-ttu-id="43c75-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="43c75-102">SYNOPSIS</span></span>
<span data-ttu-id="43c75-103">Kötegelt feladatot frissít.</span><span class="sxs-lookup"><span data-stu-id="43c75-103">Updates a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43c75-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="43c75-104">SYNTAX</span></span>

```
Set-AzureBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43c75-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="43c75-105">DESCRIPTION</span></span>
<span data-ttu-id="43c75-106">A **set-AzureBatchJob** parancsmag egy Azure-köteg-feladatot frissít.</span><span class="sxs-lookup"><span data-stu-id="43c75-106">The **Set-AzureBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="43c75-107">A Get-AzureBatchJob parancsmaggal **PSCloudJob** objektumot hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="43c75-107">Use the Get-AzureBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="43c75-108">Módosítsa az objektum tulajdonságait, majd az aktuális parancsmag segítségével végezze el a módosításokat a köteg szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="43c75-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="43c75-109">Példák</span><span class="sxs-lookup"><span data-stu-id="43c75-109">EXAMPLES</span></span>

### <span data-ttu-id="43c75-110">Példa 1: feladat frissítése</span><span class="sxs-lookup"><span data-stu-id="43c75-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzureBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzureBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="43c75-111">Az első parancs beolvassa a készletet a **Get-AzureBatchJob** függvénnyel, majd a $Job változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="43c75-111">The first command gets a pool by using **Get-AzureBatchJob** , and then stores it in the $Job variable.</span></span>
<span data-ttu-id="43c75-112">A második parancs módosítja a $Job objektum prioritási specifikációját.</span><span class="sxs-lookup"><span data-stu-id="43c75-112">The second command modifies the priority specification on the $Job object.</span></span>
<span data-ttu-id="43c75-113">A végleges parancs frissíti a kötegfájlt a $Job helyi objektumának megfelelően.</span><span class="sxs-lookup"><span data-stu-id="43c75-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="43c75-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="43c75-114">PARAMETERS</span></span>

### <span data-ttu-id="43c75-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="43c75-115">-BatchContext</span></span>
<span data-ttu-id="43c75-116">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="43c75-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="43c75-117">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="43c75-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="43c75-118">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="43c75-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="43c75-119">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="43c75-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="43c75-120">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="43c75-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="43c75-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43c75-121">-DefaultProfile</span></span>
<span data-ttu-id="43c75-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="43c75-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43c75-123">-Job</span><span class="sxs-lookup"><span data-stu-id="43c75-123">-Job</span></span>
<span data-ttu-id="43c75-124">Itt adhatja meg azt a **PSCloudJob** , amelyre a parancsmag frissíti a köteg szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="43c75-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="43c75-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43c75-125">CommonParameters</span></span>
<span data-ttu-id="43c75-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="43c75-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43c75-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43c75-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43c75-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="43c75-128">INPUTS</span></span>

### <span data-ttu-id="43c75-129">Microsoft.Azure.Commands.BatCH. Modellek. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="43c75-129">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>
<span data-ttu-id="43c75-130">Paraméterek: Job (ByValue)</span><span class="sxs-lookup"><span data-stu-id="43c75-130">Parameters: Job (ByValue)</span></span>

### <span data-ttu-id="43c75-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="43c75-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="43c75-132">Paraméterek: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="43c75-132">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="43c75-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43c75-133">OUTPUTS</span></span>

### <span data-ttu-id="43c75-134">System. Void</span><span class="sxs-lookup"><span data-stu-id="43c75-134">System.Void</span></span>

## <span data-ttu-id="43c75-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="43c75-135">NOTES</span></span>

## <span data-ttu-id="43c75-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43c75-136">RELATED LINKS</span></span>

[<span data-ttu-id="43c75-137">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="43c75-137">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="43c75-138">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="43c75-138">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="43c75-139">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="43c75-139">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="43c75-140">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="43c75-140">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="43c75-141">Új – AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="43c75-141">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="43c75-142">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="43c75-142">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="43c75-143">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="43c75-143">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="43c75-144">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="43c75-144">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


