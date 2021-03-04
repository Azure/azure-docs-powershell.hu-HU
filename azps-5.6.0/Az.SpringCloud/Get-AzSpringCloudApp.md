---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/get-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
ms.openlocfilehash: 62a0398ca117ac623d0b21cc89908b25a4e7e1e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920273"
---
# <span data-ttu-id="11cdb-101">Get-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="11cdb-101">Get-AzSpringCloudApp</span></span>

## <span data-ttu-id="11cdb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11cdb-102">SYNOPSIS</span></span>
<span data-ttu-id="11cdb-103">Alkalmazás és tulajdonságainak lekérte.</span><span class="sxs-lookup"><span data-stu-id="11cdb-103">Get an App and its properties.</span></span>

## <span data-ttu-id="11cdb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="11cdb-104">SYNTAX</span></span>

### <span data-ttu-id="11cdb-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="11cdb-105">List (Default)</span></span>
```
Get-AzSpringCloudApp -ResourceGroupName <String> -ServiceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="11cdb-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="11cdb-106">Get</span></span>
```
Get-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-SyncStatus <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="11cdb-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="11cdb-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-SyncStatus <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="11cdb-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="11cdb-108">DESCRIPTION</span></span>
<span data-ttu-id="11cdb-109">Alkalmazás és tulajdonságainak lekérte.</span><span class="sxs-lookup"><span data-stu-id="11cdb-109">Get an App and its properties.</span></span>

## <span data-ttu-id="11cdb-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="11cdb-110">EXAMPLES</span></span>

### <span data-ttu-id="11cdb-111">1. példa: A Spring Cloud app letöltése név szerint.</span><span class="sxs-lookup"><span data-stu-id="11cdb-111">Example 1: Get Spring Cloud App by name.</span></span>
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

<span data-ttu-id="11cdb-112">Szerezze be a Spring Cloud appot név szerint.</span><span class="sxs-lookup"><span data-stu-id="11cdb-112">Get Spring Cloud App by name.</span></span>

### <span data-ttu-id="11cdb-113">2. példa: Az összes app felsorolása egy adott tavaszi felhőszolgáltatás alá.</span><span class="sxs-lookup"><span data-stu-id="11cdb-113">Example 2: List all the app under a given spring cloud service.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
Name            Type                              Location
----            ----                              --------
account-service Microsoft.AppPlatform/Spring/apps eastus
auth-service    Microsoft.AppPlatform/Spring/apps eastus
gateway         Microsoft.AppPlatform/Spring/apps eastus
```

<span data-ttu-id="11cdb-114">List all the app under a given spring cloud service.</span><span class="sxs-lookup"><span data-stu-id="11cdb-114">List all the app under a given spring cloud service.</span></span>

## <span data-ttu-id="11cdb-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11cdb-115">PARAMETERS</span></span>

### <span data-ttu-id="11cdb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11cdb-116">-DefaultProfile</span></span>
<span data-ttu-id="11cdb-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="11cdb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11cdb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11cdb-118">-InputObject</span></span>
<span data-ttu-id="11cdb-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="11cdb-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="11cdb-120">-Name</span><span class="sxs-lookup"><span data-stu-id="11cdb-120">-Name</span></span>
<span data-ttu-id="11cdb-121">Az alkalmazáserőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="11cdb-121">The name of the App resource.</span></span>

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

### <span data-ttu-id="11cdb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11cdb-122">-ResourceGroupName</span></span>
<span data-ttu-id="11cdb-123">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="11cdb-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="11cdb-124">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="11cdb-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="11cdb-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="11cdb-125">-ServiceName</span></span>
<span data-ttu-id="11cdb-126">A Szolgáltatás erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="11cdb-126">The name of the Service resource.</span></span>

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

### <span data-ttu-id="11cdb-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="11cdb-127">-SubscriptionId</span></span>
<span data-ttu-id="11cdb-128">Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="11cdb-128">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="11cdb-129">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="11cdb-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="11cdb-130">-SyncStatus</span><span class="sxs-lookup"><span data-stu-id="11cdb-130">-SyncStatus</span></span>
<span data-ttu-id="11cdb-131">Azt jelzi, hogy a szinkronizálás állapota</span><span class="sxs-lookup"><span data-stu-id="11cdb-131">Indicates whether sync status</span></span>

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

### <span data-ttu-id="11cdb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11cdb-132">CommonParameters</span></span>
<span data-ttu-id="11cdb-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11cdb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11cdb-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11cdb-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11cdb-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11cdb-135">INPUTS</span></span>

### <span data-ttu-id="11cdb-136">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="11cdb-136">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="11cdb-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11cdb-137">OUTPUTS</span></span>

### <span data-ttu-id="11cdb-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="11cdb-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="11cdb-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="11cdb-139">NOTES</span></span>

<span data-ttu-id="11cdb-140">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="11cdb-140">ALIASES</span></span>

<span data-ttu-id="11cdb-141">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="11cdb-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="11cdb-142">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="11cdb-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="11cdb-143">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="11cdb-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="11cdb-144">INPUTOBJECT: <ISpringCloudIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="11cdb-144">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="11cdb-145">`[AppName <String>]`: Az apperőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="11cdb-145">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="11cdb-146">`[BindingName <String>]`: A Kötés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="11cdb-146">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="11cdb-147">`[CertificateName <String>]`: A tanúsítványforrás neve.</span><span class="sxs-lookup"><span data-stu-id="11cdb-147">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="11cdb-148">`[DeploymentName <String>]`: A Központi telepítés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="11cdb-148">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="11cdb-149">`[DomainName <String>]`: Az egyéni tartományerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="11cdb-149">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="11cdb-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="11cdb-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="11cdb-151">`[Location <String>]`: a régió</span><span class="sxs-lookup"><span data-stu-id="11cdb-151">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="11cdb-152">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="11cdb-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="11cdb-153">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="11cdb-153">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="11cdb-154">`[ServiceName <String>]`: A Szolgáltatás erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="11cdb-154">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="11cdb-155">`[SubscriptionId <String>]`: Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="11cdb-155">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="11cdb-156">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="11cdb-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="11cdb-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11cdb-157">RELATED LINKS</span></span>

