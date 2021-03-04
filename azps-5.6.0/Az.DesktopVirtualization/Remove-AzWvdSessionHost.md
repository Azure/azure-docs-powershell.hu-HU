---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/remove-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
ms.openlocfilehash: ee8334a233c35c2b834bfb89ddf20152d466367f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925617"
---
# <span data-ttu-id="93c7e-101">Remove-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="93c7e-101">Remove-AzWvdSessionHost</span></span>

## <span data-ttu-id="93c7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93c7e-102">SYNOPSIS</span></span>
<span data-ttu-id="93c7e-103">Távolítsa el a SessionHost-t.</span><span class="sxs-lookup"><span data-stu-id="93c7e-103">Remove a SessionHost.</span></span>

## <span data-ttu-id="93c7e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="93c7e-104">SYNTAX</span></span>

### <span data-ttu-id="93c7e-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="93c7e-105">Delete (Default)</span></span>
```
Remove-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="93c7e-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="93c7e-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="93c7e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="93c7e-107">DESCRIPTION</span></span>
<span data-ttu-id="93c7e-108">Távolítsa el a SessionHost-t.</span><span class="sxs-lookup"><span data-stu-id="93c7e-108">Remove a SessionHost.</span></span>

## <span data-ttu-id="93c7e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="93c7e-109">EXAMPLES</span></span>

### <span data-ttu-id="93c7e-110">1. példa: A Windows Virtual Desktop SessionHost törlése név szerint</span><span class="sxs-lookup"><span data-stu-id="93c7e-110">Example 1: Delete a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Remove-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName
```

<span data-ttu-id="93c7e-111">Ez a parancs törli a Windows Virtual Desktop SessionHost-t egy gazdakészletben.</span><span class="sxs-lookup"><span data-stu-id="93c7e-111">This command deletes a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="93c7e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93c7e-112">PARAMETERS</span></span>

### <span data-ttu-id="93c7e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93c7e-113">-DefaultProfile</span></span>
<span data-ttu-id="93c7e-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="93c7e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93c7e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="93c7e-115">-Force</span></span>
<span data-ttu-id="93c7e-116">A jelölő kényszerítésével kényszerítheti a sessionHost törlését akkor is, ha a userSession létezik.</span><span class="sxs-lookup"><span data-stu-id="93c7e-116">Force flag to force sessionHost deletion even when userSession exists.</span></span>

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

### <span data-ttu-id="93c7e-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="93c7e-117">-HostPoolName</span></span>
<span data-ttu-id="93c7e-118">A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="93c7e-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="93c7e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93c7e-119">-InputObject</span></span>
<span data-ttu-id="93c7e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="93c7e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93c7e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="93c7e-121">-Name</span></span>
<span data-ttu-id="93c7e-122">A munkamenetgazda neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="93c7e-122">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93c7e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93c7e-123">-PassThru</span></span>
<span data-ttu-id="93c7e-124">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="93c7e-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="93c7e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93c7e-125">-ResourceGroupName</span></span>
<span data-ttu-id="93c7e-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="93c7e-126">The name of the resource group.</span></span>
<span data-ttu-id="93c7e-127">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="93c7e-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="93c7e-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="93c7e-128">-SubscriptionId</span></span>
<span data-ttu-id="93c7e-129">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="93c7e-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="93c7e-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93c7e-130">-Confirm</span></span>
<span data-ttu-id="93c7e-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="93c7e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93c7e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93c7e-132">-WhatIf</span></span>
<span data-ttu-id="93c7e-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="93c7e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93c7e-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="93c7e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93c7e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93c7e-135">CommonParameters</span></span>
<span data-ttu-id="93c7e-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93c7e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93c7e-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93c7e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93c7e-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="93c7e-138">INPUTS</span></span>

### <span data-ttu-id="93c7e-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="93c7e-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="93c7e-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="93c7e-140">OUTPUTS</span></span>

### <span data-ttu-id="93c7e-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="93c7e-141">System.Boolean</span></span>

## <span data-ttu-id="93c7e-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="93c7e-142">NOTES</span></span>

<span data-ttu-id="93c7e-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="93c7e-143">ALIASES</span></span>

<span data-ttu-id="93c7e-144">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="93c7e-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="93c7e-145">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="93c7e-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="93c7e-146">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="93c7e-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="93c7e-147">INPUTOBJECT: <IDesktopVirtualizationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="93c7e-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="93c7e-148">`[ApplicationGroupName <String>]`: Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="93c7e-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="93c7e-149">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazáscsoporton belül</span><span class="sxs-lookup"><span data-stu-id="93c7e-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="93c7e-150">`[DesktopName <String>]`: A megadott asztali csoportban található asztal neve</span><span class="sxs-lookup"><span data-stu-id="93c7e-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="93c7e-151">`[HostPoolName <String>]`: A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="93c7e-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="93c7e-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="93c7e-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="93c7e-153">`[MsixPackageFullName <String>]`: A megadott állomáspoolon belül az MSIX-csomag teljes neve verzióspecifikus csomag</span><span class="sxs-lookup"><span data-stu-id="93c7e-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="93c7e-154">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="93c7e-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="93c7e-155">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="93c7e-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="93c7e-156">`[SessionHostName <String>]`: A munkamenet állomásának neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="93c7e-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="93c7e-157">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="93c7e-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="93c7e-158">`[UserSessionId <String>]`: A megadott munkamenetgazda felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="93c7e-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="93c7e-159">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="93c7e-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="93c7e-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="93c7e-160">RELATED LINKS</span></span>

