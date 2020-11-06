---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4B373447-3078-4C1F-932E-8337AB170DEB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolUsageMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolUsageMetrics.md
ms.openlocfilehash: 4f985859cb26372a6ffc68b8521d08033fdc6670
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505667"
---
# <span data-ttu-id="5fe06-101">Get-AzureBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="5fe06-101">Get-AzureBatchPoolUsageMetrics</span></span>

## <span data-ttu-id="5fe06-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5fe06-102">SYNOPSIS</span></span>
<span data-ttu-id="5fe06-103">Egy köteg-fiók használati metrikáját kapja.</span><span class="sxs-lookup"><span data-stu-id="5fe06-103">Gets pool usage metrics for a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fe06-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5fe06-104">SYNTAX</span></span>

```
Get-AzureBatchPoolUsageMetrics [-StartTime <DateTime>] [-EndTime <DateTime>] [-Filter <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5fe06-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5fe06-105">DESCRIPTION</span></span>
<span data-ttu-id="5fe06-106">A **Get-AzureBatchPoolUsageMetrics** parancsmag Kinyeri a használati metrikákat, amelyeket a megadott fiók esetében összesítenek a különböző időintervallumok között.</span><span class="sxs-lookup"><span data-stu-id="5fe06-106">The **Get-AzureBatchPoolUsageMetrics** cmdlet gets the usage metrics, aggregated by pool across individual time intervals, for the specified account.</span></span>
<span data-ttu-id="5fe06-107">Az adott készlet és az időtartomány statisztikája is elérhető.</span><span class="sxs-lookup"><span data-stu-id="5fe06-107">You can get the statistics for a specific pool and for a time range.</span></span>

## <span data-ttu-id="5fe06-108">Példák</span><span class="sxs-lookup"><span data-stu-id="5fe06-108">EXAMPLES</span></span>

### <span data-ttu-id="5fe06-109">Példa 1: a készlet használati metrikájának beszerzése időtartományra</span><span class="sxs-lookup"><span data-stu-id="5fe06-109">Example 1: Get pool usage metrics for a time range</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $StartTime = Get-Date -Date "2016-05-16 00:00:00Z"
PS C:\> $EndTime = Get-Date -Date "2016-05-16 01:00:00Z"
PS C:\> Get-AzureBatchPoolUsageMetrics -StartTime $StartTime -EndTime $EndTime -BatchContext $context
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

<span data-ttu-id="5fe06-110">Az első parancs a **Get-AzureRmBatchAccountKeys** segítségével létrehoz egy objektumot, amely a ContosoBatchAccount nevű köteg fiók kulcsaira hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="5fe06-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="5fe06-111">A parancs a $Context változóban tárolja az objektum hivatkozását.</span><span class="sxs-lookup"><span data-stu-id="5fe06-111">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="5fe06-112">A következő két parancs a Get-Date parancsmag használatával **datetime** objektumokat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="5fe06-112">The next two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="5fe06-113">A parancsok ezeket az értékeket a $StartTimeban tárolják, és $EndTime változók a végleges paranccsal való használatra.</span><span class="sxs-lookup"><span data-stu-id="5fe06-113">The commands store these values in the $StartTime and $EndTime variables for use with the final command.</span></span>

<span data-ttu-id="5fe06-114">A végleges parancs visszaadja az összes alkalmazáskészlet-használati metrikát, összesítve a készlettel, a megadott kezdési és befejezési időpontok közötti intervallumok között.</span><span class="sxs-lookup"><span data-stu-id="5fe06-114">The final command returns all of the pool usage metrics, aggregated by pool, across time interval between the specified start and end times.</span></span>

### <span data-ttu-id="5fe06-115">2. példa: a készlet használati metrikájának beszerzése szűrő használatával</span><span class="sxs-lookup"><span data-stu-id="5fe06-115">Example 2: Get pool usage metrics by using a filter</span></span>
```
PS C:\>Get-AzureBatchPoolUsageMetrics -Filter "poolId eq 'ContosoPool'" -BatchContext $Context
DataEgressGiB      : 9.0496614575386E-06
DataIngressGiB     : 2.60043889284134E-05
EndTime            : 5/16/2016 5:30:00 PM
PoolId             : MyPool
StartTime          : 5/16/2016 5:00:00 PM
TotalCoreHours     : 12
VirtualMachineSize : standard_d4
```

<span data-ttu-id="5fe06-116">Ez a parancs a ContosoPool nevű alkalmazáskészlet használati metrikáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="5fe06-116">This command returns the usage metrics for pool named ContosoPool.</span></span>
<span data-ttu-id="5fe06-117">A parancs egy szűrő karakterláncot határoz meg a készlet megadásához, és ugyanazt a $Context értéket használja az előző példában.</span><span class="sxs-lookup"><span data-stu-id="5fe06-117">The command specifies a filter string to specify that pool, and uses the same $Context value as the previous example.</span></span>

## <span data-ttu-id="5fe06-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5fe06-118">PARAMETERS</span></span>

### <span data-ttu-id="5fe06-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5fe06-119">-BatchContext</span></span>
<span data-ttu-id="5fe06-120">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="5fe06-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5fe06-121">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5fe06-121">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="5fe06-122">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="5fe06-122">-EndTime</span></span>
<span data-ttu-id="5fe06-123">Annak az időtartománynak a végét adja meg, amelyre a parancsmag használati metrikát kap.</span><span class="sxs-lookup"><span data-stu-id="5fe06-123">Specifies the end of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="5fe06-124">Adjon meg legalább két órával korábbi időpontot.</span><span class="sxs-lookup"><span data-stu-id="5fe06-124">Specify a time at least two hours earlier.</span></span>
<span data-ttu-id="5fe06-125">Ha nem ad meg befejezési időpontot, ez a parancsmag a jelenleg elérhető utolsó összesítési intervallumot használja.</span><span class="sxs-lookup"><span data-stu-id="5fe06-125">If you do not specify an end time, this cmdlet uses the last aggregation interval currently available.</span></span>

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

### <span data-ttu-id="5fe06-126">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="5fe06-126">-Filter</span></span>
<span data-ttu-id="5fe06-127">Itt adhatja meg azt a OData-szűrési záradékot, amellyel szűrheti a parancsmag által retruns metrikákat.</span><span class="sxs-lookup"><span data-stu-id="5fe06-127">Specifies an OData filter clause to use to filter the metrics that this cmdlet retruns.</span></span>
<span data-ttu-id="5fe06-128">Az egyetlen érvényes tulajdonság egy **poolId** .</span><span class="sxs-lookup"><span data-stu-id="5fe06-128">The only valid property is **poolId** with a string value.</span></span>
<span data-ttu-id="5fe06-129">A lehetséges műveletek a következők: EQ, GE, gt, le, lt, startswith.</span><span class="sxs-lookup"><span data-stu-id="5fe06-129">Possible operations are the following: eq, ge, gt, le, lt, startswith.</span></span>

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

### <span data-ttu-id="5fe06-130">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="5fe06-130">-StartTime</span></span>
<span data-ttu-id="5fe06-131">Annak az időtartománynak a kezdetét adja meg, amelyre a parancsmag használati metrikát kap.</span><span class="sxs-lookup"><span data-stu-id="5fe06-131">Specifies the start of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="5fe06-132">Adjon meg legalább két és fél órával korábbi időpontot.</span><span class="sxs-lookup"><span data-stu-id="5fe06-132">Specify a time at least two and a half hours earlier.</span></span>
<span data-ttu-id="5fe06-133">Ha nem adja meg a kezdés időpontját, ez a parancsmag a jelenleg elérhető utolsó összesítési intervallumot használja.</span><span class="sxs-lookup"><span data-stu-id="5fe06-133">If you do not specify a start time, this cmdlet uses the last aggregation interval currently available.</span></span>

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

### <span data-ttu-id="5fe06-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fe06-134">-DefaultProfile</span></span>
<span data-ttu-id="5fe06-135">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5fe06-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fe06-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fe06-136">CommonParameters</span></span>
<span data-ttu-id="5fe06-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5fe06-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fe06-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fe06-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fe06-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fe06-139">INPUTS</span></span>

### <span data-ttu-id="5fe06-140">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5fe06-140">BatchAccountContext</span></span>
<span data-ttu-id="5fe06-141">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="5fe06-141">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="5fe06-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fe06-142">OUTPUTS</span></span>

### <span data-ttu-id="5fe06-143">PSPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="5fe06-143">PSPoolUsageMetrics</span></span>

## <span data-ttu-id="5fe06-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5fe06-144">NOTES</span></span>

## <span data-ttu-id="5fe06-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5fe06-145">RELATED LINKS</span></span>

[<span data-ttu-id="5fe06-146">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5fe06-146">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="5fe06-147">Get-AzureBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="5fe06-147">Get-AzureBatchPoolStatistics</span></span>](./Get-AzureBatchPoolStatistics.md)

[<span data-ttu-id="5fe06-148">Get-AzureBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="5fe06-148">Get-AzureBatchJobStatistics</span></span>](./Get-AzureBatchJobStatistics.md)

