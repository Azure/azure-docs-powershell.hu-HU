---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/update-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
ms.openlocfilehash: 9e8599edaa1a1c19d5b0629d290402c792cf2563
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934401"
---
# <span data-ttu-id="db6c4-101">Update-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="db6c4-101">Update-AzWvdSessionHost</span></span>

## <span data-ttu-id="db6c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db6c4-102">SYNOPSIS</span></span>
<span data-ttu-id="db6c4-103">Frissítse a munkamenetgazdát.</span><span class="sxs-lookup"><span data-stu-id="db6c4-103">Update a session host.</span></span>

## <span data-ttu-id="db6c4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="db6c4-104">SYNTAX</span></span>

### <span data-ttu-id="db6c4-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="db6c4-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AllowNewSession] [-AssignedUser <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="db6c4-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="db6c4-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-AllowNewSession]
 [-AssignedUser <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="db6c4-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="db6c4-107">DESCRIPTION</span></span>
<span data-ttu-id="db6c4-108">Frissítse a munkamenetgazdát.</span><span class="sxs-lookup"><span data-stu-id="db6c4-108">Update a session host.</span></span>

## <span data-ttu-id="db6c4-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="db6c4-109">EXAMPLES</span></span>

### <span data-ttu-id="db6c4-110">1. példa: A Windows Virtual Desktop SessionHost frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="db6c4-110">Example 1: Update a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Update-AzWvdSessionHost -ResourceGroupName ResourceGroupName `
                            -HostPoolName HostPoolName `
                            -Name SessionHostName `
                            -AllowNewSession:$false

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="db6c4-111">Ez a parancs frissíti a Windows Virtual Desktop SessionHost-t egy gazdakészletben.</span><span class="sxs-lookup"><span data-stu-id="db6c4-111">This command updates a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="db6c4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db6c4-112">PARAMETERS</span></span>

### <span data-ttu-id="db6c4-113">-AllowNewSession</span><span class="sxs-lookup"><span data-stu-id="db6c4-113">-AllowNewSession</span></span>
<span data-ttu-id="db6c4-114">Új munkamenet engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="db6c4-114">Allow a new session.</span></span>

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

### <span data-ttu-id="db6c4-115">-AssignedUser</span><span class="sxs-lookup"><span data-stu-id="db6c4-115">-AssignedUser</span></span>
<span data-ttu-id="db6c4-116">A SessionHost-hoz rendelt felhasználó.</span><span class="sxs-lookup"><span data-stu-id="db6c4-116">User assigned to SessionHost.</span></span>

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

### <span data-ttu-id="db6c4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db6c4-117">-DefaultProfile</span></span>
<span data-ttu-id="db6c4-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db6c4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db6c4-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="db6c4-119">-HostPoolName</span></span>
<span data-ttu-id="db6c4-120">A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="db6c4-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="db6c4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db6c4-121">-InputObject</span></span>
<span data-ttu-id="db6c4-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="db6c4-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="db6c4-123">-Name</span><span class="sxs-lookup"><span data-stu-id="db6c4-123">-Name</span></span>
<span data-ttu-id="db6c4-124">A munkamenetgazda neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="db6c4-124">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db6c4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db6c4-125">-ResourceGroupName</span></span>
<span data-ttu-id="db6c4-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="db6c4-126">The name of the resource group.</span></span>
<span data-ttu-id="db6c4-127">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="db6c4-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="db6c4-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="db6c4-128">-SubscriptionId</span></span>
<span data-ttu-id="db6c4-129">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="db6c4-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="db6c4-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db6c4-130">-Confirm</span></span>
<span data-ttu-id="db6c4-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="db6c4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db6c4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db6c4-132">-WhatIf</span></span>
<span data-ttu-id="db6c4-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="db6c4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db6c4-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="db6c4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db6c4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db6c4-135">CommonParameters</span></span>
<span data-ttu-id="db6c4-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db6c4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db6c4-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db6c4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db6c4-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db6c4-138">INPUTS</span></span>

### <span data-ttu-id="db6c4-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="db6c4-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="db6c4-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db6c4-140">OUTPUTS</span></span>

### <span data-ttu-id="db6c4-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.ISessionHost</span><span class="sxs-lookup"><span data-stu-id="db6c4-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.ISessionHost</span></span>

## <span data-ttu-id="db6c4-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="db6c4-142">NOTES</span></span>

<span data-ttu-id="db6c4-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="db6c4-143">ALIASES</span></span>

<span data-ttu-id="db6c4-144">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="db6c4-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="db6c4-145">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="db6c4-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="db6c4-146">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="db6c4-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="db6c4-147">INPUTOBJECT: <IDesktopVirtualizationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="db6c4-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="db6c4-148">`[ApplicationGroupName <String>]`: Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="db6c4-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="db6c4-149">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazáscsoporton belül</span><span class="sxs-lookup"><span data-stu-id="db6c4-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="db6c4-150">`[DesktopName <String>]`: A megadott asztali csoportban található asztal neve</span><span class="sxs-lookup"><span data-stu-id="db6c4-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="db6c4-151">`[HostPoolName <String>]`: A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="db6c4-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="db6c4-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="db6c4-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="db6c4-153">`[MsixPackageFullName <String>]`: A megadott állomáspoolon belül az MSIX-csomag teljes neve verzióspecifikus csomag</span><span class="sxs-lookup"><span data-stu-id="db6c4-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="db6c4-154">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="db6c4-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="db6c4-155">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="db6c4-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="db6c4-156">`[SessionHostName <String>]`: A munkamenet állomásának neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="db6c4-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="db6c4-157">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="db6c4-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="db6c4-158">`[UserSessionId <String>]`: A megadott munkamenetgazda felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="db6c4-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="db6c4-159">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="db6c4-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="db6c4-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db6c4-160">RELATED LINKS</span></span>

