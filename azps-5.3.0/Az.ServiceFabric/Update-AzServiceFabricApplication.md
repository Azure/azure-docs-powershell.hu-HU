---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
ms.openlocfilehash: e53ed405c9a03e7a9ec7a7c3694a44d513a1a1ea
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479519"
---
# <span data-ttu-id="baaf5-101">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="baaf5-101">Update-AzServiceFabricApplication</span></span>

## <span data-ttu-id="baaf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="baaf5-102">SYNOPSIS</span></span>
<span data-ttu-id="baaf5-103">Szervizáru-alkalmazás frissítése.</span><span class="sxs-lookup"><span data-stu-id="baaf5-103">Update a service fabric application.</span></span> <span data-ttu-id="baaf5-104">Ez lehetővé teszi az alkalmazásparaméterek frissítését és/vagy az alkalmazástípus verzióját, amely elindít egy alkalmazásfrissítést.</span><span class="sxs-lookup"><span data-stu-id="baaf5-104">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span> <span data-ttu-id="baaf5-105">Csak a telepített ARM támogatja.</span><span class="sxs-lookup"><span data-stu-id="baaf5-105">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="baaf5-106">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="baaf5-106">SYNTAX</span></span>

### <span data-ttu-id="baaf5-107">ByResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="baaf5-107">ByResourceGroup (Default)</span></span>
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

### <span data-ttu-id="baaf5-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="baaf5-108">ByResourceId</span></span>
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

### <span data-ttu-id="baaf5-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="baaf5-109">ByInputObject</span></span>
```
Update-AzServiceFabricApplication -InputObject <PSApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="baaf5-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="baaf5-110">DESCRIPTION</span></span>
<span data-ttu-id="baaf5-111">Ez a parancsmag az alkalmazásparaméterek frissítéséhez és az alkalmazástípus verziójának frissítéséhez használható.</span><span class="sxs-lookup"><span data-stu-id="baaf5-111">This cmdlet can be used to update application parameters and upgrade the application type version.</span></span> <span data-ttu-id="baaf5-112">A paraméter frissítése csak a ARM módosítja a modellt, csak akkor, ha új típusú verziót használ, a parancs elindít egy alkalmazásfrissítést.</span><span class="sxs-lookup"><span data-stu-id="baaf5-112">Updating the parameter will only change the model in ARM side, only when a new type version is used, the command will trigger an application upgrade.</span></span> <span data-ttu-id="baaf5-113">A megadott típusverziót már létre kell létrehozni a fürtben a **New-AzServiceFabricApplicationTypeVersion használatával.**</span><span class="sxs-lookup"><span data-stu-id="baaf5-113">The type version specified should already be created in the cluster using **New-AzServiceFabricApplicationTypeVersion**.</span></span>

## <span data-ttu-id="baaf5-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="baaf5-114">EXAMPLES</span></span>

### <span data-ttu-id="baaf5-115">1. példa</span><span class="sxs-lookup"><span data-stu-id="baaf5-115">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="baaf5-116">Ebben a példában elindítunk egy alkalmazásfrissítést, és a típusverziót "v2" verzióra frissítjük, amelyet a **New-AzServiceFabricApplicationTypeVersion** verzióval hoztak létre.</span><span class="sxs-lookup"><span data-stu-id="baaf5-116">This example will start an application upgrade to update the type version to "v2" which was created with **New-AzServiceFabricApplicationTypeVersion**.</span></span> <span data-ttu-id="baaf5-117">A használt alkalmazásparamétereket definiálni kell az alkalmazás jegyzékfájlban.</span><span class="sxs-lookup"><span data-stu-id="baaf5-117">The application parameters used should be defined in the application manifest.</span></span>

### <span data-ttu-id="baaf5-118">2. példa</span><span class="sxs-lookup"><span data-stu-id="baaf5-118">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -MinimumNodes 1 -MaximumNodes 4 -Verbose
```

<span data-ttu-id="baaf5-119">Ebben a példában frissítjük az alkalmazás minimális és maximális csomópontkorlátozását.</span><span class="sxs-lookup"><span data-stu-id="baaf5-119">This example will update the minimum and maximum number of nodes restriction for the application.</span></span>

