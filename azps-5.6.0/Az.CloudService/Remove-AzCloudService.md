---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/remove-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Remove-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Remove-AzCloudService.md
ms.openlocfilehash: 5004aa694dd0ebb90239e2fb77259df9e84c59f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939673"
---
# <span data-ttu-id="37272-101">Remove-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="37272-101">Remove-AzCloudService</span></span>

## <span data-ttu-id="37272-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37272-102">SYNOPSIS</span></span>
<span data-ttu-id="37272-103">Töröl egy felhőszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="37272-103">Deletes a cloud service.</span></span>

## <span data-ttu-id="37272-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="37272-104">SYNTAX</span></span>

### <span data-ttu-id="37272-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="37272-105">Delete (Default)</span></span>
```
Remove-AzCloudService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="37272-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="37272-106">DeleteViaIdentity</span></span>
```
Remove-AzCloudService -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="37272-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="37272-107">DESCRIPTION</span></span>
<span data-ttu-id="37272-108">Töröl egy felhőszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="37272-108">Deletes a cloud service.</span></span>

## <span data-ttu-id="37272-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="37272-109">EXAMPLES</span></span>

### <span data-ttu-id="37272-110">1. példa: Felhőszolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="37272-110">Example 1: Remove a cloud service</span></span>
```powershell
PS C:\> Remove-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
```

<span data-ttu-id="37272-111">Ez a parancs eltávolítja a ContosoCS nevű felhőszolgáltatást, amely a ContosOrg nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="37272-111">This command removes the cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="37272-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37272-112">PARAMETERS</span></span>

### <span data-ttu-id="37272-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37272-113">-AsJob</span></span>
<span data-ttu-id="37272-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="37272-114">Run the command as a job</span></span>

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

### <span data-ttu-id="37272-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37272-115">-DefaultProfile</span></span>
<span data-ttu-id="37272-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="37272-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37272-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37272-117">-InputObject</span></span>
<span data-ttu-id="37272-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="37272-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37272-119">-Name</span><span class="sxs-lookup"><span data-stu-id="37272-119">-Name</span></span>
<span data-ttu-id="37272-120">A felhőszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="37272-120">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37272-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="37272-121">-NoWait</span></span>
<span data-ttu-id="37272-122">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="37272-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="37272-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37272-123">-PassThru</span></span>
<span data-ttu-id="37272-124">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="37272-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="37272-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37272-125">-ResourceGroupName</span></span>
<span data-ttu-id="37272-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="37272-126">Name of the resource group.</span></span>

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

### <span data-ttu-id="37272-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="37272-127">-SubscriptionId</span></span>
<span data-ttu-id="37272-128">Előfizetési hitelesítő adatok, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="37272-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="37272-129">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="37272-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="37272-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37272-130">-Confirm</span></span>
<span data-ttu-id="37272-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="37272-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37272-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37272-132">-WhatIf</span></span>
<span data-ttu-id="37272-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="37272-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37272-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="37272-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37272-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37272-135">CommonParameters</span></span>
<span data-ttu-id="37272-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37272-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37272-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37272-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37272-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="37272-138">INPUTS</span></span>

### <span data-ttu-id="37272-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="37272-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="37272-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="37272-140">OUTPUTS</span></span>

### <span data-ttu-id="37272-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="37272-141">System.Boolean</span></span>

## <span data-ttu-id="37272-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="37272-142">NOTES</span></span>

<span data-ttu-id="37272-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="37272-143">ALIASES</span></span>

<span data-ttu-id="37272-144">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="37272-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="37272-145">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="37272-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="37272-146">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="37272-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="37272-147">INPUTOBJECT: <ICloudServiceIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="37272-147">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="37272-148">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="37272-148">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="37272-149">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="37272-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="37272-150">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="37272-150">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="37272-151">`[RoleInstanceName <String>]`: A szerepkörpéldány neve.</span><span class="sxs-lookup"><span data-stu-id="37272-151">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="37272-152">`[RoleName <String>]`: A szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="37272-152">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="37272-153">`[SubscriptionId <String>]`: Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="37272-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="37272-154">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="37272-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="37272-155">`[UpdateDomain <Int32?>]`: A frissítő tartományt azonosító egész értéket ad meg.</span><span class="sxs-lookup"><span data-stu-id="37272-155">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="37272-156">A frissítési tartományokat nulla alapú index azonosítja: az első frissítési tartomány azonosítója 0, a második 1 és így tovább.</span><span class="sxs-lookup"><span data-stu-id="37272-156">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="37272-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="37272-157">RELATED LINKS</span></span>

