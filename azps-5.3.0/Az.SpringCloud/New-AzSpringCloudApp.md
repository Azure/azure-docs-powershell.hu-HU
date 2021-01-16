---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/new-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudApp.md
ms.openlocfilehash: c8f723a66ee388244f2aab9ab556ea315f44e72c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479501"
---
# <span data-ttu-id="f26b8-101">New-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="f26b8-101">New-AzSpringCloudApp</span></span>

## <span data-ttu-id="f26b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f26b8-102">SYNOPSIS</span></span>
<span data-ttu-id="f26b8-103">Hozzon létre egy új alkalmazást, vagy frissítsen egy kilépő alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="f26b8-103">Create a new App or update an exiting App.</span></span>

## <span data-ttu-id="f26b8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f26b8-104">SYNTAX</span></span>

```
New-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f26b8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f26b8-105">DESCRIPTION</span></span>
<span data-ttu-id="f26b8-106">Hozzon létre egy új alkalmazást, vagy frissítsen egy kilépő alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="f26b8-106">Create a new App or update an exiting App.</span></span>

## <span data-ttu-id="f26b8-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f26b8-107">EXAMPLES</span></span>

### <span data-ttu-id="f26b8-108">1. példa: Tavaszi felhőalkalmazás létrehozása.</span><span class="sxs-lookup"><span data-stu-id="f26b8-108">Example 1: Create a spring cloud app.</span></span>
```powershell
PS C:\> New-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
ActiveDeploymentName    :
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

<span data-ttu-id="f26b8-109">Létrehozhat egy tavaszi felhőalkalmazást.</span><span class="sxs-lookup"><span data-stu-id="f26b8-109">Create a spring cloud app.</span></span>

## <span data-ttu-id="f26b8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f26b8-110">PARAMETERS</span></span>

### <span data-ttu-id="f26b8-111">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="f26b8-111">-ActiveDeploymentName</span></span>
<span data-ttu-id="f26b8-112">Az app aktív központi telepítésének neve</span><span class="sxs-lookup"><span data-stu-id="f26b8-112">Name of the active deployment of the App</span></span>

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

### <span data-ttu-id="f26b8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f26b8-113">-AsJob</span></span>
<span data-ttu-id="f26b8-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="f26b8-114">Run the command as a job</span></span>

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

### <span data-ttu-id="f26b8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f26b8-115">-DefaultProfile</span></span>
<span data-ttu-id="f26b8-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f26b8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f26b8-117">-Fqdn</span><span class="sxs-lookup"><span data-stu-id="f26b8-117">-Fqdn</span></span>
<span data-ttu-id="f26b8-118">Teljesen minősített DNS-név.</span><span class="sxs-lookup"><span data-stu-id="f26b8-118">Fully qualified dns Name.</span></span>

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

### <span data-ttu-id="f26b8-119">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="f26b8-119">-HttpsOnly</span></span>
<span data-ttu-id="f26b8-120">Azt jelzi, hogy csak https engedélyezett-e.</span><span class="sxs-lookup"><span data-stu-id="f26b8-120">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="f26b8-121">-Location</span><span class="sxs-lookup"><span data-stu-id="f26b8-121">-Location</span></span>
<span data-ttu-id="f26b8-122">Az alkalmazás FÖLDRAJZI helye, mindig ugyanaz a szülőerőforrással</span><span class="sxs-lookup"><span data-stu-id="f26b8-122">The GEO location of the application, always the same with its parent resource</span></span>

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

### <span data-ttu-id="f26b8-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f26b8-123">-Name</span></span>
<span data-ttu-id="f26b8-124">Az alkalmazáserőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f26b8-124">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f26b8-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f26b8-125">-NoWait</span></span>
<span data-ttu-id="f26b8-126">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="f26b8-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f26b8-127">-PersistentDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="f26b8-127">-PersistentDiskMountPath</span></span>
<span data-ttu-id="f26b8-128">Az állandó lemez csatlakoztatási útvonala</span><span class="sxs-lookup"><span data-stu-id="f26b8-128">Mount path of the persistent disk</span></span>

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

### <span data-ttu-id="f26b8-129">-PersistentDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="f26b8-129">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="f26b8-130">Az állandó lemez mérete GB-ban</span><span class="sxs-lookup"><span data-stu-id="f26b8-130">Size of the persistent disk in GB</span></span>

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

### <span data-ttu-id="f26b8-131">-Public</span><span class="sxs-lookup"><span data-stu-id="f26b8-131">-Public</span></span>
<span data-ttu-id="f26b8-132">Azt jelzi, hogy az app elérhetővé teszi-e a nyilvános végpontot</span><span class="sxs-lookup"><span data-stu-id="f26b8-132">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="f26b8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f26b8-133">-ResourceGroupName</span></span>
<span data-ttu-id="f26b8-134">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f26b8-134">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="f26b8-135">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="f26b8-135">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="f26b8-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f26b8-136">-ServiceName</span></span>
<span data-ttu-id="f26b8-137">A Szolgáltatás erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f26b8-137">The name of the Service resource.</span></span>

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

### <span data-ttu-id="f26b8-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f26b8-138">-SubscriptionId</span></span>
<span data-ttu-id="f26b8-139">Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="f26b8-139">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="f26b8-140">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="f26b8-140">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f26b8-141">-TemporaryDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="f26b8-141">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="f26b8-142">Az ideiglenes lemez csatlakoztatási útvonala</span><span class="sxs-lookup"><span data-stu-id="f26b8-142">Mount path of the temporary disk</span></span>

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

### <span data-ttu-id="f26b8-143">-TemporaryDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="f26b8-143">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="f26b8-144">Az ideiglenes lemez mérete GB-ban</span><span class="sxs-lookup"><span data-stu-id="f26b8-144">Size of the temporary disk in GB</span></span>

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

### <span data-ttu-id="f26b8-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f26b8-145">-Confirm</span></span>
<span data-ttu-id="f26b8-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f26b8-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f26b8-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f26b8-147">-WhatIf</span></span>
<span data-ttu-id="f26b8-148">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f26b8-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f26b8-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f26b8-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f26b8-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f26b8-150">CommonParameters</span></span>
<span data-ttu-id="f26b8-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f26b8-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f26b8-152">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f26b8-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f26b8-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f26b8-153">INPUTS</span></span>

## <span data-ttu-id="f26b8-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f26b8-154">OUTPUTS</span></span>

### <span data-ttu-id="f26b8-155">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="f26b8-155">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="f26b8-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f26b8-156">NOTES</span></span>

<span data-ttu-id="f26b8-157">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f26b8-157">ALIASES</span></span>

## <span data-ttu-id="f26b8-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f26b8-158">RELATED LINKS</span></span>