### <span data-ttu-id="baaf5-120">3. példa</span><span class="sxs-lookup"><span data-stu-id="baaf5-120">Example 3</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"} -HealthCheckStableDurationSec 0 -HealthCheckWaitDurationSec 0 -HealthCheckRetryTimeoutSec 0 -UpgradeDomainTimeoutSec 5000 -UpgradeTimeoutSec 7000 -FailureAction Rollback -UpgradeReplicaSetCheckTimeoutSec 300 -ForceRestart
```

<span data-ttu-id="baaf5-121">Ez a példa elindít egy alkalmazásfrissítést, hogy a típusverziót "v2" verzióra frissítse, és beállítja az aktuális frissítésből életbe lépő frissítési házirend-paramétereket is.</span><span class="sxs-lookup"><span data-stu-id="baaf5-121">This example will start an application upgrade to update the type version to "v2" and also sets some upgrade policy parameters that will take effect from the current upgrade.</span></span>

### <span data-ttu-id="baaf5-122">4. példa</span><span class="sxs-lookup"><span data-stu-id="baaf5-122">Example 4</span></span>
```powershell
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="baaf5-123">Ez a példa frissíti az alkalmazásparamétereket, de ezek a módosítások csak az alkalmazásra való következő verziófrissítésig lépnek hatályba.</span><span class="sxs-lookup"><span data-stu-id="baaf5-123">This example updates the application parameters but these changes will only take effect until the next version upgrade to the application.</span></span>

## <span data-ttu-id="baaf5-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="baaf5-124">PARAMETERS</span></span>

### <span data-ttu-id="baaf5-125">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="baaf5-125">-ApplicationParameter</span></span>
<span data-ttu-id="baaf5-126">Adja meg az alkalmazásparamétereket kulcs-/értékpárokként.</span><span class="sxs-lookup"><span data-stu-id="baaf5-126">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="baaf5-127">Ezeknek a paramétereknek léteznie kell az alkalmazás jegyzékfájlban.</span><span class="sxs-lookup"><span data-stu-id="baaf5-127">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="baaf5-128">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="baaf5-128">-ApplicationTypeVersion</span></span>
<span data-ttu-id="baaf5-129">Az alkalmazástípus verziójának megadása</span><span class="sxs-lookup"><span data-stu-id="baaf5-129">Specify the application type version</span></span>

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

### <span data-ttu-id="baaf5-130">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="baaf5-130">-ClusterName</span></span>
<span data-ttu-id="baaf5-131">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="baaf5-131">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="baaf5-132">-ConsiderWarningAsError</span><span class="sxs-lookup"><span data-stu-id="baaf5-132">-ConsiderWarningAsError</span></span>
<span data-ttu-id="baaf5-133">Azt jelzi, hogy egy figyelmeztető állapoteseményt hibaeseményként kell-e kezelnie az állapot értékelése során.</span><span class="sxs-lookup"><span data-stu-id="baaf5-133">Indicates whether to treat a warning health event as an error event during health evaluation.</span></span>

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

### <span data-ttu-id="baaf5-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baaf5-134">-DefaultProfile</span></span>
<span data-ttu-id="baaf5-135">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="baaf5-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="baaf5-136">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span><span class="sxs-lookup"><span data-stu-id="baaf5-136">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span></span>
<span data-ttu-id="baaf5-137">A figyelt frissítéshez használt alapértelmezett szolgáltatástípus állapoti házirendjére vonatkozó nem használt partíciók maximális százalékos aránya szolgáltatásonként.</span><span class="sxs-lookup"><span data-stu-id="baaf5-137">Specifies the maximum percent of unhelthy partitions per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="baaf5-138">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span><span class="sxs-lookup"><span data-stu-id="baaf5-138">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span></span>
<span data-ttu-id="baaf5-139">A figyelt frissítéshez használt alapértelmezett szolgáltatástípus állapoti házirendjében szolgáltatásonként engedélyezett nem használt másolatok maximális százalékos aránya.</span><span class="sxs-lookup"><span data-stu-id="baaf5-139">Specifies the maximum percent of unhelthy replicas per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="baaf5-140">-DefaultServiceTypeUnhealthyServicesMaxPercent</span><span class="sxs-lookup"><span data-stu-id="baaf5-140">-DefaultServiceTypeUnhealthyServicesMaxPercent</span></span>
<span data-ttu-id="baaf5-141">A figyelt frissítéshez az alapértelmezett szolgáltatástípus állapoti házirendjében engedélyezett nem használt szolgáltatások maximális százalékos aránya.</span><span class="sxs-lookup"><span data-stu-id="baaf5-141">Specifies the maximum percent of unhelthy services allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="baaf5-142">-FailureAction</span><span class="sxs-lookup"><span data-stu-id="baaf5-142">-FailureAction</span></span>
<span data-ttu-id="baaf5-143">A figyelt frissítés sikertelen frissítések esetén szükséges művelet.</span><span class="sxs-lookup"><span data-stu-id="baaf5-143">Specifies the action to take if the monitored upgrade fails.</span></span>
<span data-ttu-id="baaf5-144">A paraméter elfogadható értékei a Rollback vagy a Manual.</span><span class="sxs-lookup"><span data-stu-id="baaf5-144">The acceptable values for this parameter are Rollback or Manual.</span></span>

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

