---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
ms.openlocfilehash: 5e26bd47c9c53b88442505aeb66d81a96c137b1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492007"
---
# <span data-ttu-id="89567-101">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="89567-101">Set-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="89567-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="89567-102">SYNOPSIS</span></span>
<span data-ttu-id="89567-103">Ütemtervet állít be.</span><span class="sxs-lookup"><span data-stu-id="89567-103">Sets a job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89567-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="89567-104">SYNTAX</span></span>

```
Set-AzureBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89567-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="89567-105">DESCRIPTION</span></span>
<span data-ttu-id="89567-106">A **set-AzureBatchJobSchedule** parancsmag az Azure kötegelt szolgáltatásban végez ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="89567-106">The **Set-AzureBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="89567-107">Példák</span><span class="sxs-lookup"><span data-stu-id="89567-107">EXAMPLES</span></span>

## <span data-ttu-id="89567-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="89567-108">PARAMETERS</span></span>

### <span data-ttu-id="89567-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="89567-109">-BatchContext</span></span>
<span data-ttu-id="89567-110">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="89567-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="89567-111">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="89567-111">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="89567-112">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="89567-112">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="89567-113">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="89567-113">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="89567-114">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="89567-114">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="89567-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89567-115">-DefaultProfile</span></span>
<span data-ttu-id="89567-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="89567-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89567-117">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="89567-117">-JobSchedule</span></span>
<span data-ttu-id="89567-118">Olyan **PSCloudJobSchedule** -objektumot ad meg, amely egy projekt ütemtervét képviseli.</span><span class="sxs-lookup"><span data-stu-id="89567-118">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="89567-119">**PSCloudJobSchedule** objektum beolvasásához használja az Get-AzureBatchJobSchedule parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="89567-119">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89567-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89567-120">CommonParameters</span></span>
<span data-ttu-id="89567-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="89567-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89567-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89567-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89567-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="89567-123">INPUTS</span></span>

### <span data-ttu-id="89567-124">Microsoft.Azure.Commands.BatCH. Modellek. PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="89567-124">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>
<span data-ttu-id="89567-125">Paraméterek: JobSchedule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="89567-125">Parameters: JobSchedule (ByValue)</span></span>

### <span data-ttu-id="89567-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="89567-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="89567-127">Paraméterek: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="89567-127">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="89567-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89567-128">OUTPUTS</span></span>

### <span data-ttu-id="89567-129">System. Void</span><span class="sxs-lookup"><span data-stu-id="89567-129">System.Void</span></span>

## <span data-ttu-id="89567-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="89567-130">NOTES</span></span>

## <span data-ttu-id="89567-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89567-131">RELATED LINKS</span></span>

[<span data-ttu-id="89567-132">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="89567-132">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="89567-133">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="89567-133">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="89567-134">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="89567-134">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="89567-135">Új – AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="89567-135">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="89567-136">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="89567-136">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="89567-137">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="89567-137">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


