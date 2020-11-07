---
Module Name: Az.DataFactory
Module Guid: e3c0f6bc-fe96-41a0-88f4-5e490a91f05d
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.datafactory
Help Version: 0.5.3.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Az.DataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Az.DataFactory.md
ms.openlocfilehash: 8a7d51ac8d4c925b41a27c20ff26bd27fd929d23
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93657810"
---
# <span data-ttu-id="0a3b3-101">Az. DataFactory modul</span><span class="sxs-lookup"><span data-stu-id="0a3b3-101">Az.DataFactory Module</span></span>
## <span data-ttu-id="0a3b3-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="0a3b3-102">Description</span></span>
<span data-ttu-id="0a3b3-103">Az Azure Data Factory v2 az adatintegrációs platform, amely túllép az Azure Data Factory V1's és az idősorozatos naplózási adatok kötegelt feldolgozásán, valamint a modern adatraktározási minták és forgatókönyvek, a lift és a műszak SSIS, valamint az adatalapú SaaS-alkalmazások támogatásához szükséges általános célú app-modellt.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-103">Azure Data Factory V2 is the data integration platform that goes beyond Azure Data Factory V1's orchestration and batch-processing of time-series log data, with a general purpose app model supporting modern data warehousing patterns and scenarios, lift-and-shift SSIS, and data-driven SaaS applications.</span></span> <span data-ttu-id="0a3b3-104">Megbízható és biztonságos adatintegrációs munkafolyamatok írása és kezelése a méretarányban.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-104">Compose and manage reliable and secure data integration workflows at scale.</span></span> <span data-ttu-id="0a3b3-105">Natív ADF-adatösszekötők és-integrációs futtatókörnyezetek segítségével áthelyezheti és átalakíthatja a Felhőbeli és a helyszíni adatforrásokat, amelyek strukturálatlan, félig strukturált és strukturált Hadoop, Azure Data Lake, Spark, SQL Server, Cosmos DB és sok más adatplatformmal is használhatók.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-105">Use native ADF data connectors and Integration Runtimes to move and transform cloud and on-premises data that can be unstructured, semi-structured, and structured with Hadoop, Azure Data Lake, Spark, SQL Server, Cosmos DB and many other data platforms.</span></span>

## <span data-ttu-id="0a3b3-106">Az. DataFactory parancsmagok</span><span class="sxs-lookup"><span data-stu-id="0a3b3-106">Az.DataFactory Cmdlets</span></span>
### [<span data-ttu-id="0a3b3-107">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="0a3b3-107">Get-AzDataFactory</span></span>](Get-AzDataFactory.md)
<span data-ttu-id="0a3b3-108">Információt kap az adatgyárakról.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-108">Gets information about Data Factories.</span></span>

### [<span data-ttu-id="0a3b3-109">Get-AzDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="0a3b3-109">Get-AzDataFactoryActivityWindow</span></span>](Get-AzDataFactoryActivityWindow.md)
<span data-ttu-id="0a3b3-110">Információt kap az adatgyárhoz társított tevékenység-ablakokról.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-110">Gets information about activity windows associated with a data factory.</span></span>

### [<span data-ttu-id="0a3b3-111">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="0a3b3-111">Get-AzDataFactoryDataset</span></span>](Get-AzDataFactoryDataset.md)
<span data-ttu-id="0a3b3-112">Információt kap az adatkészletekről az Azure Data Factory-ban.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-112">Gets information about datasets in Azure Data Factory.</span></span>

### [<span data-ttu-id="0a3b3-113">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="0a3b3-113">Get-AzDataFactoryGateway</span></span>](Get-AzDataFactoryGateway.md)
<span data-ttu-id="0a3b3-114">Információt kap az Azure Data Factory logikai átjáróról.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-114">Gets information about logical gateways in Azure Data Factory.</span></span>

