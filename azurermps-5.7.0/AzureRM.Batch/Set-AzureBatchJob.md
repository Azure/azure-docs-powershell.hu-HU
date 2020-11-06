---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
ms.openlocfilehash: a878002c509fd2a895f61a97af1bef2afebc3691
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503072"
---
# <span data-ttu-id="b2b4c-101">Set-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b2b4c-101">Set-AzureBatchJob</span></span>

## <span data-ttu-id="b2b4c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b2b4c-102">SYNOPSIS</span></span>
<span data-ttu-id="b2b4c-103">Kötegelt feladatot frissít.</span><span class="sxs-lookup"><span data-stu-id="b2b4c-103">Updates a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2b4c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b2b4c-104">SYNTAX</span></span>

```
Set-AzureBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2b4c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b2b4c-105">DESCRIPTION</span></span>
<span data-ttu-id="b2b4c-106">A **set-AzureBatchJob** parancsmag egy Azure-köteg-feladatot frissít.</span><span class="sxs-lookup"><span data-stu-id="b2b4c-106">The **Set-AzureBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="b2b4c-107">A Get-AzureBatchJob parancsmaggal **PSCloudJob** objektumot hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="b2b4c-107">Use the Get-AzureBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="b2b4c-108">Módosítsa az objektum tulajdonságait, majd az aktuális parancsmag segítségével végezze el a módosításokat a köteg szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="b2b4c-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="b2b4c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b2b4c-109">EXAMPLES</span></span>

### <span data-ttu-id="b2b4c-110">Példa 1: feladat frissítése</span><span class="sxs-lookup"><span data-stu-id="b2b4c-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzureBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzureBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="b2b4c-111">Az első parancs beolvassa a készletet a **Get-AzureBatchJob** függvénnyel, majd a $Job változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b2b4c-111">The first command gets a pool by using **Get-AzureBatchJob** , and then stores it in the $Job variable.</span></span>

<span data-ttu-id="b2b4c-112">A második parancs módosítja a $Job objektum prioritási specifikációját.</span><span class="sxs-lookup"><span data-stu-id="b2b4c-112">The second command modifies the priority specification on the $Job object.</span></span>

<span data-ttu-id="b2b4c-113">A végleges parancs frissíti a kötegfájlt a $Job helyi objektumának megfelelően.</span><span class="sxs-lookup"><span data-stu-id="b2b4c-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="b2b4c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b2b4c-114">PARAMETERS</span></span>

### <span data-ttu-id="b2b4c-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b2b4c-115">-BatchContext</span></span>
<span data-ttu-id="b2b4c-116">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="b2b4c-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b2b4c-117">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="b2b4c-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b2b4c-118">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="b2b4c-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b2b4c-119">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="b2b4c-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b2b4c-120">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="b2b4c-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b2b4c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2b4c-121">-DefaultProfile</span></span>
<span data-ttu-id="b2b4c-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b2b4c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2b4c-123">-Job</span><span class="sxs-lookup"><span data-stu-id="b2b4c-123">-Job</span></span>
<span data-ttu-id="b2b4c-124">Itt adhatja meg azt a **PSCloudJob** , amelyre a parancsmag frissíti a köteg szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="b2b4c-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: PSCloudJob
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2b4c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2b4c-125">CommonParameters</span></span>
<span data-ttu-id="b2b4c-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b2b4c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2b4c-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2b4c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2b4c-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2b4c-128">INPUTS</span></span>

### <span data-ttu-id="b2b4c-129">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b2b4c-129">BatchAccountContext</span></span>
<span data-ttu-id="b2b4c-130">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b2b4c-130">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="b2b4c-131">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="b2b4c-131">PSCloudJob</span></span>
<span data-ttu-id="b2b4c-132">A ' Job ' paraméter elfogadja a "PSCloudJob" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b2b4c-132">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="b2b4c-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2b4c-133">OUTPUTS</span></span>

## <span data-ttu-id="b2b4c-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b2b4c-134">NOTES</span></span>

## <span data-ttu-id="b2b4c-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b2b4c-135">RELATED LINKS</span></span>

[<span data-ttu-id="b2b4c-136">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b2b4c-136">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="b2b4c-137">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b2b4c-137">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="b2b4c-138">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b2b4c-138">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="b2b4c-139">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b2b4c-139">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="b2b4c-140">Új – AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b2b4c-140">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="b2b4c-141">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b2b4c-141">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="b2b4c-142">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b2b4c-142">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="b2b4c-143">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="b2b4c-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


