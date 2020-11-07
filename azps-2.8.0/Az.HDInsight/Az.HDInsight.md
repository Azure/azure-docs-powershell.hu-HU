---
Module Name: Az.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
ms.openlocfilehash: 33e1e9ac0b62d378954280d8dd81361c0d075a1e
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/15/2019
ms.locfileid: "93665534"
---
# <span data-ttu-id="85930-101">Az. HDInsight modul</span><span class="sxs-lookup"><span data-stu-id="85930-101">Az.HDInsight Module</span></span>
## <span data-ttu-id="85930-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="85930-102">Description</span></span>
<span data-ttu-id="85930-103">Az ebben a szakaszban szereplő témakörök az Azure Resource Manager (ARM) keretrendszerben az Azure PowerShell-parancsmagok a Microsoft Azure HDInsight című témakörben olvashatók.</span><span class="sxs-lookup"><span data-stu-id="85930-103">The topics in this section document the Azure PowerShell cmdlets for Microsoft Azure HDInsight in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="85930-104">Ezek a parancsmagok a HDInsight-fürtök és a rajtuk futó feladatok kezelésére szolgálnak.</span><span class="sxs-lookup"><span data-stu-id="85930-104">These cmdlets are used to manage HDInsight clusters and the jobs that run on them.</span></span> <span data-ttu-id="85930-105">A parancsmagok a Microsoft. Azure. commands. HDInsight névtérben találhatók.</span><span class="sxs-lookup"><span data-stu-id="85930-105">The cmdlets exist in the Microsoft.Azure.Commands.HDInsight namespace.</span></span>

## <span data-ttu-id="85930-106">Az. HDInsight parancsmagok</span><span class="sxs-lookup"><span data-stu-id="85930-106">Az.HDInsight Cmdlets</span></span>
### [<span data-ttu-id="85930-107">Add-AzHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="85930-107">Add-AzHDInsightClusterIdentity</span></span>](Add-AzHDInsightClusterIdentity.md)
<span data-ttu-id="85930-108">A fürt identitását hozzáadja a fürtkonfiguráció-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="85930-108">Adds a cluster identity to a cluster configuration object.</span></span>

### [<span data-ttu-id="85930-109">Add-AzHDInsightComponentVersion</span><span class="sxs-lookup"><span data-stu-id="85930-109">Add-AzHDInsightComponentVersion</span></span>](Add-AzHDInsightComponentVersion.md)
<span data-ttu-id="85930-110">A fürtben futó szolgáltatás verziójának hozzáadása a fürtkonfiguráció-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="85930-110">Adds a version for a service running in a cluster to a cluster configuration object.</span></span>

### [<span data-ttu-id="85930-111">Add-AzHDInsightConfigValue</span><span class="sxs-lookup"><span data-stu-id="85930-111">Add-AzHDInsightConfigValue</span></span>](Add-AzHDInsightConfigValue.md)
<span data-ttu-id="85930-112">A Hadoop konfigurációs érték testreszabása és/vagy a kaptár megosztott tár testreszabása a fürtkonfigurációs objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="85930-112">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

### [<span data-ttu-id="85930-113">Add-AzHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="85930-113">Add-AzHDInsightMetastore</span></span>](Add-AzHDInsightMetastore.md)
<span data-ttu-id="85930-114">Felvesz egy SQL-adatbázist, amely kaptárként vagy Oozie metastore-objektumként szolgál.</span><span class="sxs-lookup"><span data-stu-id="85930-114">Adds a SQL Database to serve as a Hive or Oozie metastore to a cluster configuration object.</span></span>

### [<span data-ttu-id="85930-115">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="85930-115">Add-AzHDInsightScriptAction</span></span>](Add-AzHDInsightScriptAction.md)
<span data-ttu-id="85930-116">Parancsfájl-műveleteket ad egy fürtkonfiguráció-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="85930-116">Adds a script action to a cluster configuration object.</span></span>

### [<span data-ttu-id="85930-117">Add-AzHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="85930-117">Add-AzHDInsightSecurityProfile</span></span>](Add-AzHDInsightSecurityProfile.md)
<span data-ttu-id="85930-118">Biztonsági profilt ad hozzá a fürtkonfiguráció-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="85930-118">Adds a security profile to a cluster configuration object.</span></span>

