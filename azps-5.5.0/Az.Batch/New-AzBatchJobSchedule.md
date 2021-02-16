---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 87E7FA51-427E-4DB8-A6A2-D8638FD3DB8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJobSchedule.md
ms.openlocfilehash: ab1293bf147424bb9a7315cb541b9bf22fe4a357
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162490"
---
# <span data-ttu-id="87d6f-101">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="87d6f-101">New-AzBatchJobSchedule</span></span>

## <span data-ttu-id="87d6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87d6f-102">SYNOPSIS</span></span>
<span data-ttu-id="87d6f-103">Létrehozza a munkabeosztást a Batch szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="87d6f-103">Creates a job schedule in the Batch service.</span></span>

## <span data-ttu-id="87d6f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="87d6f-104">SYNTAX</span></span>

```
New-AzBatchJobSchedule [-Id] <String> [-DisplayName <String>] -Schedule <PSSchedule>
 -JobSpecification <PSJobSpecification> [-Metadata <IDictionary>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87d6f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="87d6f-105">DESCRIPTION</span></span>
<span data-ttu-id="87d6f-106">A **New-AzBatchSchedule** parancsmag létrehoz egy feladatütemtervet az Azure Batch szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="87d6f-106">The **New-AzBatchJobSchedule** cmdlet creates a job schedule in the Azure Batch service.</span></span>
<span data-ttu-id="87d6f-107">A *BatchAccountContext* paraméter megadja azt a fiókot, amelyben ez a parancsmag létrehozza az ütemezést.</span><span class="sxs-lookup"><span data-stu-id="87d6f-107">The *BatchAccountContext* parameter specifies the account in which this cmdlet creates the schedule.</span></span>

## <span data-ttu-id="87d6f-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="87d6f-108">EXAMPLES</span></span>

### <span data-ttu-id="87d6f-109">1. példa: Munkabeosztás létrehozása</span><span class="sxs-lookup"><span data-stu-id="87d6f-109">Example 1: Create a job schedule</span></span>
```
PS C:\>$Schedule = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSSchedule"
PS C:\> $Schedule.RecurrenceInterval = [TimeSpan]::FromDays(1)
PS C:\> $JobSpecification = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSJobSpecification"
PS C:\> $JobSpecification.PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $JobSpecification.PoolInformation.PoolId = "ContosoPool06"
PS C:\> New-AzBatchJobSchedule -Id "JobSchedule17" -Schedule $Schedule -JobSpecification $JobSpecification -BatchContext $Context
```

<span data-ttu-id="87d6f-110">Ez a példa munkabeosztást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="87d6f-110">This example creates a job schedule.</span></span>
<span data-ttu-id="87d6f-111">Az első öt parancs **PSSchedule,** **PSJobSpecification és** **PSPoolInformation objektumokat** hoz létre és módosít.</span><span class="sxs-lookup"><span data-stu-id="87d6f-111">The first five commands create and modify **PSSchedule**, **PSJobSpecification**, and **PSPoolInformation** objects.</span></span>
<span data-ttu-id="87d6f-112">A parancsok a New-Object Azure PowerShell szokásos szintaxisát használják.</span><span class="sxs-lookup"><span data-stu-id="87d6f-112">The commands use the New-Object cmdlet and standard Azure PowerShell syntax.</span></span>
<span data-ttu-id="87d6f-113">A parancsok ezeket az objektumokat a $Schedule és $JobSpecification tárolják.</span><span class="sxs-lookup"><span data-stu-id="87d6f-113">The commands store these objects in the $Schedule and $JobSpecification variables.</span></span>
<span data-ttu-id="87d6f-114">Az utolsó parancs létrehoz egy munkabeosztást, amely a Feladat ütemezése17 azonosítót is létrehozza.</span><span class="sxs-lookup"><span data-stu-id="87d6f-114">The final command creates a job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="87d6f-115">Ez az ütemezés egynapos ismétlődési időközzel hoz létre feladatokat.</span><span class="sxs-lookup"><span data-stu-id="87d6f-115">This schedule creates jobs with a recurrence interval of one day.</span></span>
<span data-ttu-id="87d6f-116">A feladatok a ContosoPool06 azonosítójú készleten futnak, az ötödik parancsban meghatározottak szerint.</span><span class="sxs-lookup"><span data-stu-id="87d6f-116">The jobs run on the pool that has the ID ContosoPool06, as specified in the fifth command.</span></span>
<span data-ttu-id="87d6f-117">A **Get-AzBatchAccountKey** parancsmaggal kontextust rendelhet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="87d6f-117">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="87d6f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87d6f-118">PARAMETERS</span></span>

### <span data-ttu-id="87d6f-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="87d6f-119">-BatchContext</span></span>
<span data-ttu-id="87d6f-120">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatással való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="87d6f-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="87d6f-121">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor az Azure Active Directory-hitelesítést fogja használni a Batch szolgáltatás használata során.</span><span class="sxs-lookup"><span data-stu-id="87d6f-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="87d6f-122">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="87d6f-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="87d6f-123">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="87d6f-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="87d6f-124">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="87d6f-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="87d6f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87d6f-125">-DefaultProfile</span></span>
<span data-ttu-id="87d6f-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="87d6f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87d6f-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="87d6f-127">-DisplayName</span></span>
<span data-ttu-id="87d6f-128">A beosztás megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="87d6f-128">Specifies a display name for the job schedule.</span></span>

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

### <span data-ttu-id="87d6f-129">-Id</span><span class="sxs-lookup"><span data-stu-id="87d6f-129">-Id</span></span>
<span data-ttu-id="87d6f-130">A parancsmag által létrehozott feladatütemterv azonosítója.</span><span class="sxs-lookup"><span data-stu-id="87d6f-130">Specifies the ID of the job schedule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="87d6f-131">-JobSpecification</span><span class="sxs-lookup"><span data-stu-id="87d6f-131">-JobSpecification</span></span>
<span data-ttu-id="87d6f-132">Megadja a feladatütemtervben a parancsmag által megadott feladatok részleteit.</span><span class="sxs-lookup"><span data-stu-id="87d6f-132">Specifies the details of the jobs that this cmdlet includes in the job schedule.</span></span>

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

### <span data-ttu-id="87d6f-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="87d6f-133">-Metadata</span></span>
<span data-ttu-id="87d6f-134">Meghatározza a beosztáshoz hozzáadni a metaadatokat kulcs-érték párokként.</span><span class="sxs-lookup"><span data-stu-id="87d6f-134">Specifies metadata, as key/value pairs, to add to the job schedule.</span></span>
<span data-ttu-id="87d6f-135">A kulcs a metaadatok neve.</span><span class="sxs-lookup"><span data-stu-id="87d6f-135">The key is the metadata name.</span></span>
<span data-ttu-id="87d6f-136">Az érték a metaadatérték.</span><span class="sxs-lookup"><span data-stu-id="87d6f-136">The value is the metadata value.</span></span>

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

### <span data-ttu-id="87d6f-137">-Schedule</span><span class="sxs-lookup"><span data-stu-id="87d6f-137">-Schedule</span></span>
<span data-ttu-id="87d6f-138">Azt az ütemezést adja meg, amely meghatározza, hogy mikor kell feladatokat létrehozni.</span><span class="sxs-lookup"><span data-stu-id="87d6f-138">Specifies the schedule that determines when to create jobs.</span></span>

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

### <span data-ttu-id="87d6f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87d6f-139">CommonParameters</span></span>
<span data-ttu-id="87d6f-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87d6f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87d6f-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87d6f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87d6f-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="87d6f-142">INPUTS</span></span>

### <span data-ttu-id="87d6f-143">System.String</span><span class="sxs-lookup"><span data-stu-id="87d6f-143">System.String</span></span>

### <span data-ttu-id="87d6f-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="87d6f-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="87d6f-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87d6f-145">OUTPUTS</span></span>

### <span data-ttu-id="87d6f-146">System.Void</span><span class="sxs-lookup"><span data-stu-id="87d6f-146">System.Void</span></span>

## <span data-ttu-id="87d6f-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="87d6f-147">NOTES</span></span>

## <span data-ttu-id="87d6f-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87d6f-148">RELATED LINKS</span></span>

[<span data-ttu-id="87d6f-149">Disable-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="87d6f-149">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="87d6f-150">Enable-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="87d6f-150">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="87d6f-151">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="87d6f-151">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="87d6f-152">Get-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="87d6f-152">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="87d6f-153">Remove-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="87d6f-153">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="87d6f-154">Stop-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="87d6f-154">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="87d6f-155">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="87d6f-155">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
