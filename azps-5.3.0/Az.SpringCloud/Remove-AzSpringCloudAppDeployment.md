---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 25b7b5c93f769982364a0df8f14f5fbe2f804fa2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375715"
---
# <span data-ttu-id="ba7d9-101">Remove-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="ba7d9-101">Remove-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="ba7d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba7d9-102">SYNOPSIS</span></span>
<span data-ttu-id="ba7d9-103">Művelet egy központi telepítés törléséhez.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-103">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="ba7d9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ba7d9-104">SYNTAX</span></span>

### <span data-ttu-id="ba7d9-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ba7d9-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ba7d9-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ba7d9-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ba7d9-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ba7d9-107">DESCRIPTION</span></span>
<span data-ttu-id="ba7d9-108">Művelet egy központi telepítés törléséhez.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-108">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="ba7d9-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ba7d9-109">EXAMPLES</span></span>

### <span data-ttu-id="ba7d9-110">1. példa: A Tavaszi felhőbeli telepítés eltávolítása név szerint.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-110">Example 1: Remove Spring Cloud Deployment by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="ba7d9-111">Távolítsa el a Tavaszi felhőbeli telepítést név szerint.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-111">Remove Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="ba7d9-112">2. példa: A tavaszi felhőbeli telepítés eltávolítása a vízvezetékből.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-112">Example 2: Remove Spring Cloud Deployment from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Remove-AzSpringCloudAppDeployment
```

<span data-ttu-id="ba7d9-113">Távolítsa el a Tavaszi felhőbeli telepítést a vízvezetékből.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-113">Remove Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="ba7d9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba7d9-114">PARAMETERS</span></span>

### <span data-ttu-id="ba7d9-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="ba7d9-115">-AppName</span></span>
<span data-ttu-id="ba7d9-116">Az alkalmazáserőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba7d9-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba7d9-117">-AsJob</span></span>
<span data-ttu-id="ba7d9-118">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="ba7d9-118">Run the command as a job</span></span>

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

### <span data-ttu-id="ba7d9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba7d9-119">-DefaultProfile</span></span>
<span data-ttu-id="ba7d9-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba7d9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba7d9-121">-InputObject</span></span>
<span data-ttu-id="ba7d9-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba7d9-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ba7d9-123">-Name</span></span>
<span data-ttu-id="ba7d9-124">A Központi telepítés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba7d9-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ba7d9-125">-NoWait</span></span>
<span data-ttu-id="ba7d9-126">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="ba7d9-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ba7d9-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba7d9-127">-PassThru</span></span>
<span data-ttu-id="ba7d9-128">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="ba7d9-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ba7d9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba7d9-129">-ResourceGroupName</span></span>
<span data-ttu-id="ba7d9-130">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ba7d9-131">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba7d9-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ba7d9-132">-ServiceName</span></span>
<span data-ttu-id="ba7d9-133">A Szolgáltatás erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-133">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba7d9-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ba7d9-134">-SubscriptionId</span></span>
<span data-ttu-id="ba7d9-135">Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ba7d9-136">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba7d9-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba7d9-137">-Confirm</span></span>
<span data-ttu-id="ba7d9-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba7d9-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba7d9-139">-WhatIf</span></span>
<span data-ttu-id="ba7d9-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba7d9-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba7d9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba7d9-142">CommonParameters</span></span>
<span data-ttu-id="ba7d9-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba7d9-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba7d9-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba7d9-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ba7d9-145">INPUTS</span></span>

### <span data-ttu-id="ba7d9-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="ba7d9-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="ba7d9-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba7d9-147">OUTPUTS</span></span>

### <span data-ttu-id="ba7d9-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ba7d9-148">System.Boolean</span></span>

## <span data-ttu-id="ba7d9-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ba7d9-149">NOTES</span></span>

<span data-ttu-id="ba7d9-150">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="ba7d9-150">ALIASES</span></span>

<span data-ttu-id="ba7d9-151">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="ba7d9-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ba7d9-152">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ba7d9-153">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ba7d9-154">INPUTOBJECT: <ISpringCloudIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="ba7d9-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ba7d9-155">`[AppName <String>]`: Az apperőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="ba7d9-156">`[BindingName <String>]`: A Kötés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="ba7d9-157">`[CertificateName <String>]`: A tanúsítványforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="ba7d9-158">`[DeploymentName <String>]`: A Központi telepítés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="ba7d9-159">`[DomainName <String>]`: Az egyéni tartományerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="ba7d9-160">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="ba7d9-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ba7d9-161">`[Location <String>]`: a régió</span><span class="sxs-lookup"><span data-stu-id="ba7d9-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="ba7d9-162">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="ba7d9-163">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="ba7d9-164">`[ServiceName <String>]`: A Szolgáltatás erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="ba7d9-165">`[SubscriptionId <String>]`: Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="ba7d9-166">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ba7d9-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba7d9-167">RELATED LINKS</span></span>