### [<span data-ttu-id="0a3b3-115">Get-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="0a3b3-115">Get-AzDataFactoryGatewayAuthKey</span></span>](Get-AzDataFactoryGatewayAuthKey.md)
<span data-ttu-id="0a3b3-116">Az Azure Data Factory átjáró Auth kulcsát kapja.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-116">Gets gateway auth key for an Azure Data Factory.</span></span>

### [<span data-ttu-id="0a3b3-117">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="0a3b3-117">Get-AzDataFactoryHub</span></span>](Get-AzDataFactoryHub.md)
<span data-ttu-id="0a3b3-118">Információt kap az Azure Data Factory hubokról.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-118">Gets information about hubs in Azure Data Factory.</span></span>

### [<span data-ttu-id="0a3b3-119">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="0a3b3-119">Get-AzDataFactoryLinkedService</span></span>](Get-AzDataFactoryLinkedService.md)
<span data-ttu-id="0a3b3-120">Információt kap az Azure Data Factory kapcsolt szolgáltatásairól.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-120">Gets information about linked services in Azure Data Factory.</span></span>

### [<span data-ttu-id="0a3b3-121">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="0a3b3-121">Get-AzDataFactoryPipeline</span></span>](Get-AzDataFactoryPipeline.md)
<span data-ttu-id="0a3b3-122">Információt kap a csővezetékekről az Azure Data Factory-ban.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-122">Gets information about pipelines in Azure Data Factory.</span></span>

### [<span data-ttu-id="0a3b3-123">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="0a3b3-123">Get-AzDataFactoryRun</span></span>](Get-AzDataFactoryRun.md)
<span data-ttu-id="0a3b3-124">Az Azure Data Factory-ban az adatkészletek adatszeleteit futtatja.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-124">Gets runs for a data slice of a dataset in Azure Data Factory.</span></span>

### [<span data-ttu-id="0a3b3-125">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="0a3b3-125">Get-AzDataFactorySlice</span></span>](Get-AzDataFactorySlice.md)
<span data-ttu-id="0a3b3-126">Adatszeletek beolvasása adatkészlethez az Azure Data Factory-ban</span><span class="sxs-lookup"><span data-stu-id="0a3b3-126">Gets data slices for a dataset in Azure Data Factory.</span></span>

### [<span data-ttu-id="0a3b3-127">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0a3b3-127">Get-AzDataFactoryV2</span></span>](Get-AzDataFactoryV2.md)
<span data-ttu-id="0a3b3-128">Információt kap az adatgyárról.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-128">Gets information about Data Factory.</span></span>

### [<span data-ttu-id="0a3b3-129">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="0a3b3-129">Get-AzDataFactoryV2ActivityRun</span></span>](Get-AzDataFactoryV2ActivityRun.md)
<span data-ttu-id="0a3b3-130">A tevékenységekről szóló információkat a csővezeték-futás során futtatja.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-130">Gets information about activity runs for a pipeline run.</span></span>

### [<span data-ttu-id="0a3b3-131">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="0a3b3-131">Get-AzDataFactoryV2Dataset</span></span>](Get-AzDataFactoryV2Dataset.md)
<span data-ttu-id="0a3b3-132">Információt kap az adatfeldolgozó-adatkészletekről.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-132">Gets information about datasets in Data Factory.</span></span>

### [<span data-ttu-id="0a3b3-133">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0a3b3-133">Get-AzDataFactoryV2IntegrationRuntime</span></span>](Get-AzDataFactoryV2IntegrationRuntime.md)
<span data-ttu-id="0a3b3-134">Információt kap az integrációs futtatókörnyezet erőforrásairól.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-134">Gets information about integration runtime resources.</span></span>

### [<span data-ttu-id="0a3b3-135">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="0a3b3-135">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>](Get-AzDataFactoryV2IntegrationRuntimeKey.md)
<span data-ttu-id="0a3b3-136">Egy önállóan működtetett integrációs futásidejű kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-136">Gets keys for a self-hosted integration runtime.</span></span>

