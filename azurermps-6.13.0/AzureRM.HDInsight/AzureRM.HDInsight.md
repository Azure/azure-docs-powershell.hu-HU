---
Module Name: AzureRM.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/AzureRM.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/AzureRM.HDInsight.md
ms.openlocfilehash: bbbb418a8e101fa1b806bc910132f44e40158190
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93490208"
---
# <span data-ttu-id="eddab-101">AzureRM. HDInsight modul</span><span class="sxs-lookup"><span data-stu-id="eddab-101">AzureRM.HDInsight Module</span></span>
## <span data-ttu-id="eddab-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="eddab-102">Description</span></span>
<span data-ttu-id="eddab-103">Az ebben a szakaszban szereplő témakörök az Azure Resource Manager (ARM) keretrendszerben az Azure PowerShell-parancsmagok a Microsoft Azure HDInsight című témakörben olvashatók.</span><span class="sxs-lookup"><span data-stu-id="eddab-103">The topics in this section document the Azure PowerShell cmdlets for Microsoft Azure HDInsight in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="eddab-104">Ezek a parancsmagok a HDInsight-fürtök és a rajtuk futó feladatok kezelésére szolgálnak.</span><span class="sxs-lookup"><span data-stu-id="eddab-104">These cmdlets are used to manage HDInsight clusters and the jobs that run on them.</span></span> <span data-ttu-id="eddab-105">A parancsmagok a Microsoft. Azure. commands. HDInsight névtérben találhatók.</span><span class="sxs-lookup"><span data-stu-id="eddab-105">The cmdlets exist in the Microsoft.Azure.Commands.HDInsight namespace.</span></span>

## <span data-ttu-id="eddab-106">AzureRM. HDInsight parancsmagok</span><span class="sxs-lookup"><span data-stu-id="eddab-106">AzureRM.HDInsight Cmdlets</span></span>
### [<span data-ttu-id="eddab-107">Add-AzureRmHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="eddab-107">Add-AzureRmHDInsightClusterIdentity</span></span>](Add-AzureRmHDInsightClusterIdentity.md)
<span data-ttu-id="eddab-108">A fürt identitását hozzáadja a fürtkonfiguráció-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="eddab-108">Adds a cluster identity to a cluster configuration object.</span></span>

### [<span data-ttu-id="eddab-109">Add-AzureRmHDInsightComponentVersion</span><span class="sxs-lookup"><span data-stu-id="eddab-109">Add-AzureRmHDInsightComponentVersion</span></span>](Add-AzureRmHDInsightComponentVersion.md)
<span data-ttu-id="eddab-110">A fürtben futó szolgáltatás verziójának hozzáadása a fürtkonfiguráció-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="eddab-110">Adds a version for a service running in a cluster to a cluster configuration object.</span></span>

### [<span data-ttu-id="eddab-111">Add-AzureRmHDInsightConfigValues</span><span class="sxs-lookup"><span data-stu-id="eddab-111">Add-AzureRmHDInsightConfigValues</span></span>](Add-AzureRmHDInsightConfigValues.md)
<span data-ttu-id="eddab-112">A Hadoop konfigurációs érték testreszabása és/vagy a kaptár megosztott tár testreszabása a fürtkonfigurációs objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="eddab-112">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

### [<span data-ttu-id="eddab-113">Add-AzureRmHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="eddab-113">Add-AzureRmHDInsightMetastore</span></span>](Add-AzureRmHDInsightMetastore.md)
<span data-ttu-id="eddab-114">Felvesz egy SQL-adatbázist, amely kaptárként vagy Oozie metastore-objektumként szolgál.</span><span class="sxs-lookup"><span data-stu-id="eddab-114">Adds a SQL Database to serve as a Hive or Oozie metastore to a cluster configuration object.</span></span>

### [<span data-ttu-id="eddab-115">Add-AzureRmHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="eddab-115">Add-AzureRmHDInsightScriptAction</span></span>](Add-AzureRmHDInsightScriptAction.md)
<span data-ttu-id="eddab-116">Parancsfájl-műveleteket ad egy fürtkonfiguráció-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="eddab-116">Adds a script action to a cluster configuration object.</span></span>

### [<span data-ttu-id="eddab-117">Add-AzureRmHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="eddab-117">Add-AzureRmHDInsightSecurityProfile</span></span>](Add-AzureRmHDInsightSecurityProfile.md)
<span data-ttu-id="eddab-118">Felvesz egy biztonsági profileto a fürtkonfigurációs objektumba.</span><span class="sxs-lookup"><span data-stu-id="eddab-118">Adds a security profileto a cluster configuration object.</span></span>

