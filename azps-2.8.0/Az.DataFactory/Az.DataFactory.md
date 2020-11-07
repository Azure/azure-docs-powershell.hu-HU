---
Module Name: Az.DataFactory
Module Guid: e3c0f6bc-fe96-41a0-88f4-5e490a91f05d
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.datafactory
Help Version: 0.5.3.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Az.DataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Az.DataFactory.md
ms.openlocfilehash: 8fccc742860bf66016470826b2e837747306514a
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/15/2019
ms.locfileid: "93665482"
---
# <span data-ttu-id="ab279-101">Az. DataFactory modul</span><span class="sxs-lookup"><span data-stu-id="ab279-101">Az.DataFactory Module</span></span>
## <span data-ttu-id="ab279-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="ab279-102">Description</span></span>
<span data-ttu-id="ab279-103">Az Azure Data Factory v2 az adatintegrációs platform, amely túllép az Azure Data Factory V1's és az idősorozatos naplózási adatok kötegelt feldolgozásán, valamint a modern adatraktározási minták és forgatókönyvek, a lift és a műszak SSIS, valamint az adatalapú SaaS-alkalmazások támogatásához szükséges általános célú app-modellt.</span><span class="sxs-lookup"><span data-stu-id="ab279-103">Azure Data Factory V2 is the data integration platform that goes beyond Azure Data Factory V1's orchestration and batch-processing of time-series log data, with a general purpose app model supporting modern data warehousing patterns and scenarios, lift-and-shift SSIS, and data-driven SaaS applications.</span></span> <span data-ttu-id="ab279-104">Megbízható és biztonságos adatintegrációs munkafolyamatok írása és kezelése a méretarányban.</span><span class="sxs-lookup"><span data-stu-id="ab279-104">Compose and manage reliable and secure data integration workflows at scale.</span></span> <span data-ttu-id="ab279-105">Natív ADF-adatösszekötők és-integrációs futtatókörnyezetek segítségével áthelyezheti és átalakíthatja a Felhőbeli és a helyszíni adatforrásokat, amelyek strukturálatlan, félig strukturált és strukturált Hadoop, Azure Data Lake, Spark, SQL Server, Cosmos DB és sok más adatplatformmal is használhatók.</span><span class="sxs-lookup"><span data-stu-id="ab279-105">Use native ADF data connectors and Integration Runtimes to move and transform cloud and on-premises data that can be unstructured, semi-structured, and structured with Hadoop, Azure Data Lake, Spark, SQL Server, Cosmos DB and many other data platforms.</span></span>

## <span data-ttu-id="ab279-106">Az. DataFactory parancsmagok</span><span class="sxs-lookup"><span data-stu-id="ab279-106">Az.DataFactory Cmdlets</span></span>
### [<span data-ttu-id="ab279-107">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="ab279-107">Get-AzDataFactory</span></span>](Get-AzDataFactory.md)
<span data-ttu-id="ab279-108">Információt kap az adatgyárakról.</span><span class="sxs-lookup"><span data-stu-id="ab279-108">Gets information about Data Factories.</span></span>

### [<span data-ttu-id="ab279-109">Get-AzDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="ab279-109">Get-AzDataFactoryActivityWindow</span></span>](Get-AzDataFactoryActivityWindow.md)
<span data-ttu-id="ab279-110">Információt kap az adatgyárhoz társított tevékenység-ablakokról.</span><span class="sxs-lookup"><span data-stu-id="ab279-110">Gets information about activity windows associated with a data factory.</span></span>

### [<span data-ttu-id="ab279-111">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="ab279-111">Get-AzDataFactoryDataset</span></span>](Get-AzDataFactoryDataset.md)
<span data-ttu-id="ab279-112">Információt kap az adatkészletekről az Azure Data Factory-ban.</span><span class="sxs-lookup"><span data-stu-id="ab279-112">Gets information about datasets in Azure Data Factory.</span></span>

### [<span data-ttu-id="ab279-113">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="ab279-113">Get-AzDataFactoryGateway</span></span>](Get-AzDataFactoryGateway.md)
<span data-ttu-id="ab279-114">Információt kap az Azure Data Factory logikai átjáróról.</span><span class="sxs-lookup"><span data-stu-id="ab279-114">Gets information about logical gateways in Azure Data Factory.</span></span>

