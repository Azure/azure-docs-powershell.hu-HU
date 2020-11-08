---
Module Name: Az.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
ms.openlocfilehash: e3c3bb9d4d8225823ec84750c8292288ce25c15b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185383"
---
# <span data-ttu-id="b562d-101">Az. HDInsight modul</span><span class="sxs-lookup"><span data-stu-id="b562d-101">Az.HDInsight Module</span></span>
## <span data-ttu-id="b562d-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="b562d-102">Description</span></span>
<span data-ttu-id="b562d-103">Az ebben a szakaszban szereplő témakörök az Azure Resource Manager (ARM) keretrendszerben az Azure PowerShell-parancsmagok a Microsoft Azure HDInsight című témakörben olvashatók.</span><span class="sxs-lookup"><span data-stu-id="b562d-103">The topics in this section document the Azure PowerShell cmdlets for Microsoft Azure HDInsight in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="b562d-104">Ezek a parancsmagok a HDInsight-fürtök és a rajtuk futó feladatok kezelésére szolgálnak.</span><span class="sxs-lookup"><span data-stu-id="b562d-104">These cmdlets are used to manage HDInsight clusters and the jobs that run on them.</span></span> <span data-ttu-id="b562d-105">A parancsmagok a Microsoft. Azure. commands. HDInsight névtérben találhatók.</span><span class="sxs-lookup"><span data-stu-id="b562d-105">The cmdlets exist in the Microsoft.Azure.Commands.HDInsight namespace.</span></span>

## <span data-ttu-id="b562d-106">Az. HDInsight parancsmagok</span><span class="sxs-lookup"><span data-stu-id="b562d-106">Az.HDInsight Cmdlets</span></span>
### [<span data-ttu-id="b562d-107">Add-AzHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="b562d-107">Add-AzHDInsightClusterIdentity</span></span>](Add-AzHDInsightClusterIdentity.md)
<span data-ttu-id="b562d-108">A fürt identitását hozzáadja a fürtkonfiguráció-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="b562d-108">Adds a cluster identity to a cluster configuration object.</span></span>

### [<span data-ttu-id="b562d-109">Add-AzHDInsightComponentVersion</span><span class="sxs-lookup"><span data-stu-id="b562d-109">Add-AzHDInsightComponentVersion</span></span>](Add-AzHDInsightComponentVersion.md)
<span data-ttu-id="b562d-110">A fürtben futó szolgáltatás verziójának hozzáadása a fürtkonfiguráció-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="b562d-110">Adds a version for a service running in a cluster to a cluster configuration object.</span></span>

### [<span data-ttu-id="b562d-111">Add-AzHDInsightConfigValue</span><span class="sxs-lookup"><span data-stu-id="b562d-111">Add-AzHDInsightConfigValue</span></span>](Add-AzHDInsightConfigValue.md)
<span data-ttu-id="b562d-112">A Hadoop konfigurációs érték testreszabása és/vagy a kaptár megosztott tár testreszabása a fürtkonfigurációs objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="b562d-112">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

### [<span data-ttu-id="b562d-113">Add-AzHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="b562d-113">Add-AzHDInsightMetastore</span></span>](Add-AzHDInsightMetastore.md)
<span data-ttu-id="b562d-114">Felvesz egy SQL-adatbázist, amely kaptárként vagy Oozie metastore-objektumként szolgál.</span><span class="sxs-lookup"><span data-stu-id="b562d-114">Adds a SQL Database to serve as a Hive or Oozie metastore to a cluster configuration object.</span></span>

### [<span data-ttu-id="b562d-115">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="b562d-115">Add-AzHDInsightScriptAction</span></span>](Add-AzHDInsightScriptAction.md)
<span data-ttu-id="b562d-116">Parancsfájl-műveleteket ad egy fürtkonfiguráció-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="b562d-116">Adds a script action to a cluster configuration object.</span></span>

