---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 87E7FA51-427E-4DB8-A6A2-D8638FD3DB8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
ms.openlocfilehash: 0524a55284d5c93db006248c12aa5a44f40deee7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494167"
---
# <span data-ttu-id="f857d-101">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f857d-101">New-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="f857d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f857d-102">SYNOPSIS</span></span>
<span data-ttu-id="f857d-103">Projekt-ütemtervet hoz létre a köteg szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="f857d-103">Creates a job schedule in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f857d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f857d-104">SYNTAX</span></span>

```
New-AzureBatchJobSchedule [-Id] <String> [-DisplayName <String>] -Schedule <PSSchedule>
 -JobSpecification <PSJobSpecification> [-Metadata <IDictionary>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f857d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f857d-105">DESCRIPTION</span></span>
<span data-ttu-id="f857d-106">A **New-AzureBatchJobSchedule** parancsmag az Azure-köteg szolgáltatásban hoz létre ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="f857d-106">The **New-AzureBatchJobSchedule** cmdlet creates a job schedule in the Azure Batch service.</span></span>
<span data-ttu-id="f857d-107">A *BatchAccountContext* paraméter azt a fiókot adja meg, amelyben ez a parancsmag létrehozta az ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="f857d-107">The *BatchAccountContext* parameter specifies the account in which this cmdlet creates the schedule.</span></span>

## <span data-ttu-id="f857d-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f857d-108">EXAMPLES</span></span>

### <span data-ttu-id="f857d-109">1. példa: munkabeosztás létrehozása</span><span class="sxs-lookup"><span data-stu-id="f857d-109">Example 1: Create a job schedule</span></span>
```
PS C:\>$Schedule = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSSchedule"
PS C:\> $Schedule.RecurrenceInterval = [TimeSpan]::FromDays(1)
PS C:\> $JobSpecification = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSJobSpecification"
PS C:\> $JobSpecification.PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $JobSpecification.PoolInformation.PoolId = "ContosoPool06"
PS C:\> New-AzureBatchJobSchedule -Id "JobSchedule17" -Schedule $Schedule -JobSpecification $JobSpecification -BatchContext $Context
```

<span data-ttu-id="f857d-110">Ez a példa ütemtervet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f857d-110">This example creates a job schedule.</span></span>
<span data-ttu-id="f857d-111">Az első öt parancs **PSSchedule** -, **PSJobSpecification** -és **PSPoolInformation** -objektumokat hoz létre és módosíthat.</span><span class="sxs-lookup"><span data-stu-id="f857d-111">The first five commands create and modify **PSSchedule** , **PSJobSpecification** , and **PSPoolInformation** objects.</span></span>
<span data-ttu-id="f857d-112">A parancsok az New-Object parancsmagot és a standard Azure PowerShell-szintaxist használják.</span><span class="sxs-lookup"><span data-stu-id="f857d-112">The commands use the New-Object cmdlet and standard Azure PowerShell syntax.</span></span>
<span data-ttu-id="f857d-113">A parancsok ezeket az objektumokat a $Schedule és $JobSpecification változók tárolják.</span><span class="sxs-lookup"><span data-stu-id="f857d-113">The commands store these objects in the $Schedule and $JobSpecification variables.</span></span>
<span data-ttu-id="f857d-114">A végleges parancs létrehozza az azonosító JobSchedule17 tartalmazó ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="f857d-114">The final command creates a job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="f857d-115">Ez az ütemezés olyan feladatokat hoz létre, amelyek egy nap ismétlődési intervallumát jelentik.</span><span class="sxs-lookup"><span data-stu-id="f857d-115">This schedule creates jobs with a recurrence interval of one day.</span></span>
<span data-ttu-id="f857d-116">A feladatok azon a készleten futnak, amelyen az ID ContosoPool06 szerepel az ötödik parancsban megadott módon.</span><span class="sxs-lookup"><span data-stu-id="f857d-116">The jobs run on the pool that has the ID ContosoPool06, as specified in the fifth command.</span></span>
<span data-ttu-id="f857d-117">A **Get-AzureRmBatchAccountKeys** parancsmaggal rendelhet környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="f857d-117">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="f857d-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f857d-118">PARAMETERS</span></span>

### <span data-ttu-id="f857d-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f857d-119">-BatchContext</span></span>
<span data-ttu-id="f857d-120">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="f857d-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f857d-121">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="f857d-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f857d-122">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="f857d-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f857d-123">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="f857d-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f857d-124">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="f857d-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f857d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f857d-125">-DefaultProfile</span></span>
<span data-ttu-id="f857d-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f857d-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f857d-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f857d-127">-DisplayName</span></span>
<span data-ttu-id="f857d-128">A projekt ütemterv megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f857d-128">Specifies a display name for the job schedule.</span></span>

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

### <span data-ttu-id="f857d-129">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="f857d-129">-Id</span></span>
<span data-ttu-id="f857d-130">A parancsmag által létrehozott projekt-ütemterv AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f857d-130">Specifies the ID of the job schedule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f857d-131">-JobSpecification</span><span class="sxs-lookup"><span data-stu-id="f857d-131">-JobSpecification</span></span>
<span data-ttu-id="f857d-132">Azokat a feladatokat adja meg, amelyeket a parancsmag a projekt ütemtervében tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="f857d-132">Specifies the details of the jobs that this cmdlet includes in the job schedule.</span></span>

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

### <span data-ttu-id="f857d-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="f857d-133">-Metadata</span></span>
<span data-ttu-id="f857d-134">Metaadatokat ad meg kulcs/érték párokként a projekt ütemtervéhez való hozzáadáshoz.</span><span class="sxs-lookup"><span data-stu-id="f857d-134">Specifies metadata, as key/value pairs, to add to the job schedule.</span></span>
<span data-ttu-id="f857d-135">A kulcs a metaadat neve.</span><span class="sxs-lookup"><span data-stu-id="f857d-135">The key is the metadata name.</span></span>
<span data-ttu-id="f857d-136">Az érték a metaadat-érték.</span><span class="sxs-lookup"><span data-stu-id="f857d-136">The value is the metadata value.</span></span>

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

### <span data-ttu-id="f857d-137">– Ütemezés</span><span class="sxs-lookup"><span data-stu-id="f857d-137">-Schedule</span></span>
<span data-ttu-id="f857d-138">A feladatok létrehozásának időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f857d-138">Specifies the schedule that determines when to create jobs.</span></span>

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

### <span data-ttu-id="f857d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f857d-139">CommonParameters</span></span>
<span data-ttu-id="f857d-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f857d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f857d-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f857d-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f857d-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f857d-142">INPUTS</span></span>

### <span data-ttu-id="f857d-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f857d-143">System.String</span></span>

### <span data-ttu-id="f857d-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f857d-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="f857d-145">Paraméterek: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f857d-145">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="f857d-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f857d-146">OUTPUTS</span></span>

### <span data-ttu-id="f857d-147">System. Void</span><span class="sxs-lookup"><span data-stu-id="f857d-147">System.Void</span></span>

## <span data-ttu-id="f857d-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f857d-148">NOTES</span></span>

## <span data-ttu-id="f857d-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f857d-149">RELATED LINKS</span></span>

[<span data-ttu-id="f857d-150">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f857d-150">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="f857d-151">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f857d-151">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="f857d-152">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="f857d-152">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="f857d-153">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f857d-153">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="f857d-154">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f857d-154">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="f857d-155">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f857d-155">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="f857d-156">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f857d-156">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