### [<span data-ttu-id="eddab-119">Add-AzureRmHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="eddab-119">Add-AzureRmHDInsightStorage</span></span>](Add-AzureRmHDInsightStorage.md)
<span data-ttu-id="eddab-120">Azure-tárterületet ad hozzá egy fürtkonfiguráció-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="eddab-120">Adds an Azure Storage key to a cluster configuration object.</span></span>

### [<span data-ttu-id="eddab-121">Disable-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="eddab-121">Disable-AzureRmHDInsightOperationsManagementSuite</span></span>](Disable-AzureRmHDInsightOperationsManagementSuite.md)
<span data-ttu-id="eddab-122">Letiltja a műveleti menedzsment programcsomagot (OMS) egy HDInsight-fürtben, és a releváns naplók az engedélyezés során meghatározott OMS-munkaterületre áramlanak.</span><span class="sxs-lookup"><span data-stu-id="eddab-122">Disables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will stop flowing to the OMS workspace specified during enable.</span></span>

### [<span data-ttu-id="eddab-123">Enable-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="eddab-123">Enable-AzureRmHDInsightOperationsManagementSuite</span></span>](Enable-AzureRmHDInsightOperationsManagementSuite.md)
<span data-ttu-id="eddab-124">Engedélyezi a Operations Management Suite (OMS) HDInsight-fürtöt, és a megfelelő naplók az engedélyezés során megadott OMS-munkaterületre kerülnek.</span><span class="sxs-lookup"><span data-stu-id="eddab-124">Enables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will be sent to the OMS workspace specified during enable.</span></span>

### [<span data-ttu-id="eddab-125">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="eddab-125">Get-AzureRmHDInsightCluster</span></span>](Get-AzureRmHDInsightCluster.md)
<span data-ttu-id="eddab-126">A jelenlegi előfizetéshez vagy egy meghatározott erőforráscsoporthoz tartozó összes Azure HDInsight-szektorcsoport beszerzése és listázása, vagy egy adott fürt beolvasása.</span><span class="sxs-lookup"><span data-stu-id="eddab-126">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

### [<span data-ttu-id="eddab-127">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="eddab-127">Get-AzureRmHDInsightJob</span></span>](Get-AzureRmHDInsightJob.md)
<span data-ttu-id="eddab-128">Kinyeri a feladatok listáját egy fürtből, és megfordítja őket fordított időrendi sorrendben, vagy egy adott feladatot lekérdez.</span><span class="sxs-lookup"><span data-stu-id="eddab-128">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

### [<span data-ttu-id="eddab-129">Get-AzureRmHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="eddab-129">Get-AzureRmHDInsightJobOutput</span></span>](Get-AzureRmHDInsightJobOutput.md)
<span data-ttu-id="eddab-130">A megadott fürthöz társított tárolási fiókból kapja meg a napló kimenetét.</span><span class="sxs-lookup"><span data-stu-id="eddab-130">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

### [<span data-ttu-id="eddab-131">Get-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="eddab-131">Get-AzureRmHDInsightOperationsManagementSuite</span></span>](Get-AzureRmHDInsightOperationsManagementSuite.md)
<span data-ttu-id="eddab-132">A OMS (Operations Management Suite) telepítésének állapotát kapja meg a fürtön.</span><span class="sxs-lookup"><span data-stu-id="eddab-132">Gets the status of Operations Management Suite (OMS) installation on the cluster.</span></span>

### [<span data-ttu-id="eddab-133">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="eddab-133">Get-AzureRmHDInsightPersistedScriptAction</span></span>](Get-AzureRmHDInsightPersistedScriptAction.md)
<span data-ttu-id="eddab-134">Beolvassa a fürtök állandó parancsfájlokkal kapcsolatos műveleteit, és időrendi sorrendben listázza őket, illetve a megadott, kimaradt parancsfájlokra vonatkozó adatokat kap.</span><span class="sxs-lookup"><span data-stu-id="eddab-134">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

### [<span data-ttu-id="eddab-135">Get-AzureRmHDInsightProperties</span><span class="sxs-lookup"><span data-stu-id="eddab-135">Get-AzureRmHDInsightProperties</span></span>](Get-AzureRmHDInsightProperties.md)
<span data-ttu-id="eddab-136">Beolvassa a HDInsight szolgáltatás tulajdonságait, például a rendelkezésre álló helyeket és a kapacitást.</span><span class="sxs-lookup"><span data-stu-id="eddab-136">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

