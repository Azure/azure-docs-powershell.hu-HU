---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4B373447-3078-4C1F-932E-8337AB170DEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolusagemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolUsageMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolUsageMetric.md
ms.openlocfilehash: 1700e20318a502f32386638f94a9c5c86c271d7d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322458"
---
# <span data-ttu-id="a5333-101">Get-AzBatchPoolUsageMetric</span><span class="sxs-lookup"><span data-stu-id="a5333-101">Get-AzBatchPoolUsageMetric</span></span>

## <span data-ttu-id="a5333-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5333-102">SYNOPSIS</span></span>
<span data-ttu-id="a5333-103">Készlethasználati metrikákat kap egy Batch-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="a5333-103">Gets pool usage metrics for a Batch account.</span></span>

## <span data-ttu-id="a5333-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a5333-104">SYNTAX</span></span>

```
Get-AzBatchPoolUsageMetric [-StartTime <DateTime>] [-EndTime <DateTime>] [-Filter <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5333-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a5333-105">DESCRIPTION</span></span>
<span data-ttu-id="a5333-106">A **Get-AzBatchPoolUsageMetric** parancsmag a megadott fiók használati metrikákat kapja meg készlet szerint összesítve az egyes időintervallumokban.</span><span class="sxs-lookup"><span data-stu-id="a5333-106">The **Get-AzBatchPoolUsageMetric** cmdlet gets the usage metrics, aggregated by pool across individual time intervals, for the specified account.</span></span>
<span data-ttu-id="a5333-107">Egy adott készlet és egy időtartomány statisztikáját is lekértheti.</span><span class="sxs-lookup"><span data-stu-id="a5333-107">You can get the statistics for a specific pool and for a time range.</span></span>

## <span data-ttu-id="a5333-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a5333-108">EXAMPLES</span></span>

### <span data-ttu-id="a5333-109">1. példa: Készlethasználati metrikák lekérte egy időtartományra</span><span class="sxs-lookup"><span data-stu-id="a5333-109">Example 1: Get pool usage metrics for a time range</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $StartTime = Get-Date -Date "2016-05-16 00:00:00Z"
PS C:\> $EndTime = Get-Date -Date "2016-05-16 01:00:00Z"
PS C:\> Get-AzBatchPoolUsageMetric -StartTime $StartTime -EndTime $EndTime -BatchContext $context
DataEgressGiB      : 6.68875873088837E-06
DataIngressGiB     : 1.9485130906105E-05
EndTime            : 5/16/2016 12:30:00 AM
PoolId             : testpool1
StartTime          : 5/16/2016 12:00:00 AM
TotalCoreHours     : 8
VirtualMachineSize : standard_d4

DataEgressGiB      : 5.61587512493134E-06
DataIngressGiB     : 1.76150351762772E-05
EndTime            : 5/16/2016 12:30:00 AM
PoolId             : testpool2
StartTime          : 5/16/2016 12:00:00 AM
TotalCoreHours     : 12
VirtualMachineSize : standard_d4

DataEgressGiB      : 7.36676156520844E-06
DataIngressGiB     : 2.10804864764214E-05
EndTime            : 5/16/2016 1:00:00 AM
PoolId             : testpool1
StartTime          : 5/16/2016 12:30:00 AM
TotalCoreHours     : 7.99999999955555
VirtualMachineSize : standard_d4

DataEgressGiB      : 5.80586493015289E-06
DataIngressGiB     : 1.80602073669434E-05
EndTime            : 5/16/2016 1:00:00 AM
PoolId             : testpool2
StartTime          : 5/16/2016 12:30:00 AM
TotalCoreHours     : 11.9999999993333
VirtualMachineSize : standard_d4
```

<span data-ttu-id="a5333-110">Az első parancs létrehoz egy objektumhivatkozást a ContosoBatchAccount nevű kötegfiók fiókkulcsára a **Get-AzBatchAccountKey paranccsal.**</span><span class="sxs-lookup"><span data-stu-id="a5333-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="a5333-111">A parancs ezt az objektumhivatkozást a $Context tárolja.</span><span class="sxs-lookup"><span data-stu-id="a5333-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="a5333-112">A következő két parancs a **Get-Date** parancsmag használatával hoz létre DateTime-objektumokat.</span><span class="sxs-lookup"><span data-stu-id="a5333-112">The next two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="a5333-113">A parancsok ezeket az értékeket a $StartTime és $EndTime tárolják a végleges parancshoz való használatra.</span><span class="sxs-lookup"><span data-stu-id="a5333-113">The commands store these values in the $StartTime and $EndTime variables for use with the final command.</span></span>
<span data-ttu-id="a5333-114">A végleges parancs a készlethasználati metrikákat adja vissza készlet szerint összesítve, a megadott kezdési és záró időpont közötti időintervallumon keresztül.</span><span class="sxs-lookup"><span data-stu-id="a5333-114">The final command returns all of the pool usage metrics, aggregated by pool, across time interval between the specified start and end times.</span></span>

