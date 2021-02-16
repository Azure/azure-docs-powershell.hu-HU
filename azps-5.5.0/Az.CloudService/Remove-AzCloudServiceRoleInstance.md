---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/remove-azcloudserviceroleinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Remove-AzCloudServiceRoleInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Remove-AzCloudServiceRoleInstance.md
ms.openlocfilehash: 8d44cc541cf44e03e2946ce428eb96c2f902bf84
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162347"
---
# <span data-ttu-id="e0c1e-101">Remove-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="e0c1e-101">Remove-AzCloudServiceRoleInstance</span></span>

## <span data-ttu-id="e0c1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0c1e-102">SYNOPSIS</span></span>
<span data-ttu-id="e0c1e-103">Törli a szerepkörpéldányokat egy felhőszolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="e0c1e-103">Deletes role instances in a cloud service.</span></span>

## <span data-ttu-id="e0c1e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e0c1e-104">SYNTAX</span></span>

### <span data-ttu-id="e0c1e-105">DeleteExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e0c1e-105">DeleteExpanded (Default)</span></span>
```
Remove-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstance <String[]> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e0c1e-106">DeleteViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e0c1e-106">DeleteViaIdentityExpanded</span></span>
```
Remove-AzCloudServiceRoleInstance -InputObject <ICloudServiceIdentity> -RoleInstance <String[]>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e0c1e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e0c1e-107">DESCRIPTION</span></span>
<span data-ttu-id="e0c1e-108">Törli a szerepkörpéldányokat egy felhőszolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="e0c1e-108">Deletes role instances in a cloud service.</span></span>

## <span data-ttu-id="e0c1e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e0c1e-109">EXAMPLES</span></span>

### <span data-ttu-id="e0c1e-110">1. példa: Felhőszolgáltatás szerepkörpéldányának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e0c1e-110">Example 1: Remove a cloud service role instance</span></span>
```powershell
PS C:\> Remove-AzCloudServiceInstance -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="e0c1e-111">Ez a parancs eltávolítja a ContosoCS nevű ContosoFrontEnd_IN_0 nevű felhőszolgáltatás szerepkörpéldányát, amely a ContosOrg nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="e0c1e-111">This command removes the role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="e0c1e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0c1e-112">PARAMETERS</span></span>

### <span data-ttu-id="e0c1e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0c1e-113">-AsJob</span></span>
<span data-ttu-id="e0c1e-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="e0c1e-114">Run the command as a job</span></span>

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

### <span data-ttu-id="e0c1e-115">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="e0c1e-115">-CloudServiceName</span></span>
<span data-ttu-id="e0c1e-116">A felhőszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="e0c1e-116">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0c1e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0c1e-117">-DefaultProfile</span></span>
<span data-ttu-id="e0c1e-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e0c1e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0c1e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0c1e-119">-InputObject</span></span>
<span data-ttu-id="e0c1e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e0c1e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: DeleteViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0c1e-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e0c1e-121">-NoWait</span></span>
<span data-ttu-id="e0c1e-122">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="e0c1e-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e0c1e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0c1e-123">-PassThru</span></span>
<span data-ttu-id="e0c1e-124">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="e0c1e-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e0c1e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0c1e-125">-ResourceGroupName</span></span>
<span data-ttu-id="e0c1e-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e0c1e-126">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0c1e-127">-RoleInstance</span><span class="sxs-lookup"><span data-stu-id="e0c1e-127">-RoleInstance</span></span>
<span data-ttu-id="e0c1e-128">A felhőbeli szolgáltatási szerepkör példánynevének listája.</span><span class="sxs-lookup"><span data-stu-id="e0c1e-128">List of cloud service role instance names.</span></span>
<span data-ttu-id="e0c1e-129">A "\*" érték a felhőszolgáltatás összes szerepkörpéldányát alá fogja írni.</span><span class="sxs-lookup"><span data-stu-id="e0c1e-129">Value of '\*' will signify all role instances of the cloud service.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0c1e-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e0c1e-130">-SubscriptionId</span></span>
<span data-ttu-id="e0c1e-131">Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="e0c1e-131">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e0c1e-132">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="e0c1e-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0c1e-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0c1e-133">-Confirm</span></span>
<span data-ttu-id="e0c1e-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e0c1e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0c1e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0c1e-135">-WhatIf</span></span>
<span data-ttu-id="e0c1e-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e0c1e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0c1e-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e0c1e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0c1e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0c1e-138">CommonParameters</span></span>
<span data-ttu-id="e0c1e-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0c1e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0c1e-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0c1e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0c1e-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e0c1e-141">INPUTS</span></span>

### <span data-ttu-id="e0c1e-142">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="e0c1e-142">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="e0c1e-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0c1e-143">OUTPUTS</span></span>

### <span data-ttu-id="e0c1e-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e0c1e-144">System.Boolean</span></span>

## <span data-ttu-id="e0c1e-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e0c1e-145">NOTES</span></span>

<span data-ttu-id="e0c1e-146">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e0c1e-146">ALIASES</span></span>

<span data-ttu-id="e0c1e-147">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="e0c1e-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e0c1e-148">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="e0c1e-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e0c1e-149">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e0c1e-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e0c1e-150">INPUTOBJECT: <ICloudServiceIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="e0c1e-150">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e0c1e-151">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="e0c1e-151">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="e0c1e-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="e0c1e-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e0c1e-153">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="e0c1e-153">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="e0c1e-154">`[RoleInstanceName <String>]`: A szerepkörpéldány neve.</span><span class="sxs-lookup"><span data-stu-id="e0c1e-154">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="e0c1e-155">`[RoleName <String>]`: A szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="e0c1e-155">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="e0c1e-156">`[SubscriptionId <String>]`: Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="e0c1e-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e0c1e-157">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="e0c1e-157">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="e0c1e-158">`[UpdateDomain <Int32?>]`: A frissítő tartományt azonosító egész számértéket ad meg.</span><span class="sxs-lookup"><span data-stu-id="e0c1e-158">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="e0c1e-159">A frissítési tartományokat nulla alapú index azonosítja: az első frissítési tartomány azonosítója 0, a második 1 és így tovább.</span><span class="sxs-lookup"><span data-stu-id="e0c1e-159">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="e0c1e-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0c1e-160">RELATED LINKS</span></span>