### [<span data-ttu-id="0a3b3-137">Get-AzDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="0a3b3-137">Get-AzDataFactoryV2IntegrationRuntimeMetric</span></span>](Get-AzDataFactoryV2IntegrationRuntimeMetric.md)
<span data-ttu-id="0a3b3-138">Az integrációs futtatókörnyezet metrikus adatait kapja.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-138">Gets metric data for an integration runtime.</span></span> 

### [<span data-ttu-id="0a3b3-139">Get-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="0a3b3-139">Get-AzDataFactoryV2IntegrationRuntimeNode</span></span>](Get-AzDataFactoryV2IntegrationRuntimeNode.md)
<span data-ttu-id="0a3b3-140">Beolvassa az integrációs futtatókörnyezet csomópontjának adatait.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-140">Gets an integration runtime node infomation.</span></span>

### [<span data-ttu-id="0a3b3-141">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="0a3b3-141">Get-AzDataFactoryV2LinkedService</span></span>](Get-AzDataFactoryV2LinkedService.md)
<span data-ttu-id="0a3b3-142">Információt kap az adatfeldolgozó kapcsolt szolgáltatásairól.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-142">Gets information about linked services in Data Factory.</span></span>

### [<span data-ttu-id="0a3b3-143">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="0a3b3-143">Get-AzDataFactoryV2Pipeline</span></span>](Get-AzDataFactoryV2Pipeline.md)
<span data-ttu-id="0a3b3-144">Információt kap az adatfeldolgozási folyamatokról.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-144">Gets information about pipelines in Data Factory.</span></span>

### [<span data-ttu-id="0a3b3-145">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="0a3b3-145">Get-AzDataFactoryV2PipelineRun</span></span>](Get-AzDataFactoryV2PipelineRun.md)
<span data-ttu-id="0a3b3-146">Információt kap a csővezetékről.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-146">Gets information about pipeline runs.</span></span>

### [<span data-ttu-id="0a3b3-147">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0a3b3-147">Get-AzDataFactoryV2Trigger</span></span>](Get-AzDataFactoryV2Trigger.md)
<span data-ttu-id="0a3b3-148">Információt kap az eseményindítókkal kapcsolatban az adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-148">Gets information about triggers in a data factory.</span></span>

### [<span data-ttu-id="0a3b3-149">Get-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="0a3b3-149">Get-AzDataFactoryV2TriggerRun</span></span>](Get-AzDataFactoryV2TriggerRun.md)
<span data-ttu-id="0a3b3-150">Információt ad az indításról.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-150">Returns information about trigger runs.</span></span>

### [<span data-ttu-id="0a3b3-151">Meghívó-AzDataFactoryV2IntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="0a3b3-151">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span></span>](Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md)
<span data-ttu-id="0a3b3-152">Önkiszolgáló integrációs futtatókörnyezet frissítése</span><span class="sxs-lookup"><span data-stu-id="0a3b3-152">Upgrades self-hosted integration runtime.</span></span>

### [<span data-ttu-id="0a3b3-153">Meghívó-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="0a3b3-153">Invoke-AzDataFactoryV2Pipeline</span></span>](Invoke-AzDataFactoryV2Pipeline.md)
  <span data-ttu-id="0a3b3-154">Arra hívja fel a futószalagot, hogy indítsa el a futtatását.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-154">Invokes a pipeline to start a run for it.</span></span>

### [<span data-ttu-id="0a3b3-155">Új – AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="0a3b3-155">New-AzDataFactory</span></span>](New-AzDataFactory.md)
<span data-ttu-id="0a3b3-156">Adatfeldolgozót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-156">Creates a data factory.</span></span>

### [<span data-ttu-id="0a3b3-157">Új – AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="0a3b3-157">New-AzDataFactoryDataset</span></span>](New-AzDataFactoryDataset.md)
<span data-ttu-id="0a3b3-158">Adatkészletet hoz létre az adatfeldolgozóban.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-158">Creates a dataset in Data Factory.</span></span>

