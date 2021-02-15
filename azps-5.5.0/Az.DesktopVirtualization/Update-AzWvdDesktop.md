---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
ms.openlocfilehash: 31a9ecc324938ae3518887d58ac2a762b374328c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209727"
---
# <span data-ttu-id="a2beb-101">Update-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="a2beb-101">Update-AzWvdDesktop</span></span>

## <span data-ttu-id="a2beb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2beb-102">SYNOPSIS</span></span>
<span data-ttu-id="a2beb-103">Frissítsen egy asztalt.</span><span class="sxs-lookup"><span data-stu-id="a2beb-103">Update a desktop.</span></span>

## <span data-ttu-id="a2beb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a2beb-104">SYNTAX</span></span>

### <span data-ttu-id="a2beb-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a2beb-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a2beb-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a2beb-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="a2beb-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a2beb-107">DESCRIPTION</span></span>
<span data-ttu-id="a2beb-108">Frissítsen egy asztalt.</span><span class="sxs-lookup"><span data-stu-id="a2beb-108">Update a desktop.</span></span>

## <span data-ttu-id="a2beb-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a2beb-109">EXAMPLES</span></span>

### <span data-ttu-id="a2beb-110">1. példa: Windows virtuális asztal frissítése</span><span class="sxs-lookup"><span data-stu-id="a2beb-110">Example 1: Update a Windows Virtual Desktop Desktop</span></span>
```powershell
PS C:\> Update-AzWvdDesktop -ResourceGroupName ResourceGroupName `
                             -GroupName ApplicationGroupName `
                             -Name DesktopName `
                             -FriendlyName 'Friendly name' `
                             -Description 'Description' `

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="a2beb-111">Ez a parancs frissíti a Windows virtuális asztalt egy applicaton groupban.</span><span class="sxs-lookup"><span data-stu-id="a2beb-111">This command updates a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

## <span data-ttu-id="a2beb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2beb-112">PARAMETERS</span></span>

### <span data-ttu-id="a2beb-113">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="a2beb-113">-ApplicationGroupName</span></span>
<span data-ttu-id="a2beb-114">Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a2beb-114">The name of the application group</span></span>

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

### <span data-ttu-id="a2beb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2beb-115">-DefaultProfile</span></span>
<span data-ttu-id="a2beb-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2beb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2beb-117">-Leírás</span><span class="sxs-lookup"><span data-stu-id="a2beb-117">-Description</span></span>
<span data-ttu-id="a2beb-118">Az asztal leírása.</span><span class="sxs-lookup"><span data-stu-id="a2beb-118">Description of Desktop.</span></span>

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

### <span data-ttu-id="a2beb-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a2beb-119">-FriendlyName</span></span>
<span data-ttu-id="a2beb-120">Az asztal rövid neve.</span><span class="sxs-lookup"><span data-stu-id="a2beb-120">Friendly name of Desktop.</span></span>

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

### <span data-ttu-id="a2beb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2beb-121">-InputObject</span></span>
<span data-ttu-id="a2beb-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="a2beb-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a2beb-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a2beb-123">-Name</span></span>
<span data-ttu-id="a2beb-124">Az asztal neve a megadott asztali csoportban</span><span class="sxs-lookup"><span data-stu-id="a2beb-124">The name of the desktop within the specified desktop group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DesktopName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2beb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2beb-125">-ResourceGroupName</span></span>
<span data-ttu-id="a2beb-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a2beb-126">The name of the resource group.</span></span>
<span data-ttu-id="a2beb-127">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="a2beb-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a2beb-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a2beb-128">-SubscriptionId</span></span>
<span data-ttu-id="a2beb-129">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a2beb-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a2beb-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="a2beb-130">-Tag</span></span>
<span data-ttu-id="a2beb-131">frissítend kell a címkéket</span><span class="sxs-lookup"><span data-stu-id="a2beb-131">tags to be updated</span></span>

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

### <span data-ttu-id="a2beb-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2beb-132">-Confirm</span></span>
<span data-ttu-id="a2beb-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a2beb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2beb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2beb-134">-WhatIf</span></span>
<span data-ttu-id="a2beb-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a2beb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2beb-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a2beb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2beb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2beb-137">CommonParameters</span></span>
<span data-ttu-id="a2beb-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2beb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2beb-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2beb-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2beb-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a2beb-140">INPUTS</span></span>

### <span data-ttu-id="a2beb-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="a2beb-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="a2beb-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2beb-142">OUTPUTS</span></span>

### <span data-ttu-id="a2beb-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span><span class="sxs-lookup"><span data-stu-id="a2beb-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span></span>

## <span data-ttu-id="a2beb-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a2beb-144">NOTES</span></span>

<span data-ttu-id="a2beb-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a2beb-145">ALIASES</span></span>

<span data-ttu-id="a2beb-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="a2beb-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a2beb-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="a2beb-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a2beb-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a2beb-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a2beb-149">INPUTOBJECT: <IDesktopVirtualizationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="a2beb-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a2beb-150">`[ApplicationGroupName <String>]`: Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a2beb-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="a2beb-151">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazáscsoporton belül</span><span class="sxs-lookup"><span data-stu-id="a2beb-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="a2beb-152">`[DesktopName <String>]`: A megadott asztali csoportban található asztal neve</span><span class="sxs-lookup"><span data-stu-id="a2beb-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="a2beb-153">`[HostPoolName <String>]`: A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="a2beb-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="a2beb-154">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="a2beb-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a2beb-155">`[MsixPackageFullName <String>]`: A megadott állomáspoolon belül az MSIX-csomag teljes neve verzióspecifikus csomag</span><span class="sxs-lookup"><span data-stu-id="a2beb-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="a2beb-156">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a2beb-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a2beb-157">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="a2beb-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="a2beb-158">`[SessionHostName <String>]`: A munkamenet állomásának neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="a2beb-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="a2beb-159">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a2beb-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a2beb-160">`[UserSessionId <String>]`: A megadott munkamenetgazda felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="a2beb-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="a2beb-161">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="a2beb-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="a2beb-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2beb-162">RELATED LINKS</span></span>

