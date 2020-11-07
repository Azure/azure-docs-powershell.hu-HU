---
Module Name: Az.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
ms.openlocfilehash: 78153558764d12a63d6c1b599da2067338969628
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93657854"
---
# <span data-ttu-id="9885d-101">Az. HDInsight modul</span><span class="sxs-lookup"><span data-stu-id="9885d-101">Az.HDInsight Module</span></span>
## <span data-ttu-id="9885d-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="9885d-102">Description</span></span>
<span data-ttu-id="9885d-103">Az ebben a szakaszban szereplő témakörök az Azure Resource Manager (ARM) keretrendszerben az Azure PowerShell-parancsmagok a Microsoft Azure HDInsight című témakörben olvashatók.</span><span class="sxs-lookup"><span data-stu-id="9885d-103">The topics in this section document the Azure PowerShell cmdlets for Microsoft Azure HDInsight in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="9885d-104">Ezek a parancsmagok a HDInsight-fürtök és a rajtuk futó feladatok kezelésére szolgálnak.</span><span class="sxs-lookup"><span data-stu-id="9885d-104">These cmdlets are used to manage HDInsight clusters and the jobs that run on them.</span></span> <span data-ttu-id="9885d-105">A parancsmagok a Microsoft. Azure. commands. HDInsight névtérben találhatók.</span><span class="sxs-lookup"><span data-stu-id="9885d-105">The cmdlets exist in the Microsoft.Azure.Commands.HDInsight namespace.</span></span>

## <span data-ttu-id="9885d-106">Az. HDInsight parancsmagok</span><span class="sxs-lookup"><span data-stu-id="9885d-106">Az.HDInsight Cmdlets</span></span>
### [<span data-ttu-id="9885d-107">Add-AzHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="9885d-107">Add-AzHDInsightClusterIdentity</span></span>](Add-AzHDInsightClusterIdentity.md)
<span data-ttu-id="9885d-108">A fürt identitását hozzáadja a fürtkonfiguráció-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="9885d-108">Adds a cluster identity to a cluster configuration object.</span></span>

### [<span data-ttu-id="9885d-109">Add-AzHDInsightComponentVersion</span><span class="sxs-lookup"><span data-stu-id="9885d-109">Add-AzHDInsightComponentVersion</span></span>](Add-AzHDInsightComponentVersion.md)
<span data-ttu-id="9885d-110">A fürtben futó szolgáltatás verziójának hozzáadása a fürtkonfiguráció-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="9885d-110">Adds a version for a service running in a cluster to a cluster configuration object.</span></span>

### [<span data-ttu-id="9885d-111">Add-AzHDInsightConfigValue</span><span class="sxs-lookup"><span data-stu-id="9885d-111">Add-AzHDInsightConfigValue</span></span>](Add-AzHDInsightConfigValue.md)
<span data-ttu-id="9885d-112">A Hadoop konfigurációs érték testreszabása és/vagy a kaptár megosztott tár testreszabása a fürtkonfigurációs objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="9885d-112">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

### [<span data-ttu-id="9885d-113">Add-AzHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="9885d-113">Add-AzHDInsightMetastore</span></span>](Add-AzHDInsightMetastore.md)
<span data-ttu-id="9885d-114">Felvesz egy SQL-adatbázist, amely kaptárként vagy Oozie metastore-objektumként szolgál.</span><span class="sxs-lookup"><span data-stu-id="9885d-114">Adds a SQL Database to serve as a Hive or Oozie metastore to a cluster configuration object.</span></span>

### [<span data-ttu-id="9885d-115">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="9885d-115">Add-AzHDInsightScriptAction</span></span>](Add-AzHDInsightScriptAction.md)
<span data-ttu-id="9885d-116">Parancsfájl-műveleteket ad egy fürtkonfiguráció-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="9885d-116">Adds a script action to a cluster configuration object.</span></span>

### [<span data-ttu-id="9885d-117">Add-AzHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="9885d-117">Add-AzHDInsightSecurityProfile</span></span>](Add-AzHDInsightSecurityProfile.md)
<span data-ttu-id="9885d-118">Felvesz egy biztonsági profileto a fürtkonfigurációs objektumba.</span><span class="sxs-lookup"><span data-stu-id="9885d-118">Adds a security profileto a cluster configuration object.</span></span>