### [<span data-ttu-id="0a3b3-159">Új – AzDataFactoryEncryptValue</span><span class="sxs-lookup"><span data-stu-id="0a3b3-159">New-AzDataFactoryEncryptValue</span></span>](New-AzDataFactoryEncryptValue.md)
<span data-ttu-id="0a3b3-160">A bizalmas adatokat titkosítja.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-160">Encrypts sensitive data.</span></span>

### [<span data-ttu-id="0a3b3-161">Új – AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="0a3b3-161">New-AzDataFactoryGateway</span></span>](New-AzDataFactoryGateway.md)
<span data-ttu-id="0a3b3-162">Átjárót hoz létre egy Azure Data Factory számára.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-162">Creates a gateway for an Azure Data Factory.</span></span>

### [<span data-ttu-id="0a3b3-163">Új – AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="0a3b3-163">New-AzDataFactoryGatewayAuthKey</span></span>](New-AzDataFactoryGatewayAuthKey.md)
<span data-ttu-id="0a3b3-164">Hitelesítő kulcs létrehozása Azure Data Factory átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-164">Creates auth key for an Azure Data Factory Gateway.</span></span>

### [<span data-ttu-id="0a3b3-165">Új – AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="0a3b3-165">New-AzDataFactoryHub</span></span>](New-AzDataFactoryHub.md)
<span data-ttu-id="0a3b3-166">Az Azure Data Factory hub-t hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-166">Creates a hub for an Azure Data Factory.</span></span>

### [<span data-ttu-id="0a3b3-167">Új – AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="0a3b3-167">New-AzDataFactoryLinkedService</span></span>](New-AzDataFactoryLinkedService.md)
<span data-ttu-id="0a3b3-168">Az adattárolók vagy a Felhőbeli szolgáltatások kapcsolata az Azure Data Factory szolgáltatással.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-168">Links a data store or a cloud service to an Azure Data Factory.</span></span>

### [<span data-ttu-id="0a3b3-169">Új – AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="0a3b3-169">New-AzDataFactoryPipeline</span></span>](New-AzDataFactoryPipeline.md)
<span data-ttu-id="0a3b3-170">Futószalagot hoz létre az adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-170">Creates a pipeline in Data Factory.</span></span>

### [<span data-ttu-id="0a3b3-171">Új – AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="0a3b3-171">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>](New-AzDataFactoryV2IntegrationRuntimeKey.md)
<span data-ttu-id="0a3b3-172">Önkiszolgáló integrációs futásidejű kulcs újbóli létrehozása</span><span class="sxs-lookup"><span data-stu-id="0a3b3-172">Regenerate self-hosted integration runtime key.</span></span>

### [<span data-ttu-id="0a3b3-173">Új – AzDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="0a3b3-173">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span></span>](New-AzDataFactoryV2LinkedServiceEncryptedCredential.md)
<span data-ttu-id="0a3b3-174">Hitelesítő adatok titkosítása a kapcsolódó szolgáltatásban meghatározott integrációs futtatókörnyezettel.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-174">Encrypt credential in linked service with specified integration runtime.</span></span>

### [<span data-ttu-id="0a3b3-175">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="0a3b3-175">Remove-AzDataFactory</span></span>](Remove-AzDataFactory.md)
<span data-ttu-id="0a3b3-176">Az adatfeldolgozó eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-176">Removes a data factory.</span></span>

### [<span data-ttu-id="0a3b3-177">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="0a3b3-177">Remove-AzDataFactoryDataset</span></span>](Remove-AzDataFactoryDataset.md)
<span data-ttu-id="0a3b3-178">Az Azure Data Factory adatkészletének eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-178">Removes a dataset from Azure Data Factory.</span></span>