### <span data-ttu-id="a5333-115">2. példa: Készlethasználati metrikák lekérte egy szűrő használatával</span><span class="sxs-lookup"><span data-stu-id="a5333-115">Example 2: Get pool usage metrics by using a filter</span></span>
```
PS C:\>Get-AzBatchPoolUsageMetric -Filter "poolId eq 'ContosoPool'" -BatchContext $Context
DataEgressGiB      : 9.0496614575386E-06
DataIngressGiB     : 2.60043889284134E-05
EndTime            : 5/16/2016 5:30:00 PM
PoolId             : MyPool
StartTime          : 5/16/2016 5:00:00 PM
TotalCoreHours     : 12
VirtualMachineSize : standard_d4
```

<span data-ttu-id="a5333-116">Ez a parancs a ContosoPool nevű készlet használati metrikákat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="a5333-116">This command returns the usage metrics for pool named ContosoPool.</span></span>
<span data-ttu-id="a5333-117">A parancs meghatároz egy szűrő karakterláncot a készlet megadásához, és ugyanazt a $Context használja, mint az előző példában.</span><span class="sxs-lookup"><span data-stu-id="a5333-117">The command specifies a filter string to specify that pool, and uses the same $Context value as the previous example.</span></span>

## <span data-ttu-id="a5333-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5333-118">PARAMETERS</span></span>

### <span data-ttu-id="a5333-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a5333-119">-BatchContext</span></span>
<span data-ttu-id="a5333-120">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="a5333-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a5333-121">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="a5333-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a5333-122">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="a5333-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a5333-123">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="a5333-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a5333-124">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="a5333-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a5333-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5333-125">-DefaultProfile</span></span>
<span data-ttu-id="a5333-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a5333-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5333-127">-EndTime</span><span class="sxs-lookup"><span data-stu-id="a5333-127">-EndTime</span></span>
<span data-ttu-id="a5333-128">Annak az időtartománynak a végét adja meg, amelyhez a parancsmag használati metrikákat kap.</span><span class="sxs-lookup"><span data-stu-id="a5333-128">Specifies the end of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="a5333-129">Adjon meg egy legalább két órával korábban.</span><span class="sxs-lookup"><span data-stu-id="a5333-129">Specify a time at least two hours earlier.</span></span>
<span data-ttu-id="a5333-130">Ha nem ad meg záróidőt, ez a parancsmag a jelenleg rendelkezésre álló utolsó összegzési időközt használja.</span><span class="sxs-lookup"><span data-stu-id="a5333-130">If you do not specify an end time, this cmdlet uses the last aggregation interval currently available.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5333-131">-Filter</span><span class="sxs-lookup"><span data-stu-id="a5333-131">-Filter</span></span>
<span data-ttu-id="a5333-132">Egy OData-szűrő záradékot ad meg a parancsmag által visszaadott metrikák szűréséhez.</span><span class="sxs-lookup"><span data-stu-id="a5333-132">Specifies an OData filter clause to use to filter the metrics that this cmdlet returns.</span></span>
<span data-ttu-id="a5333-133">Az egyetlen érvényes tulajdonság a **poolId** karakterlánc értékkel.</span><span class="sxs-lookup"><span data-stu-id="a5333-133">The only valid property is **poolId** with a string value.</span></span>
<span data-ttu-id="a5333-134">Lehetséges műveletek: eq, ge, gt, le, lt, startswith.</span><span class="sxs-lookup"><span data-stu-id="a5333-134">Possible operations are the following: eq, ge, gt, le, lt, startswith.</span></span>

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

### <span data-ttu-id="a5333-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a5333-135">-StartTime</span></span>
<span data-ttu-id="a5333-136">Azt az időtartományt adja meg, amelyhez a parancsmag használati metrikákat kap.</span><span class="sxs-lookup"><span data-stu-id="a5333-136">Specifies the start of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="a5333-137">Adjon meg egy legalább két és fél órával korábban.</span><span class="sxs-lookup"><span data-stu-id="a5333-137">Specify a time at least two and a half hours earlier.</span></span>
<span data-ttu-id="a5333-138">Ha nem ad meg kezdési időt, ez a parancsmag a jelenleg rendelkezésre álló utolsó összesítési időközt használja.</span><span class="sxs-lookup"><span data-stu-id="a5333-138">If you do not specify a start time, this cmdlet uses the last aggregation interval currently available.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5333-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5333-139">CommonParameters</span></span>
<span data-ttu-id="a5333-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5333-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5333-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5333-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5333-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a5333-142">INPUTS</span></span>

### <span data-ttu-id="a5333-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a5333-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a5333-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5333-144">OUTPUTS</span></span>

### <span data-ttu-id="a5333-145">Microsoft.Azure.Commands.Bat. Models.PSPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="a5333-145">Microsoft.Azure.Commands.Batch.Models.PSPoolUsageMetrics</span></span>

## <span data-ttu-id="a5333-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a5333-146">NOTES</span></span>

## <span data-ttu-id="a5333-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5333-147">RELATED LINKS</span></span>

[<span data-ttu-id="a5333-148">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="a5333-148">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="a5333-149">Get-AzBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="a5333-149">Get-AzBatchPoolStatistics</span></span>](./Get-AzBatchPoolStatistic.md)

[<span data-ttu-id="a5333-150">Get-AzBatchStatistics</span><span class="sxs-lookup"><span data-stu-id="a5333-150">Get-AzBatchJobStatistics</span></span>](./Get-AzBatchJobStatistic.md)
