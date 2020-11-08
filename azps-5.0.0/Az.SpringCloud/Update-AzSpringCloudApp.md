---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/update-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
ms.openlocfilehash: f8da3fe762abc3f281a8a06dd365cd0271eb0ac9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185224"
---
# <span data-ttu-id="472ab-101">Update-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="472ab-101">Update-AzSpringCloudApp</span></span>

## <span data-ttu-id="472ab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="472ab-102">SYNOPSIS</span></span>
<span data-ttu-id="472ab-103">Művelet a kilépés app frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="472ab-103">Operation to update an exiting App.</span></span>

## <span data-ttu-id="472ab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="472ab-104">SYNTAX</span></span>

### <span data-ttu-id="472ab-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="472ab-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="472ab-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="472ab-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-ActiveDeploymentName <String>] [-Fqdn <String>]
 [-HttpsOnly] [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>]
 [-Public] [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="472ab-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="472ab-107">DESCRIPTION</span></span>
<span data-ttu-id="472ab-108">Művelet a kilépés app frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="472ab-108">Operation to update an exiting App.</span></span>

## <span data-ttu-id="472ab-109">Példák</span><span class="sxs-lookup"><span data-stu-id="472ab-109">EXAMPLES</span></span>

### <span data-ttu-id="472ab-110">1. példa: a tavaszi felhő alkalmazás frissítése név szerint.</span><span class="sxs-lookup"><span data-stu-id="472ab-110">Example 1: Update Spring Cloud App by name.</span></span>
```powershell
PS C:\> Update-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -ActiveDeploymentName default
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

<span data-ttu-id="472ab-111">Frissítse a tavaszi felhő alkalmazást név szerint.</span><span class="sxs-lookup"><span data-stu-id="472ab-111">Update Spring Cloud App by name.</span></span>

### <span data-ttu-id="472ab-112">2. példa: a tavaszi felhő alkalmazás frissítése a pipe-ról</span><span class="sxs-lookup"><span data-stu-id="472ab-112">Example 2: Update Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Update-AzSpringCloudApp -ActiveDeploymentName default
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

<span data-ttu-id="472ab-113">A tavaszi felhő alkalmazás frissítése a pipe-ról</span><span class="sxs-lookup"><span data-stu-id="472ab-113">Update Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="472ab-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="472ab-114">PARAMETERS</span></span>

### <span data-ttu-id="472ab-115">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="472ab-115">-ActiveDeploymentName</span></span>
<span data-ttu-id="472ab-116">Az alkalmazás aktív bevezetésének neve</span><span class="sxs-lookup"><span data-stu-id="472ab-116">Name of the active deployment of the App</span></span>

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

### <span data-ttu-id="472ab-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="472ab-117">-AsJob</span></span>
<span data-ttu-id="472ab-118">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="472ab-118">Run the command as a job</span></span>

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

### <span data-ttu-id="472ab-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="472ab-119">-DefaultProfile</span></span>
<span data-ttu-id="472ab-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="472ab-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="472ab-121">-FQDN</span><span class="sxs-lookup"><span data-stu-id="472ab-121">-Fqdn</span></span>
<span data-ttu-id="472ab-122">Teljesen minősített DNS-név.</span><span class="sxs-lookup"><span data-stu-id="472ab-122">Fully qualified dns Name.</span></span>

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

### <span data-ttu-id="472ab-123">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="472ab-123">-HttpsOnly</span></span>
<span data-ttu-id="472ab-124">Annak jelzése, hogy csak HTTPS engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="472ab-124">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="472ab-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="472ab-125">-InputObject</span></span>
<span data-ttu-id="472ab-126">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="472ab-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="472ab-127">-Hely</span><span class="sxs-lookup"><span data-stu-id="472ab-127">-Location</span></span>
<span data-ttu-id="472ab-128">Az alkalmazás földrajzi helye mindig ugyanaz, mint a szülő-erőforrás</span><span class="sxs-lookup"><span data-stu-id="472ab-128">The GEO location of the application, always the same with its parent resource</span></span>

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

### <span data-ttu-id="472ab-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="472ab-129">-Name</span></span>
<span data-ttu-id="472ab-130">Az App-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="472ab-130">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="472ab-131">-Várva</span><span class="sxs-lookup"><span data-stu-id="472ab-131">-NoWait</span></span>
<span data-ttu-id="472ab-132">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="472ab-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="472ab-133">-PersistentDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="472ab-133">-PersistentDiskMountPath</span></span>
<span data-ttu-id="472ab-134">Az állandó lemez csatlakoztatási útja</span><span class="sxs-lookup"><span data-stu-id="472ab-134">Mount path of the persistent disk</span></span>

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

### <span data-ttu-id="472ab-135">-PersistentDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="472ab-135">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="472ab-136">Az állandó lemez mérete GB-ban</span><span class="sxs-lookup"><span data-stu-id="472ab-136">Size of the persistent disk in GB</span></span>

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

### <span data-ttu-id="472ab-137">– Nyilvános</span><span class="sxs-lookup"><span data-stu-id="472ab-137">-Public</span></span>
<span data-ttu-id="472ab-138">Azt jelzi, hogy az alkalmazás kiteszi-e a nyilvános végpontot</span><span class="sxs-lookup"><span data-stu-id="472ab-138">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="472ab-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="472ab-139">-ResourceGroupName</span></span>
<span data-ttu-id="472ab-140">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="472ab-140">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="472ab-141">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="472ab-141">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="472ab-142">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="472ab-142">-ServiceName</span></span>
<span data-ttu-id="472ab-143">A szolgáltatás erőforrásának neve.</span><span class="sxs-lookup"><span data-stu-id="472ab-143">The name of the Service resource.</span></span>

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

### <span data-ttu-id="472ab-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="472ab-144">-SubscriptionId</span></span>
<span data-ttu-id="472ab-145">Megkapja az előfizetés AZONOSÍTÓját, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="472ab-145">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="472ab-146">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="472ab-146">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="472ab-147">-TemporaryDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="472ab-147">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="472ab-148">Az ideiglenes lemez csatlakoztatási útvonala</span><span class="sxs-lookup"><span data-stu-id="472ab-148">Mount path of the temporary disk</span></span>

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

### <span data-ttu-id="472ab-149">-TemporaryDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="472ab-149">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="472ab-150">Az ideiglenes lemez mérete GB-ban</span><span class="sxs-lookup"><span data-stu-id="472ab-150">Size of the temporary disk in GB</span></span>

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

### <span data-ttu-id="472ab-151">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="472ab-151">-Confirm</span></span>
<span data-ttu-id="472ab-152">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="472ab-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="472ab-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="472ab-153">-WhatIf</span></span>
<span data-ttu-id="472ab-154">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="472ab-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="472ab-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="472ab-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="472ab-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="472ab-156">CommonParameters</span></span>
<span data-ttu-id="472ab-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="472ab-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="472ab-158">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="472ab-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="472ab-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="472ab-159">INPUTS</span></span>

### <span data-ttu-id="472ab-160">Microsoft. Azure. PowerShell. parancsmagok. SpringCloud. models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="472ab-160">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="472ab-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="472ab-161">OUTPUTS</span></span>

### <span data-ttu-id="472ab-162">Microsoft. Azure. PowerShell. parancsmagok. SpringCloud. modellek. Api20200701. IAppResource</span><span class="sxs-lookup"><span data-stu-id="472ab-162">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="472ab-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="472ab-163">NOTES</span></span>

<span data-ttu-id="472ab-164">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="472ab-164">ALIASES</span></span>

<span data-ttu-id="472ab-165">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="472ab-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="472ab-166">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="472ab-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="472ab-167">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="472ab-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="472ab-168">INPUTOBJECT <ISpringCloudIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="472ab-168">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="472ab-169">`[AppName <String>]`: Az App-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="472ab-169">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="472ab-170">`[BindingName <String>]`: A kötési erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="472ab-170">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="472ab-171">`[CertificateName <String>]`: A tanúsítvány-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="472ab-171">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="472ab-172">`[DeploymentName <String>]`: A telepítő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="472ab-172">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="472ab-173">`[DomainName <String>]`: Az egyéni tartomány-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="472ab-173">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="472ab-174">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="472ab-174">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="472ab-175">`[Location <String>]`: a régió</span><span class="sxs-lookup"><span data-stu-id="472ab-175">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="472ab-176">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="472ab-176">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="472ab-177">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="472ab-177">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="472ab-178">`[ServiceName <String>]`: A szolgáltatás-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="472ab-178">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="472ab-179">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót kapja.</span><span class="sxs-lookup"><span data-stu-id="472ab-179">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="472ab-180">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="472ab-180">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="472ab-181">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="472ab-181">RELATED LINKS</span></span>