### [<span data-ttu-id="b562d-117">Add-AzHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="b562d-117">Add-AzHDInsightSecurityProfile</span></span>](Add-AzHDInsightSecurityProfile.md)
<span data-ttu-id="b562d-118">Biztonsági profilt ad hozzá a fürtkonfiguráció-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="b562d-118">Adds a security profile to a cluster configuration object.</span></span>

### [<span data-ttu-id="b562d-119">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="b562d-119">Add-AzHDInsightStorage</span></span>](Add-AzHDInsightStorage.md)
<span data-ttu-id="b562d-120">Azure-tárterületet ad hozzá egy fürtkonfiguráció-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="b562d-120">Adds an Azure Storage key to a cluster configuration object.</span></span>

### [<span data-ttu-id="b562d-121">Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="b562d-121">Disable-AzHDInsightMonitoring</span></span>](Disable-AzHDInsightMonitoring.md)
<span data-ttu-id="b562d-122">Letiltja a figyelést egy HDInsight-fürtben, és a releváns naplók az engedélyezés során meghatározott figyelési munkaterületre áramlanak.</span><span class="sxs-lookup"><span data-stu-id="b562d-122">Disables monitoring in a HDInsight cluster and relevant logs will stop flowing to the monitoring workspace specified during enable.</span></span>

### [<span data-ttu-id="b562d-123">Enable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="b562d-123">Enable-AzHDInsightMonitoring</span></span>](Enable-AzHDInsightMonitoring.md)
<span data-ttu-id="b562d-124">Lehetővé teszi a HDInsight-fürtök figyelését, és a megfelelő naplók az engedélyezés során megadott figyelési munkaterületre kerülnek.</span><span class="sxs-lookup"><span data-stu-id="b562d-124">Enables monitoring in a HDInsight cluster and relevant logs will be sent to the monitoring workspace specified during enable.</span></span>

### [<span data-ttu-id="b562d-125">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="b562d-125">Get-AzHDInsightCluster</span></span>](Get-AzHDInsightCluster.md)
<span data-ttu-id="b562d-126">A jelenlegi előfizetéshez vagy egy meghatározott erőforráscsoporthoz tartozó összes Azure HDInsight-szektorcsoport beszerzése és listázása, vagy egy adott fürt beolvasása.</span><span class="sxs-lookup"><span data-stu-id="b562d-126">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

### [<span data-ttu-id="b562d-127">Get-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="b562d-127">Get-AzHDInsightClusterAutoscaleConfiguration</span></span>](Get-AzHDInsightClusterAutoscaleConfiguration.md)
<span data-ttu-id="b562d-128">Beilleszti a HDInsight-fürt automatikus méretarányos konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="b562d-128">Gets the autoscale configuration of HDInsight cluster.</span></span>

### [<span data-ttu-id="b562d-129">Get-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="b562d-129">Get-AzHDInsightHost</span></span>](Get-AzHDInsightHost.md)
<span data-ttu-id="b562d-130">Felsorolja a HDInsight-fürt állomásait.</span><span class="sxs-lookup"><span data-stu-id="b562d-130">Lists the hosts of the HDInsight cluster.</span></span>

### [<span data-ttu-id="b562d-131">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b562d-131">Get-AzHDInsightJob</span></span>](Get-AzHDInsightJob.md)
<span data-ttu-id="b562d-132">Kinyeri a feladatok listáját egy fürtből, és megfordítja őket fordított időrendi sorrendben, vagy egy adott feladatot lekérdez.</span><span class="sxs-lookup"><span data-stu-id="b562d-132">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

### [<span data-ttu-id="b562d-133">Get-AzHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="b562d-133">Get-AzHDInsightJobOutput</span></span>](Get-AzHDInsightJobOutput.md)
<span data-ttu-id="b562d-134">A megadott fürthöz társított tárolási fiókból kapja meg a napló kimenetét.</span><span class="sxs-lookup"><span data-stu-id="b562d-134">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