### [<span data-ttu-id="85930-119">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="85930-119">Add-AzHDInsightStorage</span></span>](Add-AzHDInsightStorage.md)
<span data-ttu-id="85930-120">Azure-tárterületet ad hozzá egy fürtkonfiguráció-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="85930-120">Adds an Azure Storage key to a cluster configuration object.</span></span>

### [<span data-ttu-id="85930-121">Disable-AzHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="85930-121">Disable-AzHDInsightOperationsManagementSuite</span></span>](Disable-AzHDInsightOperationsManagementSuite.md)
<span data-ttu-id="85930-122">Letiltja a műveleti menedzsment programcsomagot (OMS) egy HDInsight-fürtben, és a releváns naplók az engedélyezés során meghatározott OMS-munkaterületre áramlanak.</span><span class="sxs-lookup"><span data-stu-id="85930-122">Disables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will stop flowing to the OMS workspace specified during enable.</span></span>

### [<span data-ttu-id="85930-123">Enable-AzHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="85930-123">Enable-AzHDInsightOperationsManagementSuite</span></span>](Enable-AzHDInsightOperationsManagementSuite.md)
<span data-ttu-id="85930-124">Engedélyezi a Operations Management Suite (OMS) HDInsight-fürtöt, és a megfelelő naplók az engedélyezés során megadott OMS-munkaterületre kerülnek.</span><span class="sxs-lookup"><span data-stu-id="85930-124">Enables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will be sent to the OMS workspace specified during enable.</span></span>

### [<span data-ttu-id="85930-125">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="85930-125">Get-AzHDInsightCluster</span></span>](Get-AzHDInsightCluster.md)
<span data-ttu-id="85930-126">A jelenlegi előfizetéshez vagy egy meghatározott erőforráscsoporthoz tartozó összes Azure HDInsight-szektorcsoport beszerzése és listázása, vagy egy adott fürt beolvasása.</span><span class="sxs-lookup"><span data-stu-id="85930-126">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

### [<span data-ttu-id="85930-127">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="85930-127">Get-AzHDInsightJob</span></span>](Get-AzHDInsightJob.md)
<span data-ttu-id="85930-128">Kinyeri a feladatok listáját egy fürtből, és megfordítja őket fordított időrendi sorrendben, vagy egy adott feladatot lekérdez.</span><span class="sxs-lookup"><span data-stu-id="85930-128">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

### [<span data-ttu-id="85930-129">Get-AzHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="85930-129">Get-AzHDInsightJobOutput</span></span>](Get-AzHDInsightJobOutput.md)
<span data-ttu-id="85930-130">A megadott fürthöz társított tárolási fiókból kapja meg a napló kimenetét.</span><span class="sxs-lookup"><span data-stu-id="85930-130">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

### [<span data-ttu-id="85930-131">Get-AzHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="85930-131">Get-AzHDInsightOperationsManagementSuite</span></span>](Get-AzHDInsightOperationsManagementSuite.md)
<span data-ttu-id="85930-132">A OMS (Operations Management Suite) telepítésének állapotát kapja meg a fürtön.</span><span class="sxs-lookup"><span data-stu-id="85930-132">Gets the status of Operations Management Suite (OMS) installation on the cluster.</span></span>

### [<span data-ttu-id="85930-133">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="85930-133">Get-AzHDInsightPersistedScriptAction</span></span>](Get-AzHDInsightPersistedScriptAction.md)
<span data-ttu-id="85930-134">Beolvassa a fürtök állandó parancsfájlokkal kapcsolatos műveleteit, és időrendi sorrendben listázza őket, illetve a megadott, kimaradt parancsfájlokra vonatkozó adatokat kap.</span><span class="sxs-lookup"><span data-stu-id="85930-134">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

### [<span data-ttu-id="85930-135">Get-AzHDInsightProperty</span><span class="sxs-lookup"><span data-stu-id="85930-135">Get-AzHDInsightProperty</span></span>](Get-AzHDInsightProperty.md)
<span data-ttu-id="85930-136">Beolvassa a HDInsight szolgáltatás tulajdonságait, például a rendelkezésre álló helyeket és a kapacitást.</span><span class="sxs-lookup"><span data-stu-id="85930-136">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