### [<span data-ttu-id="ab279-115">Get-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="ab279-115">Get-AzDataFactoryGatewayAuthKey</span></span>](Get-AzDataFactoryGatewayAuthKey.md)
<span data-ttu-id="ab279-116">Az Azure Data Factory átjáró Auth kulcsát kapja.</span><span class="sxs-lookup"><span data-stu-id="ab279-116">Gets gateway auth key for an Azure Data Factory.</span></span>

### [<span data-ttu-id="ab279-117">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="ab279-117">Get-AzDataFactoryHub</span></span>](Get-AzDataFactoryHub.md)
<span data-ttu-id="ab279-118">Információt kap az Azure Data Factory hubokról.</span><span class="sxs-lookup"><span data-stu-id="ab279-118">Gets information about hubs in Azure Data Factory.</span></span>

### [<span data-ttu-id="ab279-119">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="ab279-119">Get-AzDataFactoryLinkedService</span></span>](Get-AzDataFactoryLinkedService.md)
<span data-ttu-id="ab279-120">Információt kap az Azure Data Factory kapcsolt szolgáltatásairól.</span><span class="sxs-lookup"><span data-stu-id="ab279-120">Gets information about linked services in Azure Data Factory.</span></span>

### [<span data-ttu-id="ab279-121">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="ab279-121">Get-AzDataFactoryPipeline</span></span>](Get-AzDataFactoryPipeline.md)
<span data-ttu-id="ab279-122">Információt kap a csővezetékekről az Azure Data Factory-ban.</span><span class="sxs-lookup"><span data-stu-id="ab279-122">Gets information about pipelines in Azure Data Factory.</span></span>

### [<span data-ttu-id="ab279-123">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="ab279-123">Get-AzDataFactoryRun</span></span>](Get-AzDataFactoryRun.md)
<span data-ttu-id="ab279-124">Az Azure Data Factory-ban az adatkészletek adatszeleteit futtatja.</span><span class="sxs-lookup"><span data-stu-id="ab279-124">Gets runs for a data slice of a dataset in Azure Data Factory.</span></span>

### [<span data-ttu-id="ab279-125">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="ab279-125">Get-AzDataFactorySlice</span></span>](Get-AzDataFactorySlice.md)
<span data-ttu-id="ab279-126">Adatszeletek beolvasása adatkészlethez az Azure Data Factory-ban</span><span class="sxs-lookup"><span data-stu-id="ab279-126">Gets data slices for a dataset in Azure Data Factory.</span></span>

### [<span data-ttu-id="ab279-127">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ab279-127">Get-AzDataFactoryV2</span></span>](Get-AzDataFactoryV2.md)
<span data-ttu-id="ab279-128">Információt kap az adatgyárról.</span><span class="sxs-lookup"><span data-stu-id="ab279-128">Gets information about Data Factory.</span></span>

### [<span data-ttu-id="ab279-129">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="ab279-129">Get-AzDataFactoryV2ActivityRun</span></span>](Get-AzDataFactoryV2ActivityRun.md)
<span data-ttu-id="ab279-130">A tevékenységekről szóló információkat a csővezeték-futás során futtatja.</span><span class="sxs-lookup"><span data-stu-id="ab279-130">Gets information about activity runs for a pipeline run.</span></span>

### [<span data-ttu-id="ab279-131">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="ab279-131">Get-AzDataFactoryV2Dataset</span></span>](Get-AzDataFactoryV2Dataset.md)
<span data-ttu-id="ab279-132">Információt kap az adatfeldolgozó-adatkészletekről.</span><span class="sxs-lookup"><span data-stu-id="ab279-132">Gets information about datasets in Data Factory.</span></span>

### [<span data-ttu-id="ab279-133">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ab279-133">Get-AzDataFactoryV2IntegrationRuntime</span></span>](Get-AzDataFactoryV2IntegrationRuntime.md)
<span data-ttu-id="ab279-134">Információt kap az integrációs futtatókörnyezet erőforrásairól.</span><span class="sxs-lookup"><span data-stu-id="ab279-134">Gets information about integration runtime resources.</span></span>