### [<span data-ttu-id="0a3b3-179">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="0a3b3-179">Remove-AzDataFactoryGateway</span></span>](Remove-AzDataFactoryGateway.md)
<span data-ttu-id="0a3b3-180">Átjáró eltávolítása az Azure Data Factory programból.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-180">Removes a gateway from Azure Data Factory.</span></span>

### [<span data-ttu-id="0a3b3-181">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="0a3b3-181">Remove-AzDataFactoryHub</span></span>](Remove-AzDataFactoryHub.md)
<span data-ttu-id="0a3b3-182">A hub eltávolítása az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-182">Removes a hub from Azure Data Factory.</span></span>

### [<span data-ttu-id="0a3b3-183">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="0a3b3-183">Remove-AzDataFactoryLinkedService</span></span>](Remove-AzDataFactoryLinkedService.md)
<span data-ttu-id="0a3b3-184">Egy kapcsolt szolgáltatás eltávolítása az Azure Data Factory alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-184">Removes a linked service from Azure Data Factory.</span></span>

### [<span data-ttu-id="0a3b3-185">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="0a3b3-185">Remove-AzDataFactoryPipeline</span></span>](Remove-AzDataFactoryPipeline.md)
<span data-ttu-id="0a3b3-186">Az Azure Data Factory futószalagjának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-186">Removes a pipeline from Azure Data Factory.</span></span>

### [<span data-ttu-id="0a3b3-187">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0a3b3-187">Remove-AzDataFactoryV2</span></span>](Remove-AzDataFactoryV2.md)
<span data-ttu-id="0a3b3-188">Az adatfeldolgozó eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-188">Removes a data factory.</span></span>

### [<span data-ttu-id="0a3b3-189">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="0a3b3-189">Remove-AzDataFactoryV2Dataset</span></span>](Remove-AzDataFactoryV2Dataset.md)
<span data-ttu-id="0a3b3-190">Adatkészlet eltávolítása az adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-190">Removes a dataset from Data Factory.</span></span>

### [<span data-ttu-id="0a3b3-191">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0a3b3-191">Remove-AzDataFactoryV2IntegrationRuntime</span></span>](Remove-AzDataFactoryV2IntegrationRuntime.md)
<span data-ttu-id="0a3b3-192">Az integrációs futtatókörnyezet eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-192">Removes an integration runtime.</span></span>

### [<span data-ttu-id="0a3b3-193">Remove-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="0a3b3-193">Remove-AzDataFactoryV2IntegrationRuntimeNode</span></span>](Remove-AzDataFactoryV2IntegrationRuntimeNode.md)
<span data-ttu-id="0a3b3-194">A megadott nevű csomópont eltávolítása az integrációs futtatókörnyezetben.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-194">Remove a node with the given name on an integration runtime.</span></span>

### [<span data-ttu-id="0a3b3-195">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="0a3b3-195">Remove-AzDataFactoryV2LinkedService</span></span>](Remove-AzDataFactoryV2LinkedService.md)
<span data-ttu-id="0a3b3-196">Egy kapcsolt szolgáltatás eltávolítása az adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-196">Removes a linked service from Data Factory.</span></span>

### [<span data-ttu-id="0a3b3-197">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="0a3b3-197">Remove-AzDataFactoryV2Pipeline</span></span>](Remove-AzDataFactoryV2Pipeline.md)
<span data-ttu-id="0a3b3-198">Csővezeték eltávolítása az adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-198">Removes a pipeline from Data Factory.</span></span>

### [<span data-ttu-id="0a3b3-199">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0a3b3-199">Remove-AzDataFactoryV2Trigger</span></span>](Remove-AzDataFactoryV2Trigger.md)
<span data-ttu-id="0a3b3-200">Az indítót eltávolítja az adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-200">Removes a trigger from a data factory.</span></span>

### [<span data-ttu-id="0a3b3-201">Önéletrajz – AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="0a3b3-201">Resume-AzDataFactoryPipeline</span></span>](Resume-AzDataFactoryPipeline.md)
<span data-ttu-id="0a3b3-202">Felfüggesztett csővezeték folytatása az adatfeldolgozóban.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-202">Resumes a suspended pipeline in Data Factory.</span></span>