### [<span data-ttu-id="85930-137">Get-AzHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="85930-137">Get-AzHDInsightScriptActionHistory</span></span>](Get-AzHDInsightScriptActionHistory.md)
<span data-ttu-id="85930-138">Egy fürt parancsfájl-végrehajtási előzményeit jeleníti meg, és megfordítja őket fordított időrendi sorrendben, vagy egy korábban végrehajtott parancsfájl-művelet részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="85930-138">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

### [<span data-ttu-id="85930-139">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="85930-139">Grant-AzHDInsightRdpServicesAccess</span></span>](Grant-AzHDInsightRdpServicesAccess.md)
<span data-ttu-id="85930-140">RDP-elérést ad vissza a Windows-fürthöz.</span><span class="sxs-lookup"><span data-stu-id="85930-140">Grants RDP access to the Windows cluster.</span></span>

### [<span data-ttu-id="85930-141">Meghívó-AzHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="85930-141">Invoke-AzHDInsightHiveJob</span></span>](Invoke-AzHDInsightHiveJob.md)
<span data-ttu-id="85930-142">A kaptár-lekérdezést elküldi egy HDInsight-fürtnek, és egy műveletben lekérdezi a lekérdezés eredményét.</span><span class="sxs-lookup"><span data-stu-id="85930-142">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

### [<span data-ttu-id="85930-143">Új – AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="85930-143">New-AzHDInsightCluster</span></span>](New-AzHDInsightCluster.md)
<span data-ttu-id="85930-144">Azure HDInsight-fürtöt hoz létre az aktuális előfizetéshez megadott erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="85930-144">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

### [<span data-ttu-id="85930-145">Új – AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="85930-145">New-AzHDInsightClusterConfig</span></span>](New-AzHDInsightClusterConfig.md)
<span data-ttu-id="85930-146">Nem állandó fürtkonfiguráció-objektumot hoz létre, amely leírja az Azure HDInsight-fürtös konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="85930-146">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

### [<span data-ttu-id="85930-147">Új – AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="85930-147">New-AzHDInsightHiveJobDefinition</span></span>](New-AzHDInsightHiveJobDefinition.md)
<span data-ttu-id="85930-148">Kaptár-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="85930-148">Creates a Hive job object.</span></span>

### [<span data-ttu-id="85930-149">Új – AzHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="85930-149">New-AzHDInsightMapReduceJobDefinition</span></span>](New-AzHDInsightMapReduceJobDefinition.md)
<span data-ttu-id="85930-150">Létrehoz egy MapReduce.</span><span class="sxs-lookup"><span data-stu-id="85930-150">Creates a MapReduce job object.</span></span>

### [<span data-ttu-id="85930-151">Új – AzHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="85930-151">New-AzHDInsightPigJobDefinition</span></span>](New-AzHDInsightPigJobDefinition.md)
<span data-ttu-id="85930-152">Egy Pig-Job objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="85930-152">Creates a Pig job object.</span></span>

### [<span data-ttu-id="85930-153">Új – AzHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="85930-153">New-AzHDInsightSqoopJobDefinition</span></span>](New-AzHDInsightSqoopJobDefinition.md)
<span data-ttu-id="85930-154">Létrehoz egy Sqoop.</span><span class="sxs-lookup"><span data-stu-id="85930-154">Creates a Sqoop job object.</span></span>

### [<span data-ttu-id="85930-155">Új – AzHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="85930-155">New-AzHDInsightStreamingMapReduceJobDefinition</span></span>](New-AzHDInsightStreamingMapReduceJobDefinition.md)
<span data-ttu-id="85930-156">Adatfolyam-MapReduce hoz létre.</span><span class="sxs-lookup"><span data-stu-id="85930-156">Creates a Streaming MapReduce job object.</span></span>

### [<span data-ttu-id="85930-157">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="85930-157">Remove-AzHDInsightCluster</span></span>](Remove-AzHDInsightCluster.md)
<span data-ttu-id="85930-158">Eltávolítja a megadott HDInsight-fürtöt az aktuális előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="85930-158">Removes the specified HDInsight cluster from the current subscription.</span></span>

