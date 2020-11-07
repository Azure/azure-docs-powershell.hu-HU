---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 44D877F1-D066-4C9C-A797-05EF03785B54
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPool.md
ms.openlocfilehash: a94b4b8bee590fa31972d2b80c9c3f2d06c566e6
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847909"
---
# <span data-ttu-id="85a1b-101">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="85a1b-101">Get-AzBatchPool</span></span>

## <span data-ttu-id="85a1b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="85a1b-102">SYNOPSIS</span></span>
<span data-ttu-id="85a1b-103">A megadott köteg fiók alatti köteg-gyűjtőket kap.</span><span class="sxs-lookup"><span data-stu-id="85a1b-103">Gets Batch pools under the specified Batch account.</span></span>

## <span data-ttu-id="85a1b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="85a1b-104">SYNTAX</span></span>

### <span data-ttu-id="85a1b-105">ODataFilter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="85a1b-105">ODataFilter (Default)</span></span>
```
Get-AzBatchPool [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85a1b-106">Azonosító</span><span class="sxs-lookup"><span data-stu-id="85a1b-106">Id</span></span>
```
Get-AzBatchPool [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85a1b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="85a1b-107">DESCRIPTION</span></span>
<span data-ttu-id="85a1b-108">A **Get-AzBatchPool** parancsmag a *BatchContext* paraméterrel megadott köteg fiók alatt kapja meg az Azure batch-készleteket.</span><span class="sxs-lookup"><span data-stu-id="85a1b-108">The **Get-AzBatchPool** cmdlet gets the Azure Batch pools under the Batch account specified with the *BatchContext* parameter.</span></span>
<span data-ttu-id="85a1b-109">Az *ID* paraméterrel egyetlen készletet kaphat, vagy használhatja a *szűrő* paramétert az Open Data Protocol (OData) szűrővel egyező medencék beszerzésére.</span><span class="sxs-lookup"><span data-stu-id="85a1b-109">You can use the *Id* parameter to get a single pool, or you can use the *Filter* parameter to get the pools that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="85a1b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="85a1b-110">EXAMPLES</span></span>

### <span data-ttu-id="85a1b-111">Példa 1: készlet beszerzése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="85a1b-111">Example 1: Get a pool by ID</span></span>
```
PS C:\>Get-AzBatchPool -Id "MyPool" -BatchContext $Context
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

<span data-ttu-id="85a1b-112">Ez a parancs a medencét azonosító MyPool kapja.</span><span class="sxs-lookup"><span data-stu-id="85a1b-112">This command gets the pool with ID MyPool.</span></span>

### <span data-ttu-id="85a1b-113">2. példa: az összes készlet lekérése OData-szűrő használatával</span><span class="sxs-lookup"><span data-stu-id="85a1b-113">Example 2: Get all pools using an OData filter</span></span>
```
PS C:\>Get-AzBatchPool -Filter "startswith(id,'My')" -BatchContext $Context
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

<span data-ttu-id="85a1b-114">Ez a parancs azokat a készleteket kapja meg, amelyek azonosítói a *szűrő* paraméterrel kezdődnek.</span><span class="sxs-lookup"><span data-stu-id="85a1b-114">This command gets the pools whose IDs start with My by using the *Filter* parameter.</span></span>

## <span data-ttu-id="85a1b-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="85a1b-115">PARAMETERS</span></span>

### <span data-ttu-id="85a1b-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="85a1b-116">-BatchContext</span></span>
<span data-ttu-id="85a1b-117">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="85a1b-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="85a1b-118">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="85a1b-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="85a1b-119">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="85a1b-119">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="85a1b-120">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="85a1b-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="85a1b-121">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="85a1b-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="85a1b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85a1b-122">-DefaultProfile</span></span>
<span data-ttu-id="85a1b-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="85a1b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85a1b-124">– Kibontás</span><span class="sxs-lookup"><span data-stu-id="85a1b-124">-Expand</span></span>
<span data-ttu-id="85a1b-125">Az Open Data Protocol (OData) kibontási záradékát adja meg.</span><span class="sxs-lookup"><span data-stu-id="85a1b-125">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="85a1b-126">Adjon meg egy értéket ehhez a paraméterhez a fő entitáshoz tartozó társított entitások beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="85a1b-126">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="85a1b-127">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="85a1b-127">-Filter</span></span>
<span data-ttu-id="85a1b-128">Megadja a OData-szűrési záradékot a medencék lekérdezéséhez.</span><span class="sxs-lookup"><span data-stu-id="85a1b-128">Specifies the OData filter clause to use when querying for pools.</span></span>
<span data-ttu-id="85a1b-129">Ha nem ad meg szűrőt, a függvény a *BatchContext* paraméterrel megadott köteg fiók alatti összes készletet adja vissza.</span><span class="sxs-lookup"><span data-stu-id="85a1b-129">If you do not specify a filter, all pools under the Batch account specified with the *BatchContext* parameter are returned.</span></span>

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

### <span data-ttu-id="85a1b-130">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="85a1b-130">-Id</span></span>
<span data-ttu-id="85a1b-131">A beolvasott készlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="85a1b-131">Specifies the ID of the pool to get.</span></span>
<span data-ttu-id="85a1b-132">A helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="85a1b-132">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="85a1b-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="85a1b-133">-MaxCount</span></span>
<span data-ttu-id="85a1b-134">A visszaadható készletek maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="85a1b-134">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="85a1b-135">Ha a nulla (0) vagy annál kisebb értéket adja meg, a parancsmag nem használ felső határértéket.</span><span class="sxs-lookup"><span data-stu-id="85a1b-135">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="85a1b-136">Az alapértelmezett érték a 1000.</span><span class="sxs-lookup"><span data-stu-id="85a1b-136">The default value is 1000.</span></span>

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

### <span data-ttu-id="85a1b-137">-Válassza a</span><span class="sxs-lookup"><span data-stu-id="85a1b-137">-Select</span></span>
<span data-ttu-id="85a1b-138">Egy OData Select záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="85a1b-138">Specifies an OData select clause.</span></span>
<span data-ttu-id="85a1b-139">Adjon meg egy értéket ehhez a paraméterhez, ha konkrét tulajdonságokat szeretne beszerezni az objektum összes tulajdonsága helyett.</span><span class="sxs-lookup"><span data-stu-id="85a1b-139">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="85a1b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85a1b-140">CommonParameters</span></span>
<span data-ttu-id="85a1b-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="85a1b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85a1b-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85a1b-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85a1b-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="85a1b-143">INPUTS</span></span>

### <span data-ttu-id="85a1b-144">System. String</span><span class="sxs-lookup"><span data-stu-id="85a1b-144">System.String</span></span>

### <span data-ttu-id="85a1b-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="85a1b-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="85a1b-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="85a1b-146">OUTPUTS</span></span>

### <span data-ttu-id="85a1b-147">Microsoft.Azure.Commands.BatCH. Modellek. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="85a1b-147">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

## <span data-ttu-id="85a1b-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="85a1b-148">NOTES</span></span>

## <span data-ttu-id="85a1b-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="85a1b-149">RELATED LINKS</span></span>

[<span data-ttu-id="85a1b-150">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="85a1b-150">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="85a1b-151">Új – AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="85a1b-151">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="85a1b-152">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="85a1b-152">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="85a1b-153">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="85a1b-153">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