### [<span data-ttu-id="ab279-135">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="ab279-135">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>](Get-AzDataFactoryV2IntegrationRuntimeKey.md)
<span data-ttu-id="ab279-136">Egy önállóan működtetett integrációs futásidejű kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="ab279-136">Gets keys for a self-hosted integration runtime.</span></span>

### [<span data-ttu-id="ab279-137">Get-AzDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="ab279-137">Get-AzDataFactoryV2IntegrationRuntimeMetric</span></span>](Get-AzDataFactoryV2IntegrationRuntimeMetric.md)
<span data-ttu-id="ab279-138">Az integrációs futtatókörnyezet metrikus adatait kapja.</span><span class="sxs-lookup"><span data-stu-id="ab279-138">Gets metric data for an integration runtime.</span></span> 

### [<span data-ttu-id="ab279-139">Get-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="ab279-139">Get-AzDataFactoryV2IntegrationRuntimeNode</span></span>](Get-AzDataFactoryV2IntegrationRuntimeNode.md)
<span data-ttu-id="ab279-140">Beolvassa az integrációs futtatókörnyezet csomópontjának adatait.</span><span class="sxs-lookup"><span data-stu-id="ab279-140">Gets an integration runtime node information.</span></span>

### [<span data-ttu-id="ab279-141">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="ab279-141">Get-AzDataFactoryV2LinkedService</span></span>](Get-AzDataFactoryV2LinkedService.md)
<span data-ttu-id="ab279-142">Információt kap az adatfeldolgozó kapcsolt szolgáltatásairól.</span><span class="sxs-lookup"><span data-stu-id="ab279-142">Gets information about linked services in Data Factory.</span></span>

### [<span data-ttu-id="ab279-143">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="ab279-143">Get-AzDataFactoryV2Pipeline</span></span>](Get-AzDataFactoryV2Pipeline.md)
<span data-ttu-id="ab279-144">Információt kap az adatfeldolgozási folyamatokról.</span><span class="sxs-lookup"><span data-stu-id="ab279-144">Gets information about pipelines in Data Factory.</span></span>

### [<span data-ttu-id="ab279-145">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="ab279-145">Get-AzDataFactoryV2PipelineRun</span></span>](Get-AzDataFactoryV2PipelineRun.md)
<span data-ttu-id="ab279-146">Információt kap a csővezetékről.</span><span class="sxs-lookup"><span data-stu-id="ab279-146">Gets information about pipeline runs.</span></span>

### [<span data-ttu-id="ab279-147">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="ab279-147">Get-AzDataFactoryV2Trigger</span></span>](Get-AzDataFactoryV2Trigger.md)
<span data-ttu-id="ab279-148">Információt kap az eseményindítókkal kapcsolatban az adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="ab279-148">Gets information about triggers in a data factory.</span></span>

### [<span data-ttu-id="ab279-149">Get-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="ab279-149">Get-AzDataFactoryV2TriggerRun</span></span>](Get-AzDataFactoryV2TriggerRun.md)
<span data-ttu-id="ab279-150">Információt ad az indításról.</span><span class="sxs-lookup"><span data-stu-id="ab279-150">Returns information about trigger runs.</span></span>

### [<span data-ttu-id="ab279-151">Meghívó-AzDataFactoryV2IntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="ab279-151">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span></span>](Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md)
<span data-ttu-id="ab279-152">Önkiszolgáló integrációs futtatókörnyezet frissítése</span><span class="sxs-lookup"><span data-stu-id="ab279-152">Upgrades self-hosted integration runtime.</span></span>

### [<span data-ttu-id="ab279-153">Meghívó-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="ab279-153">Invoke-AzDataFactoryV2Pipeline</span></span>](Invoke-AzDataFactoryV2Pipeline.md)
  <span data-ttu-id="ab279-154">Arra hívja fel a futószalagot, hogy indítsa el a futtatását.</span><span class="sxs-lookup"><span data-stu-id="ab279-154">Invokes a pipeline to start a run for it.</span></span>

### [<span data-ttu-id="ab279-155">Új – AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="ab279-155">New-AzDataFactory</span></span>](New-AzDataFactory.md)
<span data-ttu-id="ab279-156">Adatfeldolgozót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ab279-156">Creates a data factory.</span></span>

