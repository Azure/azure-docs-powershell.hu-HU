---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 44D877F1-D066-4C9C-A797-05EF03785B54
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
ms.openlocfilehash: 6f89e7db5d2df2c475be1ac9875fd1e87217db77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680778"
---
# <span data-ttu-id="6b63f-101">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="6b63f-101">Get-AzureBatchPool</span></span>

## <span data-ttu-id="6b63f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6b63f-102">SYNOPSIS</span></span>
<span data-ttu-id="6b63f-103">A megadott köteg fiók alatti köteg-gyűjtőket kap.</span><span class="sxs-lookup"><span data-stu-id="6b63f-103">Gets Batch pools under the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b63f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6b63f-104">SYNTAX</span></span>

### <span data-ttu-id="6b63f-105">ODataFilter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6b63f-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchPool [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b63f-106">Azonosító</span><span class="sxs-lookup"><span data-stu-id="6b63f-106">Id</span></span>
```
Get-AzureBatchPool [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b63f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6b63f-107">DESCRIPTION</span></span>
<span data-ttu-id="6b63f-108">A **Get-AzureBatchPool** parancsmag a *BatchContext* paraméterrel megadott köteg fiók alatt kapja meg az Azure batch-készleteket.</span><span class="sxs-lookup"><span data-stu-id="6b63f-108">The **Get-AzureBatchPool** cmdlet gets the Azure Batch pools under the Batch account specified with the *BatchContext* parameter.</span></span>
<span data-ttu-id="6b63f-109">Az *ID* paraméterrel egyetlen készletet kaphat, vagy használhatja a *szűrő* paramétert az Open Data Protocol (OData) szűrővel egyező medencék beszerzésére.</span><span class="sxs-lookup"><span data-stu-id="6b63f-109">You can use the *Id* parameter to get a single pool, or you can use the *Filter* parameter to get the pools that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="6b63f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6b63f-110">EXAMPLES</span></span>

### <span data-ttu-id="6b63f-111">Példa 1: készlet beszerzése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="6b63f-111">Example 1: Get a pool by ID</span></span>
```
PS C:\>Get-AzureBatchPool -Id "MyPool" -BatchContext $Context
AllocationState                      : Resizing
AllocationStateTransitionTime        : 7/25/2015 9:30:28 PM
AutoScaleEnabled                     : False
AutoScaleFormula                     : 
AutoScaleRun                         : 
CertificateReferences                : 
CreationTime                         : 7/25/2015 9:30:28 PM
CurrentDedicated                     : 0
CurrentOSVersion                     : *
DisplayName                          : 
ETag                                 : 0x8D29538429CF04C
Id                                   : MyPool
InterComputeNodeCommunicationEnabled : False
LastModified                         : 7/25/2015 9:30:28 PM
MaxTasksPerComputeNode               : 1
Metadata                             : 
OSFamily                             : 4
ResizeError                          : 
ResizeTimeout                        : 00:05:00
TaskSchedulingPolicy                 : Microsoft.Azure.Commands.Batch.Models.PSTaskSchedulingPolicy
StartTask                            : 
State                                : Active
StateTransitionTime                  : 7/25/2015 9:30:28 PM
Statistics                           : 
TargetDedicated                      : 1
TargetOSVersion                      : *
Url                                  : https://cmdletexample.westus.batch.azure.com/pools/MyPool
VirtualMachineSize                   : small
```

<span data-ttu-id="6b63f-112">Ez a parancs a medencét azonosító MyPool kapja.</span><span class="sxs-lookup"><span data-stu-id="6b63f-112">This command gets the pool with ID MyPool.</span></span>

### <span data-ttu-id="6b63f-113">2. példa: az összes készlet lekérése OData-szűrő használatával</span><span class="sxs-lookup"><span data-stu-id="6b63f-113">Example 2: Get all pools using an OData filter</span></span>
```
PS C:\>Get-AzureBatchPool -Filter "startswith(id,'My')" -BatchContext $Context
AllocationState                      : Resizing
AllocationStateTransitionTime        : 7/25/2015 9:30:28 PM
AutoScaleEnabled                     : False
AutoScaleFormula                     : 
AutoScaleRun                         : 
CertificateReferences                : 
CreationTime                         : 7/25/2015 9:30:28 PM
CurrentDedicated                     : 0
CurrentOSVersion                     : *
DisplayName                          : 
ETag                                 : 0x8D29538429CF04C
Id                                   : MyPool
InterComputeNodeCommunicationEnabled : False
LastModified                         : 7/25/2015 9:30:28 PM
MaxTasksPerComputeNode               : 1
Metadata                             : 
OSFamily                             : 4
ResizeError                          : 
ResizeTimeout                        : 00:05:00
TaskSchedulingPolicy                 : Microsoft.Azure.Commands.Batch.Models.PSTaskSchedulingPolicy
StartTask                            : 
State                                : Active
StateTransitionTime                  : 7/25/2015 9:30:28 PM
Statistics                           : 
TargetDedicated                      : 1
TargetOSVersion                      : *
Url                                  : https://cmdletexample.westus.batch.azure.com/pools/MyPool
VirtualMachineSize                   : small
```

<span data-ttu-id="6b63f-114">Ez a parancs azokat a készleteket kapja meg, amelyek azonosítói a *szűrő* paraméterrel kezdődnek.</span><span class="sxs-lookup"><span data-stu-id="6b63f-114">This command gets the pools whose IDs start with My by using the *Filter* parameter.</span></span>

## <span data-ttu-id="6b63f-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6b63f-115">PARAMETERS</span></span>

### <span data-ttu-id="6b63f-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6b63f-116">-BatchContext</span></span>
<span data-ttu-id="6b63f-117">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="6b63f-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6b63f-118">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6b63f-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="6b63f-119">– Kibontás</span><span class="sxs-lookup"><span data-stu-id="6b63f-119">-Expand</span></span>
<span data-ttu-id="6b63f-120">Az Open Data Protocol (OData) kibontási záradékát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b63f-120">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="6b63f-121">Adjon meg egy értéket ehhez a paraméterhez a fő entitáshoz tartozó társított entitások beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="6b63f-121">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="6b63f-122">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="6b63f-122">-Filter</span></span>
<span data-ttu-id="6b63f-123">Megadja a OData-szűrési záradékot a medencék lekérdezéséhez.</span><span class="sxs-lookup"><span data-stu-id="6b63f-123">Specifies the OData filter clause to use when querying for pools.</span></span>
<span data-ttu-id="6b63f-124">Ha nem ad meg szűrőt, a függvény a *BatchContext* paraméterrel megadott köteg fiók alatti összes készletet adja vissza.</span><span class="sxs-lookup"><span data-stu-id="6b63f-124">If you do not specify a filter, all pools under the Batch account specified with the *BatchContext* parameter are returned.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b63f-125">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="6b63f-125">-Id</span></span>
<span data-ttu-id="6b63f-126">A beolvasott készlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b63f-126">Specifies the ID of the pool to get.</span></span>
<span data-ttu-id="6b63f-127">A helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="6b63f-127">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b63f-128">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="6b63f-128">-MaxCount</span></span>
<span data-ttu-id="6b63f-129">A visszaadható készletek maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b63f-129">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="6b63f-130">Ha a nulla (0) vagy annál kisebb értéket adja meg, a parancsmag nem használ felső határértéket.</span><span class="sxs-lookup"><span data-stu-id="6b63f-130">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="6b63f-131">Az alapértelmezett érték a 1000.</span><span class="sxs-lookup"><span data-stu-id="6b63f-131">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b63f-132">-Válassza a</span><span class="sxs-lookup"><span data-stu-id="6b63f-132">-Select</span></span>
<span data-ttu-id="6b63f-133">Egy OData Select záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="6b63f-133">Specifies an OData select clause.</span></span>
<span data-ttu-id="6b63f-134">Adjon meg egy értéket ehhez a paraméterhez, ha konkrét tulajdonságokat szeretne beszerezni az objektum összes tulajdonsága helyett.</span><span class="sxs-lookup"><span data-stu-id="6b63f-134">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="6b63f-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b63f-135">-DefaultProfile</span></span>
<span data-ttu-id="6b63f-136">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b63f-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b63f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b63f-137">CommonParameters</span></span>
<span data-ttu-id="6b63f-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6b63f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b63f-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b63f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b63f-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b63f-140">INPUTS</span></span>

### <span data-ttu-id="6b63f-141">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6b63f-141">BatchAccountContext</span></span>
<span data-ttu-id="6b63f-142">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="6b63f-142">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="6b63f-143">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="6b63f-143">String</span></span>
<span data-ttu-id="6b63f-144">Az ' azonosító ' paraméter a pipeline "string" típusú értékét fogadja el.</span><span class="sxs-lookup"><span data-stu-id="6b63f-144">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="6b63f-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b63f-145">OUTPUTS</span></span>

### <span data-ttu-id="6b63f-146">PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="6b63f-146">PSCloudPool</span></span>

## <span data-ttu-id="6b63f-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6b63f-147">NOTES</span></span>

## <span data-ttu-id="6b63f-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b63f-148">RELATED LINKS</span></span>

[<span data-ttu-id="6b63f-149">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6b63f-149">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="6b63f-150">Új – AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="6b63f-150">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="6b63f-151">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="6b63f-151">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="6b63f-152">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="6b63f-152">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


