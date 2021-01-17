---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplicationGroup.md
ms.openlocfilehash: 59ff3c3bd973e3b2189e7f06cd067eaca42870f5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469918"
---
# <span data-ttu-id="f829d-101">Remove-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="f829d-101">Remove-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="f829d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f829d-102">SYNOPSIS</span></span>
<span data-ttu-id="f829d-103">Alkalmazáscsoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f829d-103">Remove an applicationGroup.</span></span>

## <span data-ttu-id="f829d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f829d-104">SYNTAX</span></span>

### <span data-ttu-id="f829d-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f829d-105">Delete (Default)</span></span>
```
Remove-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f829d-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f829d-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f829d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f829d-107">DESCRIPTION</span></span>
<span data-ttu-id="f829d-108">Alkalmazáscsoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f829d-108">Remove an applicationGroup.</span></span>

## <span data-ttu-id="f829d-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f829d-109">EXAMPLES</span></span>

### <span data-ttu-id="f829d-110">1. példa: A Windows virtuális asztali alkalmazáscsoport törlése név szerint</span><span class="sxs-lookup"><span data-stu-id="f829d-110">Example 1: Delete a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Remove-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName
```

<span data-ttu-id="f829d-111">Ez a parancs törli a Windows virtuális asztali alkalmazáscsoportját egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="f829d-111">This command deletes a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="f829d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f829d-112">PARAMETERS</span></span>

### <span data-ttu-id="f829d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f829d-113">-DefaultProfile</span></span>
<span data-ttu-id="f829d-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f829d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f829d-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f829d-115">-InputObject</span></span>
<span data-ttu-id="f829d-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="f829d-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f829d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f829d-117">-Name</span></span>
<span data-ttu-id="f829d-118">Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="f829d-118">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f829d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f829d-119">-PassThru</span></span>
<span data-ttu-id="f829d-120">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="f829d-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f829d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f829d-121">-ResourceGroupName</span></span>
<span data-ttu-id="f829d-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f829d-122">The name of the resource group.</span></span>
<span data-ttu-id="f829d-123">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="f829d-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f829d-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f829d-124">-SubscriptionId</span></span>
<span data-ttu-id="f829d-125">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f829d-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f829d-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f829d-126">-Confirm</span></span>
<span data-ttu-id="f829d-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f829d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f829d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f829d-128">-WhatIf</span></span>
<span data-ttu-id="f829d-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f829d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f829d-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f829d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f829d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f829d-131">CommonParameters</span></span>
<span data-ttu-id="f829d-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f829d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f829d-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f829d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f829d-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f829d-134">INPUTS</span></span>

### <span data-ttu-id="f829d-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="f829d-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="f829d-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f829d-136">OUTPUTS</span></span>

### <span data-ttu-id="f829d-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f829d-137">System.Boolean</span></span>

## <span data-ttu-id="f829d-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f829d-138">NOTES</span></span>

<span data-ttu-id="f829d-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f829d-139">ALIASES</span></span>

<span data-ttu-id="f829d-140">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="f829d-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f829d-141">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="f829d-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f829d-142">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f829d-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f829d-143">INPUTOBJECT: <IDesktopVirtualizationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="f829d-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f829d-144">`[ApplicationGroupName <String>]`: Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="f829d-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="f829d-145">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazáscsoporton belül</span><span class="sxs-lookup"><span data-stu-id="f829d-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="f829d-146">`[DesktopName <String>]`: A megadott asztali csoportban található asztal neve</span><span class="sxs-lookup"><span data-stu-id="f829d-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="f829d-147">`[HostPoolName <String>]`: A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="f829d-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="f829d-148">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="f829d-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f829d-149">`[MsixPackageFullName <String>]`: A megadott állomáspoolon belül az MSIX-csomag teljes neve verzióspecifikus csomag</span><span class="sxs-lookup"><span data-stu-id="f829d-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="f829d-150">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f829d-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f829d-151">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="f829d-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="f829d-152">`[SessionHostName <String>]`: A munkamenet állomásának neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="f829d-152">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="f829d-153">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f829d-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f829d-154">`[UserSessionId <String>]`: A megadott munkamenetgazda felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="f829d-154">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="f829d-155">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="f829d-155">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="f829d-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f829d-156">RELATED LINKS</span></span>

