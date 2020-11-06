---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
ms.openlocfilehash: 85e47b9f9bea7a19bb11817c414e5d3b9a35d6a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501476"
---
# <span data-ttu-id="7f036-101">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7f036-101">Set-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="7f036-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7f036-102">SYNOPSIS</span></span>
<span data-ttu-id="7f036-103">Ütemtervet állít be.</span><span class="sxs-lookup"><span data-stu-id="7f036-103">Sets a job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f036-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7f036-104">SYNTAX</span></span>

```
Set-AzureBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f036-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7f036-105">DESCRIPTION</span></span>
<span data-ttu-id="7f036-106">A **set-AzureBatchJobSchedule** parancsmag az Azure kötegelt szolgáltatásban végez ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="7f036-106">The **Set-AzureBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="7f036-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7f036-107">EXAMPLES</span></span>

## <span data-ttu-id="7f036-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7f036-108">PARAMETERS</span></span>

### <span data-ttu-id="7f036-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7f036-109">-BatchContext</span></span>
<span data-ttu-id="7f036-110">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="7f036-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7f036-111">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="7f036-111">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7f036-112">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="7f036-112">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7f036-113">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="7f036-113">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7f036-114">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="7f036-114">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="7f036-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f036-115">-DefaultProfile</span></span>
<span data-ttu-id="7f036-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7f036-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f036-117">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="7f036-117">-JobSchedule</span></span>
<span data-ttu-id="7f036-118">Olyan **PSCloudJobSchedule** -objektumot ad meg, amely egy projekt ütemtervét képviseli.</span><span class="sxs-lookup"><span data-stu-id="7f036-118">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="7f036-119">**PSCloudJobSchedule** objektum beolvasásához használja az Get-AzureBatchJobSchedule parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7f036-119">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

```yaml
Type: PSCloudJobSchedule
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f036-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f036-120">CommonParameters</span></span>
<span data-ttu-id="7f036-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7f036-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f036-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f036-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f036-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f036-123">INPUTS</span></span>

### <span data-ttu-id="7f036-124">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7f036-124">BatchAccountContext</span></span>
<span data-ttu-id="7f036-125">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="7f036-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="7f036-126">PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7f036-126">PSCloudJobSchedule</span></span>
<span data-ttu-id="7f036-127">A ' JobSchedule ' paraméter az "PSCloudJobSchedule" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="7f036-127">Parameter 'JobSchedule' accepts value of type 'PSCloudJobSchedule' from the pipeline</span></span>

## <span data-ttu-id="7f036-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f036-128">OUTPUTS</span></span>

## <span data-ttu-id="7f036-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7f036-129">NOTES</span></span>

## <span data-ttu-id="7f036-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7f036-130">RELATED LINKS</span></span>

[<span data-ttu-id="7f036-131">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7f036-131">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="7f036-132">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7f036-132">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="7f036-133">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7f036-133">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="7f036-134">Új – AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7f036-134">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="7f036-135">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7f036-135">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="7f036-136">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7f036-136">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


