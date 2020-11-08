---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 87E7FA51-427E-4DB8-A6A2-D8638FD3DB8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJobSchedule.md
ms.openlocfilehash: ab1293bf147424bb9a7315cb541b9bf22fe4a357
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024906"
---
# <span data-ttu-id="8cc89-101">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8cc89-101">New-AzBatchJobSchedule</span></span>

## <span data-ttu-id="8cc89-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8cc89-102">SYNOPSIS</span></span>
<span data-ttu-id="8cc89-103">Projekt-ütemtervet hoz létre a köteg szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="8cc89-103">Creates a job schedule in the Batch service.</span></span>

## <span data-ttu-id="8cc89-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8cc89-104">SYNTAX</span></span>

```
New-AzBatchJobSchedule [-Id] <String> [-DisplayName <String>] -Schedule <PSSchedule>
 -JobSpecification <PSJobSpecification> [-Metadata <IDictionary>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cc89-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8cc89-105">DESCRIPTION</span></span>
<span data-ttu-id="8cc89-106">A **New-AzBatchJobSchedule** parancsmag az Azure-köteg szolgáltatásban hoz létre ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="8cc89-106">The **New-AzBatchJobSchedule** cmdlet creates a job schedule in the Azure Batch service.</span></span>
<span data-ttu-id="8cc89-107">A *BatchAccountContext* paraméter azt a fiókot adja meg, amelyben ez a parancsmag létrehozta az ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="8cc89-107">The *BatchAccountContext* parameter specifies the account in which this cmdlet creates the schedule.</span></span>

## <span data-ttu-id="8cc89-108">Példák</span><span class="sxs-lookup"><span data-stu-id="8cc89-108">EXAMPLES</span></span>

### <span data-ttu-id="8cc89-109">1. példa: munkabeosztás létrehozása</span><span class="sxs-lookup"><span data-stu-id="8cc89-109">Example 1: Create a job schedule</span></span>
```
PS C:\>$Schedule = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSSchedule"
PS C:\> $Schedule.RecurrenceInterval = [TimeSpan]::FromDays(1)
PS C:\> $JobSpecification = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSJobSpecification"
PS C:\> $JobSpecification.PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $JobSpecification.PoolInformation.PoolId = "ContosoPool06"
PS C:\> New-AzBatchJobSchedule -Id "JobSchedule17" -Schedule $Schedule -JobSpecification $JobSpecification -BatchContext $Context
```

<span data-ttu-id="8cc89-110">Ez a példa ütemtervet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8cc89-110">This example creates a job schedule.</span></span>
<span data-ttu-id="8cc89-111">Az első öt parancs **PSSchedule** -, **PSJobSpecification** -és **PSPoolInformation** -objektumokat hoz létre és módosíthat.</span><span class="sxs-lookup"><span data-stu-id="8cc89-111">The first five commands create and modify **PSSchedule** , **PSJobSpecification** , and **PSPoolInformation** objects.</span></span>
<span data-ttu-id="8cc89-112">A parancsok az New-Object parancsmagot és a standard Azure PowerShell-szintaxist használják.</span><span class="sxs-lookup"><span data-stu-id="8cc89-112">The commands use the New-Object cmdlet and standard Azure PowerShell syntax.</span></span>
<span data-ttu-id="8cc89-113">A parancsok ezeket az objektumokat a $Schedule és $JobSpecification változók tárolják.</span><span class="sxs-lookup"><span data-stu-id="8cc89-113">The commands store these objects in the $Schedule and $JobSpecification variables.</span></span>
<span data-ttu-id="8cc89-114">A végleges parancs létrehozza az azonosító JobSchedule17 tartalmazó ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="8cc89-114">The final command creates a job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="8cc89-115">Ez az ütemezés olyan feladatokat hoz létre, amelyek egy nap ismétlődési intervallumát jelentik.</span><span class="sxs-lookup"><span data-stu-id="8cc89-115">This schedule creates jobs with a recurrence interval of one day.</span></span>
<span data-ttu-id="8cc89-116">A feladatok azon a készleten futnak, amelyen az ID ContosoPool06 szerepel az ötödik parancsban megadott módon.</span><span class="sxs-lookup"><span data-stu-id="8cc89-116">The jobs run on the pool that has the ID ContosoPool06, as specified in the fifth command.</span></span>
<span data-ttu-id="8cc89-117">A **Get-AzBatchAccountKey** parancsmaggal rendelhet környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="8cc89-117">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="8cc89-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8cc89-118">PARAMETERS</span></span>

### <span data-ttu-id="8cc89-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8cc89-119">-BatchContext</span></span>
<span data-ttu-id="8cc89-120">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="8cc89-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8cc89-121">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="8cc89-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8cc89-122">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="8cc89-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8cc89-123">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="8cc89-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8cc89-124">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="8cc89-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8cc89-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cc89-125">-DefaultProfile</span></span>
<span data-ttu-id="8cc89-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8cc89-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8cc89-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8cc89-127">-DisplayName</span></span>
<span data-ttu-id="8cc89-128">A projekt ütemterv megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8cc89-128">Specifies a display name for the job schedule.</span></span>

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

### <span data-ttu-id="8cc89-129">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="8cc89-129">-Id</span></span>
<span data-ttu-id="8cc89-130">A parancsmag által létrehozott projekt-ütemterv AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8cc89-130">Specifies the ID of the job schedule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8cc89-131">-JobSpecification</span><span class="sxs-lookup"><span data-stu-id="8cc89-131">-JobSpecification</span></span>
<span data-ttu-id="8cc89-132">Azokat a feladatokat adja meg, amelyeket a parancsmag a projekt ütemtervében tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="8cc89-132">Specifies the details of the jobs that this cmdlet includes in the job schedule.</span></span>

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

### <span data-ttu-id="8cc89-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="8cc89-133">-Metadata</span></span>
<span data-ttu-id="8cc89-134">Metaadatokat ad meg kulcs/érték párokként a projekt ütemtervéhez való hozzáadáshoz.</span><span class="sxs-lookup"><span data-stu-id="8cc89-134">Specifies metadata, as key/value pairs, to add to the job schedule.</span></span>
<span data-ttu-id="8cc89-135">A kulcs a metaadat neve.</span><span class="sxs-lookup"><span data-stu-id="8cc89-135">The key is the metadata name.</span></span>
<span data-ttu-id="8cc89-136">Az érték a metaadat-érték.</span><span class="sxs-lookup"><span data-stu-id="8cc89-136">The value is the metadata value.</span></span>

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

### <span data-ttu-id="8cc89-137">– Ütemezés</span><span class="sxs-lookup"><span data-stu-id="8cc89-137">-Schedule</span></span>
<span data-ttu-id="8cc89-138">A feladatok létrehozásának időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8cc89-138">Specifies the schedule that determines when to create jobs.</span></span>

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

### <span data-ttu-id="8cc89-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cc89-139">CommonParameters</span></span>
<span data-ttu-id="8cc89-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8cc89-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cc89-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8cc89-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cc89-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8cc89-142">INPUTS</span></span>

### <span data-ttu-id="8cc89-143">System. String</span><span class="sxs-lookup"><span data-stu-id="8cc89-143">System.String</span></span>

### <span data-ttu-id="8cc89-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8cc89-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8cc89-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8cc89-145">OUTPUTS</span></span>

### <span data-ttu-id="8cc89-146">System. Void</span><span class="sxs-lookup"><span data-stu-id="8cc89-146">System.Void</span></span>

## <span data-ttu-id="8cc89-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8cc89-147">NOTES</span></span>

## <span data-ttu-id="8cc89-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8cc89-148">RELATED LINKS</span></span>

[<span data-ttu-id="8cc89-149">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8cc89-149">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="8cc89-150">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8cc89-150">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="8cc89-151">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="8cc89-151">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="8cc89-152">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8cc89-152">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="8cc89-153">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8cc89-153">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="8cc89-154">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8cc89-154">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="8cc89-155">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="8cc89-155">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