### [<span data-ttu-id="ab279-157">Új – AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="ab279-157">New-AzDataFactoryDataset</span></span>](New-AzDataFactoryDataset.md)
<span data-ttu-id="ab279-158">Adatkészletet hoz létre az adatfeldolgozóban.</span><span class="sxs-lookup"><span data-stu-id="ab279-158">Creates a dataset in Data Factory.</span></span>

### [<span data-ttu-id="ab279-159">Új – AzDataFactoryEncryptValue</span><span class="sxs-lookup"><span data-stu-id="ab279-159">New-AzDataFactoryEncryptValue</span></span>](New-AzDataFactoryEncryptValue.md)
<span data-ttu-id="ab279-160">A bizalmas adatokat titkosítja.</span><span class="sxs-lookup"><span data-stu-id="ab279-160">Encrypts sensitive data.</span></span>

### [<span data-ttu-id="ab279-161">Új – AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="ab279-161">New-AzDataFactoryGateway</span></span>](New-AzDataFactoryGateway.md)
<span data-ttu-id="ab279-162">Átjárót hoz létre egy Azure Data Factory számára.</span><span class="sxs-lookup"><span data-stu-id="ab279-162">Creates a gateway for an Azure Data Factory.</span></span>

### [<span data-ttu-id="ab279-163">Új – AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="ab279-163">New-AzDataFactoryGatewayAuthKey</span></span>](New-AzDataFactoryGatewayAuthKey.md)
<span data-ttu-id="ab279-164">Hitelesítő kulcs létrehozása Azure Data Factory átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="ab279-164">Creates auth key for an Azure Data Factory Gateway.</span></span>

### [<span data-ttu-id="ab279-165">Új – AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="ab279-165">New-AzDataFactoryHub</span></span>](New-AzDataFactoryHub.md)
<span data-ttu-id="ab279-166">Az Azure Data Factory hub-t hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ab279-166">Creates a hub for an Azure Data Factory.</span></span>

### [<span data-ttu-id="ab279-167">Új – AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="ab279-167">New-AzDataFactoryLinkedService</span></span>](New-AzDataFactoryLinkedService.md)
<span data-ttu-id="ab279-168">Az adattárolók vagy a Felhőbeli szolgáltatások kapcsolata az Azure Data Factory szolgáltatással.</span><span class="sxs-lookup"><span data-stu-id="ab279-168">Links a data store or a cloud service to an Azure Data Factory.</span></span>

### [<span data-ttu-id="ab279-169">Új – AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="ab279-169">New-AzDataFactoryPipeline</span></span>](New-AzDataFactoryPipeline.md)
<span data-ttu-id="ab279-170">Futószalagot hoz létre az adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="ab279-170">Creates a pipeline in Data Factory.</span></span>

### [<span data-ttu-id="ab279-171">Új – AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="ab279-171">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>](New-AzDataFactoryV2IntegrationRuntimeKey.md)
<span data-ttu-id="ab279-172">Önkiszolgáló integrációs futásidejű kulcs újbóli létrehozása</span><span class="sxs-lookup"><span data-stu-id="ab279-172">Regenerate self-hosted integration runtime key.</span></span>

### [<span data-ttu-id="ab279-173">Új – AzDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="ab279-173">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span></span>](New-AzDataFactoryV2LinkedServiceEncryptedCredential.md)
<span data-ttu-id="ab279-174">Hitelesítő adatok titkosítása a kapcsolódó szolgáltatásban meghatározott integrációs futtatókörnyezettel.</span><span class="sxs-lookup"><span data-stu-id="ab279-174">Encrypt credential in linked service with specified integration runtime.</span></span>

### [<span data-ttu-id="ab279-175">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="ab279-175">Remove-AzDataFactory</span></span>](Remove-AzDataFactory.md)
<span data-ttu-id="ab279-176">Az adatfeldolgozó eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="ab279-176">Removes a data factory.</span></span>

### [<span data-ttu-id="ab279-177">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="ab279-177">Remove-AzDataFactoryDataset</span></span>](Remove-AzDataFactoryDataset.md)
<span data-ttu-id="ab279-178">Az Azure Data Factory adatkészletének eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="ab279-178">Removes a dataset from Azure Data Factory.</span></span>

