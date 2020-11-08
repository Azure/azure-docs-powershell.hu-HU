---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4B373447-3078-4C1F-932E-8337AB170DEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolusagemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolUsageMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolUsageMetric.md
ms.openlocfilehash: cabef75fb55cc3b8409edb3425de84531209b479
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "94017179"
---
# <span data-ttu-id="8af6b-101">Get-AzBatchPoolUsageMetric</span><span class="sxs-lookup"><span data-stu-id="8af6b-101">Get-AzBatchPoolUsageMetric</span></span>

## <span data-ttu-id="8af6b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8af6b-102">SYNOPSIS</span></span>
<span data-ttu-id="8af6b-103">Egy köteg-fiók használati metrikáját kapja.</span><span class="sxs-lookup"><span data-stu-id="8af6b-103">Gets pool usage metrics for a Batch account.</span></span>

## <span data-ttu-id="8af6b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8af6b-104">SYNTAX</span></span>

```
Get-AzBatchPoolUsageMetric [-StartTime <DateTime>] [-EndTime <DateTime>] [-Filter <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8af6b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8af6b-105">DESCRIPTION</span></span>
<span data-ttu-id="8af6b-106">A **Get-AzBatchPoolUsageMetric** parancsmag Kinyeri a használati metrikákat, amelyeket a megadott fiók esetében összesítenek a különböző időintervallumok között.</span><span class="sxs-lookup"><span data-stu-id="8af6b-106">The **Get-AzBatchPoolUsageMetric** cmdlet gets the usage metrics, aggregated by pool across individual time intervals, for the specified account.</span></span>
<span data-ttu-id="8af6b-107">Az adott készlet és az időtartomány statisztikája is elérhető.</span><span class="sxs-lookup"><span data-stu-id="8af6b-107">You can get the statistics for a specific pool and for a time range.</span></span>

## <span data-ttu-id="8af6b-108">Példák</span><span class="sxs-lookup"><span data-stu-id="8af6b-108">EXAMPLES</span></span>

### <span data-ttu-id="8af6b-109">Példa 1: a készlet használati metrikájának beszerzése időtartományra</span><span class="sxs-lookup"><span data-stu-id="8af6b-109">Example 1: Get pool usage metrics for a time range</span></span>
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

<span data-ttu-id="8af6b-110">Az első parancs a **Get-AzBatchAccountKey** segítségével létrehoz egy objektumot, amely a ContosoBatchAccount nevű köteg fiók kulcsaira hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="8af6b-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="8af6b-111">A parancs a $Context változóban tárolja az objektum hivatkozását.</span><span class="sxs-lookup"><span data-stu-id="8af6b-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="8af6b-112">A következő két parancs a Get-Date parancsmag használatával **datetime** objektumokat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8af6b-112">The next two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="8af6b-113">A parancsok ezeket az értékeket a $StartTimeban tárolják, és $EndTime változók a végleges paranccsal való használatra.</span><span class="sxs-lookup"><span data-stu-id="8af6b-113">The commands store these values in the $StartTime and $EndTime variables for use with the final command.</span></span>
<span data-ttu-id="8af6b-114">A végleges parancs visszaadja az összes alkalmazáskészlet-használati metrikát, összesítve a készlettel, a megadott kezdési és befejezési időpontok közötti intervallumok között.</span><span class="sxs-lookup"><span data-stu-id="8af6b-114">The final command returns all of the pool usage metrics, aggregated by pool, across time interval between the specified start and end times.</span></span>

### <span data-ttu-id="8af6b-115">2. példa: a készlet használati metrikájának beszerzése szűrő használatával</span><span class="sxs-lookup"><span data-stu-id="8af6b-115">Example 2: Get pool usage metrics by using a filter</span></span>
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

<span data-ttu-id="8af6b-116">Ez a parancs a ContosoPool nevű alkalmazáskészlet használati metrikáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="8af6b-116">This command returns the usage metrics for pool named ContosoPool.</span></span>
<span data-ttu-id="8af6b-117">A parancs egy szűrő karakterláncot határoz meg a készlet megadásához, és ugyanazt a $Context értéket használja az előző példában.</span><span class="sxs-lookup"><span data-stu-id="8af6b-117">The command specifies a filter string to specify that pool, and uses the same $Context value as the previous example.</span></span>

## <span data-ttu-id="8af6b-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8af6b-118">PARAMETERS</span></span>

### <span data-ttu-id="8af6b-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8af6b-119">-BatchContext</span></span>
<span data-ttu-id="8af6b-120">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="8af6b-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8af6b-121">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="8af6b-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8af6b-122">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="8af6b-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8af6b-123">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="8af6b-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8af6b-124">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="8af6b-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8af6b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8af6b-125">-DefaultProfile</span></span>
<span data-ttu-id="8af6b-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8af6b-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8af6b-127">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="8af6b-127">-EndTime</span></span>
<span data-ttu-id="8af6b-128">Annak az időtartománynak a végét adja meg, amelyre a parancsmag használati metrikát kap.</span><span class="sxs-lookup"><span data-stu-id="8af6b-128">Specifies the end of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="8af6b-129">Adjon meg legalább két órával korábbi időpontot.</span><span class="sxs-lookup"><span data-stu-id="8af6b-129">Specify a time at least two hours earlier.</span></span>
<span data-ttu-id="8af6b-130">Ha nem ad meg befejezési időpontot, ez a parancsmag a jelenleg elérhető utolsó összesítési intervallumot használja.</span><span class="sxs-lookup"><span data-stu-id="8af6b-130">If you do not specify an end time, this cmdlet uses the last aggregation interval currently available.</span></span>

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

### <span data-ttu-id="8af6b-131">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="8af6b-131">-Filter</span></span>
<span data-ttu-id="8af6b-132">A parancsmag által visszaadott metrikák szűréséhez használható OData-szűrő záradékot adja meg.</span><span class="sxs-lookup"><span data-stu-id="8af6b-132">Specifies an OData filter clause to use to filter the metrics that this cmdlet returns.</span></span>
<span data-ttu-id="8af6b-133">Az egyetlen érvényes tulajdonság egy **poolId** .</span><span class="sxs-lookup"><span data-stu-id="8af6b-133">The only valid property is **poolId** with a string value.</span></span>
<span data-ttu-id="8af6b-134">A lehetséges műveletek a következők: EQ, GE, gt, le, lt, startswith.</span><span class="sxs-lookup"><span data-stu-id="8af6b-134">Possible operations are the following: eq, ge, gt, le, lt, startswith.</span></span>

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

### <span data-ttu-id="8af6b-135">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="8af6b-135">-StartTime</span></span>
<span data-ttu-id="8af6b-136">Annak az időtartománynak a kezdetét adja meg, amelyre a parancsmag használati metrikát kap.</span><span class="sxs-lookup"><span data-stu-id="8af6b-136">Specifies the start of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="8af6b-137">Adjon meg legalább két és fél órával korábbi időpontot.</span><span class="sxs-lookup"><span data-stu-id="8af6b-137">Specify a time at least two and a half hours earlier.</span></span>
<span data-ttu-id="8af6b-138">Ha nem adja meg a kezdés időpontját, ez a parancsmag a jelenleg elérhető utolsó összesítési intervallumot használja.</span><span class="sxs-lookup"><span data-stu-id="8af6b-138">If you do not specify a start time, this cmdlet uses the last aggregation interval currently available.</span></span>

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

### <span data-ttu-id="8af6b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8af6b-139">CommonParameters</span></span>
<span data-ttu-id="8af6b-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8af6b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8af6b-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8af6b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8af6b-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8af6b-142">INPUTS</span></span>

### <span data-ttu-id="8af6b-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8af6b-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8af6b-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8af6b-144">OUTPUTS</span></span>

### <span data-ttu-id="8af6b-145">Microsoft.Azure.Commands.BatCH. Modellek. PSPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="8af6b-145">Microsoft.Azure.Commands.Batch.Models.PSPoolUsageMetrics</span></span>

## <span data-ttu-id="8af6b-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8af6b-146">NOTES</span></span>

## <span data-ttu-id="8af6b-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8af6b-147">RELATED LINKS</span></span>

[<span data-ttu-id="8af6b-148">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="8af6b-148">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="8af6b-149">Get-AzBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="8af6b-149">Get-AzBatchPoolStatistics</span></span>](./Get-AzBatchPoolStatistic.md)

[<span data-ttu-id="8af6b-150">Get-AzBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="8af6b-150">Get-AzBatchJobStatistics</span></span>](./Get-AzBatchJobStatistic.md)


