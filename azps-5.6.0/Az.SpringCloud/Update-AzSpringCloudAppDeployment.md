---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.SpringCloud/update-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 466bf2908cf1da940a369d2276dbf39106d60515
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005302"
---
# <span data-ttu-id="568d0-101">Update-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="568d0-101">Update-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="568d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="568d0-102">SYNOPSIS</span></span>
<span data-ttu-id="568d0-103">A kilépő telepítés frissítésére használható művelet.</span><span class="sxs-lookup"><span data-stu-id="568d0-103">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="568d0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="568d0-104">SYNTAX</span></span>

### <span data-ttu-id="568d0-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="568d0-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="568d0-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="568d0-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-Cpu <Int32>]
 [-EnvironmentVariable <Hashtable>] [-JvmOption <String>] [-MemoryInGb <Int32>]
 [-RuntimeVersion <RuntimeVersion>] [-SourceArtifactSelector <String>] [-SourceRelativePath <String>]
 [-SourceType <UserSourceType>] [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="568d0-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="568d0-107">DESCRIPTION</span></span>
<span data-ttu-id="568d0-108">A kilépő telepítés frissítésére használható művelet.</span><span class="sxs-lookup"><span data-stu-id="568d0-108">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="568d0-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="568d0-109">EXAMPLES</span></span>

### <span data-ttu-id="568d0-110">1. példa: A tavaszi felhőbeli telepítés frissítése név szerint.</span><span class="sxs-lookup"><span data-stu-id="568d0-110">Example 1: Update Spring Cloud Deployment by name.</span></span>
```powershell
PS C:\> Update-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default -SourceRelativePath resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
Active                               : True
AppName                              : gateway
CreatedTime                          :
DeploymentSettingCpu                 : 1
DeploymentSettingEnvironmentVariable : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettingsEnvironmentVariables
DeploymentSettingInstanceCount       : 1
DeploymentSettingJvmOption           :
DeploymentSettingMemoryInGb          : 1
DeploymentSettingRuntimeVersion      : Java_8
Id                                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway/deployments/default
Instance                             : {gateway-default-7-fb79b6b5d-kvmpz}
Name                                 : default
ProvisioningState                    : Succeeded
SourceArtifactSelector               :
SourceRelativePath                   : resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
SourceType                           : Jar
SourceVersion                        :
Status                               : Running
Type                                 : Microsoft.AppPlatform/Spring/apps/deployments
DeploymentSetting                    : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettings
Property                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentResourceProperties
Source                               : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.UserSourceInfo
```

<span data-ttu-id="568d0-111">Frissítse a Tavaszi felhőbeli telepítést név szerint.</span><span class="sxs-lookup"><span data-stu-id="568d0-111">Update Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="568d0-112">2. példa: A tavaszi felhőbeli telepítés frissítése a pipe-ból.</span><span class="sxs-lookup"><span data-stu-id="568d0-112">Example 2: Update Spring Cloud Deployment from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Update-AzSpringCloudAppDeployment -SourceRelativePath resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
Active                               : True
AppName                              : gateway
CreatedTime                          :
DeploymentSettingCpu                 : 1
DeploymentSettingEnvironmentVariable : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettingsEnvironmentVariables
DeploymentSettingInstanceCount       : 1
DeploymentSettingJvmOption           :
DeploymentSettingMemoryInGb          : 1
DeploymentSettingRuntimeVersion      : Java_8
Id                                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway/deployments/default
Instance                             : {gateway-default-7-fb79b6b5d-kvmpz}
Name                                 : default
ProvisioningState                    : Succeeded
SourceArtifactSelector               :
SourceRelativePath                   : resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
SourceType                           : Jar
SourceVersion                        :
Status                               : Running
Type                                 : Microsoft.AppPlatform/Spring/apps/deployments
DeploymentSetting                    : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettings
Property                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentResourceProperties
Source                               : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.UserSourceInfo
```

<span data-ttu-id="568d0-113">Frissítse a tavaszi felhőbeli telepítést a pipe-ból.</span><span class="sxs-lookup"><span data-stu-id="568d0-113">Update Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="568d0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="568d0-114">PARAMETERS</span></span>

### <span data-ttu-id="568d0-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="568d0-115">-AppName</span></span>
<span data-ttu-id="568d0-116">Az alkalmazáserőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="568d0-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="568d0-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="568d0-117">-AsJob</span></span>
<span data-ttu-id="568d0-118">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="568d0-118">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="568d0-119">-Cpu</span><span class="sxs-lookup"><span data-stu-id="568d0-119">-Cpu</span></span>
<span data-ttu-id="568d0-120">Kötelező processzor</span><span class="sxs-lookup"><span data-stu-id="568d0-120">Required CPU</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="568d0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="568d0-121">-DefaultProfile</span></span>
<span data-ttu-id="568d0-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="568d0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="568d0-123">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="568d0-123">-EnvironmentVariable</span></span>
<span data-ttu-id="568d0-124">Környezeti változók gyűjteménye</span><span class="sxs-lookup"><span data-stu-id="568d0-124">Collection of environment variables</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="568d0-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="568d0-125">-InputObject</span></span>
<span data-ttu-id="568d0-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="568d0-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="568d0-127">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="568d0-127">-JvmOption</span></span>
<span data-ttu-id="568d0-128">JVM paraméter</span><span class="sxs-lookup"><span data-stu-id="568d0-128">JVM parameter</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="568d0-129">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="568d0-129">-MemoryInGb</span></span>
<span data-ttu-id="568d0-130">A szükséges memória mérete GB-ban</span><span class="sxs-lookup"><span data-stu-id="568d0-130">Required Memory size in GB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="568d0-131">-Name</span><span class="sxs-lookup"><span data-stu-id="568d0-131">-Name</span></span>
<span data-ttu-id="568d0-132">A Központi telepítés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="568d0-132">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="568d0-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="568d0-133">-NoWait</span></span>
<span data-ttu-id="568d0-134">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="568d0-134">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="568d0-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="568d0-135">-ResourceGroupName</span></span>
<span data-ttu-id="568d0-136">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="568d0-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="568d0-137">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="568d0-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="568d0-138">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="568d0-138">-RuntimeVersion</span></span>
<span data-ttu-id="568d0-139">Runtime version</span><span class="sxs-lookup"><span data-stu-id="568d0-139">Runtime version</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Support.RuntimeVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="568d0-140">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="568d0-140">-ServiceName</span></span>
<span data-ttu-id="568d0-141">A Szolgáltatás erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="568d0-141">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="568d0-142">-SourceArtifactSele</span><span class="sxs-lookup"><span data-stu-id="568d0-142">-SourceArtifactSelector</span></span>
<span data-ttu-id="568d0-143">Selector for the artifact to be used for the deployment for multi-module projects.</span><span class="sxs-lookup"><span data-stu-id="568d0-143">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="568d0-144">Ennek kell lennie a célmodulhoz/projekthez vezető relatív elérési útnak.</span><span class="sxs-lookup"><span data-stu-id="568d0-144">This should bethe relative path to the target module/project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="568d0-145">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="568d0-145">-SourceRelativePath</span></span>
<span data-ttu-id="568d0-146">A forrást tároló tárhely relatív elérési útja</span><span class="sxs-lookup"><span data-stu-id="568d0-146">Relative path of the storage which stores the source</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="568d0-147">-SourceType</span><span class="sxs-lookup"><span data-stu-id="568d0-147">-SourceType</span></span>
<span data-ttu-id="568d0-148">A feltöltött forrás típusa</span><span class="sxs-lookup"><span data-stu-id="568d0-148">Type of the source uploaded</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Support.UserSourceType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="568d0-149">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="568d0-149">-SourceVersion</span></span>
<span data-ttu-id="568d0-150">A forrás verziója</span><span class="sxs-lookup"><span data-stu-id="568d0-150">Version of the source</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="568d0-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="568d0-151">-SubscriptionId</span></span>
<span data-ttu-id="568d0-152">Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="568d0-152">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="568d0-153">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="568d0-153">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="568d0-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="568d0-154">-Confirm</span></span>
<span data-ttu-id="568d0-155">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="568d0-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="568d0-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="568d0-156">-WhatIf</span></span>
<span data-ttu-id="568d0-157">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="568d0-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="568d0-158">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="568d0-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="568d0-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="568d0-159">CommonParameters</span></span>
<span data-ttu-id="568d0-160">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="568d0-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="568d0-161">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="568d0-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="568d0-162">INPUTS</span><span class="sxs-lookup"><span data-stu-id="568d0-162">INPUTS</span></span>

### <span data-ttu-id="568d0-163">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="568d0-163">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="568d0-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="568d0-164">OUTPUTS</span></span>

### <span data-ttu-id="568d0-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="568d0-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="568d0-166">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="568d0-166">NOTES</span></span>

<span data-ttu-id="568d0-167">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="568d0-167">ALIASES</span></span>

<span data-ttu-id="568d0-168">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="568d0-168">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="568d0-169">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="568d0-169">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="568d0-170">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="568d0-170">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="568d0-171">INPUTOBJECT: <ISpringCloudIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="568d0-171">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="568d0-172">`[AppName <String>]`: Az apperőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="568d0-172">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="568d0-173">`[BindingName <String>]`: A Kötés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="568d0-173">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="568d0-174">`[CertificateName <String>]`: A tanúsítványforrás neve.</span><span class="sxs-lookup"><span data-stu-id="568d0-174">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="568d0-175">`[DeploymentName <String>]`: A Központi telepítés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="568d0-175">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="568d0-176">`[DomainName <String>]`: Az egyéni tartományerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="568d0-176">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="568d0-177">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="568d0-177">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="568d0-178">`[Location <String>]`: a régió</span><span class="sxs-lookup"><span data-stu-id="568d0-178">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="568d0-179">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="568d0-179">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="568d0-180">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="568d0-180">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="568d0-181">`[ServiceName <String>]`: A Szolgáltatás erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="568d0-181">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="568d0-182">`[SubscriptionId <String>]`: Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="568d0-182">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="568d0-183">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="568d0-183">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="568d0-184">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="568d0-184">RELATED LINKS</span></span>