### [<span data-ttu-id="9885d-119">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="9885d-119">Add-AzHDInsightStorage</span></span>](Add-AzHDInsightStorage.md)
<span data-ttu-id="9885d-120">Azure-tárterületet ad hozzá egy fürtkonfiguráció-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="9885d-120">Adds an Azure Storage key to a cluster configuration object.</span></span>

### [<span data-ttu-id="9885d-121">Disable-AzHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="9885d-121">Disable-AzHDInsightOperationsManagementSuite</span></span>](Disable-AzHDInsightOperationsManagementSuite.md)
<span data-ttu-id="9885d-122">Letiltja a műveleti menedzsment programcsomagot (OMS) egy HDInsight-fürtben, és a releváns naplók az engedélyezés során meghatározott OMS-munkaterületre áramlanak.</span><span class="sxs-lookup"><span data-stu-id="9885d-122">Disables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will stop flowing to the OMS workspace specified during enable.</span></span>

### [<span data-ttu-id="9885d-123">Enable-AzHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="9885d-123">Enable-AzHDInsightOperationsManagementSuite</span></span>](Enable-AzHDInsightOperationsManagementSuite.md)
<span data-ttu-id="9885d-124">Engedélyezi a Operations Management Suite (OMS) HDInsight-fürtöt, és a megfelelő naplók az engedélyezés során megadott OMS-munkaterületre kerülnek.</span><span class="sxs-lookup"><span data-stu-id="9885d-124">Enables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will be sent to the OMS workspace specified during enable.</span></span>

### [<span data-ttu-id="9885d-125">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9885d-125">Get-AzHDInsightCluster</span></span>](Get-AzHDInsightCluster.md)
<span data-ttu-id="9885d-126">A jelenlegi előfizetéshez vagy egy meghatározott erőforráscsoporthoz tartozó összes Azure HDInsight-szektorcsoport beszerzése és listázása, vagy egy adott fürt beolvasása.</span><span class="sxs-lookup"><span data-stu-id="9885d-126">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

### [<span data-ttu-id="9885d-127">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9885d-127">Get-AzHDInsightJob</span></span>](Get-AzHDInsightJob.md)
<span data-ttu-id="9885d-128">Kinyeri a feladatok listáját egy fürtből, és megfordítja őket fordított időrendi sorrendben, vagy egy adott feladatot lekérdez.</span><span class="sxs-lookup"><span data-stu-id="9885d-128">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

### [<span data-ttu-id="9885d-129">Get-AzHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="9885d-129">Get-AzHDInsightJobOutput</span></span>](Get-AzHDInsightJobOutput.md)
<span data-ttu-id="9885d-130">A megadott fürthöz társított tárolási fiókból kapja meg a napló kimenetét.</span><span class="sxs-lookup"><span data-stu-id="9885d-130">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

### [<span data-ttu-id="9885d-131">Get-AzHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="9885d-131">Get-AzHDInsightOperationsManagementSuite</span></span>](Get-AzHDInsightOperationsManagementSuite.md)
<span data-ttu-id="9885d-132">A OMS (Operations Management Suite) telepítésének állapotát kapja meg a fürtön.</span><span class="sxs-lookup"><span data-stu-id="9885d-132">Gets the status of Operations Management Suite (OMS) installation on the cluster.</span></span>

### [<span data-ttu-id="9885d-133">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="9885d-133">Get-AzHDInsightPersistedScriptAction</span></span>](Get-AzHDInsightPersistedScriptAction.md)
<span data-ttu-id="9885d-134">Beolvassa a fürtök állandó parancsfájlokkal kapcsolatos műveleteit, és időrendi sorrendben listázza őket, illetve a megadott, kimaradt parancsfájlokra vonatkozó adatokat kap.</span><span class="sxs-lookup"><span data-stu-id="9885d-134">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

### [<span data-ttu-id="9885d-135">Get-AzHDInsightProperty</span><span class="sxs-lookup"><span data-stu-id="9885d-135">Get-AzHDInsightProperty</span></span>](Get-AzHDInsightProperty.md)
<span data-ttu-id="9885d-136">Beolvassa a HDInsight szolgáltatás tulajdonságait, például a rendelkezésre álló helyeket és a kapacitást.</span><span class="sxs-lookup"><span data-stu-id="9885d-136">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

