---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/update-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
ms.openlocfilehash: ba31f4d7c81392a30f4f8b9073d967b2a57cfab7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185219"
---
# <span data-ttu-id="dab78-101">Update-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="dab78-101">Update-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="dab78-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dab78-102">SYNOPSIS</span></span>
<span data-ttu-id="dab78-103">Művelet a kilépés a központi példányból</span><span class="sxs-lookup"><span data-stu-id="dab78-103">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="dab78-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dab78-104">SYNTAX</span></span>

### <span data-ttu-id="dab78-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dab78-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="dab78-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="dab78-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-Cpu <Int32>]
 [-EnvironmentVariable <Hashtable>] [-JvmOption <String>] [-MemoryInGb <Int32>]
 [-RuntimeVersion <RuntimeVersion>] [-SourceArtifactSelector <String>] [-SourceRelativePath <String>]
 [-SourceType <UserSourceType>] [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dab78-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="dab78-107">DESCRIPTION</span></span>
<span data-ttu-id="dab78-108">Művelet a kilépés a központi példányból</span><span class="sxs-lookup"><span data-stu-id="dab78-108">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="dab78-109">Példák</span><span class="sxs-lookup"><span data-stu-id="dab78-109">EXAMPLES</span></span>

### <span data-ttu-id="dab78-110">Példa 1: a tavaszi Felhőbeli központi telepítések frissítése név szerint.</span><span class="sxs-lookup"><span data-stu-id="dab78-110">Example 1: Update Spring Cloud Deployment by name.</span></span>
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

<span data-ttu-id="dab78-111">Frissítse a tavaszi felhő telepítését név szerint.</span><span class="sxs-lookup"><span data-stu-id="dab78-111">Update Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="dab78-112">2. példa: a tavaszi Felhőbeli központi telepítő frissítése a pipe-ról</span><span class="sxs-lookup"><span data-stu-id="dab78-112">Example 2: Update Spring Cloud Deployment from pipe.</span></span>
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

<span data-ttu-id="dab78-113">Frissítse a tavaszi felhő telepítését a pipe-ról.</span><span class="sxs-lookup"><span data-stu-id="dab78-113">Update Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="dab78-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dab78-114">PARAMETERS</span></span>

### <span data-ttu-id="dab78-115">-Appnév</span><span class="sxs-lookup"><span data-stu-id="dab78-115">-AppName</span></span>
<span data-ttu-id="dab78-116">Az App-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="dab78-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="dab78-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dab78-117">-AsJob</span></span>
<span data-ttu-id="dab78-118">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="dab78-118">Run the command as a job</span></span>

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

### <span data-ttu-id="dab78-119">-CPU</span><span class="sxs-lookup"><span data-stu-id="dab78-119">-Cpu</span></span>
<span data-ttu-id="dab78-120">Szükséges processzor</span><span class="sxs-lookup"><span data-stu-id="dab78-120">Required CPU</span></span>

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

### <span data-ttu-id="dab78-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dab78-121">-DefaultProfile</span></span>
<span data-ttu-id="dab78-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dab78-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dab78-123">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="dab78-123">-EnvironmentVariable</span></span>
<span data-ttu-id="dab78-124">Környezeti változók begyűjtése</span><span class="sxs-lookup"><span data-stu-id="dab78-124">Collection of environment variables</span></span>

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

### <span data-ttu-id="dab78-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dab78-125">-InputObject</span></span>
<span data-ttu-id="dab78-126">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="dab78-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="dab78-127">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="dab78-127">-JvmOption</span></span>
<span data-ttu-id="dab78-128">JVM paraméter</span><span class="sxs-lookup"><span data-stu-id="dab78-128">JVM parameter</span></span>

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

### <span data-ttu-id="dab78-129">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="dab78-129">-MemoryInGb</span></span>
<span data-ttu-id="dab78-130">A szükséges memória-méret GB-ban</span><span class="sxs-lookup"><span data-stu-id="dab78-130">Required Memory size in GB</span></span>

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

### <span data-ttu-id="dab78-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dab78-131">-Name</span></span>
<span data-ttu-id="dab78-132">A központi telepítő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="dab78-132">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="dab78-133">-Várva</span><span class="sxs-lookup"><span data-stu-id="dab78-133">-NoWait</span></span>
<span data-ttu-id="dab78-134">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="dab78-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dab78-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dab78-135">-ResourceGroupName</span></span>
<span data-ttu-id="dab78-136">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="dab78-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="dab78-137">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="dab78-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="dab78-138">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="dab78-138">-RuntimeVersion</span></span>
<span data-ttu-id="dab78-139">Futásidejű verzió</span><span class="sxs-lookup"><span data-stu-id="dab78-139">Runtime version</span></span>

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

### <span data-ttu-id="dab78-140">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="dab78-140">-ServiceName</span></span>
<span data-ttu-id="dab78-141">A szolgáltatás erőforrásának neve.</span><span class="sxs-lookup"><span data-stu-id="dab78-141">The name of the Service resource.</span></span>

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

### <span data-ttu-id="dab78-142">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="dab78-142">-SourceArtifactSelector</span></span>
<span data-ttu-id="dab78-143">Annak a tárgynak a kijelölése, amelyet a többmodulos projektek telepítéséhez szeretne használni.</span><span class="sxs-lookup"><span data-stu-id="dab78-143">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="dab78-144">Ehhez a cél modul/projekt relatív elérési útját kell bemutatnia.</span><span class="sxs-lookup"><span data-stu-id="dab78-144">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="dab78-145">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="dab78-145">-SourceRelativePath</span></span>
<span data-ttu-id="dab78-146">A forrást tároló tárterület relatív elérési útja</span><span class="sxs-lookup"><span data-stu-id="dab78-146">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="dab78-147">-SourceType</span><span class="sxs-lookup"><span data-stu-id="dab78-147">-SourceType</span></span>
<span data-ttu-id="dab78-148">A feltöltendő forrás típusa</span><span class="sxs-lookup"><span data-stu-id="dab78-148">Type of the source uploaded</span></span>

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

### <span data-ttu-id="dab78-149">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="dab78-149">-SourceVersion</span></span>
<span data-ttu-id="dab78-150">A forrás verziója</span><span class="sxs-lookup"><span data-stu-id="dab78-150">Version of the source</span></span>

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

### <span data-ttu-id="dab78-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dab78-151">-SubscriptionId</span></span>
<span data-ttu-id="dab78-152">Megkapja az előfizetés AZONOSÍTÓját, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="dab78-152">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="dab78-153">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="dab78-153">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="dab78-154">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dab78-154">-Confirm</span></span>
<span data-ttu-id="dab78-155">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dab78-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dab78-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dab78-156">-WhatIf</span></span>
<span data-ttu-id="dab78-157">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dab78-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dab78-158">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dab78-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dab78-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dab78-159">CommonParameters</span></span>
<span data-ttu-id="dab78-160">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dab78-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dab78-161">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="dab78-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dab78-162">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dab78-162">INPUTS</span></span>

### <span data-ttu-id="dab78-163">Microsoft. Azure. PowerShell. parancsmagok. SpringCloud. models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="dab78-163">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="dab78-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dab78-164">OUTPUTS</span></span>

### <span data-ttu-id="dab78-165">Microsoft. Azure. PowerShell. parancsmagok. SpringCloud. modellek. Api20200701. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="dab78-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="dab78-166">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dab78-166">NOTES</span></span>

<span data-ttu-id="dab78-167">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="dab78-167">ALIASES</span></span>

<span data-ttu-id="dab78-168">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="dab78-168">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dab78-169">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="dab78-169">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dab78-170">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="dab78-170">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dab78-171">INPUTOBJECT <ISpringCloudIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="dab78-171">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dab78-172">`[AppName <String>]`: Az App-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="dab78-172">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="dab78-173">`[BindingName <String>]`: A kötési erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="dab78-173">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="dab78-174">`[CertificateName <String>]`: A tanúsítvány-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="dab78-174">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="dab78-175">`[DeploymentName <String>]`: A telepítő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="dab78-175">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="dab78-176">`[DomainName <String>]`: Az egyéni tartomány-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="dab78-176">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="dab78-177">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="dab78-177">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dab78-178">`[Location <String>]`: a régió</span><span class="sxs-lookup"><span data-stu-id="dab78-178">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="dab78-179">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="dab78-179">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="dab78-180">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="dab78-180">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="dab78-181">`[ServiceName <String>]`: A szolgáltatás-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="dab78-181">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="dab78-182">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót kapja.</span><span class="sxs-lookup"><span data-stu-id="dab78-182">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="dab78-183">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="dab78-183">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="dab78-184">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dab78-184">RELATED LINKS</span></span>