### [<span data-ttu-id="eddab-137">Get-AzureRmHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="eddab-137">Get-AzureRmHDInsightScriptActionHistory</span></span>](Get-AzureRmHDInsightScriptActionHistory.md)
<span data-ttu-id="eddab-138">Egy fürt parancsfájl-végrehajtási előzményeit jeleníti meg, és megfordítja őket fordított időrendi sorrendben, vagy egy korábban végrehajtott parancsfájl-művelet részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="eddab-138">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

### [<span data-ttu-id="eddab-139">Grant-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="eddab-139">Grant-AzureRmHDInsightHttpServicesAccess</span></span>](Grant-AzureRmHDInsightHttpServicesAccess.md)
<span data-ttu-id="eddab-140">HTTP-hozzáférést biztosít a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="eddab-140">Grants HTTP access to the cluster.</span></span>

### [<span data-ttu-id="eddab-141">Grant-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="eddab-141">Grant-AzureRmHDInsightRdpServicesAccess</span></span>](Grant-AzureRmHDInsightRdpServicesAccess.md)
<span data-ttu-id="eddab-142">RDP-elérést ad vissza a Windows-fürthöz.</span><span class="sxs-lookup"><span data-stu-id="eddab-142">Grants RDP access to the Windows cluster.</span></span>

### [<span data-ttu-id="eddab-143">Meghívó-AzureRmHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="eddab-143">Invoke-AzureRmHDInsightHiveJob</span></span>](Invoke-AzureRmHDInsightHiveJob.md)
<span data-ttu-id="eddab-144">A kaptár-lekérdezést elküldi egy HDInsight-fürtnek, és egy műveletben lekérdezi a lekérdezés eredményét.</span><span class="sxs-lookup"><span data-stu-id="eddab-144">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

### [<span data-ttu-id="eddab-145">Új – AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="eddab-145">New-AzureRmHDInsightCluster</span></span>](New-AzureRmHDInsightCluster.md)
<span data-ttu-id="eddab-146">Azure HDInsight-fürtöt hoz létre az aktuális előfizetéshez megadott erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="eddab-146">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

### [<span data-ttu-id="eddab-147">Új – AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="eddab-147">New-AzureRmHDInsightClusterConfig</span></span>](New-AzureRmHDInsightClusterConfig.md)
<span data-ttu-id="eddab-148">Nem állandó fürtkonfiguráció-objektumot hoz létre, amely leírja az Azure HDInsight-fürtös konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="eddab-148">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

### [<span data-ttu-id="eddab-149">Új – AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="eddab-149">New-AzureRmHDInsightHiveJobDefinition</span></span>](New-AzureRmHDInsightHiveJobDefinition.md)
<span data-ttu-id="eddab-150">Kaptár-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="eddab-150">Creates a Hive job object.</span></span>

### [<span data-ttu-id="eddab-151">Új – AzureRmHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="eddab-151">New-AzureRmHDInsightMapReduceJobDefinition</span></span>](New-AzureRmHDInsightMapReduceJobDefinition.md)
<span data-ttu-id="eddab-152">Létrehoz egy MapReduce.</span><span class="sxs-lookup"><span data-stu-id="eddab-152">Creates a MapReduce job object.</span></span>

### [<span data-ttu-id="eddab-153">Új – AzureRmHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="eddab-153">New-AzureRmHDInsightPigJobDefinition</span></span>](New-AzureRmHDInsightPigJobDefinition.md)
<span data-ttu-id="eddab-154">Egy Pig-Job objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="eddab-154">Creates a Pig job object.</span></span>

### [<span data-ttu-id="eddab-155">Új – AzureRmHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="eddab-155">New-AzureRmHDInsightSqoopJobDefinition</span></span>](New-AzureRmHDInsightSqoopJobDefinition.md)
<span data-ttu-id="eddab-156">Létrehoz egy Sqoop.</span><span class="sxs-lookup"><span data-stu-id="eddab-156">Creates a Sqoop job object.</span></span>

### [<span data-ttu-id="eddab-157">Új – AzureRmHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="eddab-157">New-AzureRmHDInsightStreamingMapReduceJobDefinition</span></span>](New-AzureRmHDInsightStreamingMapReduceJobDefinition.md)
<span data-ttu-id="eddab-158">Adatfolyam-MapReduce hoz létre.</span><span class="sxs-lookup"><span data-stu-id="eddab-158">Creates a Streaming MapReduce job object.</span></span>

### [<span data-ttu-id="eddab-159">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="eddab-159">Remove-AzureRmHDInsightCluster</span></span>](Remove-AzureRmHDInsightCluster.md)
<span data-ttu-id="eddab-160">Eltávolítja a megadott HDInsight-fürtöt az aktuális előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="eddab-160">Removes the specified HDInsight cluster from the current subscription.</span></span>

