---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
ms.openlocfilehash: 43001ca921344d334f91bfa7b594e733a3307d8d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185242"
---
# <span data-ttu-id="6e38b-101">Get-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="6e38b-101">Get-AzSpringCloudApp</span></span>

## <span data-ttu-id="6e38b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6e38b-102">SYNOPSIS</span></span>
<span data-ttu-id="6e38b-103">Az alkalmazások és a tulajdonságaik beszerzése</span><span class="sxs-lookup"><span data-stu-id="6e38b-103">Get an App and its properties.</span></span>

## <span data-ttu-id="6e38b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6e38b-104">SYNTAX</span></span>

### <span data-ttu-id="6e38b-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6e38b-105">List (Default)</span></span>
```
Get-AzSpringCloudApp -ResourceGroupName <String> -ServiceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6e38b-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="6e38b-106">Get</span></span>
```
Get-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-SyncStatus <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6e38b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6e38b-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-SyncStatus <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="6e38b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6e38b-108">DESCRIPTION</span></span>
<span data-ttu-id="6e38b-109">Az alkalmazások és a tulajdonságaik beszerzése</span><span class="sxs-lookup"><span data-stu-id="6e38b-109">Get an App and its properties.</span></span>

## <span data-ttu-id="6e38b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6e38b-110">EXAMPLES</span></span>

### <span data-ttu-id="6e38b-111">Példa 1: a tavaszi felhő alkalmazás beolvasása név szerint.</span><span class="sxs-lookup"><span data-stu-id="6e38b-111">Example 1: Get Spring Cloud App by name.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
ActiveDeploymentName    : default
CreatedTime             : 2020-08-08 15:37:43
Fqdn                    : spring-cloud-service.azuremicroservices.io
HttpsOnly               : False
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway
IdentityPrincipalId     :
IdentityTenantId        :
IdentityType            :
Location                : eastus
Name                    : gateway
PersistentDiskMountPath : /persistent
PersistentDiskSizeInGb  : 0
PersistentDiskUsedInGb  :
ProvisioningState       : Succeeded
Public                  : False
TemporaryDiskMountPath  : /tmp
TemporaryDiskSizeInGb   : 5
Type                    : Microsoft.AppPlatform/Spring/apps
Url                     :
Identity                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ManagedIdentityProperties
PersistentDisk          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.PersistentDisk
Property                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.AppResourceProperties
TemporaryDisk           : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TemporaryDisk
```

<span data-ttu-id="6e38b-112">A tavaszi felhő alkalmazás beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="6e38b-112">Get Spring Cloud App by name.</span></span>

### <span data-ttu-id="6e38b-113">2. példa: az összes app listázása az adott tavaszi Felhőbeli szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="6e38b-113">Example 2: List all the app under a given spring cloud service.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
Name            Type                              Location
----            ----                              --------
account-service Microsoft.AppPlatform/Spring/apps eastus
auth-service    Microsoft.AppPlatform/Spring/apps eastus
gateway         Microsoft.AppPlatform/Spring/apps eastus
```

<span data-ttu-id="6e38b-114">Az összes app listázása az adott tavaszi Felhőbeli szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="6e38b-114">List all the app under a given spring cloud service.</span></span>

## <span data-ttu-id="6e38b-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6e38b-115">PARAMETERS</span></span>

### <span data-ttu-id="6e38b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e38b-116">-DefaultProfile</span></span>
<span data-ttu-id="6e38b-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6e38b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e38b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e38b-118">-InputObject</span></span>
<span data-ttu-id="6e38b-119">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6e38b-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6e38b-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6e38b-120">-Name</span></span>
<span data-ttu-id="6e38b-121">Az App-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="6e38b-121">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e38b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e38b-122">-ResourceGroupName</span></span>
<span data-ttu-id="6e38b-123">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6e38b-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="6e38b-124">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="6e38b-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="6e38b-125">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="6e38b-125">-ServiceName</span></span>
<span data-ttu-id="6e38b-126">A szolgáltatás erőforrásának neve.</span><span class="sxs-lookup"><span data-stu-id="6e38b-126">The name of the Service resource.</span></span>

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

### <span data-ttu-id="6e38b-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6e38b-127">-SubscriptionId</span></span>
<span data-ttu-id="6e38b-128">Megkapja az előfizetés AZONOSÍTÓját, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="6e38b-128">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="6e38b-129">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="6e38b-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6e38b-130">-SyncStatus</span><span class="sxs-lookup"><span data-stu-id="6e38b-130">-SyncStatus</span></span>
<span data-ttu-id="6e38b-131">Azt jelzi, hogy a szinkronizálás állapota</span><span class="sxs-lookup"><span data-stu-id="6e38b-131">Indicates whether sync status</span></span>

```yaml
Type: System.String
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e38b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e38b-132">CommonParameters</span></span>
<span data-ttu-id="6e38b-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6e38b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e38b-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6e38b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e38b-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e38b-135">INPUTS</span></span>

### <span data-ttu-id="6e38b-136">Microsoft. Azure. PowerShell. parancsmagok. SpringCloud. models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="6e38b-136">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="6e38b-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e38b-137">OUTPUTS</span></span>

### <span data-ttu-id="6e38b-138">Microsoft. Azure. PowerShell. parancsmagok. SpringCloud. modellek. Api20200701. IAppResource</span><span class="sxs-lookup"><span data-stu-id="6e38b-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="6e38b-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6e38b-139">NOTES</span></span>

<span data-ttu-id="6e38b-140">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6e38b-140">ALIASES</span></span>

<span data-ttu-id="6e38b-141">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="6e38b-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6e38b-142">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="6e38b-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6e38b-143">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="6e38b-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6e38b-144">INPUTOBJECT <ISpringCloudIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="6e38b-144">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6e38b-145">`[AppName <String>]`: Az App-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="6e38b-145">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="6e38b-146">`[BindingName <String>]`: A kötési erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="6e38b-146">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="6e38b-147">`[CertificateName <String>]`: A tanúsítvány-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="6e38b-147">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="6e38b-148">`[DeploymentName <String>]`: A telepítő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="6e38b-148">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="6e38b-149">`[DomainName <String>]`: Az egyéni tartomány-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="6e38b-149">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="6e38b-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="6e38b-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6e38b-151">`[Location <String>]`: a régió</span><span class="sxs-lookup"><span data-stu-id="6e38b-151">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="6e38b-152">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6e38b-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="6e38b-153">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="6e38b-153">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="6e38b-154">`[ServiceName <String>]`: A szolgáltatás-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="6e38b-154">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="6e38b-155">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót kapja.</span><span class="sxs-lookup"><span data-stu-id="6e38b-155">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="6e38b-156">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="6e38b-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="6e38b-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e38b-157">RELATED LINKS</span></span>

