---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/remove-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplicationGroup.md
ms.openlocfilehash: 14a5aecbf2e72ea22673e18fd8ddd56a129ace10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925634"
---
# <span data-ttu-id="3c2fa-101">Remove-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="3c2fa-101">Remove-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="3c2fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c2fa-102">SYNOPSIS</span></span>
<span data-ttu-id="3c2fa-103">Alkalmazáscsoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3c2fa-103">Remove an applicationGroup.</span></span>

## <span data-ttu-id="3c2fa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3c2fa-104">SYNTAX</span></span>

### <span data-ttu-id="3c2fa-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3c2fa-105">Delete (Default)</span></span>
```
Remove-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3c2fa-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3c2fa-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3c2fa-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3c2fa-107">DESCRIPTION</span></span>
<span data-ttu-id="3c2fa-108">Alkalmazáscsoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3c2fa-108">Remove an applicationGroup.</span></span>

## <span data-ttu-id="3c2fa-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3c2fa-109">EXAMPLES</span></span>

### <span data-ttu-id="3c2fa-110">1. példa: A Windows virtuális asztali alkalmazáscsoport törlése név szerint</span><span class="sxs-lookup"><span data-stu-id="3c2fa-110">Example 1: Delete a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Remove-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName
```

<span data-ttu-id="3c2fa-111">Ez a parancs törli a Windows virtuális asztali alkalmazáscsoportját egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="3c2fa-111">This command deletes a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="3c2fa-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c2fa-112">PARAMETERS</span></span>

### <span data-ttu-id="3c2fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c2fa-113">-DefaultProfile</span></span>
<span data-ttu-id="3c2fa-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3c2fa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c2fa-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c2fa-115">-InputObject</span></span>
<span data-ttu-id="3c2fa-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="3c2fa-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3c2fa-117">-Name</span><span class="sxs-lookup"><span data-stu-id="3c2fa-117">-Name</span></span>
<span data-ttu-id="3c2fa-118">Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="3c2fa-118">The name of the application group</span></span>

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

### <span data-ttu-id="3c2fa-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c2fa-119">-PassThru</span></span>
<span data-ttu-id="3c2fa-120">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="3c2fa-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3c2fa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c2fa-121">-ResourceGroupName</span></span>
<span data-ttu-id="3c2fa-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3c2fa-122">The name of the resource group.</span></span>
<span data-ttu-id="3c2fa-123">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="3c2fa-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3c2fa-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3c2fa-124">-SubscriptionId</span></span>
<span data-ttu-id="3c2fa-125">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3c2fa-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="3c2fa-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c2fa-126">-Confirm</span></span>
<span data-ttu-id="3c2fa-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3c2fa-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c2fa-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c2fa-128">-WhatIf</span></span>
<span data-ttu-id="3c2fa-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3c2fa-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c2fa-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3c2fa-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c2fa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c2fa-131">CommonParameters</span></span>
<span data-ttu-id="3c2fa-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c2fa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c2fa-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c2fa-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c2fa-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3c2fa-134">INPUTS</span></span>

### <span data-ttu-id="3c2fa-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="3c2fa-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="3c2fa-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c2fa-136">OUTPUTS</span></span>

### <span data-ttu-id="3c2fa-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3c2fa-137">System.Boolean</span></span>

## <span data-ttu-id="3c2fa-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3c2fa-138">NOTES</span></span>

<span data-ttu-id="3c2fa-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="3c2fa-139">ALIASES</span></span>

<span data-ttu-id="3c2fa-140">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="3c2fa-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3c2fa-141">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="3c2fa-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3c2fa-142">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3c2fa-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3c2fa-143">INPUTOBJECT: <IDesktopVirtualizationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="3c2fa-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3c2fa-144">`[ApplicationGroupName <String>]`: Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="3c2fa-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="3c2fa-145">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazáscsoporton belül</span><span class="sxs-lookup"><span data-stu-id="3c2fa-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="3c2fa-146">`[DesktopName <String>]`: A megadott asztali csoportban található asztal neve</span><span class="sxs-lookup"><span data-stu-id="3c2fa-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="3c2fa-147">`[HostPoolName <String>]`: A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="3c2fa-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="3c2fa-148">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="3c2fa-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3c2fa-149">`[MsixPackageFullName <String>]`: A megadott állomáspoolon belül az MSIX-csomag teljes neve verzióspecifikus csomag</span><span class="sxs-lookup"><span data-stu-id="3c2fa-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="3c2fa-150">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3c2fa-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3c2fa-151">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="3c2fa-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="3c2fa-152">`[SessionHostName <String>]`: A munkamenet állomásának neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="3c2fa-152">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="3c2fa-153">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3c2fa-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="3c2fa-154">`[UserSessionId <String>]`: A megadott munkamenetgazda felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="3c2fa-154">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="3c2fa-155">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="3c2fa-155">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="3c2fa-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c2fa-156">RELATED LINKS</span></span>

