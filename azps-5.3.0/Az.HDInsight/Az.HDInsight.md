---
Module Name: Az.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
ms.openlocfilehash: e3c3bb9d4d8225823ec84750c8292288ce25c15b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469698"
---
# <span data-ttu-id="12dbc-101">Az.HDInsight modul</span><span class="sxs-lookup"><span data-stu-id="12dbc-101">Az.HDInsight Module</span></span>
## <span data-ttu-id="12dbc-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="12dbc-102">Description</span></span>
<span data-ttu-id="12dbc-103">A szakasz témakörei a Microsoft Azure HDInsight Azure PowerShell-parancsmagját, az Azure Resource Manager (ARM) keretrendszerben dokumentálják.</span><span class="sxs-lookup"><span data-stu-id="12dbc-103">The topics in this section document the Azure PowerShell cmdlets for Microsoft Azure HDInsight in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="12dbc-104">Ezek a parancsmagok a HDInsight-fürtök és az őket futtató feladatok kezelésére használhatók.</span><span class="sxs-lookup"><span data-stu-id="12dbc-104">These cmdlets are used to manage HDInsight clusters and the jobs that run on them.</span></span> <span data-ttu-id="12dbc-105">A parancsmagok a Microsoft.Azure.Commands.HDInsight névterében létezik.</span><span class="sxs-lookup"><span data-stu-id="12dbc-105">The cmdlets exist in the Microsoft.Azure.Commands.HDInsight namespace.</span></span>

## <span data-ttu-id="12dbc-106">Az.HDInsight parancsmagok</span><span class="sxs-lookup"><span data-stu-id="12dbc-106">Az.HDInsight Cmdlets</span></span>
### [<span data-ttu-id="12dbc-107">Add-AzHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="12dbc-107">Add-AzHDInsightClusterIdentity</span></span>](Add-AzHDInsightClusterIdentity.md)
<span data-ttu-id="12dbc-108">Fürtidentitás hozzáadása fürtkonfigurációs objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="12dbc-108">Adds a cluster identity to a cluster configuration object.</span></span>

### [<span data-ttu-id="12dbc-109">Add-AzHDInsightComponentVersion</span><span class="sxs-lookup"><span data-stu-id="12dbc-109">Add-AzHDInsightComponentVersion</span></span>](Add-AzHDInsightComponentVersion.md)
<span data-ttu-id="12dbc-110">A fürtben futó szolgáltatások verziójának hozzáadása fürtkonfigurációs objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="12dbc-110">Adds a version for a service running in a cluster to a cluster configuration object.</span></span>

### [<span data-ttu-id="12dbc-111">Add-AzHDInsightConfigValue</span><span class="sxs-lookup"><span data-stu-id="12dbc-111">Add-AzHDInsightConfigValue</span></span>](Add-AzHDInsightConfigValue.md)
<span data-ttu-id="12dbc-112">A Hadoop konfigurációs értékének és/vagy a Hive-tárak megosztott testreszabásának hozzáadása a fürtkonfigurációs objektumokhoz.</span><span class="sxs-lookup"><span data-stu-id="12dbc-112">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

### [<span data-ttu-id="12dbc-113">Add-AzHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="12dbc-113">Add-AzHDInsightMetastore</span></span>](Add-AzHDInsightMetastore.md)
<span data-ttu-id="12dbc-114">Egy fürtkonfigurációs objektumhoz hozzáad egy HIVE- vagy Oozie-metastoreként szolgáló SQL-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="12dbc-114">Adds a SQL Database to serve as a Hive or Oozie metastore to a cluster configuration object.</span></span>

### [<span data-ttu-id="12dbc-115">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="12dbc-115">Add-AzHDInsightScriptAction</span></span>](Add-AzHDInsightScriptAction.md)
<span data-ttu-id="12dbc-116">Parancsfájl-műveletet ad egy fürtkonfigurációs objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="12dbc-116">Adds a script action to a cluster configuration object.</span></span>

