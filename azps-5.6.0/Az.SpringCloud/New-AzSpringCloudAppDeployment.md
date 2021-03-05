---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.SpringCloud/new-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
ms.openlocfilehash: de1f09fe6fd484345ebf4ebd7ae2a27d4640c694
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010197"
---
# <span data-ttu-id="04b84-101">New-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="04b84-101">New-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="04b84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04b84-102">SYNOPSIS</span></span>
<span data-ttu-id="04b84-103">Hozzon létre egy új központi telepítést, vagy frissítsen egy kilépő központi telepítést.</span><span class="sxs-lookup"><span data-stu-id="04b84-103">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="04b84-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="04b84-104">SYNTAX</span></span>

```
New-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="04b84-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="04b84-105">DESCRIPTION</span></span>
<span data-ttu-id="04b84-106">Hozzon létre egy új központi telepítést, vagy frissítsen egy kilépő központi telepítést.</span><span class="sxs-lookup"><span data-stu-id="04b84-106">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="04b84-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="04b84-107">EXAMPLES</span></span>

### <span data-ttu-id="04b84-108">1. példa: 1. példa: Tavaszi felhőbeli telepítés létrehozása.</span><span class="sxs-lookup"><span data-stu-id="04b84-108">Example 1: Example 1: Create a spring cloud deployment.</span></span>
```powershell
PS C:\> New-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rp -name spring-cloud-service -AppName gateway -DeploymentName default

Active                               : False
AppName                              : gateway
CreatedTime                          :
DeploymentSettingCpu                 : 1
DeploymentSettingEnvironmentVariable : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettingsEnvironmentVariables
DeploymentSettingInstanceCount       : 1
DeploymentSettingJvmOption           :
DeploymentSettingMemoryInGb          : 1
DeploymentSettingRuntimeVersion      : Java_8
Id                                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway/deployments/default
Instance                             : {gateway-default-7-6bd6f87954-nl2wl}
Name                                 : default
ProvisioningState                    : Succeeded
SourceArtifactSelector               :
SourceRelativePath                   : <default>
SourceType                           : Jar
SourceVersion                        :
Status                               : Running
Type                                 : Microsoft.AppPlatform/Spring/apps/deployments
DeploymentSetting                    : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettings
Property                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentResourceProperties
Source                               : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.UserSourceInfo
```

<span data-ttu-id="04b84-109">Tavaszi felhőbeli telepítés létrehozása.</span><span class="sxs-lookup"><span data-stu-id="04b84-109">Create a spring cloud deployment.</span></span>

## <span data-ttu-id="04b84-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04b84-110">PARAMETERS</span></span>

### <span data-ttu-id="04b84-111">-AppName</span><span class="sxs-lookup"><span data-stu-id="04b84-111">-AppName</span></span>
<span data-ttu-id="04b84-112">Az alkalmazáserőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="04b84-112">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04b84-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04b84-113">-AsJob</span></span>
<span data-ttu-id="04b84-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="04b84-114">Run the command as a job</span></span>

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

### <span data-ttu-id="04b84-115">-Cpu</span><span class="sxs-lookup"><span data-stu-id="04b84-115">-Cpu</span></span>
<span data-ttu-id="04b84-116">Kötelező processzor</span><span class="sxs-lookup"><span data-stu-id="04b84-116">Required CPU</span></span>

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

### <span data-ttu-id="04b84-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04b84-117">-DefaultProfile</span></span>
<span data-ttu-id="04b84-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="04b84-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04b84-119">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="04b84-119">-EnvironmentVariable</span></span>
<span data-ttu-id="04b84-120">Környezeti változók gyűjteménye</span><span class="sxs-lookup"><span data-stu-id="04b84-120">Collection of environment variables</span></span>

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

### <span data-ttu-id="04b84-121">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="04b84-121">-JvmOption</span></span>
<span data-ttu-id="04b84-122">JVM paraméter</span><span class="sxs-lookup"><span data-stu-id="04b84-122">JVM parameter</span></span>

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

### <span data-ttu-id="04b84-123">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="04b84-123">-MemoryInGb</span></span>
<span data-ttu-id="04b84-124">A szükséges memória mérete GB-ban</span><span class="sxs-lookup"><span data-stu-id="04b84-124">Required Memory size in GB</span></span>

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

### <span data-ttu-id="04b84-125">-Name</span><span class="sxs-lookup"><span data-stu-id="04b84-125">-Name</span></span>
<span data-ttu-id="04b84-126">A Központi telepítés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="04b84-126">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04b84-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="04b84-127">-NoWait</span></span>
<span data-ttu-id="04b84-128">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="04b84-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="04b84-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04b84-129">-ResourceGroupName</span></span>
<span data-ttu-id="04b84-130">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="04b84-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="04b84-131">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="04b84-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04b84-132">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="04b84-132">-RuntimeVersion</span></span>
<span data-ttu-id="04b84-133">Runtime version</span><span class="sxs-lookup"><span data-stu-id="04b84-133">Runtime version</span></span>

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

### <span data-ttu-id="04b84-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="04b84-134">-ServiceName</span></span>
<span data-ttu-id="04b84-135">A Szolgáltatás erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="04b84-135">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04b84-136">-SourceArtifactSele</span><span class="sxs-lookup"><span data-stu-id="04b84-136">-SourceArtifactSelector</span></span>
<span data-ttu-id="04b84-137">Selector for the artifact to be used for the deployment for multi-module projects.</span><span class="sxs-lookup"><span data-stu-id="04b84-137">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="04b84-138">Ennek kell lennie a célmodulhoz/projekthez vezető relatív elérési útnak.</span><span class="sxs-lookup"><span data-stu-id="04b84-138">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="04b84-139">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="04b84-139">-SourceRelativePath</span></span>
<span data-ttu-id="04b84-140">A forrást tároló tárhely relatív elérési útja</span><span class="sxs-lookup"><span data-stu-id="04b84-140">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="04b84-141">-SourceType</span><span class="sxs-lookup"><span data-stu-id="04b84-141">-SourceType</span></span>
<span data-ttu-id="04b84-142">A feltöltött forrás típusa</span><span class="sxs-lookup"><span data-stu-id="04b84-142">Type of the source uploaded</span></span>

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

### <span data-ttu-id="04b84-143">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="04b84-143">-SourceVersion</span></span>
<span data-ttu-id="04b84-144">A forrás verziója</span><span class="sxs-lookup"><span data-stu-id="04b84-144">Version of the source</span></span>

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

### <span data-ttu-id="04b84-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="04b84-145">-SubscriptionId</span></span>
<span data-ttu-id="04b84-146">Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="04b84-146">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="04b84-147">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="04b84-147">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04b84-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04b84-148">-Confirm</span></span>
<span data-ttu-id="04b84-149">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="04b84-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04b84-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04b84-150">-WhatIf</span></span>
<span data-ttu-id="04b84-151">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="04b84-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04b84-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="04b84-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04b84-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04b84-153">CommonParameters</span></span>
<span data-ttu-id="04b84-154">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04b84-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04b84-155">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04b84-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04b84-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="04b84-156">INPUTS</span></span>

## <span data-ttu-id="04b84-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04b84-157">OUTPUTS</span></span>

### <span data-ttu-id="04b84-158">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="04b84-158">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="04b84-159">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="04b84-159">NOTES</span></span>

<span data-ttu-id="04b84-160">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="04b84-160">ALIASES</span></span>

## <span data-ttu-id="04b84-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04b84-161">RELATED LINKS</span></span>

