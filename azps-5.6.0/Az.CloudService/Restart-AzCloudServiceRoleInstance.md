---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/restart-azcloudserviceroleinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudServiceRoleInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudServiceRoleInstance.md
ms.openlocfilehash: f184696dbcfce35bf6e52f889d2c787214330e70
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935337"
---
# <span data-ttu-id="308cc-101">Restart-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="308cc-101">Restart-AzCloudServiceRoleInstance</span></span>

## <span data-ttu-id="308cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="308cc-102">SYNOPSIS</span></span>
<span data-ttu-id="308cc-103">A szerepkör-példány újraindítása aszinkron művelet egy szerepkörpéldány újraindítását kéri a felhőszolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="308cc-103">The Reboot Role Instance asynchronous operation requests a reboot of a role instance in the cloud service.</span></span>

## <span data-ttu-id="308cc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="308cc-104">SYNTAX</span></span>

### <span data-ttu-id="308cc-105">Újraindítás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="308cc-105">Restart (Default)</span></span>
```
Restart-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="308cc-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="308cc-106">RestartViaIdentity</span></span>
```
Restart-AzCloudServiceRoleInstance -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="308cc-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="308cc-107">DESCRIPTION</span></span>
<span data-ttu-id="308cc-108">A szerepkör-példány újraindítása aszinkron művelet egy szerepkörpéldány újraindítását kéri a felhőszolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="308cc-108">The Reboot Role Instance asynchronous operation requests a reboot of a role instance in the cloud service.</span></span>

## <span data-ttu-id="308cc-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="308cc-109">EXAMPLES</span></span>

### <span data-ttu-id="308cc-110">1. példa: Felhőszolgáltatás szerepkörpéldányának újraindítása</span><span class="sxs-lookup"><span data-stu-id="308cc-110">Example 1: Restart role instance of a cloud service</span></span>
```powershell
PS C:\> Restart-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="308cc-111">Ez a parancs újraindítja ContosoFrontEnd_IN_0 ContosOrg nevű erőforráscsoporthoz tartozó ContosoCS nevű felhőszolgáltatás szerepkörpéldányát.</span><span class="sxs-lookup"><span data-stu-id="308cc-111">This command restarts role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="308cc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="308cc-112">PARAMETERS</span></span>

### <span data-ttu-id="308cc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="308cc-113">-AsJob</span></span>
<span data-ttu-id="308cc-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="308cc-114">Run the command as a job</span></span>

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

### <span data-ttu-id="308cc-115">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="308cc-115">-CloudServiceName</span></span>
<span data-ttu-id="308cc-116">.</span><span class="sxs-lookup"><span data-stu-id="308cc-116">.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="308cc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="308cc-117">-DefaultProfile</span></span>
<span data-ttu-id="308cc-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="308cc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="308cc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="308cc-119">-InputObject</span></span>
<span data-ttu-id="308cc-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="308cc-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="308cc-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="308cc-121">-NoWait</span></span>
<span data-ttu-id="308cc-122">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="308cc-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="308cc-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="308cc-123">-PassThru</span></span>
<span data-ttu-id="308cc-124">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="308cc-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="308cc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="308cc-125">-ResourceGroupName</span></span>
<span data-ttu-id="308cc-126">.</span><span class="sxs-lookup"><span data-stu-id="308cc-126">.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="308cc-127">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="308cc-127">-RoleInstanceName</span></span>
<span data-ttu-id="308cc-128">A szerepkörpéldány neve.</span><span class="sxs-lookup"><span data-stu-id="308cc-128">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="308cc-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="308cc-129">-SubscriptionId</span></span>
<span data-ttu-id="308cc-130">Előfizetési hitelesítő adatok, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="308cc-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="308cc-131">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="308cc-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="308cc-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="308cc-132">-Confirm</span></span>
<span data-ttu-id="308cc-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="308cc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="308cc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="308cc-134">-WhatIf</span></span>
<span data-ttu-id="308cc-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="308cc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="308cc-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="308cc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="308cc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="308cc-137">CommonParameters</span></span>
<span data-ttu-id="308cc-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="308cc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="308cc-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="308cc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="308cc-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="308cc-140">INPUTS</span></span>

### <span data-ttu-id="308cc-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="308cc-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="308cc-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="308cc-142">OUTPUTS</span></span>

### <span data-ttu-id="308cc-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="308cc-143">System.Boolean</span></span>

## <span data-ttu-id="308cc-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="308cc-144">NOTES</span></span>

<span data-ttu-id="308cc-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="308cc-145">ALIASES</span></span>

<span data-ttu-id="308cc-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="308cc-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="308cc-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="308cc-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="308cc-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="308cc-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="308cc-149">INPUTOBJECT: <ICloudServiceIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="308cc-149">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="308cc-150">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="308cc-150">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="308cc-151">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="308cc-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="308cc-152">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="308cc-152">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="308cc-153">`[RoleInstanceName <String>]`: A szerepkörpéldány neve.</span><span class="sxs-lookup"><span data-stu-id="308cc-153">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="308cc-154">`[RoleName <String>]`: A szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="308cc-154">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="308cc-155">`[SubscriptionId <String>]`: Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="308cc-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="308cc-156">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="308cc-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="308cc-157">`[UpdateDomain <Int32?>]`: A frissítő tartományt azonosító egész értéket ad meg.</span><span class="sxs-lookup"><span data-stu-id="308cc-157">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="308cc-158">A frissítési tartományokat nulla alapú index azonosítja: az első frissítési tartomány azonosítója 0, a második 1 és így tovább.</span><span class="sxs-lookup"><span data-stu-id="308cc-158">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="308cc-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="308cc-159">RELATED LINKS</span></span>