### [<span data-ttu-id="0a3b3-203">Mentés-AzDataFactoryLog</span><span class="sxs-lookup"><span data-stu-id="0a3b3-203">Save-AzDataFactoryLog</span></span>](Save-AzDataFactoryLog.md)
<span data-ttu-id="0a3b3-204">Az Azure HDInsight-feldolgozásból letölthető naplófájlok.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-204">Downloads log files from Azure HDInsight processing.</span></span>

### [<span data-ttu-id="0a3b3-205">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="0a3b3-205">Set-AzDataFactoryGateway</span></span>](Set-AzDataFactoryGateway.md)
<span data-ttu-id="0a3b3-206">Az Azure Data Factory átjárójának leírását állítja be.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-206">Sets the description for a gateway in Azure Data Factory.</span></span>

### [<span data-ttu-id="0a3b3-207">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="0a3b3-207">Set-AzDataFactoryPipelineActivePeriod</span></span>](Set-AzDataFactoryPipelineActivePeriod.md)
<span data-ttu-id="0a3b3-208">Az adatszeletek aktív időszakának beállítása.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-208">Configures the active period for data slices.</span></span>

### [<span data-ttu-id="0a3b3-209">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="0a3b3-209">Set-AzDataFactorySliceStatus</span></span>](Set-AzDataFactorySliceStatus.md)
<span data-ttu-id="0a3b3-210">A szeletek állapotát állítja be egy adatkészlethez az Azure Data Factory-ban.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-210">Sets the status of slices for a dataset in Azure Data Factory.</span></span>

### [<span data-ttu-id="0a3b3-211">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0a3b3-211">Set-AzDataFactoryV2</span></span>](Set-AzDataFactoryV2.md)
<span data-ttu-id="0a3b3-212">Adatfeldolgozót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-212">Creates a data factory.</span></span>

### [<span data-ttu-id="0a3b3-213">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="0a3b3-213">Set-AzDataFactoryV2Dataset</span></span>](Set-AzDataFactoryV2Dataset.md)
<span data-ttu-id="0a3b3-214">Adatkészletet hoz létre az adatfeldolgozóban.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-214">Creates a dataset in Data Factory.</span></span>

### [<span data-ttu-id="0a3b3-215">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0a3b3-215">Set-AzDataFactoryV2IntegrationRuntime</span></span>](Set-AzDataFactoryV2IntegrationRuntime.md)
<span data-ttu-id="0a3b3-216">Az integrációs futtatókörnyezet frissítése</span><span class="sxs-lookup"><span data-stu-id="0a3b3-216">Updates an integration runtime.</span></span>

### [<span data-ttu-id="0a3b3-217">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="0a3b3-217">Set-AzDataFactoryV2LinkedService</span></span>](Set-AzDataFactoryV2LinkedService.md)
<span data-ttu-id="0a3b3-218">Az adattárolók vagy a Felhőbeli szolgáltatások összekapcsolása az adatfeldolgozó szolgáltatással.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-218">Links a data store or a cloud service to Data Factory.</span></span>

### [<span data-ttu-id="0a3b3-219">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="0a3b3-219">Set-AzDataFactoryV2Pipeline</span></span>](Set-AzDataFactoryV2Pipeline.md)
<span data-ttu-id="0a3b3-220">Futószalagot hoz létre az adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-220">Creates a pipeline in Data Factory.</span></span>

### [<span data-ttu-id="0a3b3-221">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0a3b3-221">Set-AzDataFactoryV2Trigger</span></span>](Set-AzDataFactoryV2Trigger.md)
<span data-ttu-id="0a3b3-222">Triggert hoz létre egy adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-222">Creates a trigger in a data factory.</span></span>