### [<span data-ttu-id="ab279-179">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="ab279-179">Remove-AzDataFactoryGateway</span></span>](Remove-AzDataFactoryGateway.md)
<span data-ttu-id="ab279-180">Átjáró eltávolítása az Azure Data Factory programból.</span><span class="sxs-lookup"><span data-stu-id="ab279-180">Removes a gateway from Azure Data Factory.</span></span>

### [<span data-ttu-id="ab279-181">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="ab279-181">Remove-AzDataFactoryHub</span></span>](Remove-AzDataFactoryHub.md)
<span data-ttu-id="ab279-182">A hub eltávolítása az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="ab279-182">Removes a hub from Azure Data Factory.</span></span>

### [<span data-ttu-id="ab279-183">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="ab279-183">Remove-AzDataFactoryLinkedService</span></span>](Remove-AzDataFactoryLinkedService.md)
<span data-ttu-id="ab279-184">Egy kapcsolt szolgáltatás eltávolítása az Azure Data Factory alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="ab279-184">Removes a linked service from Azure Data Factory.</span></span>

### [<span data-ttu-id="ab279-185">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="ab279-185">Remove-AzDataFactoryPipeline</span></span>](Remove-AzDataFactoryPipeline.md)
<span data-ttu-id="ab279-186">Az Azure Data Factory futószalagjának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="ab279-186">Removes a pipeline from Azure Data Factory.</span></span>

### [<span data-ttu-id="ab279-187">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ab279-187">Remove-AzDataFactoryV2</span></span>](Remove-AzDataFactoryV2.md)
<span data-ttu-id="ab279-188">Az adatfeldolgozó eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="ab279-188">Removes a data factory.</span></span>

### [<span data-ttu-id="ab279-189">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="ab279-189">Remove-AzDataFactoryV2Dataset</span></span>](Remove-AzDataFactoryV2Dataset.md)
<span data-ttu-id="ab279-190">Adatkészlet eltávolítása az adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="ab279-190">Removes a dataset from Data Factory.</span></span>

### [<span data-ttu-id="ab279-191">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ab279-191">Remove-AzDataFactoryV2IntegrationRuntime</span></span>](Remove-AzDataFactoryV2IntegrationRuntime.md)
<span data-ttu-id="ab279-192">Az integrációs futtatókörnyezet eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="ab279-192">Removes an integration runtime.</span></span>

### [<span data-ttu-id="ab279-193">Remove-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="ab279-193">Remove-AzDataFactoryV2IntegrationRuntimeNode</span></span>](Remove-AzDataFactoryV2IntegrationRuntimeNode.md)
<span data-ttu-id="ab279-194">A megadott nevű csomópont eltávolítása az integrációs futtatókörnyezetben.</span><span class="sxs-lookup"><span data-stu-id="ab279-194">Remove a node with the given name on an integration runtime.</span></span>

### [<span data-ttu-id="ab279-195">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="ab279-195">Remove-AzDataFactoryV2LinkedService</span></span>](Remove-AzDataFactoryV2LinkedService.md)
<span data-ttu-id="ab279-196">Egy kapcsolt szolgáltatás eltávolítása az adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="ab279-196">Removes a linked service from Data Factory.</span></span>

### [<span data-ttu-id="ab279-197">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="ab279-197">Remove-AzDataFactoryV2Pipeline</span></span>](Remove-AzDataFactoryV2Pipeline.md)
<span data-ttu-id="ab279-198">Csővezeték eltávolítása az adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="ab279-198">Removes a pipeline from Data Factory.</span></span>

### [<span data-ttu-id="ab279-199">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="ab279-199">Remove-AzDataFactoryV2Trigger</span></span>](Remove-AzDataFactoryV2Trigger.md)
<span data-ttu-id="ab279-200">Az indítót eltávolítja az adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="ab279-200">Removes a trigger from a data factory.</span></span>

