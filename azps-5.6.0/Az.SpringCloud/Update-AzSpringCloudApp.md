---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/update-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
ms.openlocfilehash: 2ea144ec36830286919f9cb512ccec01008428a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005318"
---
# <span data-ttu-id="df57b-101">Update-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="df57b-101">Update-AzSpringCloudApp</span></span>

## <span data-ttu-id="df57b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df57b-102">SYNOPSIS</span></span>
<span data-ttu-id="df57b-103">A kilépő appok frissítésére való művelet.</span><span class="sxs-lookup"><span data-stu-id="df57b-103">Operation to update an exiting App.</span></span>

## <span data-ttu-id="df57b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="df57b-104">SYNTAX</span></span>

### <span data-ttu-id="df57b-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="df57b-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="df57b-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="df57b-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-ActiveDeploymentName <String>] [-Fqdn <String>]
 [-HttpsOnly] [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>]
 [-Public] [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="df57b-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="df57b-107">DESCRIPTION</span></span>
<span data-ttu-id="df57b-108">A kilépő appok frissítésére való művelet.</span><span class="sxs-lookup"><span data-stu-id="df57b-108">Operation to update an exiting App.</span></span>

## <span data-ttu-id="df57b-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="df57b-109">EXAMPLES</span></span>

### <span data-ttu-id="df57b-110">1. példa: A Spring Cloud app frissítése név szerint.</span><span class="sxs-lookup"><span data-stu-id="df57b-110">Example 1: Update Spring Cloud App by name.</span></span>
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

<span data-ttu-id="df57b-111">Frissítse a Spring Cloud appot név szerint.</span><span class="sxs-lookup"><span data-stu-id="df57b-111">Update Spring Cloud App by name.</span></span>

### <span data-ttu-id="df57b-112">2. példa: A Spring Cloud app frissítése a pipe-ból.</span><span class="sxs-lookup"><span data-stu-id="df57b-112">Example 2: Update Spring Cloud App from pipe.</span></span>
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

<span data-ttu-id="df57b-113">Frissítse a Spring Cloud appot a pipe-ból.</span><span class="sxs-lookup"><span data-stu-id="df57b-113">Update Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="df57b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df57b-114">PARAMETERS</span></span>

### <span data-ttu-id="df57b-115">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="df57b-115">-ActiveDeploymentName</span></span>
<span data-ttu-id="df57b-116">Az app aktív központi telepítésének neve</span><span class="sxs-lookup"><span data-stu-id="df57b-116">Name of the active deployment of the App</span></span>

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

### <span data-ttu-id="df57b-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="df57b-117">-AsJob</span></span>
<span data-ttu-id="df57b-118">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="df57b-118">Run the command as a job</span></span>

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

### <span data-ttu-id="df57b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df57b-119">-DefaultProfile</span></span>
<span data-ttu-id="df57b-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="df57b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df57b-121">-Fqdn</span><span class="sxs-lookup"><span data-stu-id="df57b-121">-Fqdn</span></span>
<span data-ttu-id="df57b-122">Teljesen minősített DNS-név.</span><span class="sxs-lookup"><span data-stu-id="df57b-122">Fully qualified dns Name.</span></span>

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

### <span data-ttu-id="df57b-123">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="df57b-123">-HttpsOnly</span></span>
<span data-ttu-id="df57b-124">Azt jelzi, hogy csak https engedélyezett-e.</span><span class="sxs-lookup"><span data-stu-id="df57b-124">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="df57b-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df57b-125">-InputObject</span></span>
<span data-ttu-id="df57b-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="df57b-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="df57b-127">-Location</span><span class="sxs-lookup"><span data-stu-id="df57b-127">-Location</span></span>
<span data-ttu-id="df57b-128">Az alkalmazás FÖLDRAJZI helye, mindig ugyanaz a szülőerőforrással</span><span class="sxs-lookup"><span data-stu-id="df57b-128">The GEO location of the application, always the same with its parent resource</span></span>

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

### <span data-ttu-id="df57b-129">-Name</span><span class="sxs-lookup"><span data-stu-id="df57b-129">-Name</span></span>
<span data-ttu-id="df57b-130">Az alkalmazáserőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="df57b-130">The name of the App resource.</span></span>

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

### <span data-ttu-id="df57b-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="df57b-131">-NoWait</span></span>
<span data-ttu-id="df57b-132">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="df57b-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="df57b-133">-PersistentDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="df57b-133">-PersistentDiskMountPath</span></span>
<span data-ttu-id="df57b-134">Az állandó lemez csatlakoztatási útvonala</span><span class="sxs-lookup"><span data-stu-id="df57b-134">Mount path of the persistent disk</span></span>

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

### <span data-ttu-id="df57b-135">-PersistentDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="df57b-135">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="df57b-136">Az állandó lemez mérete GB-ban</span><span class="sxs-lookup"><span data-stu-id="df57b-136">Size of the persistent disk in GB</span></span>

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

### <span data-ttu-id="df57b-137">-Public</span><span class="sxs-lookup"><span data-stu-id="df57b-137">-Public</span></span>
<span data-ttu-id="df57b-138">Azt jelzi, hogy az app elérhetővé teszi-e a nyilvános végpontot</span><span class="sxs-lookup"><span data-stu-id="df57b-138">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="df57b-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df57b-139">-ResourceGroupName</span></span>
<span data-ttu-id="df57b-140">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="df57b-140">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="df57b-141">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="df57b-141">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="df57b-142">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="df57b-142">-ServiceName</span></span>
<span data-ttu-id="df57b-143">A Szolgáltatás erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="df57b-143">The name of the Service resource.</span></span>

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

### <span data-ttu-id="df57b-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="df57b-144">-SubscriptionId</span></span>
<span data-ttu-id="df57b-145">Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="df57b-145">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="df57b-146">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="df57b-146">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="df57b-147">-TemporaryDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="df57b-147">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="df57b-148">Az ideiglenes lemez csatlakoztatási útvonala</span><span class="sxs-lookup"><span data-stu-id="df57b-148">Mount path of the temporary disk</span></span>

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

### <span data-ttu-id="df57b-149">-TemporaryDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="df57b-149">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="df57b-150">Az ideiglenes lemez mérete GB-ban</span><span class="sxs-lookup"><span data-stu-id="df57b-150">Size of the temporary disk in GB</span></span>

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

### <span data-ttu-id="df57b-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df57b-151">-Confirm</span></span>
<span data-ttu-id="df57b-152">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="df57b-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df57b-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df57b-153">-WhatIf</span></span>
<span data-ttu-id="df57b-154">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="df57b-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df57b-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="df57b-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df57b-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df57b-156">CommonParameters</span></span>
<span data-ttu-id="df57b-157">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df57b-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df57b-158">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df57b-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df57b-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="df57b-159">INPUTS</span></span>

### <span data-ttu-id="df57b-160">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="df57b-160">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="df57b-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df57b-161">OUTPUTS</span></span>

### <span data-ttu-id="df57b-162">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="df57b-162">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="df57b-163">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="df57b-163">NOTES</span></span>

<span data-ttu-id="df57b-164">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="df57b-164">ALIASES</span></span>

<span data-ttu-id="df57b-165">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="df57b-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="df57b-166">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="df57b-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="df57b-167">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="df57b-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="df57b-168">INPUTOBJECT: <ISpringCloudIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="df57b-168">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="df57b-169">`[AppName <String>]`: Az apperőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="df57b-169">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="df57b-170">`[BindingName <String>]`: A Kötés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="df57b-170">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="df57b-171">`[CertificateName <String>]`: A tanúsítványforrás neve.</span><span class="sxs-lookup"><span data-stu-id="df57b-171">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="df57b-172">`[DeploymentName <String>]`: A Központi telepítés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="df57b-172">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="df57b-173">`[DomainName <String>]`: Az egyéni tartományerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="df57b-173">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="df57b-174">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="df57b-174">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="df57b-175">`[Location <String>]`: a régió</span><span class="sxs-lookup"><span data-stu-id="df57b-175">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="df57b-176">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="df57b-176">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="df57b-177">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="df57b-177">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="df57b-178">`[ServiceName <String>]`: A Szolgáltatás erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="df57b-178">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="df57b-179">`[SubscriptionId <String>]`: Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="df57b-179">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="df57b-180">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="df57b-180">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="df57b-181">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df57b-181">RELATED LINKS</span></span>

