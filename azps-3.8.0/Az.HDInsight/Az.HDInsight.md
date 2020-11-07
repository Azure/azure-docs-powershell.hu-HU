---
Module Name: Az.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
ms.openlocfilehash: 1a4413056e7658b81501067d3c0148951c05c235
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847582"
---
# <span data-ttu-id="5e151-101">Az. HDInsight modul</span><span class="sxs-lookup"><span data-stu-id="5e151-101">Az.HDInsight Module</span></span>
## <span data-ttu-id="5e151-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="5e151-102">Description</span></span>
<span data-ttu-id="5e151-103">Az ebben a szakaszban szereplő témakörök az Azure Resource Manager (ARM) keretrendszerben az Azure PowerShell-parancsmagok a Microsoft Azure HDInsight című témakörben olvashatók.</span><span class="sxs-lookup"><span data-stu-id="5e151-103">The topics in this section document the Azure PowerShell cmdlets for Microsoft Azure HDInsight in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="5e151-104">Ezek a parancsmagok a HDInsight-fürtök és a rajtuk futó feladatok kezelésére szolgálnak.</span><span class="sxs-lookup"><span data-stu-id="5e151-104">These cmdlets are used to manage HDInsight clusters and the jobs that run on them.</span></span> <span data-ttu-id="5e151-105">A parancsmagok a Microsoft. Azure. commands. HDInsight névtérben találhatók.</span><span class="sxs-lookup"><span data-stu-id="5e151-105">The cmdlets exist in the Microsoft.Azure.Commands.HDInsight namespace.</span></span>

## <span data-ttu-id="5e151-106">Az. HDInsight parancsmagok</span><span class="sxs-lookup"><span data-stu-id="5e151-106">Az.HDInsight Cmdlets</span></span>
### [<span data-ttu-id="5e151-107">Add-AzHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="5e151-107">Add-AzHDInsightClusterIdentity</span></span>](Add-AzHDInsightClusterIdentity.md)
<span data-ttu-id="5e151-108">A fürt identitását hozzáadja a fürtkonfiguráció-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="5e151-108">Adds a cluster identity to a cluster configuration object.</span></span>

### [<span data-ttu-id="5e151-109">Add-AzHDInsightComponentVersion</span><span class="sxs-lookup"><span data-stu-id="5e151-109">Add-AzHDInsightComponentVersion</span></span>](Add-AzHDInsightComponentVersion.md)
<span data-ttu-id="5e151-110">A fürtben futó szolgáltatás verziójának hozzáadása a fürtkonfiguráció-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="5e151-110">Adds a version for a service running in a cluster to a cluster configuration object.</span></span>

### [<span data-ttu-id="5e151-111">Add-AzHDInsightConfigValue</span><span class="sxs-lookup"><span data-stu-id="5e151-111">Add-AzHDInsightConfigValue</span></span>](Add-AzHDInsightConfigValue.md)
<span data-ttu-id="5e151-112">A Hadoop konfigurációs érték testreszabása és/vagy a kaptár megosztott tár testreszabása a fürtkonfigurációs objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="5e151-112">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

### [<span data-ttu-id="5e151-113">Add-AzHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="5e151-113">Add-AzHDInsightMetastore</span></span>](Add-AzHDInsightMetastore.md)
<span data-ttu-id="5e151-114">Felvesz egy SQL-adatbázist, amely kaptárként vagy Oozie metastore-objektumként szolgál.</span><span class="sxs-lookup"><span data-stu-id="5e151-114">Adds a SQL Database to serve as a Hive or Oozie metastore to a cluster configuration object.</span></span>

### [<span data-ttu-id="5e151-115">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="5e151-115">Add-AzHDInsightScriptAction</span></span>](Add-AzHDInsightScriptAction.md)
<span data-ttu-id="5e151-116">Parancsfájl-műveleteket ad egy fürtkonfiguráció-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="5e151-116">Adds a script action to a cluster configuration object.</span></span>

