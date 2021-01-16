---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
ms.openlocfilehash: e363a7bedc891c736f06b60c093483010e6b261d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375716"
---
# <span data-ttu-id="e4aa1-101">Remove-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="e4aa1-101">Remove-AzSpringCloudApp</span></span>

## <span data-ttu-id="e4aa1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4aa1-102">SYNOPSIS</span></span>
<span data-ttu-id="e4aa1-103">Művelet egy alkalmazás törléséhez.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-103">Operation to delete an App.</span></span>

## <span data-ttu-id="e4aa1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e4aa1-104">SYNTAX</span></span>

### <span data-ttu-id="e4aa1-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e4aa1-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="e4aa1-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e4aa1-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e4aa1-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e4aa1-107">DESCRIPTION</span></span>
<span data-ttu-id="e4aa1-108">Művelet egy alkalmazás törléséhez.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-108">Operation to delete an App.</span></span>

## <span data-ttu-id="e4aa1-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e4aa1-109">EXAMPLES</span></span>

### <span data-ttu-id="e4aa1-110">1. példa: A Spring Cloud app eltávolítása név szerint.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-110">Example 1: Remove Spring Cloud App by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
```

<span data-ttu-id="e4aa1-111">Távolítsa el a Spring Cloud appot név szerint.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-111">Remove Spring Cloud App by name.</span></span>

### <span data-ttu-id="e4aa1-112">2. példa: A Spring Cloud app eltávolítása a pipe-ból.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-112">Example 2: Remove Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Remove-AzSpringCloudApp
```

<span data-ttu-id="e4aa1-113">Távolítsa el a Spring Cloud appot a pipe-ból.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-113">Remove Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="e4aa1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4aa1-114">PARAMETERS</span></span>

### <span data-ttu-id="e4aa1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4aa1-115">-AsJob</span></span>
<span data-ttu-id="e4aa1-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="e4aa1-116">Run the command as a job</span></span>

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

### <span data-ttu-id="e4aa1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4aa1-117">-DefaultProfile</span></span>
<span data-ttu-id="e4aa1-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4aa1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4aa1-119">-InputObject</span></span>
<span data-ttu-id="e4aa1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e4aa1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e4aa1-121">-Name</span></span>
<span data-ttu-id="e4aa1-122">Az alkalmazáserőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-122">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4aa1-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e4aa1-123">-NoWait</span></span>
<span data-ttu-id="e4aa1-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="e4aa1-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e4aa1-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4aa1-125">-PassThru</span></span>
<span data-ttu-id="e4aa1-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="e4aa1-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e4aa1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4aa1-127">-ResourceGroupName</span></span>
<span data-ttu-id="e4aa1-128">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e4aa1-129">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e4aa1-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e4aa1-130">-ServiceName</span></span>
<span data-ttu-id="e4aa1-131">A Szolgáltatás erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-131">The name of the Service resource.</span></span>

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

### <span data-ttu-id="e4aa1-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e4aa1-132">-SubscriptionId</span></span>
<span data-ttu-id="e4aa1-133">Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-133">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="e4aa1-134">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e4aa1-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4aa1-135">-Confirm</span></span>
<span data-ttu-id="e4aa1-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4aa1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4aa1-137">-WhatIf</span></span>
<span data-ttu-id="e4aa1-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4aa1-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4aa1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4aa1-140">CommonParameters</span></span>
<span data-ttu-id="e4aa1-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4aa1-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4aa1-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4aa1-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e4aa1-143">INPUTS</span></span>

### <span data-ttu-id="e4aa1-144">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="e4aa1-144">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="e4aa1-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4aa1-145">OUTPUTS</span></span>

### <span data-ttu-id="e4aa1-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e4aa1-146">System.Boolean</span></span>

## <span data-ttu-id="e4aa1-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e4aa1-147">NOTES</span></span>

<span data-ttu-id="e4aa1-148">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e4aa1-148">ALIASES</span></span>

<span data-ttu-id="e4aa1-149">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="e4aa1-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e4aa1-150">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e4aa1-151">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e4aa1-152">INPUTOBJECT: <ISpringCloudIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="e4aa1-152">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e4aa1-153">`[AppName <String>]`: Az apperőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-153">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="e4aa1-154">`[BindingName <String>]`: A Kötés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-154">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="e4aa1-155">`[CertificateName <String>]`: A tanúsítványforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-155">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="e4aa1-156">`[DeploymentName <String>]`: A Központi telepítés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-156">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="e4aa1-157">`[DomainName <String>]`: Az egyéni tartományerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-157">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="e4aa1-158">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="e4aa1-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e4aa1-159">`[Location <String>]`: a régió</span><span class="sxs-lookup"><span data-stu-id="e4aa1-159">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="e4aa1-160">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-160">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="e4aa1-161">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-161">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="e4aa1-162">`[ServiceName <String>]`: A Szolgáltatás erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-162">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="e4aa1-163">`[SubscriptionId <String>]`: Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-163">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="e4aa1-164">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-164">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e4aa1-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4aa1-165">RELATED LINKS</span></span>

