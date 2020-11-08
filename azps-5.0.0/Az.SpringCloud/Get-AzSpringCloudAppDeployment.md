---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 3accf4b622f77edb0e3d0cea6fe67bbc1db9ff6c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185243"
---
# <span data-ttu-id="dbdf1-101">Get-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="dbdf1-101">Get-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="dbdf1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dbdf1-102">SYNOPSIS</span></span>
<span data-ttu-id="dbdf1-103">Üzembe állítás és a hozzájuk tartozó tulajdonságok beszerzése</span><span class="sxs-lookup"><span data-stu-id="dbdf1-103">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="dbdf1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dbdf1-104">SYNTAX</span></span>

### <span data-ttu-id="dbdf1-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dbdf1-105">List1 (Default)</span></span>
```
Get-AzSpringCloudAppDeployment -ResourceGroupName <String> -ServiceName <String> [-SubscriptionId <String[]>]
 [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dbdf1-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="dbdf1-106">Get</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dbdf1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dbdf1-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="dbdf1-108">Lista</span><span class="sxs-lookup"><span data-stu-id="dbdf1-108">List</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="dbdf1-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="dbdf1-109">DESCRIPTION</span></span>
<span data-ttu-id="dbdf1-110">Üzembe állítás és a hozzájuk tartozó tulajdonságok beszerzése</span><span class="sxs-lookup"><span data-stu-id="dbdf1-110">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="dbdf1-111">Példák</span><span class="sxs-lookup"><span data-stu-id="dbdf1-111">EXAMPLES</span></span>

### <span data-ttu-id="dbdf1-112">1. példa: a tavaszi felhő alkalmazás Deploymeng név szerint.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-112">Example 1: Get Spring Cloud App Deploymeng by name.</span></span>
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

<span data-ttu-id="dbdf1-113">A tavaszi felhő alkalmazás Deploymeng név szerint.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-113">Get Spring Cloud App Deploymeng by name.</span></span>

### <span data-ttu-id="dbdf1-114">2. példa: az adott tavaszi felhő alkalmazásban az összes bevezetést felsorolhatja.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-114">Example 2: List all the deployment under a given spring cloud app.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
Name    Type
----    ----
default Microsoft.AppPlatform/Spring/apps/deployments
prod    Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="dbdf1-115">Az összes bevezetést felsorolhatja egy adott tavaszi felhő alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-115">List all the deployment under a given spring cloud app.</span></span>

## <span data-ttu-id="dbdf1-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dbdf1-116">PARAMETERS</span></span>

### <span data-ttu-id="dbdf1-117">-Appnév</span><span class="sxs-lookup"><span data-stu-id="dbdf1-117">-AppName</span></span>
<span data-ttu-id="dbdf1-118">Az App-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-118">The name of the App resource.</span></span>

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

### <span data-ttu-id="dbdf1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbdf1-119">-DefaultProfile</span></span>
<span data-ttu-id="dbdf1-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbdf1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dbdf1-121">-InputObject</span></span>
<span data-ttu-id="dbdf1-122">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="dbdf1-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dbdf1-123">-Name</span></span>
<span data-ttu-id="dbdf1-124">A központi telepítő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-124">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="dbdf1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbdf1-125">-ResourceGroupName</span></span>
<span data-ttu-id="dbdf1-126">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="dbdf1-127">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="dbdf1-128">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="dbdf1-128">-ServiceName</span></span>
<span data-ttu-id="dbdf1-129">A szolgáltatás erőforrásának neve.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-129">The name of the Service resource.</span></span>

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

### <span data-ttu-id="dbdf1-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dbdf1-130">-SubscriptionId</span></span>
<span data-ttu-id="dbdf1-131">Megkapja az előfizetés AZONOSÍTÓját, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="dbdf1-132">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="dbdf1-133">-Verzió</span><span class="sxs-lookup"><span data-stu-id="dbdf1-133">-Version</span></span>
<span data-ttu-id="dbdf1-134">A listázni kívánt telepített példányok verziója</span><span class="sxs-lookup"><span data-stu-id="dbdf1-134">Version of the deployments to be listed</span></span>

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

### <span data-ttu-id="dbdf1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbdf1-135">CommonParameters</span></span>
<span data-ttu-id="dbdf1-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dbdf1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbdf1-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbdf1-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dbdf1-138">INPUTS</span></span>

### <span data-ttu-id="dbdf1-139">Microsoft. Azure. PowerShell. parancsmagok. SpringCloud. models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="dbdf1-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="dbdf1-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dbdf1-140">OUTPUTS</span></span>

### <span data-ttu-id="dbdf1-141">Microsoft. Azure. PowerShell. parancsmagok. SpringCloud. modellek. Api20200701. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="dbdf1-141">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="dbdf1-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dbdf1-142">NOTES</span></span>

<span data-ttu-id="dbdf1-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="dbdf1-143">ALIASES</span></span>

<span data-ttu-id="dbdf1-144">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="dbdf1-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dbdf1-145">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dbdf1-146">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dbdf1-147">INPUTOBJECT <ISpringCloudIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="dbdf1-147">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dbdf1-148">`[AppName <String>]`: Az App-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-148">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="dbdf1-149">`[BindingName <String>]`: A kötési erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-149">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="dbdf1-150">`[CertificateName <String>]`: A tanúsítvány-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-150">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="dbdf1-151">`[DeploymentName <String>]`: A telepítő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-151">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="dbdf1-152">`[DomainName <String>]`: Az egyéni tartomány-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-152">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="dbdf1-153">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="dbdf1-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dbdf1-154">`[Location <String>]`: a régió</span><span class="sxs-lookup"><span data-stu-id="dbdf1-154">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="dbdf1-155">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="dbdf1-156">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="dbdf1-157">`[ServiceName <String>]`: A szolgáltatás-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-157">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="dbdf1-158">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót kapja.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-158">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="dbdf1-159">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="dbdf1-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dbdf1-160">RELATED LINKS</span></span>