### [<span data-ttu-id="5e151-117">Add-AzHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="5e151-117">Add-AzHDInsightSecurityProfile</span></span>](Add-AzHDInsightSecurityProfile.md)
<span data-ttu-id="5e151-118">Biztonsági profilt ad hozzá a fürtkonfiguráció-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="5e151-118">Adds a security profile to a cluster configuration object.</span></span>

### [<span data-ttu-id="5e151-119">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="5e151-119">Add-AzHDInsightStorage</span></span>](Add-AzHDInsightStorage.md)
<span data-ttu-id="5e151-120">Azure-tárterületet ad hozzá egy fürtkonfiguráció-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="5e151-120">Adds an Azure Storage key to a cluster configuration object.</span></span>

### [<span data-ttu-id="5e151-121">Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="5e151-121">Disable-AzHDInsightMonitoring</span></span>](Disable-AzHDInsightMonitoring.md)
<span data-ttu-id="5e151-122">Letiltja a figyelést egy HDInsight-fürtben, és a releváns naplók az engedélyezés során meghatározott figyelési munkaterületre áramlanak.</span><span class="sxs-lookup"><span data-stu-id="5e151-122">Disables monitoring in a HDInsight cluster and relevant logs will stop flowing to the monitoring workspace specified during enable.</span></span>

### [<span data-ttu-id="5e151-123">Enable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="5e151-123">Enable-AzHDInsightMonitoring</span></span>](Enable-AzHDInsightMonitoring.md)
<span data-ttu-id="5e151-124">Lehetővé teszi a HDInsight-fürtök figyelését, és a megfelelő naplók az engedélyezés során megadott figyelési munkaterületre kerülnek.</span><span class="sxs-lookup"><span data-stu-id="5e151-124">Enables monitoring in a HDInsight cluster and relevant logs will be sent to the monitoring workspace specified during enable.</span></span>

### [<span data-ttu-id="5e151-125">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="5e151-125">Get-AzHDInsightCluster</span></span>](Get-AzHDInsightCluster.md)
<span data-ttu-id="5e151-126">A jelenlegi előfizetéshez vagy egy meghatározott erőforráscsoporthoz tartozó összes Azure HDInsight-szektorcsoport beszerzése és listázása, vagy egy adott fürt beolvasása.</span><span class="sxs-lookup"><span data-stu-id="5e151-126">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

### [<span data-ttu-id="5e151-127">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="5e151-127">Get-AzHDInsightJob</span></span>](Get-AzHDInsightJob.md)
<span data-ttu-id="5e151-128">Kinyeri a feladatok listáját egy fürtből, és megfordítja őket fordított időrendi sorrendben, vagy egy adott feladatot lekérdez.</span><span class="sxs-lookup"><span data-stu-id="5e151-128">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

### [<span data-ttu-id="5e151-129">Get-AzHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="5e151-129">Get-AzHDInsightJobOutput</span></span>](Get-AzHDInsightJobOutput.md)
<span data-ttu-id="5e151-130">A megadott fürthöz társított tárolási fiókból kapja meg a napló kimenetét.</span><span class="sxs-lookup"><span data-stu-id="5e151-130">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

### [<span data-ttu-id="5e151-131">Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="5e151-131">Get-AzHDInsightMonitoring</span></span>](Get-AzHDInsightMonitoring.md)
<span data-ttu-id="5e151-132">A telepítés figyelésének állapotát kapja meg a fürtben.</span><span class="sxs-lookup"><span data-stu-id="5e151-132">Gets the status of monitoring installation on the cluster.</span></span>

### [<span data-ttu-id="5e151-133">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="5e151-133">Get-AzHDInsightPersistedScriptAction</span></span>](Get-AzHDInsightPersistedScriptAction.md)
<span data-ttu-id="5e151-134">Beolvassa a fürtök állandó parancsfájlokkal kapcsolatos műveleteit, és időrendi sorrendben listázza őket, illetve a megadott, kimaradt parancsfájlokra vonatkozó adatokat kap.</span><span class="sxs-lookup"><span data-stu-id="5e151-134">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