### [<span data-ttu-id="b562d-135">Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="b562d-135">Get-AzHDInsightMonitoring</span></span>](Get-AzHDInsightMonitoring.md)
<span data-ttu-id="b562d-136">A telepítés figyelésének állapotát kapja meg a fürtben.</span><span class="sxs-lookup"><span data-stu-id="b562d-136">Gets the status of monitoring installation on the cluster.</span></span>

### [<span data-ttu-id="b562d-137">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="b562d-137">Get-AzHDInsightPersistedScriptAction</span></span>](Get-AzHDInsightPersistedScriptAction.md)
<span data-ttu-id="b562d-138">Beolvassa a fürtök állandó parancsfájlokkal kapcsolatos műveleteit, és időrendi sorrendben listázza őket, illetve a megadott, kimaradt parancsfájlokra vonatkozó adatokat kap.</span><span class="sxs-lookup"><span data-stu-id="b562d-138">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

### [<span data-ttu-id="b562d-139">Get-AzHDInsightProperty</span><span class="sxs-lookup"><span data-stu-id="b562d-139">Get-AzHDInsightProperty</span></span>](Get-AzHDInsightProperty.md)
<span data-ttu-id="b562d-140">Beolvassa a HDInsight szolgáltatás tulajdonságait, például a rendelkezésre álló helyeket és a kapacitást.</span><span class="sxs-lookup"><span data-stu-id="b562d-140">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

### [<span data-ttu-id="b562d-141">Get-AzHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="b562d-141">Get-AzHDInsightScriptActionHistory</span></span>](Get-AzHDInsightScriptActionHistory.md)
<span data-ttu-id="b562d-142">Egy fürt parancsfájl-végrehajtási előzményeit jeleníti meg, és megfordítja őket fordított időrendi sorrendben, vagy egy korábban végrehajtott parancsfájl-művelet részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b562d-142">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

### [<span data-ttu-id="b562d-143">Meghívó-AzHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="b562d-143">Invoke-AzHDInsightHiveJob</span></span>](Invoke-AzHDInsightHiveJob.md)
<span data-ttu-id="b562d-144">A kaptár-lekérdezést elküldi egy HDInsight-fürtnek, és egy műveletben lekérdezi a lekérdezés eredményét.</span><span class="sxs-lookup"><span data-stu-id="b562d-144">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

### [<span data-ttu-id="b562d-145">Új – AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="b562d-145">New-AzHDInsightCluster</span></span>](New-AzHDInsightCluster.md)
<span data-ttu-id="b562d-146">Azure HDInsight-fürtöt hoz létre az aktuális előfizetéshez megadott erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="b562d-146">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

### [<span data-ttu-id="b562d-147">Új – AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="b562d-147">New-AzHDInsightClusterAutoscaleConfiguration</span></span>](New-AzHDInsightClusterAutoscaleConfiguration.md)
<span data-ttu-id="b562d-148">Olyan nem állandó objektumot hoz létre, amely leírja az Azure HDInsight-fürtök automatikus méretarányos konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="b562d-148">Creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="b562d-149">Új – AzHDInsightClusterAutoscaleScheduleCondition</span><span class="sxs-lookup"><span data-stu-id="b562d-149">New-AzHDInsightClusterAutoscaleScheduleCondition</span></span>](New-AzHDInsightClusterAutoscaleScheduleCondition.md)
<span data-ttu-id="b562d-150">Ütemezési alapú autoscale-feltételt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b562d-150">Creates Schedule-based autoscale condition.</span></span>

### [<span data-ttu-id="b562d-151">Új – AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="b562d-151">New-AzHDInsightClusterConfig</span></span>](New-AzHDInsightClusterConfig.md)
<span data-ttu-id="b562d-152">Nem állandó fürtkonfiguráció-objektumot hoz létre, amely leírja az Azure HDInsight-fürtös konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="b562d-152">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

