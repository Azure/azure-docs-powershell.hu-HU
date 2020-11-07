---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
ms.openlocfilehash: 2e19e6b1733ccc3dfe0a802756e2c0a517232803
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680616"
---
# <span data-ttu-id="1ef19-101">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="1ef19-101">Disable-AzureBatchJob</span></span>

## <span data-ttu-id="1ef19-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1ef19-102">SYNOPSIS</span></span>
<span data-ttu-id="1ef19-103">Letiltja a kötegelt feladatot.</span><span class="sxs-lookup"><span data-stu-id="1ef19-103">Disables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ef19-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1ef19-104">SYNTAX</span></span>

```
Disable-AzureBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ef19-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1ef19-105">DESCRIPTION</span></span>
<span data-ttu-id="1ef19-106">A **disable-AzureBatchJob** parancsmag letiltja az Azure-kötegelt feladatot.</span><span class="sxs-lookup"><span data-stu-id="1ef19-106">The **Disable-AzureBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="1ef19-107">Miután engedélyezte a feladatot, az új feladatok futhatnak.</span><span class="sxs-lookup"><span data-stu-id="1ef19-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="1ef19-108">A letiltott feladatok nem futtathatnak új feladatokat.</span><span class="sxs-lookup"><span data-stu-id="1ef19-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="1ef19-109">A letiltott feladatok később is engedélyezhetők.</span><span class="sxs-lookup"><span data-stu-id="1ef19-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="1ef19-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1ef19-110">EXAMPLES</span></span>

### <span data-ttu-id="1ef19-111">Példa 1: kötegelt feladat letiltása</span><span class="sxs-lookup"><span data-stu-id="1ef19-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzureBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="1ef19-112">Ez a parancs letiltja azt a feladatot, amely az ID Job-000001 tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="1ef19-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="1ef19-113">A parancs befejezi a feladat aktív tevékenységeit.</span><span class="sxs-lookup"><span data-stu-id="1ef19-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="1ef19-114">A **Get-AzureRmBatchAccountKeys** parancsmaggal rendelhet környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="1ef19-114">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="1ef19-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1ef19-115">PARAMETERS</span></span>

### <span data-ttu-id="1ef19-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="1ef19-116">-BatchContext</span></span>
<span data-ttu-id="1ef19-117">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="1ef19-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="1ef19-118">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1ef19-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="1ef19-119">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="1ef19-119">-DisableJobOption</span></span>
<span data-ttu-id="1ef19-120">Itt adhatja meg, hogy mi történjen a parancsmag által kikapcsolt tevékenységhez társított aktív feladatokkal.</span><span class="sxs-lookup"><span data-stu-id="1ef19-120">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="1ef19-121">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="1ef19-121">Valid values are:</span></span> 

- <span data-ttu-id="1ef19-122">Újravárólista</span><span class="sxs-lookup"><span data-stu-id="1ef19-122">Requeue</span></span> 
- <span data-ttu-id="1ef19-123">Lezáró</span><span class="sxs-lookup"><span data-stu-id="1ef19-123">Terminate</span></span> 
- <span data-ttu-id="1ef19-124">várj</span><span class="sxs-lookup"><span data-stu-id="1ef19-124">Wait</span></span>

```yaml
Type: Microsoft.Azure.Batch.Common.DisableJobOption
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, Wait

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ef19-125">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="1ef19-125">-Id</span></span>
<span data-ttu-id="1ef19-126">Annak a projektnek az AZONOSÍTÓját adja meg, amelyre a parancsmag letiltja.</span><span class="sxs-lookup"><span data-stu-id="1ef19-126">Specifies the ID of the job that this cmdlet disables.</span></span>

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

### <span data-ttu-id="1ef19-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ef19-127">-DefaultProfile</span></span>
<span data-ttu-id="1ef19-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1ef19-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ef19-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ef19-129">CommonParameters</span></span>
<span data-ttu-id="1ef19-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1ef19-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ef19-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ef19-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ef19-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ef19-132">INPUTS</span></span>

### <span data-ttu-id="1ef19-133">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1ef19-133">BatchAccountContext</span></span>
<span data-ttu-id="1ef19-134">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="1ef19-134">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="1ef19-135">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="1ef19-135">String</span></span>
<span data-ttu-id="1ef19-136">Az ' azonosító ' paraméter a pipeline "string" típusú értékét fogadja el.</span><span class="sxs-lookup"><span data-stu-id="1ef19-136">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="1ef19-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ef19-137">OUTPUTS</span></span>

## <span data-ttu-id="1ef19-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1ef19-138">NOTES</span></span>

## <span data-ttu-id="1ef19-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ef19-139">RELATED LINKS</span></span>

[<span data-ttu-id="1ef19-140">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="1ef19-140">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="1ef19-141">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="1ef19-141">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="1ef19-142">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="1ef19-142">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="1ef19-143">Új – AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="1ef19-143">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="1ef19-144">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="1ef19-144">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="1ef19-145">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="1ef19-145">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="1ef19-146">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="1ef19-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