### [<span data-ttu-id="ab279-201">Önéletrajz – AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="ab279-201">Resume-AzDataFactoryPipeline</span></span>](Resume-AzDataFactoryPipeline.md)
<span data-ttu-id="ab279-202">Felfüggesztett csővezeték folytatása az adatfeldolgozóban.</span><span class="sxs-lookup"><span data-stu-id="ab279-202">Resumes a suspended pipeline in Data Factory.</span></span>

### [<span data-ttu-id="ab279-203">Mentés-AzDataFactoryLog</span><span class="sxs-lookup"><span data-stu-id="ab279-203">Save-AzDataFactoryLog</span></span>](Save-AzDataFactoryLog.md)
<span data-ttu-id="ab279-204">Az Azure HDInsight-feldolgozásból letölthető naplófájlok.</span><span class="sxs-lookup"><span data-stu-id="ab279-204">Downloads log files from Azure HDInsight processing.</span></span>

### [<span data-ttu-id="ab279-205">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="ab279-205">Set-AzDataFactoryGateway</span></span>](Set-AzDataFactoryGateway.md)
<span data-ttu-id="ab279-206">Az Azure Data Factory átjárójának leírását állítja be.</span><span class="sxs-lookup"><span data-stu-id="ab279-206">Sets the description for a gateway in Azure Data Factory.</span></span>

### [<span data-ttu-id="ab279-207">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="ab279-207">Set-AzDataFactoryPipelineActivePeriod</span></span>](Set-AzDataFactoryPipelineActivePeriod.md)
<span data-ttu-id="ab279-208">Az adatszeletek aktív időszakának beállítása.</span><span class="sxs-lookup"><span data-stu-id="ab279-208">Configures the active period for data slices.</span></span>

### [<span data-ttu-id="ab279-209">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="ab279-209">Set-AzDataFactorySliceStatus</span></span>](Set-AzDataFactorySliceStatus.md)
<span data-ttu-id="ab279-210">A szeletek állapotát állítja be egy adatkészlethez az Azure Data Factory-ban.</span><span class="sxs-lookup"><span data-stu-id="ab279-210">Sets the status of slices for a dataset in Azure Data Factory.</span></span>

### [<span data-ttu-id="ab279-211">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ab279-211">Set-AzDataFactoryV2</span></span>](Set-AzDataFactoryV2.md)
<span data-ttu-id="ab279-212">Adatfeldolgozót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ab279-212">Creates a data factory.</span></span>

### [<span data-ttu-id="ab279-213">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="ab279-213">Set-AzDataFactoryV2Dataset</span></span>](Set-AzDataFactoryV2Dataset.md)
<span data-ttu-id="ab279-214">Adatkészletet hoz létre az adatfeldolgozóban.</span><span class="sxs-lookup"><span data-stu-id="ab279-214">Creates a dataset in Data Factory.</span></span>

### [<span data-ttu-id="ab279-215">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ab279-215">Set-AzDataFactoryV2IntegrationRuntime</span></span>](Set-AzDataFactoryV2IntegrationRuntime.md)
<span data-ttu-id="ab279-216">Az integrációs futtatókörnyezet frissítése</span><span class="sxs-lookup"><span data-stu-id="ab279-216">Updates an integration runtime.</span></span>

### [<span data-ttu-id="ab279-217">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="ab279-217">Set-AzDataFactoryV2LinkedService</span></span>](Set-AzDataFactoryV2LinkedService.md)
<span data-ttu-id="ab279-218">Az adattárolók vagy a Felhőbeli szolgáltatások összekapcsolása az adatfeldolgozó szolgáltatással.</span><span class="sxs-lookup"><span data-stu-id="ab279-218">Links a data store or a cloud service to Data Factory.</span></span>

### [<span data-ttu-id="ab279-219">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="ab279-219">Set-AzDataFactoryV2Pipeline</span></span>](Set-AzDataFactoryV2Pipeline.md)
<span data-ttu-id="ab279-220">Futószalagot hoz létre az adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="ab279-220">Creates a pipeline in Data Factory.</span></span>

### [<span data-ttu-id="ab279-221">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="ab279-221">Set-AzDataFactoryV2Trigger</span></span>](Set-AzDataFactoryV2Trigger.md)
<span data-ttu-id="ab279-222">Triggert hoz létre egy adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="ab279-222">Creates a trigger in a data factory.</span></span>