### [<span data-ttu-id="9885d-137">Get-AzHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="9885d-137">Get-AzHDInsightScriptActionHistory</span></span>](Get-AzHDInsightScriptActionHistory.md)
<span data-ttu-id="9885d-138">Egy fürt parancsfájl-végrehajtási előzményeit jeleníti meg, és megfordítja őket fordított időrendi sorrendben, vagy egy korábban végrehajtott parancsfájl-művelet részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9885d-138">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

### [<span data-ttu-id="9885d-139">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="9885d-139">Grant-AzHDInsightHttpServicesAccess</span></span>](Grant-AzHDInsightHttpServicesAccess.md)
<span data-ttu-id="9885d-140">HTTP-hozzáférést biztosít a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="9885d-140">Grants HTTP access to the cluster.</span></span>

### [<span data-ttu-id="9885d-141">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="9885d-141">Grant-AzHDInsightRdpServicesAccess</span></span>](Grant-AzHDInsightRdpServicesAccess.md)
<span data-ttu-id="9885d-142">RDP-elérést ad vissza a Windows-fürthöz.</span><span class="sxs-lookup"><span data-stu-id="9885d-142">Grants RDP access to the Windows cluster.</span></span>

### [<span data-ttu-id="9885d-143">Meghívó-AzHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="9885d-143">Invoke-AzHDInsightHiveJob</span></span>](Invoke-AzHDInsightHiveJob.md)
<span data-ttu-id="9885d-144">A kaptár-lekérdezést elküldi egy HDInsight-fürtnek, és egy műveletben lekérdezi a lekérdezés eredményét.</span><span class="sxs-lookup"><span data-stu-id="9885d-144">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

### [<span data-ttu-id="9885d-145">Új – AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9885d-145">New-AzHDInsightCluster</span></span>](New-AzHDInsightCluster.md)
<span data-ttu-id="9885d-146">Azure HDInsight-fürtöt hoz létre az aktuális előfizetéshez megadott erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="9885d-146">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

### [<span data-ttu-id="9885d-147">Új – AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="9885d-147">New-AzHDInsightClusterConfig</span></span>](New-AzHDInsightClusterConfig.md)
<span data-ttu-id="9885d-148">Nem állandó fürtkonfiguráció-objektumot hoz létre, amely leírja az Azure HDInsight-fürtös konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="9885d-148">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

### [<span data-ttu-id="9885d-149">Új – AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="9885d-149">New-AzHDInsightHiveJobDefinition</span></span>](New-AzHDInsightHiveJobDefinition.md)
<span data-ttu-id="9885d-150">Kaptár-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9885d-150">Creates a Hive job object.</span></span>

### [<span data-ttu-id="9885d-151">Új – AzHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="9885d-151">New-AzHDInsightMapReduceJobDefinition</span></span>](New-AzHDInsightMapReduceJobDefinition.md)
<span data-ttu-id="9885d-152">Létrehoz egy MapReduce.</span><span class="sxs-lookup"><span data-stu-id="9885d-152">Creates a MapReduce job object.</span></span>

### [<span data-ttu-id="9885d-153">Új – AzHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="9885d-153">New-AzHDInsightPigJobDefinition</span></span>](New-AzHDInsightPigJobDefinition.md)
<span data-ttu-id="9885d-154">Egy Pig-Job objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9885d-154">Creates a Pig job object.</span></span>

### [<span data-ttu-id="9885d-155">Új – AzHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="9885d-155">New-AzHDInsightSqoopJobDefinition</span></span>](New-AzHDInsightSqoopJobDefinition.md)
<span data-ttu-id="9885d-156">Létrehoz egy Sqoop.</span><span class="sxs-lookup"><span data-stu-id="9885d-156">Creates a Sqoop job object.</span></span>

### [<span data-ttu-id="9885d-157">Új – AzHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="9885d-157">New-AzHDInsightStreamingMapReduceJobDefinition</span></span>](New-AzHDInsightStreamingMapReduceJobDefinition.md)
<span data-ttu-id="9885d-158">Adatfolyam-MapReduce hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9885d-158">Creates a Streaming MapReduce job object.</span></span>

### [<span data-ttu-id="9885d-159">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9885d-159">Remove-AzHDInsightCluster</span></span>](Remove-AzHDInsightCluster.md)
<span data-ttu-id="9885d-160">Eltávolítja a megadott HDInsight-fürtöt az aktuális előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="9885d-160">Removes the specified HDInsight cluster from the current subscription.</span></span>

