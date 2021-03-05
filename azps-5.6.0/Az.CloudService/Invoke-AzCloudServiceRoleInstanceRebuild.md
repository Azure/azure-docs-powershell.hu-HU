---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/invoke-azcloudserviceroleinstancerebuild
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceRebuild.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceRebuild.md
ms.openlocfilehash: 1f204b40bcf6cbd81449a6478d9d7d4e3f7d432d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007237"
---
# <span data-ttu-id="28550-101">Invoke-AzCloudServiceRoleInstanceRebuild</span><span class="sxs-lookup"><span data-stu-id="28550-101">Invoke-AzCloudServiceRoleInstanceRebuild</span></span>

## <span data-ttu-id="28550-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28550-102">SYNOPSIS</span></span>
<span data-ttu-id="28550-103">A szerepkörpéldány újraépítése aszinkron művelet újratelepíti az operációs rendszert a webes szerepkörök vagy a dolgozók szerepkörei példányán, és inicializálja az általuk használt tárterület-erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="28550-103">The Rebuild Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="28550-104">Ha nem szeretné inicializálni a tárterület-erőforrásokat, használhatja a Reimage szerepkörpéldányt.</span><span class="sxs-lookup"><span data-stu-id="28550-104">If you do not want to initialize storage resources, you can use Reimage Role Instance.</span></span>

## <span data-ttu-id="28550-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="28550-105">SYNTAX</span></span>

### <span data-ttu-id="28550-106">Újraépítés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="28550-106">Rebuild (Default)</span></span>
```
Invoke-AzCloudServiceRoleInstanceRebuild -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="28550-107">RebuildViaIdentity</span><span class="sxs-lookup"><span data-stu-id="28550-107">RebuildViaIdentity</span></span>
```
Invoke-AzCloudServiceRoleInstanceRebuild -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="28550-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="28550-108">DESCRIPTION</span></span>
<span data-ttu-id="28550-109">A szerepkörpéldány újraépítése aszinkron művelet újratelepíti az operációs rendszert a webes szerepkörök vagy a dolgozók szerepkörei példányán, és inicializálja az általuk használt tárterület-erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="28550-109">The Rebuild Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="28550-110">Ha nem szeretné inicializálni a tárterület-erőforrásokat, használhatja a Reimage szerepkörpéldányt.</span><span class="sxs-lookup"><span data-stu-id="28550-110">If you do not want to initialize storage resources, you can use Reimage Role Instance.</span></span>

## <span data-ttu-id="28550-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="28550-111">EXAMPLES</span></span>

### <span data-ttu-id="28550-112">1. példa: Felhőszolgáltatás szerepkörpéldányának újraépítése</span><span class="sxs-lookup"><span data-stu-id="28550-112">Example 1: Rebuild role instance of a cloud service</span></span>
```powershell
PS C:\> Invoke-AzCloudServiceRoleInstanceRebuild -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="28550-113">Ez a parancs újragondolja ContosoFrontEnd_IN_0 ContosOrg nevű erőforráscsoporthoz tartozó ContosoCS nevű felhőszolgáltatás egyik szerepkörpéldányát.</span><span class="sxs-lookup"><span data-stu-id="28550-113">This command reimages role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="28550-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28550-114">PARAMETERS</span></span>

### <span data-ttu-id="28550-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28550-115">-AsJob</span></span>
<span data-ttu-id="28550-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="28550-116">Run the command as a job</span></span>

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

### <span data-ttu-id="28550-117">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="28550-117">-CloudServiceName</span></span>
<span data-ttu-id="28550-118">.</span><span class="sxs-lookup"><span data-stu-id="28550-118">.</span></span>

```yaml
Type: System.String
Parameter Sets: Rebuild
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28550-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28550-119">-DefaultProfile</span></span>
<span data-ttu-id="28550-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="28550-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28550-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28550-121">-InputObject</span></span>
<span data-ttu-id="28550-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="28550-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: RebuildViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28550-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="28550-123">-NoWait</span></span>
<span data-ttu-id="28550-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="28550-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="28550-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28550-125">-PassThru</span></span>
<span data-ttu-id="28550-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="28550-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="28550-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28550-127">-ResourceGroupName</span></span>
<span data-ttu-id="28550-128">.</span><span class="sxs-lookup"><span data-stu-id="28550-128">.</span></span>

```yaml
Type: System.String
Parameter Sets: Rebuild
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28550-129">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="28550-129">-RoleInstanceName</span></span>
<span data-ttu-id="28550-130">A szerepkörpéldány neve.</span><span class="sxs-lookup"><span data-stu-id="28550-130">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Rebuild
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28550-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="28550-131">-SubscriptionId</span></span>
<span data-ttu-id="28550-132">Előfizetési hitelesítő adatok, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="28550-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="28550-133">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="28550-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Rebuild
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28550-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28550-134">-Confirm</span></span>
<span data-ttu-id="28550-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="28550-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28550-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28550-136">-WhatIf</span></span>
<span data-ttu-id="28550-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="28550-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28550-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="28550-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28550-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28550-139">CommonParameters</span></span>
<span data-ttu-id="28550-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28550-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28550-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28550-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28550-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="28550-142">INPUTS</span></span>

### <span data-ttu-id="28550-143">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="28550-143">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="28550-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="28550-144">OUTPUTS</span></span>

### <span data-ttu-id="28550-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="28550-145">System.Boolean</span></span>

## <span data-ttu-id="28550-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="28550-146">NOTES</span></span>

<span data-ttu-id="28550-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="28550-147">ALIASES</span></span>

<span data-ttu-id="28550-148">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="28550-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="28550-149">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="28550-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="28550-150">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="28550-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="28550-151">INPUTOBJECT: <ICloudServiceIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="28550-151">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="28550-152">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="28550-152">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="28550-153">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="28550-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="28550-154">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="28550-154">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="28550-155">`[RoleInstanceName <String>]`: A szerepkörpéldány neve.</span><span class="sxs-lookup"><span data-stu-id="28550-155">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="28550-156">`[RoleName <String>]`: A szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="28550-156">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="28550-157">`[SubscriptionId <String>]`: Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="28550-157">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="28550-158">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="28550-158">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="28550-159">`[UpdateDomain <Int32?>]`: A frissítő tartományt azonosító egész értéket ad meg.</span><span class="sxs-lookup"><span data-stu-id="28550-159">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="28550-160">A frissítési tartományokat nulla alapú index azonosítja: az első frissítési tartomány azonosítója 0, a második 1 és így tovább.</span><span class="sxs-lookup"><span data-stu-id="28550-160">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="28550-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="28550-161">RELATED LINKS</span></span>