### [<span data-ttu-id="12dbc-117">Add-AzHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="12dbc-117">Add-AzHDInsightSecurityProfile</span></span>](Add-AzHDInsightSecurityProfile.md)
<span data-ttu-id="12dbc-118">Biztonsági profil hozzáadása fürtkonfigurációs objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="12dbc-118">Adds a security profile to a cluster configuration object.</span></span>

### [<span data-ttu-id="12dbc-119">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="12dbc-119">Add-AzHDInsightStorage</span></span>](Add-AzHDInsightStorage.md)
<span data-ttu-id="12dbc-120">Hozzáad egy Azure-tárterületkulcsot egy fürtkonfigurációs objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="12dbc-120">Adds an Azure Storage key to a cluster configuration object.</span></span>

### [<span data-ttu-id="12dbc-121">Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="12dbc-121">Disable-AzHDInsightMonitoring</span></span>](Disable-AzHDInsightMonitoring.md)
<span data-ttu-id="12dbc-122">A HDInsight-fürtben való figyelés letiltása és a kapcsolódó naplók az engedélyezés során megadott figyelési munkaterületre fognak áramni.</span><span class="sxs-lookup"><span data-stu-id="12dbc-122">Disables monitoring in a HDInsight cluster and relevant logs will stop flowing to the monitoring workspace specified during enable.</span></span>

### [<span data-ttu-id="12dbc-123">Enable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="12dbc-123">Enable-AzHDInsightMonitoring</span></span>](Enable-AzHDInsightMonitoring.md)
<span data-ttu-id="12dbc-124">A HDInsight-fürtben való figyelés engedélyezése és a kapcsolódó naplók az engedélyezés során megadott figyelési munkaterületre lesznek küldve.</span><span class="sxs-lookup"><span data-stu-id="12dbc-124">Enables monitoring in a HDInsight cluster and relevant logs will be sent to the monitoring workspace specified during enable.</span></span>

### [<span data-ttu-id="12dbc-125">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="12dbc-125">Get-AzHDInsightCluster</span></span>](Get-AzHDInsightCluster.md)
<span data-ttu-id="12dbc-126">Beolvassa és felsorolja az aktuális előfizetéshez vagy adott erőforráscsoporthoz társított Összes Azure HDInsight-fürtöt, illetve lekér egy adott fürtöt.</span><span class="sxs-lookup"><span data-stu-id="12dbc-126">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

### [<span data-ttu-id="12dbc-127">Get-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="12dbc-127">Get-AzHDInsightClusterAutoscaleConfiguration</span></span>](Get-AzHDInsightClusterAutoscaleConfiguration.md)
<span data-ttu-id="12dbc-128">A HDInsight-fürt automatikus skálázási konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="12dbc-128">Gets the autoscale configuration of HDInsight cluster.</span></span>

### [<span data-ttu-id="12dbc-129">Get-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="12dbc-129">Get-AzHDInsightHost</span></span>](Get-AzHDInsightHost.md)
<span data-ttu-id="12dbc-130">A HDInsight-fürt állomáslistái.</span><span class="sxs-lookup"><span data-stu-id="12dbc-130">Lists the hosts of the HDInsight cluster.</span></span>

### [<span data-ttu-id="12dbc-131">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="12dbc-131">Get-AzHDInsightJob</span></span>](Get-AzHDInsightJob.md)
<span data-ttu-id="12dbc-132">Beolvassa a feladatok listáját egy fürtből, és fordított időrendi sorrendben listázza őket, vagy lekér egy adott feladatot.</span><span class="sxs-lookup"><span data-stu-id="12dbc-132">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

### [<span data-ttu-id="12dbc-133">Get-AzHDInsightOutput</span><span class="sxs-lookup"><span data-stu-id="12dbc-133">Get-AzHDInsightJobOutput</span></span>](Get-AzHDInsightJobOutput.md)
<span data-ttu-id="12dbc-134">Egy feladat naplókimenetét egy adott fürthöz társított tárfiókból kapja meg.</span><span class="sxs-lookup"><span data-stu-id="12dbc-134">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