### [<span data-ttu-id="eddab-161">Remove-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="eddab-161">Remove-AzureRmHDInsightPersistedScriptAction</span></span>](Remove-AzureRmHDInsightPersistedScriptAction.md)
<span data-ttu-id="eddab-162">Állandó parancsfájl-művelet eltávolítása egy HDInsight-fürtről.</span><span class="sxs-lookup"><span data-stu-id="eddab-162">Removes an persisted script action from an HDInsight cluster.</span></span>

### [<span data-ttu-id="eddab-163">Visszavonás-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="eddab-163">Revoke-AzureRmHDInsightHttpServicesAccess</span></span>](Revoke-AzureRmHDInsightHttpServicesAccess.md)
<span data-ttu-id="eddab-164">Letiltja a fürt HTTP-elérését.</span><span class="sxs-lookup"><span data-stu-id="eddab-164">Disables HTTP access to the cluster.</span></span>

### [<span data-ttu-id="eddab-165">Visszavonás-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="eddab-165">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>](Revoke-AzureRmHDInsightRdpServicesAccess.md)
<span data-ttu-id="eddab-166">Letiltja a Windows-fürtök RDP-elérését.</span><span class="sxs-lookup"><span data-stu-id="eddab-166">Disables RDP access to a Windows cluster.</span></span>

### [<span data-ttu-id="eddab-167">Set-AzureRmHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="eddab-167">Set-AzureRmHDInsightClusterSize</span></span>](Set-AzureRmHDInsightClusterSize.md)
<span data-ttu-id="eddab-168">A megadott szektorcsoportban lévő munkaállomások számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="eddab-168">Sets the number of Worker nodes in a specified cluster.</span></span>

### [<span data-ttu-id="eddab-169">Set-AzureRmHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="eddab-169">Set-AzureRmHDInsightDefaultStorage</span></span>](Set-AzureRmHDInsightDefaultStorage.md)
<span data-ttu-id="eddab-170">Beállítja az alapértelmezett tárolási fiók beállítását egy fürtkonfiguráció-objektumban.</span><span class="sxs-lookup"><span data-stu-id="eddab-170">Sets the default Storage account setting in a cluster configuration object.</span></span>

### [<span data-ttu-id="eddab-171">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="eddab-171">Set-AzureRmHDInsightPersistedScriptAction</span></span>](Set-AzureRmHDInsightPersistedScriptAction.md)
<span data-ttu-id="eddab-172">Egy korábban futtatott parancsfájlt egy állandó parancsfájl-műveletre állítja be.</span><span class="sxs-lookup"><span data-stu-id="eddab-172">Sets a previously executed script action to be a persisted script action.</span></span>

### [<span data-ttu-id="eddab-173">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="eddab-173">Start-AzureRmHDInsightJob</span></span>](Start-AzureRmHDInsightJob.md)
<span data-ttu-id="eddab-174">Meghatározott Azure HDInsight-feladatot indít egy adott fürtön.</span><span class="sxs-lookup"><span data-stu-id="eddab-174">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

### [<span data-ttu-id="eddab-175">Stop-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="eddab-175">Stop-AzureRmHDInsightJob</span></span>](Stop-AzureRmHDInsightJob.md)
<span data-ttu-id="eddab-176">Meghatározott futó feladat leállítása egy fürtben.</span><span class="sxs-lookup"><span data-stu-id="eddab-176">Stops a specified running job on a cluster.</span></span>

### [<span data-ttu-id="eddab-177">Submit-AzureRmHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="eddab-177">Submit-AzureRmHDInsightScriptAction</span></span>](Submit-AzureRmHDInsightScriptAction.md)
<span data-ttu-id="eddab-178">Új parancsfájl-művelet elküldhet egy Azure HDInsight-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="eddab-178">Submits a new script action to an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="eddab-179">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="eddab-179">Use-AzureRmHDInsightCluster</span></span>](Use-AzureRmHDInsightCluster.md)
<span data-ttu-id="eddab-180">Kijelöli az Invoke-RmAzureHDInsightHiveJob parancsmaggal használni kívánt fürtöt.</span><span class="sxs-lookup"><span data-stu-id="eddab-180">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

### [<span data-ttu-id="eddab-181">Várjon-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="eddab-181">Wait-AzureRmHDInsightJob</span></span>](Wait-AzureRmHDInsightJob.md)
<span data-ttu-id="eddab-182">A megadott feladat befejezését vagy hibáját várja.</span><span class="sxs-lookup"><span data-stu-id="eddab-182">Waits for the completion or failure of a specified job.</span></span>