### [<span data-ttu-id="b562d-153">Új – AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b562d-153">New-AzHDInsightHiveJobDefinition</span></span>](New-AzHDInsightHiveJobDefinition.md)
<span data-ttu-id="b562d-154">Kaptár-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b562d-154">Creates a Hive job object.</span></span>

### [<span data-ttu-id="b562d-155">Új – AzHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b562d-155">New-AzHDInsightMapReduceJobDefinition</span></span>](New-AzHDInsightMapReduceJobDefinition.md)
<span data-ttu-id="b562d-156">Létrehoz egy MapReduce.</span><span class="sxs-lookup"><span data-stu-id="b562d-156">Creates a MapReduce job object.</span></span>

### [<span data-ttu-id="b562d-157">Új – AzHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b562d-157">New-AzHDInsightPigJobDefinition</span></span>](New-AzHDInsightPigJobDefinition.md)
<span data-ttu-id="b562d-158">Egy Pig-Job objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b562d-158">Creates a Pig job object.</span></span>

### [<span data-ttu-id="b562d-159">Új – AzHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b562d-159">New-AzHDInsightSqoopJobDefinition</span></span>](New-AzHDInsightSqoopJobDefinition.md)
<span data-ttu-id="b562d-160">Létrehoz egy Sqoop.</span><span class="sxs-lookup"><span data-stu-id="b562d-160">Creates a Sqoop job object.</span></span>

### [<span data-ttu-id="b562d-161">Új – AzHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b562d-161">New-AzHDInsightStreamingMapReduceJobDefinition</span></span>](New-AzHDInsightStreamingMapReduceJobDefinition.md)
<span data-ttu-id="b562d-162">Adatfolyam-MapReduce hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b562d-162">Creates a Streaming MapReduce job object.</span></span>

### [<span data-ttu-id="b562d-163">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="b562d-163">Remove-AzHDInsightCluster</span></span>](Remove-AzHDInsightCluster.md)
<span data-ttu-id="b562d-164">Eltávolítja a megadott HDInsight-fürtöt az aktuális előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="b562d-164">Removes the specified HDInsight cluster from the current subscription.</span></span>

### [<span data-ttu-id="b562d-165">Remove-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="b562d-165">Remove-AzHDInsightClusterAutoscaleConfiguration</span></span>](Remove-AzHDInsightClusterAutoscaleConfiguration.md)
<span data-ttu-id="b562d-166">Eltávolítja a HDInsight-fürt automatikus méretezési konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="b562d-166">Removes the autoscale configuration of the HDInsight cluster.</span></span>

### [<span data-ttu-id="b562d-167">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="b562d-167">Remove-AzHDInsightPersistedScriptAction</span></span>](Remove-AzHDInsightPersistedScriptAction.md)
<span data-ttu-id="b562d-168">Állandó parancsfájl-művelet eltávolítása egy HDInsight-fürtről.</span><span class="sxs-lookup"><span data-stu-id="b562d-168">Removes an persisted script action from an HDInsight cluster.</span></span>

### [<span data-ttu-id="b562d-169">Újraindítás – AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="b562d-169">Restart-AzHDInsightHost</span></span>](Restart-AzHDInsightHost.md)
<span data-ttu-id="b562d-170">A HDInsight-fürt adott állomásainak újraindítása.</span><span class="sxs-lookup"><span data-stu-id="b562d-170">Restarts the specific hosts of HDInsight cluster.</span></span>

### [<span data-ttu-id="b562d-171">Set-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="b562d-171">Set-AzHDInsightClusterAutoscaleConfiguration</span></span>](Set-AzHDInsightClusterAutoscaleConfiguration.md)
<span data-ttu-id="b562d-172">Az Azure HDInsight-fürtök automatikus méretarányos konfigurációjának beállítása.</span><span class="sxs-lookup"><span data-stu-id="b562d-172">Sets the autoscale configuration of an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="b562d-173">Set-AzHDInsightClusterDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="b562d-173">Set-AzHDInsightClusterDiskEncryptionKey</span></span>](Set-AzHDInsightClusterDiskEncryptionKey.md)
<span data-ttu-id="b562d-174">Elforgatja a megadott HDInsight-fürt lemez titkosítási kulcsát.</span><span class="sxs-lookup"><span data-stu-id="b562d-174">Rotates the disk encryption key of the specified HDInsight cluster.</span></span>