### [<span data-ttu-id="5e151-135">Get-AzHDInsightProperty</span><span class="sxs-lookup"><span data-stu-id="5e151-135">Get-AzHDInsightProperty</span></span>](Get-AzHDInsightProperty.md)
<span data-ttu-id="5e151-136">Beolvassa a HDInsight szolgáltatás tulajdonságait, például a rendelkezésre álló helyeket és a kapacitást.</span><span class="sxs-lookup"><span data-stu-id="5e151-136">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

### [<span data-ttu-id="5e151-137">Get-AzHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="5e151-137">Get-AzHDInsightScriptActionHistory</span></span>](Get-AzHDInsightScriptActionHistory.md)
<span data-ttu-id="5e151-138">Egy fürt parancsfájl-végrehajtási előzményeit jeleníti meg, és megfordítja őket fordított időrendi sorrendben, vagy egy korábban végrehajtott parancsfájl-művelet részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5e151-138">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

### [<span data-ttu-id="5e151-139">Meghívó-AzHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="5e151-139">Invoke-AzHDInsightHiveJob</span></span>](Invoke-AzHDInsightHiveJob.md)
<span data-ttu-id="5e151-140">A kaptár-lekérdezést elküldi egy HDInsight-fürtnek, és egy műveletben lekérdezi a lekérdezés eredményét.</span><span class="sxs-lookup"><span data-stu-id="5e151-140">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

### [<span data-ttu-id="5e151-141">Új – AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="5e151-141">New-AzHDInsightCluster</span></span>](New-AzHDInsightCluster.md)
<span data-ttu-id="5e151-142">Azure HDInsight-fürtöt hoz létre az aktuális előfizetéshez megadott erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="5e151-142">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

### [<span data-ttu-id="5e151-143">Új – AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="5e151-143">New-AzHDInsightClusterConfig</span></span>](New-AzHDInsightClusterConfig.md)
<span data-ttu-id="5e151-144">Nem állandó fürtkonfiguráció-objektumot hoz létre, amely leírja az Azure HDInsight-fürtös konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="5e151-144">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

### [<span data-ttu-id="5e151-145">Új – AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="5e151-145">New-AzHDInsightHiveJobDefinition</span></span>](New-AzHDInsightHiveJobDefinition.md)
<span data-ttu-id="5e151-146">Kaptár-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="5e151-146">Creates a Hive job object.</span></span>

### [<span data-ttu-id="5e151-147">Új – AzHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="5e151-147">New-AzHDInsightMapReduceJobDefinition</span></span>](New-AzHDInsightMapReduceJobDefinition.md)
<span data-ttu-id="5e151-148">Létrehoz egy MapReduce.</span><span class="sxs-lookup"><span data-stu-id="5e151-148">Creates a MapReduce job object.</span></span>

### [<span data-ttu-id="5e151-149">Új – AzHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="5e151-149">New-AzHDInsightPigJobDefinition</span></span>](New-AzHDInsightPigJobDefinition.md)
<span data-ttu-id="5e151-150">Egy Pig-Job objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="5e151-150">Creates a Pig job object.</span></span>

### [<span data-ttu-id="5e151-151">Új – AzHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="5e151-151">New-AzHDInsightSqoopJobDefinition</span></span>](New-AzHDInsightSqoopJobDefinition.md)
<span data-ttu-id="5e151-152">Létrehoz egy Sqoop.</span><span class="sxs-lookup"><span data-stu-id="5e151-152">Creates a Sqoop job object.</span></span>

### [<span data-ttu-id="5e151-153">Új – AzHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="5e151-153">New-AzHDInsightStreamingMapReduceJobDefinition</span></span>](New-AzHDInsightStreamingMapReduceJobDefinition.md)
<span data-ttu-id="5e151-154">Adatfolyam-MapReduce hoz létre.</span><span class="sxs-lookup"><span data-stu-id="5e151-154">Creates a Streaming MapReduce job object.</span></span>

### [<span data-ttu-id="5e151-155">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="5e151-155">Remove-AzHDInsightCluster</span></span>](Remove-AzHDInsightCluster.md)
<span data-ttu-id="5e151-156">Eltávolítja a megadott HDInsight-fürtöt az aktuális előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="5e151-156">Removes the specified HDInsight cluster from the current subscription.</span></span>