### <span data-ttu-id="baaf5-145">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="baaf5-145">-ForceRestart</span></span>
<span data-ttu-id="baaf5-146">Azt jelzi, hogy a szolgáltatás állomása akkor is újraindul, ha a frissítés csak konfigurációt módosít.</span><span class="sxs-lookup"><span data-stu-id="baaf5-146">Indicates that the service host restarts even if the upgrade is a configuration-only change.</span></span>

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

### <span data-ttu-id="baaf5-147">-HealthCheckRetryTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="baaf5-147">-HealthCheckRetryTimeoutSec</span></span>
<span data-ttu-id="baaf5-148">Azt az időtartamot adja meg másodpercben, amely után a Service Fabric újrakezdődik az állapot-ellenőrzés, ha a korábbi állapot-ellenőrzés meghiúsul.</span><span class="sxs-lookup"><span data-stu-id="baaf5-148">Specifies the duration, in seconds, after which Service Fabric retries the health check if the previous health check fails.</span></span>

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

### <span data-ttu-id="baaf5-149">-HealthCheckStableDurationSec</span><span class="sxs-lookup"><span data-stu-id="baaf5-149">-HealthCheckStableDurationSec</span></span>
<span data-ttu-id="baaf5-150">Azt adja meg másodpercben, hogy a Service Fabric mely ideig várakozik annak ellenőrzésére, hogy az alkalmazás stabil-e, mielőtt a következő frissítési tartományra vált, vagy befejezi a frissítést.</span><span class="sxs-lookup"><span data-stu-id="baaf5-150">Specifies the duration, in seconds, that Service Fabric waits in order to verify that the application is stable before moving to the next upgrade domain or completing the upgrade.</span></span>
<span data-ttu-id="baaf5-151">Ez a várakozási időtartam közvetlenül az állapot-ellenőrzés után meggátolja az állapot nem észrevétlen változását.</span><span class="sxs-lookup"><span data-stu-id="baaf5-151">This wait duration prevents undetected changes of health right after the health check is performed.</span></span>

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

### <span data-ttu-id="baaf5-152">-HealthCheckWaitDurationSec</span><span class="sxs-lookup"><span data-stu-id="baaf5-152">-HealthCheckWaitDurationSec</span></span>
<span data-ttu-id="baaf5-153">Azt adja meg másodpercben, hogy a Service Fabric időtartamot várjon, mielőtt végrehajtja a kezdeti állapot-ellenőrzést, miután befejezte a frissítést a frissítési tartományon.</span><span class="sxs-lookup"><span data-stu-id="baaf5-153">Specifies the duration, in seconds, that Service Fabric waits before it performs the initial health check after it finishes the upgrade on the upgrade domain.</span></span>

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

### <span data-ttu-id="baaf5-154">-InputObject</span><span class="sxs-lookup"><span data-stu-id="baaf5-154">-InputObject</span></span>
<span data-ttu-id="baaf5-155">Az alkalmazáserőforrás.</span><span class="sxs-lookup"><span data-stu-id="baaf5-155">The application resource.</span></span>

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

### <span data-ttu-id="baaf5-156">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="baaf5-156">-MaximumNodeCount</span></span>
<span data-ttu-id="baaf5-157">Meghatározza, hogy legfeljebb hány csomóponton helyezzen el egy alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="baaf5-157">Specifies the maximum number of nodes on which to place an application</span></span>

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

### <span data-ttu-id="baaf5-158">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="baaf5-158">-MinimumNodeCount</span></span>
<span data-ttu-id="baaf5-159">Azt a csomópontok minimális számát adja meg, amelyekben a Service Fabric kapacitást foglal ehhez az alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="baaf5-159">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

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

### <span data-ttu-id="baaf5-160">-Name</span><span class="sxs-lookup"><span data-stu-id="baaf5-160">-Name</span></span>
<span data-ttu-id="baaf5-161">Az alkalmazás nevének megadása</span><span class="sxs-lookup"><span data-stu-id="baaf5-161">Specify the name of the application</span></span>

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