### [<span data-ttu-id="ab279-223">Start-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ab279-223">Start-AzDataFactoryV2IntegrationRuntime</span></span>](Start-AzDataFactoryV2IntegrationRuntime.md)
<span data-ttu-id="ab279-224">Felügyelt dedikált integrációs futtatókörnyezetet indít el.</span><span class="sxs-lookup"><span data-stu-id="ab279-224">Starts a managed dedicated integration runtime.</span></span>

### [<span data-ttu-id="ab279-225">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="ab279-225">Start-AzDataFactoryV2Trigger</span></span>](Start-AzDataFactoryV2Trigger.md)
<span data-ttu-id="ab279-226">Indítót indít az adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="ab279-226">Starts a trigger in a data factory.</span></span>

### [<span data-ttu-id="ab279-227">Stop-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ab279-227">Stop-AzDataFactoryV2IntegrationRuntime</span></span>](Stop-AzDataFactoryV2IntegrationRuntime.md)
<span data-ttu-id="ab279-228">Felügyelt dedikált integrációs futtatókörnyezetet állít be.</span><span class="sxs-lookup"><span data-stu-id="ab279-228">Stops a managed dedicated integration runtime.</span></span>

### [<span data-ttu-id="ab279-229">Stop-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="ab279-229">Stop-AzDataFactoryV2PipelineRun</span></span>](Stop-AzDataFactoryV2PipelineRun.md)
<span data-ttu-id="ab279-230">Az adatgyárban futó csővezeték leállítása</span><span class="sxs-lookup"><span data-stu-id="ab279-230">Stops a pipeline run in a data factory.</span></span>

### [<span data-ttu-id="ab279-231">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="ab279-231">Stop-AzDataFactoryV2Trigger</span></span>](Stop-AzDataFactoryV2Trigger.md)
<span data-ttu-id="ab279-232">Az adatgyárban lévő trigger leállítása</span><span class="sxs-lookup"><span data-stu-id="ab279-232">Stops a trigger in a data factory.</span></span>

### [<span data-ttu-id="ab279-233">Felfüggesztés – AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="ab279-233">Suspend-AzDataFactoryPipeline</span></span>](Suspend-AzDataFactoryPipeline.md)
<span data-ttu-id="ab279-234">Az Azure Data Factory csővezetékének felfüggesztése</span><span class="sxs-lookup"><span data-stu-id="ab279-234">Suspends a pipeline in Azure Data Factory.</span></span>

### [<span data-ttu-id="ab279-235">Szinkronizálás – AzDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="ab279-235">Sync-AzDataFactoryV2IntegrationRuntimeCredential</span></span>](Sync-AzDataFactoryV2IntegrationRuntimeCredential.md)
<span data-ttu-id="ab279-236">Szinkronizálja a hitelesítő adatokat az integrációs futásidejű csomópontok között.</span><span class="sxs-lookup"><span data-stu-id="ab279-236">Synchronizes credentials among integration runtime nodes.</span></span>

### [<span data-ttu-id="ab279-237">Update-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ab279-237">Update-AzDataFactoryV2</span></span>](Update-AzDataFactoryV2.md)
<span data-ttu-id="ab279-238">Frissíti az adattípusok tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="ab279-238">Updates the properties of a data factory.</span></span>

### [<span data-ttu-id="ab279-239">Update-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ab279-239">Update-AzDataFactoryV2IntegrationRuntime</span></span>](Update-AzDataFactoryV2IntegrationRuntime.md)
<span data-ttu-id="ab279-240">Az integrációs futtatókörnyezet frissítése</span><span class="sxs-lookup"><span data-stu-id="ab279-240">Updates an integration runtime.</span></span>

### [<span data-ttu-id="ab279-241">Update-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="ab279-241">Update-AzDataFactoryV2IntegrationRuntimeNode</span></span>](Update-AzDataFactoryV2IntegrationRuntimeNode.md)
<span data-ttu-id="ab279-242">Frissítheti az önkiszolgáló integrációs futásidejű csomópontot.</span><span class="sxs-lookup"><span data-stu-id="ab279-242">Updates self-hosted integration runtime node.</span></span>

