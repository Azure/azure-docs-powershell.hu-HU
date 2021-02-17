---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/stop-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Stop-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Stop-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 3f98161e56019394dc67ab8909aac3fb70a611a2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156234"
---
# <span data-ttu-id="acdaf-101">Stop-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="acdaf-101">Stop-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="acdaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acdaf-102">SYNOPSIS</span></span>
<span data-ttu-id="acdaf-103">Állítsa le az üzembe helyezést.</span><span class="sxs-lookup"><span data-stu-id="acdaf-103">Stop the deployment.</span></span>

## <span data-ttu-id="acdaf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="acdaf-104">SYNTAX</span></span>

### <span data-ttu-id="acdaf-105">Leállítás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="acdaf-105">Stop (Default)</span></span>
```
Stop-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="acdaf-106">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="acdaf-106">StopViaIdentity</span></span>
```
Stop-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="acdaf-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="acdaf-107">DESCRIPTION</span></span>
<span data-ttu-id="acdaf-108">Állítsa le az üzembe helyezést.</span><span class="sxs-lookup"><span data-stu-id="acdaf-108">Stop the deployment.</span></span>

## <span data-ttu-id="acdaf-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="acdaf-109">EXAMPLES</span></span>

### <span data-ttu-id="acdaf-110">1. példa: A Tavaszi felhőszolgáltatás leállítása név szerint.</span><span class="sxs-lookup"><span data-stu-id="acdaf-110">Example 1: Stop Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Stop-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="acdaf-111">Állítsa le a Spring Cloud Service szolgáltatást név szerint.</span><span class="sxs-lookup"><span data-stu-id="acdaf-111">Stop Spring Cloud Service by name.</span></span>

### <span data-ttu-id="acdaf-112">2. példa: Állítsa le a tavaszi felhőszolgáltatást a vízvezetékből.</span><span class="sxs-lookup"><span data-stu-id="acdaf-112">Example 2: Stop Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Stop-AzSpringCloud
```

<span data-ttu-id="acdaf-113">Állítsa le a spring cloud service-et a pipe-ból.</span><span class="sxs-lookup"><span data-stu-id="acdaf-113">Stop Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="acdaf-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="acdaf-114">PARAMETERS</span></span>

### <span data-ttu-id="acdaf-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="acdaf-115">-AppName</span></span>
<span data-ttu-id="acdaf-116">Az alkalmazáserőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="acdaf-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acdaf-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="acdaf-117">-AsJob</span></span>
<span data-ttu-id="acdaf-118">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="acdaf-118">Run the command as a job</span></span>

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

### <span data-ttu-id="acdaf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acdaf-119">-DefaultProfile</span></span>
<span data-ttu-id="acdaf-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="acdaf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acdaf-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="acdaf-121">-InputObject</span></span>
<span data-ttu-id="acdaf-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="acdaf-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: StopViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="acdaf-123">-Name</span><span class="sxs-lookup"><span data-stu-id="acdaf-123">-Name</span></span>
<span data-ttu-id="acdaf-124">A Központi telepítés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="acdaf-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acdaf-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="acdaf-125">-NoWait</span></span>
<span data-ttu-id="acdaf-126">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="acdaf-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="acdaf-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="acdaf-127">-PassThru</span></span>
<span data-ttu-id="acdaf-128">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="acdaf-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="acdaf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acdaf-129">-ResourceGroupName</span></span>
<span data-ttu-id="acdaf-130">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="acdaf-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="acdaf-131">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="acdaf-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acdaf-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="acdaf-132">-ServiceName</span></span>
<span data-ttu-id="acdaf-133">A Szolgáltatás erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="acdaf-133">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acdaf-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="acdaf-134">-SubscriptionId</span></span>
<span data-ttu-id="acdaf-135">Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="acdaf-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="acdaf-136">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="acdaf-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acdaf-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="acdaf-137">-Confirm</span></span>
<span data-ttu-id="acdaf-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="acdaf-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acdaf-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acdaf-139">-WhatIf</span></span>
<span data-ttu-id="acdaf-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="acdaf-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acdaf-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="acdaf-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acdaf-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acdaf-142">CommonParameters</span></span>
<span data-ttu-id="acdaf-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acdaf-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acdaf-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="acdaf-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acdaf-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="acdaf-145">INPUTS</span></span>

### <span data-ttu-id="acdaf-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="acdaf-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="acdaf-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="acdaf-147">OUTPUTS</span></span>

### <span data-ttu-id="acdaf-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="acdaf-148">System.Boolean</span></span>

## <span data-ttu-id="acdaf-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="acdaf-149">NOTES</span></span>

<span data-ttu-id="acdaf-150">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="acdaf-150">ALIASES</span></span>

<span data-ttu-id="acdaf-151">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="acdaf-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="acdaf-152">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="acdaf-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="acdaf-153">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="acdaf-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="acdaf-154">INPUTOBJECT: <ISpringCloudIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="acdaf-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="acdaf-155">`[AppName <String>]`: Az apperőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="acdaf-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="acdaf-156">`[BindingName <String>]`: A Kötés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="acdaf-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="acdaf-157">`[CertificateName <String>]`: A tanúsítványforrás neve.</span><span class="sxs-lookup"><span data-stu-id="acdaf-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="acdaf-158">`[DeploymentName <String>]`: A Központi telepítés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="acdaf-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="acdaf-159">`[DomainName <String>]`: Az egyéni tartományerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="acdaf-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="acdaf-160">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="acdaf-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="acdaf-161">`[Location <String>]`: a régió</span><span class="sxs-lookup"><span data-stu-id="acdaf-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="acdaf-162">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="acdaf-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="acdaf-163">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="acdaf-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="acdaf-164">`[ServiceName <String>]`: A Szolgáltatás erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="acdaf-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="acdaf-165">`[SubscriptionId <String>]`: Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="acdaf-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="acdaf-166">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="acdaf-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="acdaf-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="acdaf-167">RELATED LINKS</span></span>