### <span data-ttu-id="baaf5-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baaf5-162">-ResourceGroupName</span></span>
<span data-ttu-id="baaf5-163">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="baaf5-163">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="baaf5-164">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="baaf5-164">-ResourceId</span></span>
<span data-ttu-id="baaf5-165">Arm ResourceId of the application.</span><span class="sxs-lookup"><span data-stu-id="baaf5-165">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="baaf5-166">-ServiceTypeHealthPolicyMap</span><span class="sxs-lookup"><span data-stu-id="baaf5-166">-ServiceTypeHealthPolicyMap</span></span>
<span data-ttu-id="baaf5-167">A különböző szolgáltatástípusokhoz a következő formátumban használt állapoti házirend térképét adja meg kivonattáblaként: @ {"ServiceTypeName" : "MaxPercentUnhealthyPartitionsPerService,MaxPercentUnhealthyReplicasPerPartition,MaxPercentUnhealthyServices"}.</span><span class="sxs-lookup"><span data-stu-id="baaf5-167">Specifies the map of the health policy to use for different service types as a hash table in the following format: @ {"ServiceTypeName" : "MaxPercentUnhealthyPartitionsPerService,MaxPercentUnhealthyReplicasPerPartition,MaxPercentUnhealthyServices"}.</span></span>
<span data-ttu-id="baaf5-168">Például: @{ "ServiceTypeName01" = "5,10,5"; "ServiceTypeName02" = "5,5,5" }</span><span class="sxs-lookup"><span data-stu-id="baaf5-168">For example: @{ "ServiceTypeName01" = "5,10,5"; "ServiceTypeName02" = "5,5,5" }</span></span>

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

### <span data-ttu-id="baaf5-169">-UnhealthyDeployedApplicationsMaxPercent</span><span class="sxs-lookup"><span data-stu-id="baaf5-169">-UnhealthyDeployedApplicationsMaxPercent</span></span>
<span data-ttu-id="baaf5-170">Azt adja meg, hogy a fürt csomópontjaira telepített alkalmazáspéldányok hány százaléka hibás állapotú, mielőtt a fürt alkalmazásállapota hiba lenne.</span><span class="sxs-lookup"><span data-stu-id="baaf5-170">Specifies the maximum percentage of the application instances deployed on the nodes in the cluster that have a health state of error before the application health state for the cluster is error.</span></span>

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

### <span data-ttu-id="baaf5-171">-UpgradeDomainTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="baaf5-171">-UpgradeDomainTimeoutSec</span></span>
<span data-ttu-id="baaf5-172">Azt adja meg másodpercben, hogy a Service Fabric legfeljebb egy frissítési tartományt frissít.</span><span class="sxs-lookup"><span data-stu-id="baaf5-172">Specifies the maximum time, in seconds, that Service Fabric takes to upgrade a single upgrade domain.</span></span>
<span data-ttu-id="baaf5-173">Ezt az időszakot követően a frissítés sikertelen lesz.</span><span class="sxs-lookup"><span data-stu-id="baaf5-173">After this period, the upgrade fails.</span></span>

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

### <span data-ttu-id="baaf5-174">-UpgradeReplicaSetCheckTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="baaf5-174">-UpgradeReplicaSetCheckTimeoutSec</span></span>
<span data-ttu-id="baaf5-175">Azt adja meg, hogy a Service Fabric legfeljebb azt várja meg, amíg a szolgáltatás biztonságos állapotba kerül, ha még nem biztonságos állapotban van, mielőtt a Service Fabric továbblép a frissítésre.</span><span class="sxs-lookup"><span data-stu-id="baaf5-175">Specifies the maximum time that Service Fabric waits for a service to reconfigure into a safe state, if not already in a safe state, before Service Fabric proceeds with the upgrade.</span></span>

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

### <span data-ttu-id="baaf5-176">-UpgradeTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="baaf5-176">-UpgradeTimeoutSec</span></span>
<span data-ttu-id="baaf5-177">A Service Fabric által a teljes frissítéshez szükséges maximális időt adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="baaf5-177">Specifies the maximum time, in seconds, that Service Fabric takes for the entire upgrade.</span></span>
<span data-ttu-id="baaf5-178">Ezt az időszakot követően a frissítés sikertelen lesz.</span><span class="sxs-lookup"><span data-stu-id="baaf5-178">After this period, the upgrade fails.</span></span>

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

### <span data-ttu-id="baaf5-179">-Confirm</span><span class="sxs-lookup"><span data-stu-id="baaf5-179">-Confirm</span></span>
<span data-ttu-id="baaf5-180">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="baaf5-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="baaf5-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="baaf5-181">-WhatIf</span></span>
<span data-ttu-id="baaf5-182">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="baaf5-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="baaf5-183">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="baaf5-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="baaf5-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baaf5-184">CommonParameters</span></span>
<span data-ttu-id="baaf5-185">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baaf5-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baaf5-186">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="baaf5-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baaf5-187">INPUTS</span><span class="sxs-lookup"><span data-stu-id="baaf5-187">INPUTS</span></span>

### <span data-ttu-id="baaf5-188">System.String</span><span class="sxs-lookup"><span data-stu-id="baaf5-188">System.String</span></span>

### <span data-ttu-id="baaf5-189">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="baaf5-189">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="baaf5-190">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="baaf5-190">OUTPUTS</span></span>

### <span data-ttu-id="baaf5-191">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="baaf5-191">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="baaf5-192">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="baaf5-192">NOTES</span></span>

## <span data-ttu-id="baaf5-193">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="baaf5-193">RELATED LINKS</span></span>
