---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
ms.openlocfilehash: 665d7b64f3e8d83dd45ebc8de0cc36da960f8c35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680615"
---
# <span data-ttu-id="84f53-101">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="84f53-101">Enable-AzureBatchJob</span></span>

## <span data-ttu-id="84f53-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="84f53-102">SYNOPSIS</span></span>
<span data-ttu-id="84f53-103">Lehetővé teszi a kötegelt feladatok végrehajtását.</span><span class="sxs-lookup"><span data-stu-id="84f53-103">Enables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84f53-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="84f53-104">SYNTAX</span></span>

```
Enable-AzureBatchJob [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84f53-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="84f53-105">DESCRIPTION</span></span>
<span data-ttu-id="84f53-106">Az **enable-AzureBatchJob** parancsmag lehetővé teszi az Azure-alapú kötegelt feladatok végrehajtását.</span><span class="sxs-lookup"><span data-stu-id="84f53-106">The **Enable-AzureBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="84f53-107">Miután engedélyezte a feladatot, az új feladatok futhatnak.</span><span class="sxs-lookup"><span data-stu-id="84f53-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="84f53-108">Példák</span><span class="sxs-lookup"><span data-stu-id="84f53-108">EXAMPLES</span></span>

### <span data-ttu-id="84f53-109">1. példa: kötegelt feladat engedélyezése</span><span class="sxs-lookup"><span data-stu-id="84f53-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="84f53-110">Ez a parancs lehetővé teszi, hogy a 000001 AZONOSÍTÓJÚ feladat.</span><span class="sxs-lookup"><span data-stu-id="84f53-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="84f53-111">A Get-AzureRmBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="84f53-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="84f53-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="84f53-112">PARAMETERS</span></span>

### <span data-ttu-id="84f53-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="84f53-113">-BatchContext</span></span>
<span data-ttu-id="84f53-114">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="84f53-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="84f53-115">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="84f53-115">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="84f53-116">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="84f53-116">-Id</span></span>
<span data-ttu-id="84f53-117">Annak a projektnek az AZONOSÍTÓját adja meg, amelyre ez a parancsmag engedélyezi.</span><span class="sxs-lookup"><span data-stu-id="84f53-117">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="84f53-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84f53-118">-DefaultProfile</span></span>
<span data-ttu-id="84f53-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="84f53-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84f53-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84f53-120">CommonParameters</span></span>
<span data-ttu-id="84f53-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="84f53-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84f53-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84f53-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84f53-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="84f53-123">INPUTS</span></span>

### <span data-ttu-id="84f53-124">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="84f53-124">BatchAccountContext</span></span>
<span data-ttu-id="84f53-125">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="84f53-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="84f53-126">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="84f53-126">String</span></span>
<span data-ttu-id="84f53-127">Az ' azonosító ' paraméter a pipeline "string" típusú értékét fogadja el.</span><span class="sxs-lookup"><span data-stu-id="84f53-127">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="84f53-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="84f53-128">OUTPUTS</span></span>

## <span data-ttu-id="84f53-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="84f53-129">NOTES</span></span>

## <span data-ttu-id="84f53-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="84f53-130">RELATED LINKS</span></span>

[<span data-ttu-id="84f53-131">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="84f53-131">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="84f53-132">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="84f53-132">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="84f53-133">Új – AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="84f53-133">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="84f53-134">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="84f53-134">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="84f53-135">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="84f53-135">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="84f53-136">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="84f53-136">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