### [<span data-ttu-id="5e151-157">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="5e151-157">Remove-AzHDInsightPersistedScriptAction</span></span>](Remove-AzHDInsightPersistedScriptAction.md)
<span data-ttu-id="5e151-158">Állandó parancsfájl-művelet eltávolítása egy HDInsight-fürtről.</span><span class="sxs-lookup"><span data-stu-id="5e151-158">Removes an persisted script action from an HDInsight cluster.</span></span>

### [<span data-ttu-id="5e151-159">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="5e151-159">Set-AzHDInsightClusterSize</span></span>](Set-AzHDInsightClusterSize.md)
<span data-ttu-id="5e151-160">A megadott szektorcsoportban lévő munkaállomások számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5e151-160">Sets the number of Worker nodes in a specified cluster.</span></span>

### [<span data-ttu-id="5e151-161">Set-AzHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="5e151-161">Set-AzHDInsightDefaultStorage</span></span>](Set-AzHDInsightDefaultStorage.md)
<span data-ttu-id="5e151-162">Beállítja az alapértelmezett tárolási fiók beállítását egy fürtkonfiguráció-objektumban.</span><span class="sxs-lookup"><span data-stu-id="5e151-162">Sets the default Storage account setting in a cluster configuration object.</span></span>

### [<span data-ttu-id="5e151-163">Set-AzHDInsightGatewayCredential</span><span class="sxs-lookup"><span data-stu-id="5e151-163">Set-AzHDInsightGatewayCredential</span></span>](Set-AzHDInsightGatewayCredential.md)
<span data-ttu-id="5e151-164">Az Azure HDInsight-fürtök átjárójának HTTP-hitelesítő adatait állítja be.</span><span class="sxs-lookup"><span data-stu-id="5e151-164">Sets the gateway HTTP credentials of an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="5e151-165">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="5e151-165">Set-AzHDInsightPersistedScriptAction</span></span>](Set-AzHDInsightPersistedScriptAction.md)
<span data-ttu-id="5e151-166">Egy korábban futtatott parancsfájlt egy állandó parancsfájl-műveletre állítja be.</span><span class="sxs-lookup"><span data-stu-id="5e151-166">Sets a previously executed script action to be a persisted script action.</span></span>

### [<span data-ttu-id="5e151-167">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="5e151-167">Start-AzHDInsightJob</span></span>](Start-AzHDInsightJob.md)
<span data-ttu-id="5e151-168">Meghatározott Azure HDInsight-feladatot indít egy adott fürtön.</span><span class="sxs-lookup"><span data-stu-id="5e151-168">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

### [<span data-ttu-id="5e151-169">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="5e151-169">Stop-AzHDInsightJob</span></span>](Stop-AzHDInsightJob.md)
<span data-ttu-id="5e151-170">Meghatározott futó feladat leállítása egy fürtben.</span><span class="sxs-lookup"><span data-stu-id="5e151-170">Stops a specified running job on a cluster.</span></span>

### [<span data-ttu-id="5e151-171">Submit-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="5e151-171">Submit-AzHDInsightScriptAction</span></span>](Submit-AzHDInsightScriptAction.md)
<span data-ttu-id="5e151-172">Új parancsfájl-művelet elküldhet egy Azure HDInsight-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="5e151-172">Submits a new script action to an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="5e151-173">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="5e151-173">Use-AzHDInsightCluster</span></span>](Use-AzHDInsightCluster.md)
<span data-ttu-id="5e151-174">Kijelöli az Invoke-RmAzureHDInsightHiveJob parancsmaggal használni kívánt fürtöt.</span><span class="sxs-lookup"><span data-stu-id="5e151-174">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

### [<span data-ttu-id="5e151-175">Várjon-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="5e151-175">Wait-AzHDInsightJob</span></span>](Wait-AzHDInsightJob.md)
<span data-ttu-id="5e151-176">A megadott feladat befejezését vagy hibáját várja.</span><span class="sxs-lookup"><span data-stu-id="5e151-176">Waits for the completion or failure of a specified job.</span></span>

