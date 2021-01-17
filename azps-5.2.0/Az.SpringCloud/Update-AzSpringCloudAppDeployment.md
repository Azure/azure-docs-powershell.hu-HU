---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/update-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
ms.openlocfilehash: ba31f4d7c81392a30f4f8b9073d967b2a57cfab7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332442"
---
# <span data-ttu-id="0f24c-101">Update-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="0f24c-101">Update-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="0f24c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f24c-102">SYNOPSIS</span></span>
<span data-ttu-id="0f24c-103">A kilépő telepítés frissítésére használható művelet.</span><span class="sxs-lookup"><span data-stu-id="0f24c-103">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="0f24c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0f24c-104">SYNTAX</span></span>

### <span data-ttu-id="0f24c-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0f24c-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="0f24c-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0f24c-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-Cpu <Int32>]
 [-EnvironmentVariable <Hashtable>] [-JvmOption <String>] [-MemoryInGb <Int32>]
 [-RuntimeVersion <RuntimeVersion>] [-SourceArtifactSelector <String>] [-SourceRelativePath <String>]
 [-SourceType <UserSourceType>] [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0f24c-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0f24c-107">DESCRIPTION</span></span>
<span data-ttu-id="0f24c-108">A kilépő telepítés frissítésére használható művelet.</span><span class="sxs-lookup"><span data-stu-id="0f24c-108">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="0f24c-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0f24c-109">EXAMPLES</span></span>

### <span data-ttu-id="0f24c-110">1. példa: A tavaszi felhőbeli telepítés frissítése név szerint.</span><span class="sxs-lookup"><span data-stu-id="0f24c-110">Example 1: Update Spring Cloud Deployment by name.</span></span>
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

<span data-ttu-id="0f24c-111">Frissítse a Tavaszi felhőbeli telepítést név szerint.</span><span class="sxs-lookup"><span data-stu-id="0f24c-111">Update Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="0f24c-112">2. példa: A tavaszi felhőbeli telepítés frissítése a pipe-ból.</span><span class="sxs-lookup"><span data-stu-id="0f24c-112">Example 2: Update Spring Cloud Deployment from pipe.</span></span>
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

<span data-ttu-id="0f24c-113">Frissítse a tavaszi felhőbeli telepítést a pipe-ból.</span><span class="sxs-lookup"><span data-stu-id="0f24c-113">Update Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="0f24c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f24c-114">PARAMETERS</span></span>

### <span data-ttu-id="0f24c-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="0f24c-115">-AppName</span></span>
<span data-ttu-id="0f24c-116">Az alkalmazáserőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="0f24c-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="0f24c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f24c-117">-AsJob</span></span>
<span data-ttu-id="0f24c-118">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="0f24c-118">Run the command as a job</span></span>

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

### <span data-ttu-id="0f24c-119">-Cpu</span><span class="sxs-lookup"><span data-stu-id="0f24c-119">-Cpu</span></span>
<span data-ttu-id="0f24c-120">Kötelező processzor</span><span class="sxs-lookup"><span data-stu-id="0f24c-120">Required CPU</span></span>

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

### <span data-ttu-id="0f24c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f24c-121">-DefaultProfile</span></span>
<span data-ttu-id="0f24c-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0f24c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f24c-123">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="0f24c-123">-EnvironmentVariable</span></span>
<span data-ttu-id="0f24c-124">Környezeti változók gyűjteménye</span><span class="sxs-lookup"><span data-stu-id="0f24c-124">Collection of environment variables</span></span>

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

### <span data-ttu-id="0f24c-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f24c-125">-InputObject</span></span>
<span data-ttu-id="0f24c-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="0f24c-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0f24c-127">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="0f24c-127">-JvmOption</span></span>
<span data-ttu-id="0f24c-128">JVM paraméter</span><span class="sxs-lookup"><span data-stu-id="0f24c-128">JVM parameter</span></span>

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

### <span data-ttu-id="0f24c-129">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="0f24c-129">-MemoryInGb</span></span>
<span data-ttu-id="0f24c-130">A szükséges memória mérete GB-ban</span><span class="sxs-lookup"><span data-stu-id="0f24c-130">Required Memory size in GB</span></span>

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

### <span data-ttu-id="0f24c-131">-Name</span><span class="sxs-lookup"><span data-stu-id="0f24c-131">-Name</span></span>
<span data-ttu-id="0f24c-132">A Központi telepítés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="0f24c-132">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="0f24c-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0f24c-133">-NoWait</span></span>
<span data-ttu-id="0f24c-134">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="0f24c-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0f24c-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f24c-135">-ResourceGroupName</span></span>
<span data-ttu-id="0f24c-136">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0f24c-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="0f24c-137">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="0f24c-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="0f24c-138">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="0f24c-138">-RuntimeVersion</span></span>
<span data-ttu-id="0f24c-139">Runtime version</span><span class="sxs-lookup"><span data-stu-id="0f24c-139">Runtime version</span></span>

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

### <span data-ttu-id="0f24c-140">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0f24c-140">-ServiceName</span></span>
<span data-ttu-id="0f24c-141">A Szolgáltatás erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="0f24c-141">The name of the Service resource.</span></span>

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

### <span data-ttu-id="0f24c-142">-SourceArtifactSele</span><span class="sxs-lookup"><span data-stu-id="0f24c-142">-SourceArtifactSelector</span></span>
<span data-ttu-id="0f24c-143">Selector for the artifact to be used for the deployment for multi-module projects.</span><span class="sxs-lookup"><span data-stu-id="0f24c-143">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="0f24c-144">Ennek kell lennie a célmodulhoz/projekthez vezető relatív elérési útnak.</span><span class="sxs-lookup"><span data-stu-id="0f24c-144">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="0f24c-145">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="0f24c-145">-SourceRelativePath</span></span>
<span data-ttu-id="0f24c-146">A forrást tároló tárhely relatív elérési útja</span><span class="sxs-lookup"><span data-stu-id="0f24c-146">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="0f24c-147">-SourceType</span><span class="sxs-lookup"><span data-stu-id="0f24c-147">-SourceType</span></span>
<span data-ttu-id="0f24c-148">A feltöltött forrás típusa</span><span class="sxs-lookup"><span data-stu-id="0f24c-148">Type of the source uploaded</span></span>

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

### <span data-ttu-id="0f24c-149">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="0f24c-149">-SourceVersion</span></span>
<span data-ttu-id="0f24c-150">A forrás verziója</span><span class="sxs-lookup"><span data-stu-id="0f24c-150">Version of the source</span></span>

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

### <span data-ttu-id="0f24c-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0f24c-151">-SubscriptionId</span></span>
<span data-ttu-id="0f24c-152">Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="0f24c-152">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="0f24c-153">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="0f24c-153">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0f24c-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f24c-154">-Confirm</span></span>
<span data-ttu-id="0f24c-155">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0f24c-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f24c-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f24c-156">-WhatIf</span></span>
<span data-ttu-id="0f24c-157">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0f24c-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f24c-158">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0f24c-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f24c-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f24c-159">CommonParameters</span></span>
<span data-ttu-id="0f24c-160">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f24c-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f24c-161">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0f24c-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f24c-162">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0f24c-162">INPUTS</span></span>

### <span data-ttu-id="0f24c-163">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="0f24c-163">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="0f24c-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f24c-164">OUTPUTS</span></span>

### <span data-ttu-id="0f24c-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="0f24c-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="0f24c-166">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0f24c-166">NOTES</span></span>

<span data-ttu-id="0f24c-167">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="0f24c-167">ALIASES</span></span>

<span data-ttu-id="0f24c-168">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="0f24c-168">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0f24c-169">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="0f24c-169">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0f24c-170">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0f24c-170">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0f24c-171">INPUTOBJECT: <ISpringCloudIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="0f24c-171">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0f24c-172">`[AppName <String>]`: Az apperőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="0f24c-172">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="0f24c-173">`[BindingName <String>]`: A Kötés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="0f24c-173">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="0f24c-174">`[CertificateName <String>]`: A tanúsítványforrás neve.</span><span class="sxs-lookup"><span data-stu-id="0f24c-174">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="0f24c-175">`[DeploymentName <String>]`: A Központi telepítés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="0f24c-175">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="0f24c-176">`[DomainName <String>]`: Az egyéni tartományerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="0f24c-176">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="0f24c-177">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="0f24c-177">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0f24c-178">`[Location <String>]`: a régió</span><span class="sxs-lookup"><span data-stu-id="0f24c-178">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="0f24c-179">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0f24c-179">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="0f24c-180">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="0f24c-180">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="0f24c-181">`[ServiceName <String>]`: A Szolgáltatás erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="0f24c-181">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="0f24c-182">`[SubscriptionId <String>]`: Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="0f24c-182">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="0f24c-183">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="0f24c-183">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="0f24c-184">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f24c-184">RELATED LINKS</span></span>

