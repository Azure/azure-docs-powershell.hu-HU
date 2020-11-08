---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/new-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 0669371f589722e3da18e554df98dbf7d193ccc8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183930"
---
# <span data-ttu-id="0933e-101">New-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="0933e-101">New-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="0933e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0933e-102">SYNOPSIS</span></span>
<span data-ttu-id="0933e-103">Hozzon létre egy új központi telepítőt, vagy frissítse a kilépési telepítését.</span><span class="sxs-lookup"><span data-stu-id="0933e-103">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="0933e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0933e-104">SYNTAX</span></span>

```
New-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-InstanceCount <Int32>] [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="0933e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0933e-105">DESCRIPTION</span></span>
<span data-ttu-id="0933e-106">Hozzon létre egy új központi telepítőt, vagy frissítse a kilépési telepítését.</span><span class="sxs-lookup"><span data-stu-id="0933e-106">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="0933e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0933e-107">EXAMPLES</span></span>

### <span data-ttu-id="0933e-108">Példa 1: példa 1: a tavaszi Felhőbeli bevezetést hozza létre.</span><span class="sxs-lookup"><span data-stu-id="0933e-108">Example 1: Example 1: Create a spring cloud deployment.</span></span>
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

<span data-ttu-id="0933e-109">Tavaszi Felhőbeli bevezetést hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="0933e-109">Create a spring cloud deployment.</span></span>

## <span data-ttu-id="0933e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0933e-110">PARAMETERS</span></span>

### <span data-ttu-id="0933e-111">-Appnév</span><span class="sxs-lookup"><span data-stu-id="0933e-111">-AppName</span></span>
<span data-ttu-id="0933e-112">Az App-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="0933e-112">The name of the App resource.</span></span>

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

### <span data-ttu-id="0933e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0933e-113">-AsJob</span></span>
<span data-ttu-id="0933e-114">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="0933e-114">Run the command as a job</span></span>

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

### <span data-ttu-id="0933e-115">-CPU</span><span class="sxs-lookup"><span data-stu-id="0933e-115">-Cpu</span></span>
<span data-ttu-id="0933e-116">Szükséges processzor</span><span class="sxs-lookup"><span data-stu-id="0933e-116">Required CPU</span></span>

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

### <span data-ttu-id="0933e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0933e-117">-DefaultProfile</span></span>
<span data-ttu-id="0933e-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0933e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0933e-119">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="0933e-119">-EnvironmentVariable</span></span>
<span data-ttu-id="0933e-120">Környezeti változók begyűjtése</span><span class="sxs-lookup"><span data-stu-id="0933e-120">Collection of environment variables</span></span>

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

### <span data-ttu-id="0933e-121">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="0933e-121">-InstanceCount</span></span>
<span data-ttu-id="0933e-122">Példányok száma</span><span class="sxs-lookup"><span data-stu-id="0933e-122">Instance count</span></span>

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

### <span data-ttu-id="0933e-123">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="0933e-123">-JvmOption</span></span>
<span data-ttu-id="0933e-124">JVM paraméter</span><span class="sxs-lookup"><span data-stu-id="0933e-124">JVM parameter</span></span>

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

### <span data-ttu-id="0933e-125">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="0933e-125">-MemoryInGb</span></span>
<span data-ttu-id="0933e-126">A szükséges memória-méret GB-ban</span><span class="sxs-lookup"><span data-stu-id="0933e-126">Required Memory size in GB</span></span>

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

### <span data-ttu-id="0933e-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0933e-127">-Name</span></span>
<span data-ttu-id="0933e-128">A központi telepítő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="0933e-128">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="0933e-129">-Várva</span><span class="sxs-lookup"><span data-stu-id="0933e-129">-NoWait</span></span>
<span data-ttu-id="0933e-130">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="0933e-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0933e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0933e-131">-ResourceGroupName</span></span>
<span data-ttu-id="0933e-132">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0933e-132">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="0933e-133">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="0933e-133">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="0933e-134">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="0933e-134">-RuntimeVersion</span></span>
<span data-ttu-id="0933e-135">Futásidejű verzió</span><span class="sxs-lookup"><span data-stu-id="0933e-135">Runtime version</span></span>

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

### <span data-ttu-id="0933e-136">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="0933e-136">-ServiceName</span></span>
<span data-ttu-id="0933e-137">A szolgáltatás erőforrásának neve.</span><span class="sxs-lookup"><span data-stu-id="0933e-137">The name of the Service resource.</span></span>

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

### <span data-ttu-id="0933e-138">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="0933e-138">-SourceArtifactSelector</span></span>
<span data-ttu-id="0933e-139">Annak a tárgynak a kijelölése, amelyet a többmodulos projektek telepítéséhez szeretne használni.</span><span class="sxs-lookup"><span data-stu-id="0933e-139">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="0933e-140">Ehhez a cél modul/projekt relatív elérési útját kell bemutatnia.</span><span class="sxs-lookup"><span data-stu-id="0933e-140">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="0933e-141">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="0933e-141">-SourceRelativePath</span></span>
<span data-ttu-id="0933e-142">A forrást tároló tárterület relatív elérési útja</span><span class="sxs-lookup"><span data-stu-id="0933e-142">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="0933e-143">-SourceType</span><span class="sxs-lookup"><span data-stu-id="0933e-143">-SourceType</span></span>
<span data-ttu-id="0933e-144">A feltöltendő forrás típusa</span><span class="sxs-lookup"><span data-stu-id="0933e-144">Type of the source uploaded</span></span>

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

### <span data-ttu-id="0933e-145">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="0933e-145">-SourceVersion</span></span>
<span data-ttu-id="0933e-146">A forrás verziója</span><span class="sxs-lookup"><span data-stu-id="0933e-146">Version of the source</span></span>

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

### <span data-ttu-id="0933e-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0933e-147">-SubscriptionId</span></span>
<span data-ttu-id="0933e-148">Megkapja az előfizetés AZONOSÍTÓját, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="0933e-148">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="0933e-149">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="0933e-149">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0933e-150">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0933e-150">-Confirm</span></span>
<span data-ttu-id="0933e-151">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0933e-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0933e-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0933e-152">-WhatIf</span></span>
<span data-ttu-id="0933e-153">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0933e-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0933e-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0933e-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0933e-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0933e-155">CommonParameters</span></span>
<span data-ttu-id="0933e-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0933e-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0933e-157">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0933e-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0933e-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0933e-158">INPUTS</span></span>

## <span data-ttu-id="0933e-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0933e-159">OUTPUTS</span></span>

### <span data-ttu-id="0933e-160">Microsoft. Azure. PowerShell. parancsmagok. SpringCloud. modellek. Api20190501Preview. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="0933e-160">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IDeploymentResource</span></span>

## <span data-ttu-id="0933e-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0933e-161">NOTES</span></span>

<span data-ttu-id="0933e-162">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="0933e-162">ALIASES</span></span>

## <span data-ttu-id="0933e-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0933e-163">RELATED LINKS</span></span>

