---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/get-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
ms.openlocfilehash: b4b68f654c78da0dc2341966e3f9efaac397e504
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920266"
---
# <span data-ttu-id="5d7eb-101">Get-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="5d7eb-101">Get-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="5d7eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d7eb-102">SYNOPSIS</span></span>
<span data-ttu-id="5d7eb-103">Telepítési példány és tulajdonságainak lekérte.</span><span class="sxs-lookup"><span data-stu-id="5d7eb-103">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="5d7eb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5d7eb-104">SYNTAX</span></span>

### <span data-ttu-id="5d7eb-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5d7eb-105">List1 (Default)</span></span>
```
Get-AzSpringCloudAppDeployment -ResourceGroupName <String> -ServiceName <String> [-SubscriptionId <String[]>]
 [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5d7eb-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="5d7eb-106">Get</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5d7eb-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5d7eb-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="5d7eb-108">Lista</span><span class="sxs-lookup"><span data-stu-id="5d7eb-108">List</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5d7eb-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5d7eb-109">DESCRIPTION</span></span>
<span data-ttu-id="5d7eb-110">Telepítési példány és tulajdonságainak lekérte.</span><span class="sxs-lookup"><span data-stu-id="5d7eb-110">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="5d7eb-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5d7eb-111">EXAMPLES</span></span>

### <span data-ttu-id="5d7eb-112">1. példa: A Spring Cloud App Deploymeng telepítése név szerint.</span><span class="sxs-lookup"><span data-stu-id="5d7eb-112">Example 1: Get Spring Cloud App Deploymeng by name.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
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

<span data-ttu-id="5d7eb-113">Szerezze be a Spring Cloud App Deploymeng alkalmazást név szerint.</span><span class="sxs-lookup"><span data-stu-id="5d7eb-113">Get Spring Cloud App Deploymeng by name.</span></span>

### <span data-ttu-id="5d7eb-114">2. példa: Az összes telepítés felsorolása egy adott tavaszi felhőalkalmazás alatt.</span><span class="sxs-lookup"><span data-stu-id="5d7eb-114">Example 2: List all the deployment under a given spring cloud app.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
Name    Type
----    ----
default Microsoft.AppPlatform/Spring/apps/deployments
prod    Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="5d7eb-115">List all the deployment under a given spring cloud app.</span><span class="sxs-lookup"><span data-stu-id="5d7eb-115">List all the deployment under a given spring cloud app.</span></span>

## <span data-ttu-id="5d7eb-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d7eb-116">PARAMETERS</span></span>

### <span data-ttu-id="5d7eb-117">-AppName</span><span class="sxs-lookup"><span data-stu-id="5d7eb-117">-AppName</span></span>
<span data-ttu-id="5d7eb-118">Az alkalmazáserőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="5d7eb-118">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d7eb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d7eb-119">-DefaultProfile</span></span>
<span data-ttu-id="5d7eb-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5d7eb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d7eb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d7eb-121">-InputObject</span></span>
<span data-ttu-id="5d7eb-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="5d7eb-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d7eb-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5d7eb-123">-Name</span></span>
<span data-ttu-id="5d7eb-124">A Központi telepítés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="5d7eb-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d7eb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d7eb-125">-ResourceGroupName</span></span>
<span data-ttu-id="5d7eb-126">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5d7eb-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="5d7eb-127">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="5d7eb-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d7eb-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5d7eb-128">-ServiceName</span></span>
<span data-ttu-id="5d7eb-129">A Szolgáltatás erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="5d7eb-129">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d7eb-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5d7eb-130">-SubscriptionId</span></span>
<span data-ttu-id="5d7eb-131">Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="5d7eb-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="5d7eb-132">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="5d7eb-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d7eb-133">-Version</span><span class="sxs-lookup"><span data-stu-id="5d7eb-133">-Version</span></span>
<span data-ttu-id="5d7eb-134">A listában szereplő telepítések verziója</span><span class="sxs-lookup"><span data-stu-id="5d7eb-134">Version of the deployments to be listed</span></span>

```yaml
Type: System.String[]
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d7eb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d7eb-135">CommonParameters</span></span>
<span data-ttu-id="5d7eb-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d7eb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d7eb-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d7eb-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d7eb-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5d7eb-138">INPUTS</span></span>

### <span data-ttu-id="5d7eb-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="5d7eb-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="5d7eb-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d7eb-140">OUTPUTS</span></span>

### <span data-ttu-id="5d7eb-141">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="5d7eb-141">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="5d7eb-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5d7eb-142">NOTES</span></span>

<span data-ttu-id="5d7eb-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="5d7eb-143">ALIASES</span></span>

<span data-ttu-id="5d7eb-144">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="5d7eb-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5d7eb-145">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="5d7eb-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5d7eb-146">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5d7eb-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5d7eb-147">INPUTOBJECT: <ISpringCloudIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="5d7eb-147">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5d7eb-148">`[AppName <String>]`: Az apperőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="5d7eb-148">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="5d7eb-149">`[BindingName <String>]`: A Kötés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="5d7eb-149">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="5d7eb-150">`[CertificateName <String>]`: A tanúsítványforrás neve.</span><span class="sxs-lookup"><span data-stu-id="5d7eb-150">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="5d7eb-151">`[DeploymentName <String>]`: A Központi telepítés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="5d7eb-151">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="5d7eb-152">`[DomainName <String>]`: Az egyéni tartományerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="5d7eb-152">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="5d7eb-153">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="5d7eb-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5d7eb-154">`[Location <String>]`: a régió</span><span class="sxs-lookup"><span data-stu-id="5d7eb-154">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="5d7eb-155">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5d7eb-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="5d7eb-156">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="5d7eb-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="5d7eb-157">`[ServiceName <String>]`: A Szolgáltatás erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="5d7eb-157">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="5d7eb-158">`[SubscriptionId <String>]`: Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="5d7eb-158">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="5d7eb-159">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="5d7eb-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="5d7eb-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d7eb-160">RELATED LINKS</span></span>

