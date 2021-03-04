---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/invoke-azcloudserviceroleinstancereimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceReimage.md
ms.openlocfilehash: 644912b841475c660852adcda2cba320d9026618
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925145"
---
# <span data-ttu-id="e6b98-101">Invoke-AzCloudServiceRoleInstanceReimage</span><span class="sxs-lookup"><span data-stu-id="e6b98-101">Invoke-AzCloudServiceRoleInstanceReimage</span></span>

## <span data-ttu-id="e6b98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6b98-102">SYNOPSIS</span></span>
<span data-ttu-id="e6b98-103">A Reimage szerepkörpéldány aszinkron művelet újratelepíti az operációs rendszert a webes szerepkörök vagy a dolgozók szerepkörei példányán.</span><span class="sxs-lookup"><span data-stu-id="e6b98-103">The Reimage Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

## <span data-ttu-id="e6b98-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e6b98-104">SYNTAX</span></span>

### <span data-ttu-id="e6b98-105">Reimage (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e6b98-105">Reimage (Default)</span></span>
```
Invoke-AzCloudServiceRoleInstanceReimage -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e6b98-106">ReimageViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e6b98-106">ReimageViaIdentity</span></span>
```
Invoke-AzCloudServiceRoleInstanceReimage -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e6b98-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e6b98-107">DESCRIPTION</span></span>
<span data-ttu-id="e6b98-108">A Reimage szerepkörpéldány aszinkron művelet újratelepíti az operációs rendszert a webes szerepkörök vagy a dolgozók szerepkörei példányán.</span><span class="sxs-lookup"><span data-stu-id="e6b98-108">The Reimage Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

## <span data-ttu-id="e6b98-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e6b98-109">EXAMPLES</span></span>

### <span data-ttu-id="e6b98-110">1. példa: Felhőszolgáltatás szerepkörpéldányának újraimáltatása</span><span class="sxs-lookup"><span data-stu-id="e6b98-110">Example 1: Reimage role instance of a cloud service</span></span>
```powershell
PS C:\> Invoke-AzCloudServiceRoleInstanceReimage -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="e6b98-111">Ez a parancs újragondolja ContosoFrontEnd_IN_0 ContosOrg nevű erőforráscsoporthoz tartozó ContosoCS nevű felhőszolgáltatás egyik szerepkörpéldányát.</span><span class="sxs-lookup"><span data-stu-id="e6b98-111">This command reimages role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="e6b98-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6b98-112">PARAMETERS</span></span>

### <span data-ttu-id="e6b98-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6b98-113">-AsJob</span></span>
<span data-ttu-id="e6b98-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="e6b98-114">Run the command as a job</span></span>

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

### <span data-ttu-id="e6b98-115">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="e6b98-115">-CloudServiceName</span></span>
<span data-ttu-id="e6b98-116">.</span><span class="sxs-lookup"><span data-stu-id="e6b98-116">.</span></span>

```yaml
Type: System.String
Parameter Sets: Reimage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b98-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6b98-117">-DefaultProfile</span></span>
<span data-ttu-id="e6b98-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6b98-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6b98-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6b98-119">-InputObject</span></span>
<span data-ttu-id="e6b98-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e6b98-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: ReimageViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6b98-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e6b98-121">-NoWait</span></span>
<span data-ttu-id="e6b98-122">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="e6b98-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e6b98-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6b98-123">-PassThru</span></span>
<span data-ttu-id="e6b98-124">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="e6b98-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e6b98-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6b98-125">-ResourceGroupName</span></span>
<span data-ttu-id="e6b98-126">.</span><span class="sxs-lookup"><span data-stu-id="e6b98-126">.</span></span>

```yaml
Type: System.String
Parameter Sets: Reimage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b98-127">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="e6b98-127">-RoleInstanceName</span></span>
<span data-ttu-id="e6b98-128">A szerepkörpéldány neve.</span><span class="sxs-lookup"><span data-stu-id="e6b98-128">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Reimage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b98-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e6b98-129">-SubscriptionId</span></span>
<span data-ttu-id="e6b98-130">Előfizetési hitelesítő adatok, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="e6b98-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e6b98-131">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="e6b98-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Reimage
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b98-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6b98-132">-Confirm</span></span>
<span data-ttu-id="e6b98-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e6b98-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6b98-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6b98-134">-WhatIf</span></span>
<span data-ttu-id="e6b98-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e6b98-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6b98-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e6b98-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6b98-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6b98-137">CommonParameters</span></span>
<span data-ttu-id="e6b98-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6b98-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6b98-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6b98-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6b98-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e6b98-140">INPUTS</span></span>

### <span data-ttu-id="e6b98-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="e6b98-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="e6b98-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6b98-142">OUTPUTS</span></span>

### <span data-ttu-id="e6b98-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e6b98-143">System.Boolean</span></span>

## <span data-ttu-id="e6b98-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e6b98-144">NOTES</span></span>

<span data-ttu-id="e6b98-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e6b98-145">ALIASES</span></span>

<span data-ttu-id="e6b98-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="e6b98-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e6b98-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="e6b98-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e6b98-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e6b98-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e6b98-149">INPUTOBJECT: <ICloudServiceIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="e6b98-149">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e6b98-150">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="e6b98-150">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="e6b98-151">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="e6b98-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e6b98-152">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="e6b98-152">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="e6b98-153">`[RoleInstanceName <String>]`: A szerepkörpéldány neve.</span><span class="sxs-lookup"><span data-stu-id="e6b98-153">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="e6b98-154">`[RoleName <String>]`: A szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="e6b98-154">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="e6b98-155">`[SubscriptionId <String>]`: Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="e6b98-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e6b98-156">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="e6b98-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="e6b98-157">`[UpdateDomain <Int32?>]`: A frissítő tartományt azonosító egész értéket ad meg.</span><span class="sxs-lookup"><span data-stu-id="e6b98-157">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="e6b98-158">A frissítési tartományokat nulla alapú index azonosítja: az első frissítési tartomány azonosítója 0, a második 1 és így tovább.</span><span class="sxs-lookup"><span data-stu-id="e6b98-158">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="e6b98-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6b98-159">RELATED LINKS</span></span>