### [<span data-ttu-id="12dbc-135">Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="12dbc-135">Get-AzHDInsightMonitoring</span></span>](Get-AzHDInsightMonitoring.md)
<span data-ttu-id="12dbc-136">A fürtön telepített telepítés figyelési állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="12dbc-136">Gets the status of monitoring installation on the cluster.</span></span>

### [<span data-ttu-id="12dbc-137">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="12dbc-137">Get-AzHDInsightPersistedScriptAction</span></span>](Get-AzHDInsightPersistedScriptAction.md)
<span data-ttu-id="12dbc-138">Lejátsa egy fürt megőrzött parancsprogram-műveletét, és időrendben felsorolja őket, vagy egy adott állandó parancsfájlművelet részleteit.</span><span class="sxs-lookup"><span data-stu-id="12dbc-138">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

### [<span data-ttu-id="12dbc-139">Get-AzHDInsightProperty</span><span class="sxs-lookup"><span data-stu-id="12dbc-139">Get-AzHDInsightProperty</span></span>](Get-AzHDInsightProperty.md)
<span data-ttu-id="12dbc-140">Beszerzheti a HDInsight szolgáltatás tulajdonságait, például az elérhető helyeket és a kapacitást.</span><span class="sxs-lookup"><span data-stu-id="12dbc-140">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

### [<span data-ttu-id="12dbc-141">Get-AzHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="12dbc-141">Get-AzHDInsightScriptActionHistory</span></span>](Get-AzHDInsightScriptActionHistory.md)
<span data-ttu-id="12dbc-142">Lekérte egy fürt parancsfájl-műveletelőzményét, és fordított időrendi sorrendben listázza azt, vagy egy korábban végrehajtott parancsprogram-művelet részleteit.</span><span class="sxs-lookup"><span data-stu-id="12dbc-142">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

### [<span data-ttu-id="12dbc-143">Invoke-AzHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="12dbc-143">Invoke-AzHDInsightHiveJob</span></span>](Invoke-AzHDInsightHiveJob.md)
<span data-ttu-id="12dbc-144">Hive-lekérdezést küld egy HDInsight-fürtnek, és egy művelettel beolvassa a lekérdezés eredményét.</span><span class="sxs-lookup"><span data-stu-id="12dbc-144">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

### [<span data-ttu-id="12dbc-145">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="12dbc-145">New-AzHDInsightCluster</span></span>](New-AzHDInsightCluster.md)
<span data-ttu-id="12dbc-146">Azure HDInsight-fürtöt hoz létre a megadott erőforráscsoportban az aktuális előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="12dbc-146">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

### [<span data-ttu-id="12dbc-147">New-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="12dbc-147">New-AzHDInsightClusterAutoscaleConfiguration</span></span>](New-AzHDInsightClusterAutoscaleConfiguration.md)
<span data-ttu-id="12dbc-148">Egy nem állandó objektumot hoz létre, amely leírja egy Azure HDInsight-fürt automatikus skálázási konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="12dbc-148">Creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="12dbc-149">New-AzHDInsightClusterAutoscaleScheduleCondition</span><span class="sxs-lookup"><span data-stu-id="12dbc-149">New-AzHDInsightClusterAutoscaleScheduleCondition</span></span>](New-AzHDInsightClusterAutoscaleScheduleCondition.md)
<span data-ttu-id="12dbc-150">Automatikus ütemezési feltételt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="12dbc-150">Creates Schedule-based autoscale condition.</span></span>

### [<span data-ttu-id="12dbc-151">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="12dbc-151">New-AzHDInsightClusterConfig</span></span>](New-AzHDInsightClusterConfig.md)
<span data-ttu-id="12dbc-152">Olyan nem állandó fürtkonfigurációs objektumot hoz létre, amely leírja az Azure HDInsight-fürtkonfigurációt.</span><span class="sxs-lookup"><span data-stu-id="12dbc-152">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

### [<span data-ttu-id="12dbc-153">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="12dbc-153">New-AzHDInsightHiveJobDefinition</span></span>](New-AzHDInsightHiveJobDefinition.md)
<span data-ttu-id="12dbc-154">Létrehoz egy Hive-feladatobjektumot.</span><span class="sxs-lookup"><span data-stu-id="12dbc-154">Creates a Hive job object.</span></span>

