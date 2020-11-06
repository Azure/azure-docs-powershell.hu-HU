---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 44D877F1-D066-4C9C-A797-05EF03785B54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
ms.openlocfilehash: 2bd84d8e5d0f48c5b9a3af65944ece99369270c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493273"
---
# <span data-ttu-id="47ace-101">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="47ace-101">Get-AzureBatchPool</span></span>

## <span data-ttu-id="47ace-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="47ace-102">SYNOPSIS</span></span>
<span data-ttu-id="47ace-103">A megadott köteg fiók alatti köteg-gyűjtőket kap.</span><span class="sxs-lookup"><span data-stu-id="47ace-103">Gets Batch pools under the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47ace-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="47ace-104">SYNTAX</span></span>

### <span data-ttu-id="47ace-105">ODataFilter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="47ace-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchPool [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47ace-106">Azonosító</span><span class="sxs-lookup"><span data-stu-id="47ace-106">Id</span></span>
```
Get-AzureBatchPool [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47ace-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="47ace-107">DESCRIPTION</span></span>
<span data-ttu-id="47ace-108">A **Get-AzureBatchPool** parancsmag a *BatchContext* paraméterrel megadott köteg fiók alatt kapja meg az Azure batch-készleteket.</span><span class="sxs-lookup"><span data-stu-id="47ace-108">The **Get-AzureBatchPool** cmdlet gets the Azure Batch pools under the Batch account specified with the *BatchContext* parameter.</span></span>
<span data-ttu-id="47ace-109">Az *ID* paraméterrel egyetlen készletet kaphat, vagy használhatja a *szűrő* paramétert az Open Data Protocol (OData) szűrővel egyező medencék beszerzésére.</span><span class="sxs-lookup"><span data-stu-id="47ace-109">You can use the *Id* parameter to get a single pool, or you can use the *Filter* parameter to get the pools that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="47ace-110">Példák</span><span class="sxs-lookup"><span data-stu-id="47ace-110">EXAMPLES</span></span>

### <span data-ttu-id="47ace-111">Példa 1: készlet beszerzése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="47ace-111">Example 1: Get a pool by ID</span></span>
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

<span data-ttu-id="47ace-112">Ez a parancs a medencét azonosító MyPool kapja.</span><span class="sxs-lookup"><span data-stu-id="47ace-112">This command gets the pool with ID MyPool.</span></span>

### <span data-ttu-id="47ace-113">2. példa: az összes készlet lekérése OData-szűrő használatával</span><span class="sxs-lookup"><span data-stu-id="47ace-113">Example 2: Get all pools using an OData filter</span></span>
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

<span data-ttu-id="47ace-114">Ez a parancs azokat a készleteket kapja meg, amelyek azonosítói a *szűrő* paraméterrel kezdődnek.</span><span class="sxs-lookup"><span data-stu-id="47ace-114">This command gets the pools whose IDs start with My by using the *Filter* parameter.</span></span>

## <span data-ttu-id="47ace-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="47ace-115">PARAMETERS</span></span>

### <span data-ttu-id="47ace-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="47ace-116">-BatchContext</span></span>
<span data-ttu-id="47ace-117">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="47ace-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="47ace-118">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="47ace-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="47ace-119">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="47ace-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="47ace-120">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="47ace-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="47ace-121">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="47ace-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47ace-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47ace-122">-DefaultProfile</span></span>
<span data-ttu-id="47ace-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="47ace-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47ace-124">– Kibontás</span><span class="sxs-lookup"><span data-stu-id="47ace-124">-Expand</span></span>
<span data-ttu-id="47ace-125">Az Open Data Protocol (OData) kibontási záradékát adja meg.</span><span class="sxs-lookup"><span data-stu-id="47ace-125">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="47ace-126">Adjon meg egy értéket ehhez a paraméterhez a fő entitáshoz tartozó társított entitások beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="47ace-126">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47ace-127">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="47ace-127">-Filter</span></span>
<span data-ttu-id="47ace-128">Megadja a OData-szűrési záradékot a medencék lekérdezéséhez.</span><span class="sxs-lookup"><span data-stu-id="47ace-128">Specifies the OData filter clause to use when querying for pools.</span></span>
<span data-ttu-id="47ace-129">Ha nem ad meg szűrőt, a függvény a *BatchContext* paraméterrel megadott köteg fiók alatti összes készletet adja vissza.</span><span class="sxs-lookup"><span data-stu-id="47ace-129">If you do not specify a filter, all pools under the Batch account specified with the *BatchContext* parameter are returned.</span></span>

```yaml
Type: String
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47ace-130">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="47ace-130">-Id</span></span>
<span data-ttu-id="47ace-131">A beolvasott készlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="47ace-131">Specifies the ID of the pool to get.</span></span>
<span data-ttu-id="47ace-132">A helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="47ace-132">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47ace-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="47ace-133">-MaxCount</span></span>
<span data-ttu-id="47ace-134">A visszaadható készletek maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="47ace-134">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="47ace-135">Ha a nulla (0) vagy annál kisebb értéket adja meg, a parancsmag nem használ felső határértéket.</span><span class="sxs-lookup"><span data-stu-id="47ace-135">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="47ace-136">Az alapértelmezett érték a 1000.</span><span class="sxs-lookup"><span data-stu-id="47ace-136">The default value is 1000.</span></span>

```yaml
Type: Int32
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47ace-137">-Válassza a</span><span class="sxs-lookup"><span data-stu-id="47ace-137">-Select</span></span>
<span data-ttu-id="47ace-138">Egy OData Select záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="47ace-138">Specifies an OData select clause.</span></span>
<span data-ttu-id="47ace-139">Adjon meg egy értéket ehhez a paraméterhez, ha konkrét tulajdonságokat szeretne beszerezni az objektum összes tulajdonsága helyett.</span><span class="sxs-lookup"><span data-stu-id="47ace-139">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47ace-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47ace-140">CommonParameters</span></span>
<span data-ttu-id="47ace-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="47ace-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47ace-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47ace-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47ace-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="47ace-143">INPUTS</span></span>

### <span data-ttu-id="47ace-144">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="47ace-144">BatchAccountContext</span></span>
<span data-ttu-id="47ace-145">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="47ace-145">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="47ace-146">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="47ace-146">String</span></span>
<span data-ttu-id="47ace-147">Az ' azonosító ' paraméter a pipeline "string" típusú értékét fogadja el.</span><span class="sxs-lookup"><span data-stu-id="47ace-147">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="47ace-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47ace-148">OUTPUTS</span></span>

### <span data-ttu-id="47ace-149">PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="47ace-149">PSCloudPool</span></span>

## <span data-ttu-id="47ace-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="47ace-150">NOTES</span></span>

## <span data-ttu-id="47ace-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47ace-151">RELATED LINKS</span></span>

[<span data-ttu-id="47ace-152">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="47ace-152">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="47ace-153">Új – AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="47ace-153">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="47ace-154">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="47ace-154">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="47ace-155">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="47ace-155">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


