---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
ms.openlocfilehash: d96a26e4f37d565ac03d8585a803c355aff53b19
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838755"
---
# <span data-ttu-id="1404d-101">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="1404d-101">Update-AzServiceFabricApplication</span></span>

## <span data-ttu-id="1404d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1404d-102">SYNOPSIS</span></span>
<span data-ttu-id="1404d-103">A szolgáltatás szövet-alkalmazásának frissítése</span><span class="sxs-lookup"><span data-stu-id="1404d-103">Update a service fabric application.</span></span> <span data-ttu-id="1404d-104">Ez lehetővé teszi az alkalmazás paramétereinek frissítését és/vagy az alkalmazás típusának frissítését, amely elindítja az alkalmazások frissítését.</span><span class="sxs-lookup"><span data-stu-id="1404d-104">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

## <span data-ttu-id="1404d-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1404d-105">SYNTAX</span></span>

### <span data-ttu-id="1404d-106">ByResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1404d-106">ByResourceGroup (Default)</span></span>
```
Update-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [[-ApplicationTypeVersion] <String>] [-ApplicationParameter <Hashtable>] [-MinimumNodeCount <Int64>]
 [-MaximumNodeCount <Int64>] [-ForceRestart] [-UpgradeReplicaSetCheckTimeoutSec <Int32>]
 [-FailureAction <FailureAction>] [-HealthCheckRetryTimeoutSec <Int32>] [-HealthCheckWaitDurationSec <Int32>]
 [-HealthCheckStableDurationSec <Int32>] [-UpgradeDomainTimeoutSec <Int32>] [-UpgradeTimeoutSec <Int32>]
 [-ConsiderWarningAsError] [-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService <Int32>]
 [-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition <Int32>]
 [-DefaultServiceTypeUnhealthyServicesMaxPercent <Int32>] [-UnhealthyDeployedApplicationsMaxPercent <Int32>]
 [-ServiceTypeHealthPolicyMap <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1404d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1404d-107">ByResourceId</span></span>
```
Update-AzServiceFabricApplication [[-ApplicationTypeVersion] <String>] [-ApplicationParameter <Hashtable>]
 [-MinimumNodeCount <Int64>] [-MaximumNodeCount <Int64>] [-ForceRestart]
 [-UpgradeReplicaSetCheckTimeoutSec <Int32>] [-FailureAction <FailureAction>]
 [-HealthCheckRetryTimeoutSec <Int32>] [-HealthCheckWaitDurationSec <Int32>]
 [-HealthCheckStableDurationSec <Int32>] [-UpgradeDomainTimeoutSec <Int32>] [-UpgradeTimeoutSec <Int32>]
 [-ConsiderWarningAsError] [-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService <Int32>]
 [-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition <Int32>]
 [-DefaultServiceTypeUnhealthyServicesMaxPercent <Int32>] [-UnhealthyDeployedApplicationsMaxPercent <Int32>]
 [-ServiceTypeHealthPolicyMap <Hashtable>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1404d-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1404d-108">ByInputObject</span></span>
```
Update-AzServiceFabricApplication -InputObject <PSApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1404d-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="1404d-109">DESCRIPTION</span></span>
<span data-ttu-id="1404d-110">Ez a parancsmag az alkalmazás paramétereinek frissítésére és az alkalmazás típusa verziójának frissítésére használható.</span><span class="sxs-lookup"><span data-stu-id="1404d-110">This cmdlet can be used to update application parameters and upgrade the application type version.</span></span> <span data-ttu-id="1404d-111">A paraméter frissítése csak akkor változik meg a modellben, ha új típusú verziót használ, a parancs az alkalmazás frissítését fogja elindítani.</span><span class="sxs-lookup"><span data-stu-id="1404d-111">Updating the parameter will only change the model in ARM side, only when a new type version is used, the command will trigger an application upgrade.</span></span> <span data-ttu-id="1404d-112">A Type (típus) verzió már meg lett hozva a fürtben a **New-AzServiceFabricApplicationTypeVersion** használatával.</span><span class="sxs-lookup"><span data-stu-id="1404d-112">The type version specified should already be created in the cluster using **New-AzServiceFabricApplicationTypeVersion**.</span></span>

## <span data-ttu-id="1404d-113">Példák</span><span class="sxs-lookup"><span data-stu-id="1404d-113">EXAMPLES</span></span>

### <span data-ttu-id="1404d-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1404d-114">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="1404d-115">Ez a példa elindítja az alkalmazás frissítését, hogy frissítse a "v2" típusú verziót, amelyet a **New-AzServiceFabricApplicationTypeVersion** hoztak létre.</span><span class="sxs-lookup"><span data-stu-id="1404d-115">This example will start an application upgrade to update the type version to "v2" which was created with **New-AzServiceFabricApplicationTypeVersion**.</span></span> <span data-ttu-id="1404d-116">A használt alkalmazási paramétereket az alkalmazás jegyzékfájljában kell megadni.</span><span class="sxs-lookup"><span data-stu-id="1404d-116">The application parameters used should be defined in the application manifest.</span></span>

### <span data-ttu-id="1404d-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="1404d-117">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -MinimumNodes 1 -MaximumNodes 4 -Verbose
```

<span data-ttu-id="1404d-118">Ez a példa frissíti az alkalmazáshoz tartozó csomópontok korlátozásának minimális és maximális számát.</span><span class="sxs-lookup"><span data-stu-id="1404d-118">This example will update the minimum and maximum number of nodes restriction for the application.</span></span>

### <span data-ttu-id="1404d-119">3. példa</span><span class="sxs-lookup"><span data-stu-id="1404d-119">Example 3</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"} -HealthCheckStableDurationSec 0 -HealthCheckWaitDurationSec 0 -HealthCheckRetryTimeoutSec 0 -UpgradeDomainTimeoutSec 5000 -UpgradeTimeoutSec 7000 -FailureAction Rollback -UpgradeReplicaSetCheckTimeoutSec 300 -ForceRestart
```

<span data-ttu-id="1404d-120">Ez a példa elindítja az alkalmazás frissítését a típus verzió "v2" értékre frissítéséhez, és az aktuális frissítéstől hatályba lépnek néhány frissítési házirend-paramétert is.</span><span class="sxs-lookup"><span data-stu-id="1404d-120">This example will start an application upgrade to update the type version to "v2" and also sets some upgrade policy parameters that will take effect from the current upgrade.</span></span>

### <span data-ttu-id="1404d-121">4. példa</span><span class="sxs-lookup"><span data-stu-id="1404d-121">Example 4</span></span>
```powershell
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="1404d-122">Ez a példa frissíti az alkalmazás paramétereit, de ezek a módosítások csak akkor lépnek érvénybe, ha a következő verzióra frissítenek az alkalmazásra.</span><span class="sxs-lookup"><span data-stu-id="1404d-122">This example updates the application parameters but these changes will only take effect until the next version upgrade to the application.</span></span>

## <span data-ttu-id="1404d-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1404d-123">PARAMETERS</span></span>

### <span data-ttu-id="1404d-124">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="1404d-124">-ApplicationParameter</span></span>
<span data-ttu-id="1404d-125">Adja meg az alkalmazás paramétereit kulcs/érték párokként.</span><span class="sxs-lookup"><span data-stu-id="1404d-125">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="1404d-126">Ezek a paraméterek csak az alkalmazás jegyzékfájljában találhatók.</span><span class="sxs-lookup"><span data-stu-id="1404d-126">These parameters must exist in the application manifest.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1404d-127">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="1404d-127">-ApplicationTypeVersion</span></span>
<span data-ttu-id="1404d-128">Az alkalmazás típusa verziójának megadása</span><span class="sxs-lookup"><span data-stu-id="1404d-128">Specify the application type version</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1404d-129">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="1404d-129">-ClusterName</span></span>
<span data-ttu-id="1404d-130">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="1404d-130">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1404d-131">-ConsiderWarningAsError</span><span class="sxs-lookup"><span data-stu-id="1404d-131">-ConsiderWarningAsError</span></span>
<span data-ttu-id="1404d-132">Azt jelzi, hogy az egészségi állapot kiértékelése során hibaként kell-e kezelni a figyelmeztető esemény állapotát.</span><span class="sxs-lookup"><span data-stu-id="1404d-132">Indicates whether to treat a warning health event as an error event during health evaluation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1404d-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1404d-133">-DefaultProfile</span></span>
<span data-ttu-id="1404d-134">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1404d-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1404d-135">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span><span class="sxs-lookup"><span data-stu-id="1404d-135">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span></span>
<span data-ttu-id="1404d-136">Megadja az unhelthy-partíciókon a figyelt frissítéshez használni kívánt alapértelmezett szolgáltatás állapotházirend által megengedett maximális százalékát.</span><span class="sxs-lookup"><span data-stu-id="1404d-136">Specifies the maximum percent of unhelthy partitions per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1404d-137">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span><span class="sxs-lookup"><span data-stu-id="1404d-137">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span></span>
<span data-ttu-id="1404d-138">Megadja, hogy a rendszer az alapértelmezett unhelthy-replikák maximális százalékát adja meg az alapértelmezett szolgáltatáshoz, amelyet a figyelt frissítéshez használni kell.</span><span class="sxs-lookup"><span data-stu-id="1404d-138">Specifies the maximum percent of unhelthy replicas per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1404d-139">-DefaultServiceTypeUnhealthyServicesMaxPercent</span><span class="sxs-lookup"><span data-stu-id="1404d-139">-DefaultServiceTypeUnhealthyServicesMaxPercent</span></span>
<span data-ttu-id="1404d-140">A figyelt frissítéshez használni kívánt alapértelmezett szolgáltatási típus állapotházirend által engedélyezett unhelthy-szolgáltatások maximális százalékát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1404d-140">Specifies the maximum percent of unhelthy services allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1404d-141">-FailureAction</span><span class="sxs-lookup"><span data-stu-id="1404d-141">-FailureAction</span></span>
<span data-ttu-id="1404d-142">Azt a műveletsort adja meg, amelyet a figyelt frissítés sikertelensége esetén kell elvégezni.</span><span class="sxs-lookup"><span data-stu-id="1404d-142">Specifies the action to take if the monitored upgrade fails.</span></span>
<span data-ttu-id="1404d-143">A paraméter elfogadható értékei visszagörgetések vagy manuálisak.</span><span class="sxs-lookup"><span data-stu-id="1404d-143">The acceptable values for this parameter are Rollback or Manual.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.FailureAction
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:
Accepted values: Rollback, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1404d-144">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="1404d-144">-ForceRestart</span></span>
<span data-ttu-id="1404d-145">Azt jelzi, hogy a szolgáltatás akkor is újraindul, ha a frissítés csak a konfiguráció konfigurációjának változása.</span><span class="sxs-lookup"><span data-stu-id="1404d-145">Indicates that the service host restarts even if the upgrade is a configuration-only change.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1404d-146">-HealthCheckRetryTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="1404d-146">-HealthCheckRetryTimeoutSec</span></span>
<span data-ttu-id="1404d-147">Azt a másodpercben megadott időtartamot adja meg, amely után a szolgáltatás szerkezete újra megkísérli az állapot-ellenőrzést, ha a korábbi állapot-ellenőrzés nem működik.</span><span class="sxs-lookup"><span data-stu-id="1404d-147">Specifies the duration, in seconds, after which Service Fabric retries the health check if the previous health check fails.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1404d-148">-HealthCheckStableDurationSec</span><span class="sxs-lookup"><span data-stu-id="1404d-148">-HealthCheckStableDurationSec</span></span>
<span data-ttu-id="1404d-149">Meghatározza, hogy a szolgáltatás milyen időtartammal várjon másodpercben, hogy az alkalmazás stabil legyen, mielőtt továbblép a következő frissítés tartományba vagy a frissítés befejezése után.</span><span class="sxs-lookup"><span data-stu-id="1404d-149">Specifies the duration, in seconds, that Service Fabric waits in order to verify that the application is stable before moving to the next upgrade domain or completing the upgrade.</span></span>
<span data-ttu-id="1404d-150">Ez a várakozási idő megakadályozza az egészségi állapot észlelését az állapot ellenőrzése után.</span><span class="sxs-lookup"><span data-stu-id="1404d-150">This wait duration prevents undetected changes of health right after the health check is performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1404d-151">-HealthCheckWaitDurationSec</span><span class="sxs-lookup"><span data-stu-id="1404d-151">-HealthCheckWaitDurationSec</span></span>
<span data-ttu-id="1404d-152">Azt adja meg, hogy hány másodperc múlva történjen a szolgáltatás, hogy a szolgáltatás a frissítés után a frissítés befejezése után is megvárja a kezdeti állapot-ellenőrzést.</span><span class="sxs-lookup"><span data-stu-id="1404d-152">Specifies the duration, in seconds, that Service Fabric waits before it performs the initial health check after it finishes the upgrade on the upgrade domain.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1404d-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1404d-153">-InputObject</span></span>
<span data-ttu-id="1404d-154">Az alkalmazás-erőforrás.</span><span class="sxs-lookup"><span data-stu-id="1404d-154">The application resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1404d-155">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="1404d-155">-MaximumNodeCount</span></span>
<span data-ttu-id="1404d-156">A csomópontok maximális számát adja meg az alkalmazás elhelyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="1404d-156">Specifies the maximum number of nodes on which to place an application</span></span>

```yaml
Type: System.Int64
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1404d-157">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="1404d-157">-MinimumNodeCount</span></span>
<span data-ttu-id="1404d-158">A csomópontok minimális számát adja meg, ahol a Service Fabric az alkalmazás kapacitását lefoglalja.</span><span class="sxs-lookup"><span data-stu-id="1404d-158">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

```yaml
Type: System.Int64
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1404d-159">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1404d-159">-Name</span></span>
<span data-ttu-id="1404d-160">Az alkalmazás nevének megadása</span><span class="sxs-lookup"><span data-stu-id="1404d-160">Specify the name of the application</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1404d-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1404d-161">-ResourceGroupName</span></span>
<span data-ttu-id="1404d-162">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="1404d-162">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1404d-163">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1404d-163">-ResourceId</span></span>
<span data-ttu-id="1404d-164">A kar ResourceId az alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="1404d-164">Arm ResourceId of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1404d-165">-ServiceTypeHealthPolicyMap</span><span class="sxs-lookup"><span data-stu-id="1404d-165">-ServiceTypeHealthPolicyMap</span></span>
<span data-ttu-id="1404d-166">A különböző szolgáltatási típusokhoz használt állapotházirend térképét adja meg a következő formátumban: @ {"ServiceTypeName": "MaxPercentUnhealthyPartitionsPerService, MaxPercentUnhealthyReplicasPerPartition, MaxPercentUnhealthyServices"}.</span><span class="sxs-lookup"><span data-stu-id="1404d-166">Specifies the map of the health policy to use for different service types as a hash table in the following format: @ {"ServiceTypeName" : "MaxPercentUnhealthyPartitionsPerService,MaxPercentUnhealthyReplicasPerPartition,MaxPercentUnhealthyServices"}.</span></span>
<span data-ttu-id="1404d-167">Például: @ {"ServiceTypeName01" = "5; 10; 5"; "ServiceTypeName02" = "5; 5; 5"}</span><span class="sxs-lookup"><span data-stu-id="1404d-167">For example: @{ "ServiceTypeName01" = "5,10,5"; "ServiceTypeName02" = "5,5,5" }</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1404d-168">-UnhealthyDeployedApplicationsMaxPercent</span><span class="sxs-lookup"><span data-stu-id="1404d-168">-UnhealthyDeployedApplicationsMaxPercent</span></span>
<span data-ttu-id="1404d-169">Azt adja meg, hogy a rendszer milyen maximális százalékban adja meg a fürt azon csomópontjain telepített alkalmazás-példányok maximális százalékát, amelyek állapota hibás, mielőtt a fürthöz tartozó Application Health State hiba lép fel.</span><span class="sxs-lookup"><span data-stu-id="1404d-169">Specifies the maximum percentage of the application instances deployed on the nodes in the cluster that have a health state of error before the application health state for the cluster is error.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1404d-170">-UpgradeDomainTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="1404d-170">-UpgradeDomainTimeoutSec</span></span>
<span data-ttu-id="1404d-171">Azt adja meg, hogy hány másodpercig tartson a szolgáltatás az egyetlen frissítési tartomány frissítésekor.</span><span class="sxs-lookup"><span data-stu-id="1404d-171">Specifies the maximum time, in seconds, that Service Fabric takes to upgrade a single upgrade domain.</span></span>
<span data-ttu-id="1404d-172">Az időszak után a frissítés nem sikerült.</span><span class="sxs-lookup"><span data-stu-id="1404d-172">After this period, the upgrade fails.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1404d-173">-UpgradeReplicaSetCheckTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="1404d-173">-UpgradeReplicaSetCheckTimeoutSec</span></span>
<span data-ttu-id="1404d-174">Annak a maximális időpontnak a megadására szolgál, ameddig a szolgáltatás anyaga egy szolgáltatásra várakozik, és ha még nem biztonságos állapotban van, mielőtt a szolgáltatás a frissítéssel folytatja a frissítést.</span><span class="sxs-lookup"><span data-stu-id="1404d-174">Specifies the maximum time that Service Fabric waits for a service to reconfigure into a safe state, if not already in a safe state, before Service Fabric proceeds with the upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1404d-175">-UpgradeTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="1404d-175">-UpgradeTimeoutSec</span></span>
<span data-ttu-id="1404d-176">Azt adja meg, hogy hány másodpercig tartson a szolgáltatás a teljes frissítéshez.</span><span class="sxs-lookup"><span data-stu-id="1404d-176">Specifies the maximum time, in seconds, that Service Fabric takes for the entire upgrade.</span></span>
<span data-ttu-id="1404d-177">Az időszak után a frissítés nem sikerült.</span><span class="sxs-lookup"><span data-stu-id="1404d-177">After this period, the upgrade fails.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1404d-178">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1404d-178">-Confirm</span></span>
<span data-ttu-id="1404d-179">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1404d-179">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1404d-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1404d-180">-WhatIf</span></span>
<span data-ttu-id="1404d-181">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1404d-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1404d-182">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1404d-182">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1404d-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1404d-183">CommonParameters</span></span>
<span data-ttu-id="1404d-184">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1404d-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1404d-185">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1404d-185">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1404d-186">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1404d-186">INPUTS</span></span>

### <span data-ttu-id="1404d-187">System. String</span><span class="sxs-lookup"><span data-stu-id="1404d-187">System.String</span></span>

### <span data-ttu-id="1404d-188">Microsoft. Azure. Command. ServiceFabric. models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="1404d-188">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="1404d-189">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1404d-189">OUTPUTS</span></span>

### <span data-ttu-id="1404d-190">Microsoft. Azure. Command. ServiceFabric. models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="1404d-190">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="1404d-191">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1404d-191">NOTES</span></span>

## <span data-ttu-id="1404d-192">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1404d-192">RELATED LINKS</span></span>