### [<span data-ttu-id="12dbc-155">New-AzHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="12dbc-155">New-AzHDInsightMapReduceJobDefinition</span></span>](New-AzHDInsightMapReduceJobDefinition.md)
<span data-ttu-id="12dbc-156">MapReduce-feladatobjektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="12dbc-156">Creates a MapReduce job object.</span></span>

### [<span data-ttu-id="12dbc-157">New-AzHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="12dbc-157">New-AzHDInsightPigJobDefinition</span></span>](New-AzHDInsightPigJobDefinition.md)
<span data-ttu-id="12dbc-158">Ezzel a beállításokkal egy feladatobjektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="12dbc-158">Creates a Pig job object.</span></span>

### [<span data-ttu-id="12dbc-159">New-AzHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="12dbc-159">New-AzHDInsightSqoopJobDefinition</span></span>](New-AzHDInsightSqoopJobDefinition.md)
<span data-ttu-id="12dbc-160">Létrehoz egy Sqoop feladatobjektumot.</span><span class="sxs-lookup"><span data-stu-id="12dbc-160">Creates a Sqoop job object.</span></span>

### [<span data-ttu-id="12dbc-161">New-AzHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="12dbc-161">New-AzHDInsightStreamingMapReduceJobDefinition</span></span>](New-AzHDInsightStreamingMapReduceJobDefinition.md)
<span data-ttu-id="12dbc-162">Létrehozza a Streaming MapReduce feladatobjektumot.</span><span class="sxs-lookup"><span data-stu-id="12dbc-162">Creates a Streaming MapReduce job object.</span></span>

### [<span data-ttu-id="12dbc-163">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="12dbc-163">Remove-AzHDInsightCluster</span></span>](Remove-AzHDInsightCluster.md)
<span data-ttu-id="12dbc-164">A megadott HDInsight-fürt eltávolítása az aktuális előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="12dbc-164">Removes the specified HDInsight cluster from the current subscription.</span></span>

### [<span data-ttu-id="12dbc-165">Remove-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="12dbc-165">Remove-AzHDInsightClusterAutoscaleConfiguration</span></span>](Remove-AzHDInsightClusterAutoscaleConfiguration.md)
<span data-ttu-id="12dbc-166">A HDInsight-fürt automatikus skálázási konfigurációjának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="12dbc-166">Removes the autoscale configuration of the HDInsight cluster.</span></span>

### [<span data-ttu-id="12dbc-167">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="12dbc-167">Remove-AzHDInsightPersistedScriptAction</span></span>](Remove-AzHDInsightPersistedScriptAction.md)
<span data-ttu-id="12dbc-168">Egy megőrzött parancsfájl-műveletet eltávolít egy HDInsight-fürtből.</span><span class="sxs-lookup"><span data-stu-id="12dbc-168">Removes an persisted script action from an HDInsight cluster.</span></span>

### [<span data-ttu-id="12dbc-169">Restart-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="12dbc-169">Restart-AzHDInsightHost</span></span>](Restart-AzHDInsightHost.md)
<span data-ttu-id="12dbc-170">Újraindítja a HDInsight-fürt adott állomását.</span><span class="sxs-lookup"><span data-stu-id="12dbc-170">Restarts the specific hosts of HDInsight cluster.</span></span>

### [<span data-ttu-id="12dbc-171">Set-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="12dbc-171">Set-AzHDInsightClusterAutoscaleConfiguration</span></span>](Set-AzHDInsightClusterAutoscaleConfiguration.md)
<span data-ttu-id="12dbc-172">Beállítja egy Azure HDInsight-fürt automatikus skálázási konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="12dbc-172">Sets the autoscale configuration of an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="12dbc-173">Set-AzHDInsightClusterDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="12dbc-173">Set-AzHDInsightClusterDiskEncryptionKey</span></span>](Set-AzHDInsightClusterDiskEncryptionKey.md)
<span data-ttu-id="12dbc-174">A megadott HDInsight-fürt lemeztitkosítási kulcsának elforgatása.</span><span class="sxs-lookup"><span data-stu-id="12dbc-174">Rotates the disk encryption key of the specified HDInsight cluster.</span></span>