### [<span data-ttu-id="85930-159">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="85930-159">Remove-AzHDInsightPersistedScriptAction</span></span>](Remove-AzHDInsightPersistedScriptAction.md)
<span data-ttu-id="85930-160">Állandó parancsfájl-művelet eltávolítása egy HDInsight-fürtről.</span><span class="sxs-lookup"><span data-stu-id="85930-160">Removes an persisted script action from an HDInsight cluster.</span></span>

### [<span data-ttu-id="85930-161">Visszavonás-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="85930-161">Revoke-AzHDInsightRdpServicesAccess</span></span>](Revoke-AzHDInsightRdpServicesAccess.md)
<span data-ttu-id="85930-162">Letiltja a Windows-fürtök RDP-elérését.</span><span class="sxs-lookup"><span data-stu-id="85930-162">Disables RDP access to a Windows cluster.</span></span>

### [<span data-ttu-id="85930-163">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="85930-163">Set-AzHDInsightClusterSize</span></span>](Set-AzHDInsightClusterSize.md)
<span data-ttu-id="85930-164">A megadott szektorcsoportban lévő munkaállomások számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="85930-164">Sets the number of Worker nodes in a specified cluster.</span></span>

### [<span data-ttu-id="85930-165">Set-AzHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="85930-165">Set-AzHDInsightDefaultStorage</span></span>](Set-AzHDInsightDefaultStorage.md)
<span data-ttu-id="85930-166">Beállítja az alapértelmezett tárolási fiók beállítását egy fürtkonfiguráció-objektumban.</span><span class="sxs-lookup"><span data-stu-id="85930-166">Sets the default Storage account setting in a cluster configuration object.</span></span>

### [<span data-ttu-id="85930-167">Set-AzHDInsightGatewayCredential</span><span class="sxs-lookup"><span data-stu-id="85930-167">Set-AzHDInsightGatewayCredential</span></span>](Set-AzHDInsightGatewayCredential.md)
<span data-ttu-id="85930-168">Az Azure HDInsight-fürtök átjárójának HTTP-hitelesítő adatait állítja be.</span><span class="sxs-lookup"><span data-stu-id="85930-168">Sets the gateway HTTP credentials of an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="85930-169">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="85930-169">Set-AzHDInsightPersistedScriptAction</span></span>](Set-AzHDInsightPersistedScriptAction.md)
<span data-ttu-id="85930-170">Egy korábban futtatott parancsfájlt egy állandó parancsfájl-műveletre állítja be.</span><span class="sxs-lookup"><span data-stu-id="85930-170">Sets a previously executed script action to be a persisted script action.</span></span>

### [<span data-ttu-id="85930-171">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="85930-171">Start-AzHDInsightJob</span></span>](Start-AzHDInsightJob.md)
<span data-ttu-id="85930-172">Meghatározott Azure HDInsight-feladatot indít egy adott fürtön.</span><span class="sxs-lookup"><span data-stu-id="85930-172">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

### [<span data-ttu-id="85930-173">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="85930-173">Stop-AzHDInsightJob</span></span>](Stop-AzHDInsightJob.md)
<span data-ttu-id="85930-174">Meghatározott futó feladat leállítása egy fürtben.</span><span class="sxs-lookup"><span data-stu-id="85930-174">Stops a specified running job on a cluster.</span></span>

### [<span data-ttu-id="85930-175">Submit-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="85930-175">Submit-AzHDInsightScriptAction</span></span>](Submit-AzHDInsightScriptAction.md)
<span data-ttu-id="85930-176">Új parancsfájl-művelet elküldhet egy Azure HDInsight-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="85930-176">Submits a new script action to an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="85930-177">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="85930-177">Use-AzHDInsightCluster</span></span>](Use-AzHDInsightCluster.md)
<span data-ttu-id="85930-178">Kijelöli az Invoke-RmAzureHDInsightHiveJob parancsmaggal használni kívánt fürtöt.</span><span class="sxs-lookup"><span data-stu-id="85930-178">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

### [<span data-ttu-id="85930-179">Várjon-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="85930-179">Wait-AzHDInsightJob</span></span>](Wait-AzHDInsightJob.md)
<span data-ttu-id="85930-180">A megadott feladat befejezését vagy hibáját várja.</span><span class="sxs-lookup"><span data-stu-id="85930-180">Waits for the completion or failure of a specified job.</span></span>