### [<span data-ttu-id="9885d-161">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="9885d-161">Remove-AzHDInsightPersistedScriptAction</span></span>](Remove-AzHDInsightPersistedScriptAction.md)
<span data-ttu-id="9885d-162">Állandó parancsfájl-művelet eltávolítása egy HDInsight-fürtről.</span><span class="sxs-lookup"><span data-stu-id="9885d-162">Removes an persisted script action from an HDInsight cluster.</span></span>

### [<span data-ttu-id="9885d-163">Visszavonás-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="9885d-163">Revoke-AzHDInsightHttpServicesAccess</span></span>](Revoke-AzHDInsightHttpServicesAccess.md)
<span data-ttu-id="9885d-164">Letiltja a fürt HTTP-elérését.</span><span class="sxs-lookup"><span data-stu-id="9885d-164">Disables HTTP access to the cluster.</span></span>

### [<span data-ttu-id="9885d-165">Visszavonás-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="9885d-165">Revoke-AzHDInsightRdpServicesAccess</span></span>](Revoke-AzHDInsightRdpServicesAccess.md)
<span data-ttu-id="9885d-166">Letiltja a Windows-fürtök RDP-elérését.</span><span class="sxs-lookup"><span data-stu-id="9885d-166">Disables RDP access to a Windows cluster.</span></span>

### [<span data-ttu-id="9885d-167">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="9885d-167">Set-AzHDInsightClusterSize</span></span>](Set-AzHDInsightClusterSize.md)
<span data-ttu-id="9885d-168">A megadott szektorcsoportban lévő munkaállomások számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9885d-168">Sets the number of Worker nodes in a specified cluster.</span></span>

### [<span data-ttu-id="9885d-169">Set-AzHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="9885d-169">Set-AzHDInsightDefaultStorage</span></span>](Set-AzHDInsightDefaultStorage.md)
<span data-ttu-id="9885d-170">Beállítja az alapértelmezett tárolási fiók beállítását egy fürtkonfiguráció-objektumban.</span><span class="sxs-lookup"><span data-stu-id="9885d-170">Sets the default Storage account setting in a cluster configuration object.</span></span>

### [<span data-ttu-id="9885d-171">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="9885d-171">Set-AzHDInsightPersistedScriptAction</span></span>](Set-AzHDInsightPersistedScriptAction.md)
<span data-ttu-id="9885d-172">Egy korábban futtatott parancsfájlt egy állandó parancsfájl-műveletre állítja be.</span><span class="sxs-lookup"><span data-stu-id="9885d-172">Sets a previously executed script action to be a persisted script action.</span></span>

### [<span data-ttu-id="9885d-173">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9885d-173">Start-AzHDInsightJob</span></span>](Start-AzHDInsightJob.md)
<span data-ttu-id="9885d-174">Meghatározott Azure HDInsight-feladatot indít egy adott fürtön.</span><span class="sxs-lookup"><span data-stu-id="9885d-174">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

### [<span data-ttu-id="9885d-175">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9885d-175">Stop-AzHDInsightJob</span></span>](Stop-AzHDInsightJob.md)
<span data-ttu-id="9885d-176">Meghatározott futó feladat leállítása egy fürtben.</span><span class="sxs-lookup"><span data-stu-id="9885d-176">Stops a specified running job on a cluster.</span></span>

### [<span data-ttu-id="9885d-177">Submit-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="9885d-177">Submit-AzHDInsightScriptAction</span></span>](Submit-AzHDInsightScriptAction.md)
<span data-ttu-id="9885d-178">Új parancsfájl-művelet elküldhet egy Azure HDInsight-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="9885d-178">Submits a new script action to an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="9885d-179">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9885d-179">Use-AzHDInsightCluster</span></span>](Use-AzHDInsightCluster.md)
<span data-ttu-id="9885d-180">Kijelöli az Invoke-RmAzureHDInsightHiveJob parancsmaggal használni kívánt fürtöt.</span><span class="sxs-lookup"><span data-stu-id="9885d-180">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

### [<span data-ttu-id="9885d-181">Várjon-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9885d-181">Wait-AzHDInsightJob</span></span>](Wait-AzHDInsightJob.md)
<span data-ttu-id="9885d-182">A megadott feladat befejezését vagy hibáját várja.</span><span class="sxs-lookup"><span data-stu-id="9885d-182">Waits for the completion or failure of a specified job.</span></span>

