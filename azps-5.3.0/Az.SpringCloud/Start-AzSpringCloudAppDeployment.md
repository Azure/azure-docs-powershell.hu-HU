---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/start-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Start-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Start-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 7cab91bf5c7e95258f17a73da4e2b177e30444c9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375701"
---
# <span data-ttu-id="abf55-101">Start-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="abf55-101">Start-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="abf55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abf55-102">SYNOPSIS</span></span>
<span data-ttu-id="abf55-103">Indítsa el az üzembe helyezést.</span><span class="sxs-lookup"><span data-stu-id="abf55-103">Start the deployment.</span></span>

## <span data-ttu-id="abf55-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="abf55-104">SYNTAX</span></span>

### <span data-ttu-id="abf55-105">Start (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="abf55-105">Start (Default)</span></span>
```
Start-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="abf55-106">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="abf55-106">StartViaIdentity</span></span>
```
Start-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="abf55-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="abf55-107">DESCRIPTION</span></span>
<span data-ttu-id="abf55-108">Indítsa el az üzembe helyezést.</span><span class="sxs-lookup"><span data-stu-id="abf55-108">Start the deployment.</span></span>

## <span data-ttu-id="abf55-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="abf55-109">EXAMPLES</span></span>

### <span data-ttu-id="abf55-110">1. példa: Indítsa el a tavaszi felhőszolgáltatást név szerint.</span><span class="sxs-lookup"><span data-stu-id="abf55-110">Example 1: Start Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Start-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="abf55-111">Indítsa el a Spring Cloud Service szolgáltatást név szerint.</span><span class="sxs-lookup"><span data-stu-id="abf55-111">Start Spring Cloud Service by name.</span></span>

### <span data-ttu-id="abf55-112">2. példa: Indítsa el a tavaszi felhőszolgáltatást a pipával.</span><span class="sxs-lookup"><span data-stu-id="abf55-112">Example 2: Start Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Start-AzSpringCloud
```

<span data-ttu-id="abf55-113">Indítsa el a tavaszi felhőszolgáltatást a pipe-ból.</span><span class="sxs-lookup"><span data-stu-id="abf55-113">Start Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="abf55-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="abf55-114">PARAMETERS</span></span>

### <span data-ttu-id="abf55-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="abf55-115">-AppName</span></span>
<span data-ttu-id="abf55-116">Az alkalmazáserőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="abf55-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abf55-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="abf55-117">-AsJob</span></span>
<span data-ttu-id="abf55-118">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="abf55-118">Run the command as a job</span></span>

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

### <span data-ttu-id="abf55-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abf55-119">-DefaultProfile</span></span>
<span data-ttu-id="abf55-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="abf55-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abf55-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abf55-121">-InputObject</span></span>
<span data-ttu-id="abf55-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="abf55-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abf55-123">-Name</span><span class="sxs-lookup"><span data-stu-id="abf55-123">-Name</span></span>
<span data-ttu-id="abf55-124">A Központi telepítés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="abf55-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abf55-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="abf55-125">-NoWait</span></span>
<span data-ttu-id="abf55-126">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="abf55-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="abf55-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="abf55-127">-PassThru</span></span>
<span data-ttu-id="abf55-128">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="abf55-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="abf55-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abf55-129">-ResourceGroupName</span></span>
<span data-ttu-id="abf55-130">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="abf55-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="abf55-131">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="abf55-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abf55-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="abf55-132">-ServiceName</span></span>
<span data-ttu-id="abf55-133">A Szolgáltatás erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="abf55-133">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abf55-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="abf55-134">-SubscriptionId</span></span>
<span data-ttu-id="abf55-135">Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="abf55-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="abf55-136">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="abf55-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abf55-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="abf55-137">-Confirm</span></span>
<span data-ttu-id="abf55-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="abf55-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abf55-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abf55-139">-WhatIf</span></span>
<span data-ttu-id="abf55-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="abf55-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abf55-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="abf55-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abf55-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abf55-142">CommonParameters</span></span>
<span data-ttu-id="abf55-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abf55-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abf55-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="abf55-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abf55-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="abf55-145">INPUTS</span></span>

### <span data-ttu-id="abf55-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="abf55-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="abf55-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="abf55-147">OUTPUTS</span></span>

### <span data-ttu-id="abf55-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="abf55-148">System.Boolean</span></span>

## <span data-ttu-id="abf55-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="abf55-149">NOTES</span></span>

<span data-ttu-id="abf55-150">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="abf55-150">ALIASES</span></span>

<span data-ttu-id="abf55-151">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="abf55-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="abf55-152">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="abf55-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="abf55-153">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="abf55-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="abf55-154">INPUTOBJECT: <ISpringCloudIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="abf55-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="abf55-155">`[AppName <String>]`: Az apperőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="abf55-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="abf55-156">`[BindingName <String>]`: A Kötés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="abf55-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="abf55-157">`[CertificateName <String>]`: A tanúsítványforrás neve.</span><span class="sxs-lookup"><span data-stu-id="abf55-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="abf55-158">`[DeploymentName <String>]`: A Központi telepítés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="abf55-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="abf55-159">`[DomainName <String>]`: Az egyéni tartományerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="abf55-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="abf55-160">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="abf55-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="abf55-161">`[Location <String>]`: a régió</span><span class="sxs-lookup"><span data-stu-id="abf55-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="abf55-162">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="abf55-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="abf55-163">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="abf55-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="abf55-164">`[ServiceName <String>]`: A Szolgáltatás erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="abf55-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="abf55-165">`[SubscriptionId <String>]`: Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="abf55-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="abf55-166">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="abf55-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="abf55-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="abf55-167">RELATED LINKS</span></span>

