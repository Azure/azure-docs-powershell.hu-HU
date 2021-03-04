---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/remove-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
ms.openlocfilehash: a15dc7c72f2f7ef321f05f51d5b90c936f0406e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932874"
---
# <span data-ttu-id="4d513-101">Remove-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="4d513-101">Remove-AzWvdUserSession</span></span>

## <span data-ttu-id="4d513-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d513-102">SYNOPSIS</span></span>
<span data-ttu-id="4d513-103">Felhasználó eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4d513-103">Remove a userSession.</span></span>

## <span data-ttu-id="4d513-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4d513-104">SYNTAX</span></span>

### <span data-ttu-id="4d513-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4d513-105">Delete (Default)</span></span>
```
Remove-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4d513-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4d513-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4d513-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4d513-107">DESCRIPTION</span></span>
<span data-ttu-id="4d513-108">Felhasználó eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4d513-108">Remove a userSession.</span></span>

## <span data-ttu-id="4d513-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4d513-109">EXAMPLES</span></span>

### <span data-ttu-id="4d513-110">1. példa: A Windows Virtuális asztal felhasználófelhasználói munkamenetének törlése név szerint</span><span class="sxs-lookup"><span data-stu-id="4d513-110">Example 1: Delete a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Remove-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="4d513-111">Ez a parancs törli a Windows virtuális asztali felhasználófelhasználói munkamenetet a munkamenetgazdákban.</span><span class="sxs-lookup"><span data-stu-id="4d513-111">This command deletes a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="4d513-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d513-112">PARAMETERS</span></span>

### <span data-ttu-id="4d513-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d513-113">-DefaultProfile</span></span>
<span data-ttu-id="4d513-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4d513-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d513-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4d513-115">-Force</span></span>
<span data-ttu-id="4d513-116">A jelölő kényszerítve jelentkezzen be a userSession alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="4d513-116">Force flag to login off userSession.</span></span>

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

### <span data-ttu-id="4d513-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="4d513-117">-HostPoolName</span></span>
<span data-ttu-id="4d513-118">A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="4d513-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="4d513-119">-Id</span><span class="sxs-lookup"><span data-stu-id="4d513-119">-Id</span></span>
<span data-ttu-id="4d513-120">A megadott munkamenetgazda felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="4d513-120">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d513-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d513-121">-InputObject</span></span>
<span data-ttu-id="4d513-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="4d513-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4d513-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d513-123">-PassThru</span></span>
<span data-ttu-id="4d513-124">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="4d513-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4d513-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d513-125">-ResourceGroupName</span></span>
<span data-ttu-id="4d513-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4d513-126">The name of the resource group.</span></span>
<span data-ttu-id="4d513-127">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="4d513-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4d513-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="4d513-128">-SessionHostName</span></span>
<span data-ttu-id="4d513-129">A munkamenetgazda neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="4d513-129">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="4d513-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4d513-130">-SubscriptionId</span></span>
<span data-ttu-id="4d513-131">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4d513-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4d513-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d513-132">-Confirm</span></span>
<span data-ttu-id="4d513-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4d513-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d513-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d513-134">-WhatIf</span></span>
<span data-ttu-id="4d513-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4d513-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d513-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4d513-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d513-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d513-137">CommonParameters</span></span>
<span data-ttu-id="4d513-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d513-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d513-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d513-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d513-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4d513-140">INPUTS</span></span>

### <span data-ttu-id="4d513-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="4d513-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="4d513-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d513-142">OUTPUTS</span></span>

### <span data-ttu-id="4d513-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4d513-143">System.Boolean</span></span>

## <span data-ttu-id="4d513-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4d513-144">NOTES</span></span>

<span data-ttu-id="4d513-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="4d513-145">ALIASES</span></span>

<span data-ttu-id="4d513-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="4d513-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4d513-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="4d513-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4d513-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4d513-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4d513-149">INPUTOBJECT: <IDesktopVirtualizationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="4d513-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4d513-150">`[ApplicationGroupName <String>]`: Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="4d513-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="4d513-151">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazáscsoporton belül</span><span class="sxs-lookup"><span data-stu-id="4d513-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="4d513-152">`[DesktopName <String>]`: A megadott asztali csoportban található asztal neve</span><span class="sxs-lookup"><span data-stu-id="4d513-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="4d513-153">`[HostPoolName <String>]`: A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="4d513-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="4d513-154">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="4d513-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4d513-155">`[MsixPackageFullName <String>]`: A megadott állomáspoolon belül az MSIX-csomag teljes neve verzióspecifikus csomag</span><span class="sxs-lookup"><span data-stu-id="4d513-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="4d513-156">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4d513-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4d513-157">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="4d513-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="4d513-158">`[SessionHostName <String>]`: A munkamenet állomásának neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="4d513-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="4d513-159">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4d513-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4d513-160">`[UserSessionId <String>]`: A megadott munkamenetgazda felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="4d513-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="4d513-161">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="4d513-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="4d513-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d513-162">RELATED LINKS</span></span>

