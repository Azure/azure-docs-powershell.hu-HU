---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 87E7FA51-427E-4DB8-A6A2-D8638FD3DB8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
ms.openlocfilehash: 0a31b787b1be6d45caca74d01ee5d15d00071641
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497900"
---
# <span data-ttu-id="82bff-101">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="82bff-101">New-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="82bff-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="82bff-102">SYNOPSIS</span></span>
<span data-ttu-id="82bff-103">Projekt-ütemtervet hoz létre a köteg szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="82bff-103">Creates a job schedule in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82bff-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="82bff-104">SYNTAX</span></span>

```
New-AzureBatchJobSchedule [-Id] <String> [-DisplayName <String>] -Schedule <PSSchedule>
 -JobSpecification <PSJobSpecification> [-Metadata <IDictionary>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82bff-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="82bff-105">DESCRIPTION</span></span>
<span data-ttu-id="82bff-106">A **New-AzureBatchJobSchedule** parancsmag az Azure-köteg szolgáltatásban hoz létre ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="82bff-106">The **New-AzureBatchJobSchedule** cmdlet creates a job schedule in the Azure Batch service.</span></span>
<span data-ttu-id="82bff-107">A *BatchAccountContext* paraméter azt a fiókot adja meg, amelyben ez a parancsmag létrehozta az ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="82bff-107">The *BatchAccountContext* parameter specifies the account in which this cmdlet creates the schedule.</span></span>

## <span data-ttu-id="82bff-108">Példák</span><span class="sxs-lookup"><span data-stu-id="82bff-108">EXAMPLES</span></span>

### <span data-ttu-id="82bff-109">1. példa: munkabeosztás létrehozása</span><span class="sxs-lookup"><span data-stu-id="82bff-109">Example 1: Create a job schedule</span></span>
```
PS C:\>$Schedule = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSSchedule"
PS C:\> $Schedule.RecurrenceInterval = [TimeSpan]::FromDays(1)
PS C:\> $JobSpecification = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSJobSpecification"
PS C:\> $JobSpecification.PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $JobSpecification.PoolInformation.PoolId = "ContosoPool06"
PS C:\> New-AzureBatchJobSchedule -Id "JobSchedule17" -Schedule $Schedule -JobSpecification $JobSpecification -BatchContext $Context
```

<span data-ttu-id="82bff-110">Ez a példa ütemtervet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="82bff-110">This example creates a job schedule.</span></span>

<span data-ttu-id="82bff-111">Az első öt parancs **PSSchedule** -, **PSJobSpecification** -és **PSPoolInformation** -objektumokat hoz létre és módosíthat.</span><span class="sxs-lookup"><span data-stu-id="82bff-111">The first five commands create and modify **PSSchedule** , **PSJobSpecification** , and **PSPoolInformation** objects.</span></span>
<span data-ttu-id="82bff-112">A parancsok az New-Object parancsmagot és a standard Azure PowerShell-szintaxist használják.</span><span class="sxs-lookup"><span data-stu-id="82bff-112">The commands use the New-Object cmdlet and standard Azure PowerShell syntax.</span></span>
<span data-ttu-id="82bff-113">A parancsok ezeket az objektumokat a $Schedule és $JobSpecification változók tárolják.</span><span class="sxs-lookup"><span data-stu-id="82bff-113">The commands store these objects in the $Schedule and $JobSpecification variables.</span></span>

<span data-ttu-id="82bff-114">A végleges parancs létrehozza az azonosító JobSchedule17 tartalmazó ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="82bff-114">The final command creates a job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="82bff-115">Ez az ütemezés olyan feladatokat hoz létre, amelyek egy nap ismétlődési intervallumát jelentik.</span><span class="sxs-lookup"><span data-stu-id="82bff-115">This schedule creates jobs with a recurrence interval of one day.</span></span>
<span data-ttu-id="82bff-116">A feladatok azon a készleten futnak, amelyen az ID ContosoPool06 szerepel az ötödik parancsban megadott módon.</span><span class="sxs-lookup"><span data-stu-id="82bff-116">The jobs run on the pool that has the ID ContosoPool06, as specified in the fifth command.</span></span>
<span data-ttu-id="82bff-117">A **Get-AzureRmBatchAccountKeys** parancsmaggal rendelhet környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="82bff-117">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="82bff-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="82bff-118">PARAMETERS</span></span>

### <span data-ttu-id="82bff-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="82bff-119">-BatchContext</span></span>
<span data-ttu-id="82bff-120">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="82bff-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="82bff-121">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="82bff-121">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="82bff-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="82bff-122">-DisplayName</span></span>
<span data-ttu-id="82bff-123">A projekt ütemterv megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="82bff-123">Specifies a display name for the job schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82bff-124">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="82bff-124">-Id</span></span>
<span data-ttu-id="82bff-125">A parancsmag által létrehozott projekt-ütemterv AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="82bff-125">Specifies the ID of the job schedule that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82bff-126">-JobSpecification</span><span class="sxs-lookup"><span data-stu-id="82bff-126">-JobSpecification</span></span>
<span data-ttu-id="82bff-127">Azokat a feladatokat adja meg, amelyeket a parancsmag a projekt ütemtervében tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="82bff-127">Specifies the details of the jobs that this cmdlet includes in the job schedule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82bff-128">-Metadata</span><span class="sxs-lookup"><span data-stu-id="82bff-128">-Metadata</span></span>
<span data-ttu-id="82bff-129">Metaadatokat ad meg kulcs/érték párokként a projekt ütemtervéhez való hozzáadáshoz.</span><span class="sxs-lookup"><span data-stu-id="82bff-129">Specifies metadata, as key/value pairs, to add to the job schedule.</span></span>
<span data-ttu-id="82bff-130">A kulcs a metaadat neve.</span><span class="sxs-lookup"><span data-stu-id="82bff-130">The key is the metadata name.</span></span>
<span data-ttu-id="82bff-131">Az érték a metaadat-érték.</span><span class="sxs-lookup"><span data-stu-id="82bff-131">The value is the metadata value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82bff-132">– Ütemezés</span><span class="sxs-lookup"><span data-stu-id="82bff-132">-Schedule</span></span>
<span data-ttu-id="82bff-133">A feladatok létrehozásának időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="82bff-133">Specifies the schedule that determines when to create jobs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSSchedule
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82bff-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82bff-134">-DefaultProfile</span></span>
<span data-ttu-id="82bff-135">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="82bff-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82bff-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82bff-136">CommonParameters</span></span>
<span data-ttu-id="82bff-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="82bff-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82bff-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82bff-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82bff-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="82bff-139">INPUTS</span></span>

### <span data-ttu-id="82bff-140">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="82bff-140">BatchAccountContext</span></span>
<span data-ttu-id="82bff-141">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="82bff-141">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="82bff-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="82bff-142">OUTPUTS</span></span>

## <span data-ttu-id="82bff-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="82bff-143">NOTES</span></span>

## <span data-ttu-id="82bff-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="82bff-144">RELATED LINKS</span></span>

[<span data-ttu-id="82bff-145">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="82bff-145">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="82bff-146">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="82bff-146">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="82bff-147">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="82bff-147">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="82bff-148">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="82bff-148">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="82bff-149">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="82bff-149">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="82bff-150">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="82bff-150">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="82bff-151">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="82bff-151">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


