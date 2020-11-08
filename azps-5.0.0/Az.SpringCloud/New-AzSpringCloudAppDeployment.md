---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/new-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 37538cddb7654b665b2b2dd4935414a2cb76b45a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185233"
---
# <span data-ttu-id="cc50b-101">New-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="cc50b-101">New-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="cc50b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cc50b-102">SYNOPSIS</span></span>
<span data-ttu-id="cc50b-103">Hozzon létre egy új központi telepítőt, vagy frissítse a kilépési telepítését.</span><span class="sxs-lookup"><span data-stu-id="cc50b-103">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="cc50b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cc50b-104">SYNTAX</span></span>

```
New-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="cc50b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cc50b-105">DESCRIPTION</span></span>
<span data-ttu-id="cc50b-106">Hozzon létre egy új központi telepítőt, vagy frissítse a kilépési telepítését.</span><span class="sxs-lookup"><span data-stu-id="cc50b-106">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="cc50b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cc50b-107">EXAMPLES</span></span>

### <span data-ttu-id="cc50b-108">Példa 1: példa 1: a tavaszi Felhőbeli bevezetést hozza létre.</span><span class="sxs-lookup"><span data-stu-id="cc50b-108">Example 1: Example 1: Create a spring cloud deployment.</span></span>
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

<span data-ttu-id="cc50b-109">Tavaszi Felhőbeli bevezetést hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="cc50b-109">Create a spring cloud deployment.</span></span>

## <span data-ttu-id="cc50b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cc50b-110">PARAMETERS</span></span>

### <span data-ttu-id="cc50b-111">-Appnév</span><span class="sxs-lookup"><span data-stu-id="cc50b-111">-AppName</span></span>
<span data-ttu-id="cc50b-112">Az App-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="cc50b-112">The name of the App resource.</span></span>

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

### <span data-ttu-id="cc50b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc50b-113">-AsJob</span></span>
<span data-ttu-id="cc50b-114">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="cc50b-114">Run the command as a job</span></span>

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

### <span data-ttu-id="cc50b-115">-CPU</span><span class="sxs-lookup"><span data-stu-id="cc50b-115">-Cpu</span></span>
<span data-ttu-id="cc50b-116">Szükséges processzor</span><span class="sxs-lookup"><span data-stu-id="cc50b-116">Required CPU</span></span>

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

### <span data-ttu-id="cc50b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc50b-117">-DefaultProfile</span></span>
<span data-ttu-id="cc50b-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cc50b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc50b-119">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="cc50b-119">-EnvironmentVariable</span></span>
<span data-ttu-id="cc50b-120">Környezeti változók begyűjtése</span><span class="sxs-lookup"><span data-stu-id="cc50b-120">Collection of environment variables</span></span>

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

### <span data-ttu-id="cc50b-121">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="cc50b-121">-JvmOption</span></span>
<span data-ttu-id="cc50b-122">JVM paraméter</span><span class="sxs-lookup"><span data-stu-id="cc50b-122">JVM parameter</span></span>

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

### <span data-ttu-id="cc50b-123">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="cc50b-123">-MemoryInGb</span></span>
<span data-ttu-id="cc50b-124">A szükséges memória-méret GB-ban</span><span class="sxs-lookup"><span data-stu-id="cc50b-124">Required Memory size in GB</span></span>

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

### <span data-ttu-id="cc50b-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cc50b-125">-Name</span></span>
<span data-ttu-id="cc50b-126">A központi telepítő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="cc50b-126">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="cc50b-127">-Várva</span><span class="sxs-lookup"><span data-stu-id="cc50b-127">-NoWait</span></span>
<span data-ttu-id="cc50b-128">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="cc50b-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cc50b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc50b-129">-ResourceGroupName</span></span>
<span data-ttu-id="cc50b-130">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cc50b-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="cc50b-131">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="cc50b-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="cc50b-132">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="cc50b-132">-RuntimeVersion</span></span>
<span data-ttu-id="cc50b-133">Futásidejű verzió</span><span class="sxs-lookup"><span data-stu-id="cc50b-133">Runtime version</span></span>

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

### <span data-ttu-id="cc50b-134">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="cc50b-134">-ServiceName</span></span>
<span data-ttu-id="cc50b-135">A szolgáltatás erőforrásának neve.</span><span class="sxs-lookup"><span data-stu-id="cc50b-135">The name of the Service resource.</span></span>

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

### <span data-ttu-id="cc50b-136">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="cc50b-136">-SourceArtifactSelector</span></span>
<span data-ttu-id="cc50b-137">Annak a tárgynak a kijelölése, amelyet a többmodulos projektek telepítéséhez szeretne használni.</span><span class="sxs-lookup"><span data-stu-id="cc50b-137">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="cc50b-138">Ehhez a cél modul/projekt relatív elérési útját kell bemutatnia.</span><span class="sxs-lookup"><span data-stu-id="cc50b-138">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="cc50b-139">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="cc50b-139">-SourceRelativePath</span></span>
<span data-ttu-id="cc50b-140">A forrást tároló tárterület relatív elérési útja</span><span class="sxs-lookup"><span data-stu-id="cc50b-140">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="cc50b-141">-SourceType</span><span class="sxs-lookup"><span data-stu-id="cc50b-141">-SourceType</span></span>
<span data-ttu-id="cc50b-142">A feltöltendő forrás típusa</span><span class="sxs-lookup"><span data-stu-id="cc50b-142">Type of the source uploaded</span></span>

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

### <span data-ttu-id="cc50b-143">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="cc50b-143">-SourceVersion</span></span>
<span data-ttu-id="cc50b-144">A forrás verziója</span><span class="sxs-lookup"><span data-stu-id="cc50b-144">Version of the source</span></span>

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

### <span data-ttu-id="cc50b-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cc50b-145">-SubscriptionId</span></span>
<span data-ttu-id="cc50b-146">Megkapja az előfizetés AZONOSÍTÓját, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="cc50b-146">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="cc50b-147">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="cc50b-147">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cc50b-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cc50b-148">-Confirm</span></span>
<span data-ttu-id="cc50b-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cc50b-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc50b-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc50b-150">-WhatIf</span></span>
<span data-ttu-id="cc50b-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cc50b-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc50b-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cc50b-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc50b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc50b-153">CommonParameters</span></span>
<span data-ttu-id="cc50b-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cc50b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc50b-155">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cc50b-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc50b-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc50b-156">INPUTS</span></span>

## <span data-ttu-id="cc50b-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc50b-157">OUTPUTS</span></span>

### <span data-ttu-id="cc50b-158">Microsoft. Azure. PowerShell. parancsmagok. SpringCloud. modellek. Api20200701. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="cc50b-158">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="cc50b-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cc50b-159">NOTES</span></span>

<span data-ttu-id="cc50b-160">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="cc50b-160">ALIASES</span></span>

## <span data-ttu-id="cc50b-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc50b-161">RELATED LINKS</span></span>