### [<span data-ttu-id="b562d-175">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="b562d-175">Set-AzHDInsightClusterSize</span></span>](Set-AzHDInsightClusterSize.md)
<span data-ttu-id="b562d-176">A megadott szektorcsoportban lévő munkaállomások számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b562d-176">Sets the number of Worker nodes in a specified cluster.</span></span>

### [<span data-ttu-id="b562d-177">Set-AzHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="b562d-177">Set-AzHDInsightDefaultStorage</span></span>](Set-AzHDInsightDefaultStorage.md)
<span data-ttu-id="b562d-178">Beállítja az alapértelmezett tárolási fiók beállítását egy fürtkonfiguráció-objektumban.</span><span class="sxs-lookup"><span data-stu-id="b562d-178">Sets the default Storage account setting in a cluster configuration object.</span></span>

### [<span data-ttu-id="b562d-179">Set-AzHDInsightGatewayCredential</span><span class="sxs-lookup"><span data-stu-id="b562d-179">Set-AzHDInsightGatewayCredential</span></span>](Set-AzHDInsightGatewayCredential.md)
<span data-ttu-id="b562d-180">Az Azure HDInsight-fürtök átjárójának HTTP-hitelesítő adatait állítja be.</span><span class="sxs-lookup"><span data-stu-id="b562d-180">Sets the gateway HTTP credentials of an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="b562d-181">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="b562d-181">Set-AzHDInsightPersistedScriptAction</span></span>](Set-AzHDInsightPersistedScriptAction.md)
<span data-ttu-id="b562d-182">Egy korábban futtatott parancsfájlt egy állandó parancsfájl-műveletre állítja be.</span><span class="sxs-lookup"><span data-stu-id="b562d-182">Sets a previously executed script action to be a persisted script action.</span></span>

### [<span data-ttu-id="b562d-183">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b562d-183">Start-AzHDInsightJob</span></span>](Start-AzHDInsightJob.md)
<span data-ttu-id="b562d-184">Meghatározott Azure HDInsight-feladatot indít egy adott fürtön.</span><span class="sxs-lookup"><span data-stu-id="b562d-184">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

### [<span data-ttu-id="b562d-185">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b562d-185">Stop-AzHDInsightJob</span></span>](Stop-AzHDInsightJob.md)
<span data-ttu-id="b562d-186">Meghatározott futó feladat leállítása egy fürtben.</span><span class="sxs-lookup"><span data-stu-id="b562d-186">Stops a specified running job on a cluster.</span></span>

### [<span data-ttu-id="b562d-187">Submit-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="b562d-187">Submit-AzHDInsightScriptAction</span></span>](Submit-AzHDInsightScriptAction.md)
<span data-ttu-id="b562d-188">Új parancsfájl-művelet elküldhet egy Azure HDInsight-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="b562d-188">Submits a new script action to an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="b562d-189">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="b562d-189">Use-AzHDInsightCluster</span></span>](Use-AzHDInsightCluster.md)
<span data-ttu-id="b562d-190">Kijelöli az Invoke-RmAzureHDInsightHiveJob parancsmaggal használni kívánt fürtöt.</span><span class="sxs-lookup"><span data-stu-id="b562d-190">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

### [<span data-ttu-id="b562d-191">Várjon-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b562d-191">Wait-AzHDInsightJob</span></span>](Wait-AzHDInsightJob.md)
<span data-ttu-id="b562d-192">A megadott feladat befejezését vagy hibáját várja.</span><span class="sxs-lookup"><span data-stu-id="b562d-192">Waits for the completion or failure of a specified job.</span></span>