### [<span data-ttu-id="0a3b3-223">Start-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0a3b3-223">Start-AzDataFactoryV2IntegrationRuntime</span></span>](Start-AzDataFactoryV2IntegrationRuntime.md)
<span data-ttu-id="0a3b3-224">Felügyelt dedikált integrációs futtatókörnyezetet indít el.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-224">Starts a managed dedicated integration runtime.</span></span>

### [<span data-ttu-id="0a3b3-225">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0a3b3-225">Start-AzDataFactoryV2Trigger</span></span>](Start-AzDataFactoryV2Trigger.md)
<span data-ttu-id="0a3b3-226">Indítót indít az adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-226">Starts a trigger in a data factory.</span></span>

### [<span data-ttu-id="0a3b3-227">Stop-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0a3b3-227">Stop-AzDataFactoryV2IntegrationRuntime</span></span>](Stop-AzDataFactoryV2IntegrationRuntime.md)
<span data-ttu-id="0a3b3-228">Felügyelt dedikált integrációs futtatókörnyezetet állít be.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-228">Stops a managed dedicated integration runtime.</span></span>

### [<span data-ttu-id="0a3b3-229">Stop-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="0a3b3-229">Stop-AzDataFactoryV2PipelineRun</span></span>](Stop-AzDataFactoryV2PipelineRun.md)
<span data-ttu-id="0a3b3-230">Leállít egy pieline a Data Factory-ban.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-230">Stops a pieline run in a data factory.</span></span>

### [<span data-ttu-id="0a3b3-231">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0a3b3-231">Stop-AzDataFactoryV2Trigger</span></span>](Stop-AzDataFactoryV2Trigger.md)
<span data-ttu-id="0a3b3-232">Az adatgyárban lévő trigger leállítása</span><span class="sxs-lookup"><span data-stu-id="0a3b3-232">Stops a trigger in a data factory.</span></span>

### [<span data-ttu-id="0a3b3-233">Felfüggesztés – AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="0a3b3-233">Suspend-AzDataFactoryPipeline</span></span>](Suspend-AzDataFactoryPipeline.md)
<span data-ttu-id="0a3b3-234">Az Azure Data Factory csővezetékének felfüggesztése</span><span class="sxs-lookup"><span data-stu-id="0a3b3-234">Suspends a pipeline in Azure Data Factory.</span></span>

### [<span data-ttu-id="0a3b3-235">Szinkronizálás – AzDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="0a3b3-235">Sync-AzDataFactoryV2IntegrationRuntimeCredential</span></span>](Sync-AzDataFactoryV2IntegrationRuntimeCredential.md)
<span data-ttu-id="0a3b3-236">Szinkronizálja a hitelesítő adatokat az integrációs futásidejű csomópontok között.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-236">Synchronizes credentials among integration runtime nodes.</span></span>

### [<span data-ttu-id="0a3b3-237">Update-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0a3b3-237">Update-AzDataFactoryV2</span></span>](Update-AzDataFactoryV2.md)
<span data-ttu-id="0a3b3-238">Frissíti az adattípusok tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-238">Updates the properties of a data factory.</span></span>

### [<span data-ttu-id="0a3b3-239">Update-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0a3b3-239">Update-AzDataFactoryV2IntegrationRuntime</span></span>](Update-AzDataFactoryV2IntegrationRuntime.md)
<span data-ttu-id="0a3b3-240">Az integrációs futtatókörnyezet frissítése</span><span class="sxs-lookup"><span data-stu-id="0a3b3-240">Updates an integration runtime.</span></span>

### [<span data-ttu-id="0a3b3-241">Update-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="0a3b3-241">Update-AzDataFactoryV2IntegrationRuntimeNode</span></span>](Update-AzDataFactoryV2IntegrationRuntimeNode.md)
<span data-ttu-id="0a3b3-242">Frissítheti az önkiszolgáló integrációs futásidejű csomópontot.</span><span class="sxs-lookup"><span data-stu-id="0a3b3-242">Updates self-hosted integration runtime node.</span></span>

