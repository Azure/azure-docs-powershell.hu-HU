---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloud.md
ms.openlocfilehash: 913011a9230b70c59b772eae306913c1e1e87432
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165019"
---
# <span data-ttu-id="15a54-101">Remove-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="15a54-101">Remove-AzSpringCloud</span></span>

## <span data-ttu-id="15a54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15a54-102">SYNOPSIS</span></span>
<span data-ttu-id="15a54-103">Művelet egy szolgáltatás törléséhez.</span><span class="sxs-lookup"><span data-stu-id="15a54-103">Operation to delete a Service.</span></span>

## <span data-ttu-id="15a54-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="15a54-104">SYNTAX</span></span>

### <span data-ttu-id="15a54-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="15a54-105">Delete (Default)</span></span>
```
Remove-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="15a54-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="15a54-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="15a54-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="15a54-107">DESCRIPTION</span></span>
<span data-ttu-id="15a54-108">Szolgáltatás törlésének művelete.</span><span class="sxs-lookup"><span data-stu-id="15a54-108">Operation to delete a Service.</span></span>

## <span data-ttu-id="15a54-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="15a54-109">EXAMPLES</span></span>

### <span data-ttu-id="15a54-110">1. példa: A Tavaszi felhőszolgáltatás eltávolítása név szerint.</span><span class="sxs-lookup"><span data-stu-id="15a54-110">Example 1: Remove Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
```

<span data-ttu-id="15a54-111">Távolítsa el a Tavaszi felhőszolgáltatást név szerint.</span><span class="sxs-lookup"><span data-stu-id="15a54-111">Remove Spring Cloud Service by name.</span></span>

### <span data-ttu-id="15a54-112">2. példa: A Tavaszi felhőszolgáltatás eltávolítása a vízvezetékből.</span><span class="sxs-lookup"><span data-stu-id="15a54-112">Example 2: Remove Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service | Remove-AzSpringCloud
```

<span data-ttu-id="15a54-113">Távolítsa el a Tavaszi felhőszolgáltatást a vízvezetékből.</span><span class="sxs-lookup"><span data-stu-id="15a54-113">Remove Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="15a54-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15a54-114">PARAMETERS</span></span>

### <span data-ttu-id="15a54-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="15a54-115">-AsJob</span></span>
<span data-ttu-id="15a54-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="15a54-116">Run the command as a job</span></span>

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

### <span data-ttu-id="15a54-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15a54-117">-DefaultProfile</span></span>
<span data-ttu-id="15a54-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="15a54-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15a54-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15a54-119">-InputObject</span></span>
<span data-ttu-id="15a54-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="15a54-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="15a54-121">-Name</span><span class="sxs-lookup"><span data-stu-id="15a54-121">-Name</span></span>
<span data-ttu-id="15a54-122">A Szolgáltatás erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="15a54-122">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a54-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="15a54-123">-NoWait</span></span>
<span data-ttu-id="15a54-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="15a54-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="15a54-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15a54-125">-PassThru</span></span>
<span data-ttu-id="15a54-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="15a54-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="15a54-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15a54-127">-ResourceGroupName</span></span>
<span data-ttu-id="15a54-128">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="15a54-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="15a54-129">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="15a54-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="15a54-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="15a54-130">-SubscriptionId</span></span>
<span data-ttu-id="15a54-131">Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="15a54-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="15a54-132">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="15a54-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="15a54-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15a54-133">-Confirm</span></span>
<span data-ttu-id="15a54-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="15a54-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15a54-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15a54-135">-WhatIf</span></span>
<span data-ttu-id="15a54-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="15a54-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15a54-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="15a54-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15a54-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15a54-138">CommonParameters</span></span>
<span data-ttu-id="15a54-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15a54-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15a54-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15a54-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15a54-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="15a54-141">INPUTS</span></span>

### <span data-ttu-id="15a54-142">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="15a54-142">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="15a54-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15a54-143">OUTPUTS</span></span>

### <span data-ttu-id="15a54-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="15a54-144">System.Boolean</span></span>

## <span data-ttu-id="15a54-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="15a54-145">NOTES</span></span>

<span data-ttu-id="15a54-146">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="15a54-146">ALIASES</span></span>

<span data-ttu-id="15a54-147">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="15a54-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="15a54-148">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="15a54-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="15a54-149">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="15a54-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="15a54-150">INPUTOBJECT: <ISpringCloudIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="15a54-150">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="15a54-151">`[AppName <String>]`: Az apperőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="15a54-151">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="15a54-152">`[BindingName <String>]`: A Kötés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="15a54-152">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="15a54-153">`[CertificateName <String>]`: A tanúsítványforrás neve.</span><span class="sxs-lookup"><span data-stu-id="15a54-153">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="15a54-154">`[DeploymentName <String>]`: A Központi telepítés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="15a54-154">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="15a54-155">`[DomainName <String>]`: Az egyéni tartományerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="15a54-155">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="15a54-156">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="15a54-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="15a54-157">`[Location <String>]`: a régió</span><span class="sxs-lookup"><span data-stu-id="15a54-157">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="15a54-158">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="15a54-158">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="15a54-159">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="15a54-159">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="15a54-160">`[ServiceName <String>]`: A Szolgáltatás erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="15a54-160">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="15a54-161">`[SubscriptionId <String>]`: Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="15a54-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="15a54-162">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="15a54-162">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="15a54-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15a54-163">RELATED LINKS</span></span>

