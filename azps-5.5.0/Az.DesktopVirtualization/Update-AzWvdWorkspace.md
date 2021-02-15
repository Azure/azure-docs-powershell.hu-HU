---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
ms.openlocfilehash: 8a20777cfd6e28c3edc127117687b7aef801d94e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209710"
---
# <span data-ttu-id="e645c-101">Update-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="e645c-101">Update-AzWvdWorkspace</span></span>

## <span data-ttu-id="e645c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e645c-102">SYNOPSIS</span></span>
<span data-ttu-id="e645c-103">Munkaterület frissítése</span><span class="sxs-lookup"><span data-stu-id="e645c-103">Update a workspace.</span></span>

## <span data-ttu-id="e645c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e645c-104">SYNTAX</span></span>

### <span data-ttu-id="e645c-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e645c-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e645c-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e645c-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-ApplicationGroupReference <String[]>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e645c-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e645c-107">DESCRIPTION</span></span>
<span data-ttu-id="e645c-108">Munkaterület frissítése</span><span class="sxs-lookup"><span data-stu-id="e645c-108">Update a workspace.</span></span>

## <span data-ttu-id="e645c-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e645c-109">EXAMPLES</span></span>

### <span data-ttu-id="e645c-110">1. példa: Virtuális asztali Windows-munkaterület frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="e645c-110">Example 1: Update a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> Update-AzWvdWorkspace -ResourceGroupName ResourceGroupName `
                        -Name WorkspaceName `
                        -FriendlyName 'Friendly Name' `
                        -ApplicationGroupReference "/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName1","/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName2" `
                        -Description 'Description'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="e645c-111">Ez a parancs frissíti a Windows virtuális asztali munkaterületét egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="e645c-111">This command updates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="e645c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e645c-112">PARAMETERS</span></span>

### <span data-ttu-id="e645c-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="e645c-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="e645c-114">Az applicationGroup-hivatkozások listája.</span><span class="sxs-lookup"><span data-stu-id="e645c-114">List of applicationGroup links.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e645c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e645c-115">-DefaultProfile</span></span>
<span data-ttu-id="e645c-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e645c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e645c-117">-Leírás</span><span class="sxs-lookup"><span data-stu-id="e645c-117">-Description</span></span>
<span data-ttu-id="e645c-118">A Munkaterület leírása.</span><span class="sxs-lookup"><span data-stu-id="e645c-118">Description of Workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e645c-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="e645c-119">-FriendlyName</span></span>
<span data-ttu-id="e645c-120">A Munkaterület felhasználóbarát neve.</span><span class="sxs-lookup"><span data-stu-id="e645c-120">Friendly name of Workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e645c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e645c-121">-InputObject</span></span>
<span data-ttu-id="e645c-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e645c-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e645c-123">-Name</span><span class="sxs-lookup"><span data-stu-id="e645c-123">-Name</span></span>
<span data-ttu-id="e645c-124">A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="e645c-124">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e645c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e645c-125">-ResourceGroupName</span></span>
<span data-ttu-id="e645c-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e645c-126">The name of the resource group.</span></span>
<span data-ttu-id="e645c-127">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="e645c-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e645c-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e645c-128">-SubscriptionId</span></span>
<span data-ttu-id="e645c-129">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e645c-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e645c-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="e645c-130">-Tag</span></span>
<span data-ttu-id="e645c-131">frissítend kell a címkéket</span><span class="sxs-lookup"><span data-stu-id="e645c-131">tags to be updated</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e645c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e645c-132">-Confirm</span></span>
<span data-ttu-id="e645c-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e645c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e645c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e645c-134">-WhatIf</span></span>
<span data-ttu-id="e645c-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e645c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e645c-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e645c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e645c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e645c-137">CommonParameters</span></span>
<span data-ttu-id="e645c-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e645c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e645c-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e645c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e645c-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e645c-140">INPUTS</span></span>

### <span data-ttu-id="e645c-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="e645c-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="e645c-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e645c-142">OUTPUTS</span></span>

### <span data-ttu-id="e645c-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="e645c-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span></span>

## <span data-ttu-id="e645c-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e645c-144">NOTES</span></span>

<span data-ttu-id="e645c-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e645c-145">ALIASES</span></span>

<span data-ttu-id="e645c-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="e645c-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e645c-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="e645c-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e645c-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e645c-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e645c-149">INPUTOBJECT: <IDesktopVirtualizationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="e645c-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e645c-150">`[ApplicationGroupName <String>]`: Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e645c-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="e645c-151">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazáscsoporton belül</span><span class="sxs-lookup"><span data-stu-id="e645c-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="e645c-152">`[DesktopName <String>]`: Az asztal neve a megadott asztali csoportban</span><span class="sxs-lookup"><span data-stu-id="e645c-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="e645c-153">`[HostPoolName <String>]`: A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="e645c-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="e645c-154">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="e645c-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e645c-155">`[MsixPackageFullName <String>]`: A megadott állomáspoolon belül az MSIX-csomag teljes neve verzióspecifikus csomag</span><span class="sxs-lookup"><span data-stu-id="e645c-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="e645c-156">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e645c-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e645c-157">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="e645c-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="e645c-158">`[SessionHostName <String>]`: A munkamenet állomásának neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="e645c-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="e645c-159">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e645c-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e645c-160">`[UserSessionId <String>]`: A megadott munkamenetgazda felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="e645c-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="e645c-161">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="e645c-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="e645c-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e645c-162">RELATED LINKS</span></span>