### [<span data-ttu-id="12dbc-175">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="12dbc-175">Set-AzHDInsightClusterSize</span></span>](Set-AzHDInsightClusterSize.md)
<span data-ttu-id="12dbc-176">Beállítja egy adott fürt dolgozói csomópontjainak számát.</span><span class="sxs-lookup"><span data-stu-id="12dbc-176">Sets the number of Worker nodes in a specified cluster.</span></span>

### [<span data-ttu-id="12dbc-177">Set-AzHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="12dbc-177">Set-AzHDInsightDefaultStorage</span></span>](Set-AzHDInsightDefaultStorage.md)
<span data-ttu-id="12dbc-178">Egy fürtkonfigurációs objektum alapértelmezett tárfiók-beállítását állítja be.</span><span class="sxs-lookup"><span data-stu-id="12dbc-178">Sets the default Storage account setting in a cluster configuration object.</span></span>

### [<span data-ttu-id="12dbc-179">Set-AzHDInsightGatewayCredential</span><span class="sxs-lookup"><span data-stu-id="12dbc-179">Set-AzHDInsightGatewayCredential</span></span>](Set-AzHDInsightGatewayCredential.md)
<span data-ttu-id="12dbc-180">Beállítja egy Azure HDInsight-fürt átjáró HTTP-hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="12dbc-180">Sets the gateway HTTP credentials of an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="12dbc-181">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="12dbc-181">Set-AzHDInsightPersistedScriptAction</span></span>](Set-AzHDInsightPersistedScriptAction.md)
<span data-ttu-id="12dbc-182">Egy korábban végrehajtott parancsfájl-műveletet állandó parancsfájl-műveletként állít be.</span><span class="sxs-lookup"><span data-stu-id="12dbc-182">Sets a previously executed script action to be a persisted script action.</span></span>

### [<span data-ttu-id="12dbc-183">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="12dbc-183">Start-AzHDInsightJob</span></span>](Start-AzHDInsightJob.md)
<span data-ttu-id="12dbc-184">Egy megadott Azure HDInsight-feladatot kezd egy adott fürtön.</span><span class="sxs-lookup"><span data-stu-id="12dbc-184">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

### [<span data-ttu-id="12dbc-185">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="12dbc-185">Stop-AzHDInsightJob</span></span>](Stop-AzHDInsightJob.md)
<span data-ttu-id="12dbc-186">Leállít egy megadott futó feladatot egy fürtön.</span><span class="sxs-lookup"><span data-stu-id="12dbc-186">Stops a specified running job on a cluster.</span></span>

### [<span data-ttu-id="12dbc-187">Submit-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="12dbc-187">Submit-AzHDInsightScriptAction</span></span>](Submit-AzHDInsightScriptAction.md)
<span data-ttu-id="12dbc-188">Új parancsfájl-műveletet küld egy Azure HDInsight-fürtnek.</span><span class="sxs-lookup"><span data-stu-id="12dbc-188">Submits a new script action to an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="12dbc-189">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="12dbc-189">Use-AzHDInsightCluster</span></span>](Use-AzHDInsightCluster.md)
<span data-ttu-id="12dbc-190">A parancsmaggal együtt használni kívánt Invoke-RmAzureHDInsightHiveJob kijelölése.</span><span class="sxs-lookup"><span data-stu-id="12dbc-190">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

### [<span data-ttu-id="12dbc-191">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="12dbc-191">Wait-AzHDInsightJob</span></span>](Wait-AzHDInsightJob.md)
<span data-ttu-id="12dbc-192">Megvárja egy adott feladat elvégzését vagy sikertelenségét.</span><span class="sxs-lookup"><span data-stu-id="12dbc-192">Waits for the completion or failure of a specified job.</span></span>

