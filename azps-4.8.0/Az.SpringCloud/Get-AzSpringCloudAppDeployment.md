---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
ms.openlocfilehash: d33f649d71a8fb3f4a112ac77937f37d867a24c4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183942"
---
# <span data-ttu-id="1913b-101">Get-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="1913b-101">Get-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="1913b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1913b-102">SYNOPSIS</span></span>
<span data-ttu-id="1913b-103">Üzembe állítás és a hozzájuk tartozó tulajdonságok beszerzése</span><span class="sxs-lookup"><span data-stu-id="1913b-103">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="1913b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1913b-104">SYNTAX</span></span>

### <span data-ttu-id="1913b-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1913b-105">List (Default)</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1913b-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="1913b-106">Get</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1913b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1913b-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="1913b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1913b-108">DESCRIPTION</span></span>
<span data-ttu-id="1913b-109">Üzembe állítás és a hozzájuk tartozó tulajdonságok beszerzése</span><span class="sxs-lookup"><span data-stu-id="1913b-109">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="1913b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1913b-110">EXAMPLES</span></span>

### <span data-ttu-id="1913b-111">1. példa: a tavaszi felhő alkalmazás Deploymeng név szerint.</span><span class="sxs-lookup"><span data-stu-id="1913b-111">Example 1: Get Spring Cloud App Deploymeng by name.</span></span>
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

<span data-ttu-id="1913b-112">A tavaszi felhő alkalmazás Deploymeng név szerint.</span><span class="sxs-lookup"><span data-stu-id="1913b-112">Get Spring Cloud App Deploymeng by name.</span></span>

### <span data-ttu-id="1913b-113">2. példa: az adott tavaszi felhő alkalmazásban az összes bevezetést felsorolhatja.</span><span class="sxs-lookup"><span data-stu-id="1913b-113">Example 2: List all the deployment under a given spring cloud app.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
Name    Type
----    ----
default Microsoft.AppPlatform/Spring/apps/deployments
prod    Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="1913b-114">Az összes bevezetést felsorolhatja egy adott tavaszi felhő alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="1913b-114">List all the deployment under a given spring cloud app.</span></span>

## <span data-ttu-id="1913b-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1913b-115">PARAMETERS</span></span>

### <span data-ttu-id="1913b-116">-Appnév</span><span class="sxs-lookup"><span data-stu-id="1913b-116">-AppName</span></span>
<span data-ttu-id="1913b-117">Az App-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="1913b-117">The name of the App resource.</span></span>

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

### <span data-ttu-id="1913b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1913b-118">-DefaultProfile</span></span>
<span data-ttu-id="1913b-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1913b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1913b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1913b-120">-InputObject</span></span>
<span data-ttu-id="1913b-121">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1913b-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1913b-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1913b-122">-Name</span></span>
<span data-ttu-id="1913b-123">A központi telepítő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="1913b-123">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="1913b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1913b-124">-ResourceGroupName</span></span>
<span data-ttu-id="1913b-125">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1913b-125">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="1913b-126">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="1913b-126">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="1913b-127">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="1913b-127">-ServiceName</span></span>
<span data-ttu-id="1913b-128">A szolgáltatás erőforrásának neve.</span><span class="sxs-lookup"><span data-stu-id="1913b-128">The name of the Service resource.</span></span>

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

### <span data-ttu-id="1913b-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1913b-129">-SubscriptionId</span></span>
<span data-ttu-id="1913b-130">Megkapja az előfizetés AZONOSÍTÓját, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="1913b-130">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="1913b-131">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="1913b-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1913b-132">-Verzió</span><span class="sxs-lookup"><span data-stu-id="1913b-132">-Version</span></span>
<span data-ttu-id="1913b-133">A listázni kívánt telepített példányok verziója</span><span class="sxs-lookup"><span data-stu-id="1913b-133">Version of the deployments to be listed</span></span>

```yaml
Type: System.String[]
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1913b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1913b-134">CommonParameters</span></span>
<span data-ttu-id="1913b-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1913b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1913b-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1913b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1913b-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1913b-137">INPUTS</span></span>

### <span data-ttu-id="1913b-138">Microsoft. Azure. PowerShell. parancsmagok. SpringCloud. models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="1913b-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="1913b-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1913b-139">OUTPUTS</span></span>

### <span data-ttu-id="1913b-140">Microsoft. Azure. PowerShell. parancsmagok. SpringCloud. modellek. Api20190501Preview. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="1913b-140">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IDeploymentResource</span></span>

## <span data-ttu-id="1913b-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1913b-141">NOTES</span></span>

<span data-ttu-id="1913b-142">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="1913b-142">ALIASES</span></span>

<span data-ttu-id="1913b-143">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="1913b-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1913b-144">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="1913b-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1913b-145">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="1913b-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1913b-146">INPUTOBJECT <ISpringCloudIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="1913b-146">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1913b-147">`[AppName <String>]`: Az App-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="1913b-147">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="1913b-148">`[BindingName <String>]`: A kötési erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="1913b-148">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="1913b-149">`[CertificateName <String>]`: A tanúsítvány-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="1913b-149">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="1913b-150">`[DeploymentName <String>]`: A telepítő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="1913b-150">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="1913b-151">`[DomainName <String>]`: Az egyéni tartomány-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="1913b-151">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="1913b-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="1913b-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1913b-153">`[Location <String>]`: a régió</span><span class="sxs-lookup"><span data-stu-id="1913b-153">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="1913b-154">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1913b-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="1913b-155">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="1913b-155">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="1913b-156">`[ServiceName <String>]`: A szolgáltatás-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="1913b-156">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="1913b-157">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót kapja.</span><span class="sxs-lookup"><span data-stu-id="1913b-157">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="1913b-158">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="1913b-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1913b-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1913b-159">RELATED LINKS</span></span>

