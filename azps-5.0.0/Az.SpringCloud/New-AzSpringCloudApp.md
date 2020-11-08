---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/new-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudApp.md
ms.openlocfilehash: c8f723a66ee388244f2aab9ab556ea315f44e72c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185237"
---
# <span data-ttu-id="30e90-101">New-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="30e90-101">New-AzSpringCloudApp</span></span>

## <span data-ttu-id="30e90-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="30e90-102">SYNOPSIS</span></span>
<span data-ttu-id="30e90-103">Hozzon létre egy új alkalmazást, vagy frissítse a kilépés alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="30e90-103">Create a new App or update an exiting App.</span></span>

## <span data-ttu-id="30e90-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="30e90-104">SYNTAX</span></span>

```
New-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="30e90-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="30e90-105">DESCRIPTION</span></span>
<span data-ttu-id="30e90-106">Hozzon létre egy új alkalmazást, vagy frissítse a kilépés alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="30e90-106">Create a new App or update an exiting App.</span></span>

## <span data-ttu-id="30e90-107">Példák</span><span class="sxs-lookup"><span data-stu-id="30e90-107">EXAMPLES</span></span>

### <span data-ttu-id="30e90-108">1. példa: a tavaszi felhő alkalmazás létrehozása</span><span class="sxs-lookup"><span data-stu-id="30e90-108">Example 1: Create a spring cloud app.</span></span>
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

<span data-ttu-id="30e90-109">A tavaszi felhő alkalmazás létrehozása</span><span class="sxs-lookup"><span data-stu-id="30e90-109">Create a spring cloud app.</span></span>

## <span data-ttu-id="30e90-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="30e90-110">PARAMETERS</span></span>

### <span data-ttu-id="30e90-111">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="30e90-111">-ActiveDeploymentName</span></span>
<span data-ttu-id="30e90-112">Az alkalmazás aktív bevezetésének neve</span><span class="sxs-lookup"><span data-stu-id="30e90-112">Name of the active deployment of the App</span></span>

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

### <span data-ttu-id="30e90-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30e90-113">-AsJob</span></span>
<span data-ttu-id="30e90-114">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="30e90-114">Run the command as a job</span></span>

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

### <span data-ttu-id="30e90-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30e90-115">-DefaultProfile</span></span>
<span data-ttu-id="30e90-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="30e90-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30e90-117">-FQDN</span><span class="sxs-lookup"><span data-stu-id="30e90-117">-Fqdn</span></span>
<span data-ttu-id="30e90-118">Teljesen minősített DNS-név.</span><span class="sxs-lookup"><span data-stu-id="30e90-118">Fully qualified dns Name.</span></span>

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

### <span data-ttu-id="30e90-119">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="30e90-119">-HttpsOnly</span></span>
<span data-ttu-id="30e90-120">Annak jelzése, hogy csak HTTPS engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="30e90-120">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="30e90-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="30e90-121">-Location</span></span>
<span data-ttu-id="30e90-122">Az alkalmazás földrajzi helye mindig ugyanaz, mint a szülő-erőforrás</span><span class="sxs-lookup"><span data-stu-id="30e90-122">The GEO location of the application, always the same with its parent resource</span></span>

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

### <span data-ttu-id="30e90-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="30e90-123">-Name</span></span>
<span data-ttu-id="30e90-124">Az App-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="30e90-124">The name of the App resource.</span></span>

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

### <span data-ttu-id="30e90-125">-Várva</span><span class="sxs-lookup"><span data-stu-id="30e90-125">-NoWait</span></span>
<span data-ttu-id="30e90-126">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="30e90-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="30e90-127">-PersistentDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="30e90-127">-PersistentDiskMountPath</span></span>
<span data-ttu-id="30e90-128">Az állandó lemez csatlakoztatási útja</span><span class="sxs-lookup"><span data-stu-id="30e90-128">Mount path of the persistent disk</span></span>

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

### <span data-ttu-id="30e90-129">-PersistentDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="30e90-129">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="30e90-130">Az állandó lemez mérete GB-ban</span><span class="sxs-lookup"><span data-stu-id="30e90-130">Size of the persistent disk in GB</span></span>

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

### <span data-ttu-id="30e90-131">– Nyilvános</span><span class="sxs-lookup"><span data-stu-id="30e90-131">-Public</span></span>
<span data-ttu-id="30e90-132">Azt jelzi, hogy az alkalmazás kiteszi-e a nyilvános végpontot</span><span class="sxs-lookup"><span data-stu-id="30e90-132">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="30e90-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30e90-133">-ResourceGroupName</span></span>
<span data-ttu-id="30e90-134">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="30e90-134">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="30e90-135">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="30e90-135">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="30e90-136">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="30e90-136">-ServiceName</span></span>
<span data-ttu-id="30e90-137">A szolgáltatás erőforrásának neve.</span><span class="sxs-lookup"><span data-stu-id="30e90-137">The name of the Service resource.</span></span>

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

### <span data-ttu-id="30e90-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="30e90-138">-SubscriptionId</span></span>
<span data-ttu-id="30e90-139">Megkapja az előfizetés AZONOSÍTÓját, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="30e90-139">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="30e90-140">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="30e90-140">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="30e90-141">-TemporaryDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="30e90-141">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="30e90-142">Az ideiglenes lemez csatlakoztatási útvonala</span><span class="sxs-lookup"><span data-stu-id="30e90-142">Mount path of the temporary disk</span></span>

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

### <span data-ttu-id="30e90-143">-TemporaryDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="30e90-143">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="30e90-144">Az ideiglenes lemez mérete GB-ban</span><span class="sxs-lookup"><span data-stu-id="30e90-144">Size of the temporary disk in GB</span></span>

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

### <span data-ttu-id="30e90-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="30e90-145">-Confirm</span></span>
<span data-ttu-id="30e90-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="30e90-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30e90-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30e90-147">-WhatIf</span></span>
<span data-ttu-id="30e90-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="30e90-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30e90-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="30e90-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30e90-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30e90-150">CommonParameters</span></span>
<span data-ttu-id="30e90-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="30e90-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30e90-152">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="30e90-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30e90-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="30e90-153">INPUTS</span></span>

## <span data-ttu-id="30e90-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="30e90-154">OUTPUTS</span></span>

### <span data-ttu-id="30e90-155">Microsoft. Azure. PowerShell. parancsmagok. SpringCloud. modellek. Api20200701. IAppResource</span><span class="sxs-lookup"><span data-stu-id="30e90-155">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="30e90-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="30e90-156">NOTES</span></span>

<span data-ttu-id="30e90-157">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="30e90-157">ALIASES</span></span>

## <span data-ttu-id="30e90-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="30e90-158">RELATED LINKS</span></span>

