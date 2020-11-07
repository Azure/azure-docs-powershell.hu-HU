---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
ms.openlocfilehash: 81ace9fd18b916f8f4788cf5878af1a620a61882
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679748"
---
# <span data-ttu-id="ad594-101">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="ad594-101">Enable-AzureBatchJob</span></span>

## <span data-ttu-id="ad594-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ad594-102">SYNOPSIS</span></span>
<span data-ttu-id="ad594-103">Lehetővé teszi a kötegelt feladatok végrehajtását.</span><span class="sxs-lookup"><span data-stu-id="ad594-103">Enables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad594-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ad594-104">SYNTAX</span></span>

```
Enable-AzureBatchJob [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad594-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ad594-105">DESCRIPTION</span></span>
<span data-ttu-id="ad594-106">Az **enable-AzureBatchJob** parancsmag lehetővé teszi az Azure-alapú kötegelt feladatok végrehajtását.</span><span class="sxs-lookup"><span data-stu-id="ad594-106">The **Enable-AzureBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="ad594-107">Miután engedélyezte a feladatot, az új feladatok futhatnak.</span><span class="sxs-lookup"><span data-stu-id="ad594-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="ad594-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ad594-108">EXAMPLES</span></span>

### <span data-ttu-id="ad594-109">1. példa: kötegelt feladat engedélyezése</span><span class="sxs-lookup"><span data-stu-id="ad594-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="ad594-110">Ez a parancs lehetővé teszi, hogy a 000001 AZONOSÍTÓJÚ feladat.</span><span class="sxs-lookup"><span data-stu-id="ad594-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="ad594-111">A Get-AzureRmBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="ad594-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="ad594-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ad594-112">PARAMETERS</span></span>

### <span data-ttu-id="ad594-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ad594-113">-BatchContext</span></span>
<span data-ttu-id="ad594-114">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="ad594-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ad594-115">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="ad594-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ad594-116">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="ad594-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ad594-117">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="ad594-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ad594-118">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="ad594-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ad594-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad594-119">-DefaultProfile</span></span>
<span data-ttu-id="ad594-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad594-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad594-121">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="ad594-121">-Id</span></span>
<span data-ttu-id="ad594-122">Annak a projektnek az AZONOSÍTÓját adja meg, amelyre ez a parancsmag engedélyezi.</span><span class="sxs-lookup"><span data-stu-id="ad594-122">Specifies the ID of the job that this cmdlet enables.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad594-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad594-123">CommonParameters</span></span>
<span data-ttu-id="ad594-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ad594-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad594-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad594-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad594-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad594-126">INPUTS</span></span>

### <span data-ttu-id="ad594-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ad594-127">BatchAccountContext</span></span>
<span data-ttu-id="ad594-128">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="ad594-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="ad594-129">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="ad594-129">String</span></span>
<span data-ttu-id="ad594-130">Az ' azonosító ' paraméter a pipeline "string" típusú értékét fogadja el.</span><span class="sxs-lookup"><span data-stu-id="ad594-130">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="ad594-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad594-131">OUTPUTS</span></span>

## <span data-ttu-id="ad594-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ad594-132">NOTES</span></span>

## <span data-ttu-id="ad594-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad594-133">RELATED LINKS</span></span>

[<span data-ttu-id="ad594-134">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="ad594-134">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="ad594-135">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="ad594-135">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="ad594-136">Új – AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="ad594-136">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="ad594-137">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="ad594-137">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="ad594-138">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="ad594-138">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="ad594-139">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="ad594-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


