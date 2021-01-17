---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 44D877F1-D066-4C9C-A797-05EF03785B54
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPool.md
ms.openlocfilehash: f861397569671d5269e12edee564acdb55519977
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356452"
---
# <span data-ttu-id="8a5c7-101">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="8a5c7-101">Get-AzBatchPool</span></span>

## <span data-ttu-id="8a5c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a5c7-102">SYNOPSIS</span></span>
<span data-ttu-id="8a5c7-103">Kötegkészleteket kap a megadott Batch-fiók alatt.</span><span class="sxs-lookup"><span data-stu-id="8a5c7-103">Gets Batch pools under the specified Batch account.</span></span>

## <span data-ttu-id="8a5c7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8a5c7-104">SYNTAX</span></span>

### <span data-ttu-id="8a5c7-105">ODataFilter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8a5c7-105">ODataFilter (Default)</span></span>
```
Get-AzBatchPool [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a5c7-106">Azonosító</span><span class="sxs-lookup"><span data-stu-id="8a5c7-106">Id</span></span>
```
Get-AzBatchPool [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a5c7-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8a5c7-107">DESCRIPTION</span></span>
<span data-ttu-id="8a5c7-108">A **Get-AzBatchPool** parancsmag a BatchContext paraméterrel megadott Batch-fiók alatt kapja meg az *Azure Batch-kötegkészleteket.*</span><span class="sxs-lookup"><span data-stu-id="8a5c7-108">The **Get-AzBatchPool** cmdlet gets the Azure Batch pools under the Batch account specified with the *BatchContext* parameter.</span></span>
<span data-ttu-id="8a5c7-109">Az Azonosító  paramétert használva egyetlen készletet kaphat,  vagy a Szűrő paramétert használva lekértheti az OData-szűrőnek megfelelő készleteket.</span><span class="sxs-lookup"><span data-stu-id="8a5c7-109">You can use the *Id* parameter to get a single pool, or you can use the *Filter* parameter to get the pools that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="8a5c7-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8a5c7-110">EXAMPLES</span></span>

### <span data-ttu-id="8a5c7-111">1. példa: Készlet lekérte azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="8a5c7-111">Example 1: Get a pool by ID</span></span>
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
VirtualMachineSize                   : standard_d1_v2
```

<span data-ttu-id="8a5c7-112">Ez a parancs a készletet a Saját várólista azonosítóval kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8a5c7-112">This command gets the pool with ID MyPool.</span></span>

### <span data-ttu-id="8a5c7-113">2. példa: Az összes készlet lekérte az OData-szűrőt</span><span class="sxs-lookup"><span data-stu-id="8a5c7-113">Example 2: Get all pools using an OData filter</span></span>
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
VirtualMachineSize                   : standard_d1_v2
```

<span data-ttu-id="8a5c7-114">Ez a parancs a Szűrő paraméter használatával bekérte a Saját kezdetú adatokat használó *készleteket.*</span><span class="sxs-lookup"><span data-stu-id="8a5c7-114">This command gets the pools whose IDs start with My by using the *Filter* parameter.</span></span>

## <span data-ttu-id="8a5c7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a5c7-115">PARAMETERS</span></span>

### <span data-ttu-id="8a5c7-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8a5c7-116">-BatchContext</span></span>
<span data-ttu-id="8a5c7-117">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="8a5c7-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8a5c7-118">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="8a5c7-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8a5c7-119">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="8a5c7-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8a5c7-120">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="8a5c7-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8a5c7-121">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="8a5c7-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8a5c7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a5c7-122">-DefaultProfile</span></span>
<span data-ttu-id="8a5c7-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8a5c7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a5c7-124">-Kibontás</span><span class="sxs-lookup"><span data-stu-id="8a5c7-124">-Expand</span></span>
<span data-ttu-id="8a5c7-125">OData-kibontó záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="8a5c7-125">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="8a5c7-126">Adjon meg egy értéket a paraméterhez a bejő fő entitás társított entitásának lekérthez.</span><span class="sxs-lookup"><span data-stu-id="8a5c7-126">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="8a5c7-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="8a5c7-127">-Filter</span></span>
<span data-ttu-id="8a5c7-128">A készletek lekérdezéséhez használható OData-szűrő záradékot adja meg.</span><span class="sxs-lookup"><span data-stu-id="8a5c7-128">Specifies the OData filter clause to use when querying for pools.</span></span>
<span data-ttu-id="8a5c7-129">Ha nem ad meg szűrőt, a *BatchContext* paraméterrel megadott Batch-fiókban található összes készletet visszaadja a függvény.</span><span class="sxs-lookup"><span data-stu-id="8a5c7-129">If you do not specify a filter, all pools under the Batch account specified with the *BatchContext* parameter are returned.</span></span>

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

### <span data-ttu-id="8a5c7-130">-Id</span><span class="sxs-lookup"><span data-stu-id="8a5c7-130">-Id</span></span>
<span data-ttu-id="8a5c7-131">A lekért készlet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8a5c7-131">Specifies the ID of the pool to get.</span></span>
<span data-ttu-id="8a5c7-132">Helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="8a5c7-132">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="8a5c7-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="8a5c7-133">-MaxCount</span></span>
<span data-ttu-id="8a5c7-134">Azt adja meg, hogy legfeljebb hány készletet kell visszaadni.</span><span class="sxs-lookup"><span data-stu-id="8a5c7-134">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="8a5c7-135">Ha nullát (0) vagy kisebb értéket ad meg, a parancsmag nem használ felső korlátot.</span><span class="sxs-lookup"><span data-stu-id="8a5c7-135">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="8a5c7-136">Az alapértelmezett érték 1000.</span><span class="sxs-lookup"><span data-stu-id="8a5c7-136">The default value is 1000.</span></span>

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

### <span data-ttu-id="8a5c7-137">-Válassza a</span><span class="sxs-lookup"><span data-stu-id="8a5c7-137">-Select</span></span>
<span data-ttu-id="8a5c7-138">OData-választó záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="8a5c7-138">Specifies an OData select clause.</span></span>
<span data-ttu-id="8a5c7-139">A paraméter értékét megadva az összes objektumtulajdonság helyett konkrét tulajdonságokat kap.</span><span class="sxs-lookup"><span data-stu-id="8a5c7-139">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="8a5c7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a5c7-140">CommonParameters</span></span>
<span data-ttu-id="8a5c7-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a5c7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a5c7-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a5c7-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a5c7-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8a5c7-143">INPUTS</span></span>

### <span data-ttu-id="8a5c7-144">System.String</span><span class="sxs-lookup"><span data-stu-id="8a5c7-144">System.String</span></span>

### <span data-ttu-id="8a5c7-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8a5c7-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8a5c7-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a5c7-146">OUTPUTS</span></span>

### <span data-ttu-id="8a5c7-147">Microsoft.Azure.Commands.Bat. Models.PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="8a5c7-147">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

## <span data-ttu-id="8a5c7-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8a5c7-148">NOTES</span></span>

## <span data-ttu-id="8a5c7-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8a5c7-149">RELATED LINKS</span></span>

[<span data-ttu-id="8a5c7-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="8a5c7-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="8a5c7-151">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="8a5c7-151">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="8a5c7-152">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="8a5c7-152">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="8a5c7-153">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="8a5c7-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
