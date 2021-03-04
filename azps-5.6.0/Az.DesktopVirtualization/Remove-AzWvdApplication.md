---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/remove-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplication.md
ms.openlocfilehash: 0d8f3f3fa1f89c2045b10e07a5f7b11358222234
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925641"
---
# <span data-ttu-id="d6cfd-101">Remove-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="d6cfd-101">Remove-AzWvdApplication</span></span>

## <span data-ttu-id="d6cfd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6cfd-102">SYNOPSIS</span></span>
<span data-ttu-id="d6cfd-103">Alkalmazás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d6cfd-103">Remove an application.</span></span>

## <span data-ttu-id="d6cfd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d6cfd-104">SYNTAX</span></span>

### <span data-ttu-id="d6cfd-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d6cfd-105">Delete (Default)</span></span>
```
Remove-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d6cfd-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d6cfd-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d6cfd-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d6cfd-107">DESCRIPTION</span></span>
<span data-ttu-id="d6cfd-108">Alkalmazás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d6cfd-108">Remove an application.</span></span>

## <span data-ttu-id="d6cfd-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d6cfd-109">EXAMPLES</span></span>

### <span data-ttu-id="d6cfd-110">1. példa: Windows virtuális asztali alkalmazás törlése név szerint</span><span class="sxs-lookup"><span data-stu-id="d6cfd-110">Example 1: Delete a Windows Virtual Desktop Application by name</span></span>
```powershell
PS C:\> Remove-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName
```

<span data-ttu-id="d6cfd-111">Ez a parancs törli a Windows virtuális asztali alkalmazást egy applicaton-csoportban.</span><span class="sxs-lookup"><span data-stu-id="d6cfd-111">This command deletes a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="d6cfd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6cfd-112">PARAMETERS</span></span>

### <span data-ttu-id="d6cfd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6cfd-113">-DefaultProfile</span></span>
<span data-ttu-id="d6cfd-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6cfd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6cfd-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="d6cfd-115">-GroupName</span></span>
<span data-ttu-id="d6cfd-116">Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="d6cfd-116">The name of the application group</span></span>

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

### <span data-ttu-id="d6cfd-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6cfd-117">-InputObject</span></span>
<span data-ttu-id="d6cfd-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="d6cfd-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d6cfd-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d6cfd-119">-Name</span></span>
<span data-ttu-id="d6cfd-120">Az alkalmazás neve a megadott alkalmazáscsoportban</span><span class="sxs-lookup"><span data-stu-id="d6cfd-120">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6cfd-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6cfd-121">-PassThru</span></span>
<span data-ttu-id="d6cfd-122">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="d6cfd-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d6cfd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6cfd-123">-ResourceGroupName</span></span>
<span data-ttu-id="d6cfd-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d6cfd-124">The name of the resource group.</span></span>
<span data-ttu-id="d6cfd-125">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="d6cfd-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d6cfd-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d6cfd-126">-SubscriptionId</span></span>
<span data-ttu-id="d6cfd-127">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d6cfd-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d6cfd-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6cfd-128">-Confirm</span></span>
<span data-ttu-id="d6cfd-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d6cfd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6cfd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6cfd-130">-WhatIf</span></span>
<span data-ttu-id="d6cfd-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d6cfd-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6cfd-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d6cfd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6cfd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6cfd-133">CommonParameters</span></span>
<span data-ttu-id="d6cfd-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6cfd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6cfd-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6cfd-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6cfd-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d6cfd-136">INPUTS</span></span>

### <span data-ttu-id="d6cfd-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="d6cfd-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="d6cfd-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6cfd-138">OUTPUTS</span></span>

### <span data-ttu-id="d6cfd-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d6cfd-139">System.Boolean</span></span>

## <span data-ttu-id="d6cfd-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d6cfd-140">NOTES</span></span>

<span data-ttu-id="d6cfd-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d6cfd-141">ALIASES</span></span>

<span data-ttu-id="d6cfd-142">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="d6cfd-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d6cfd-143">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="d6cfd-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d6cfd-144">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d6cfd-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d6cfd-145">INPUTOBJECT: <IDesktopVirtualizationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="d6cfd-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d6cfd-146">`[ApplicationGroupName <String>]`: Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="d6cfd-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="d6cfd-147">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazáscsoporton belül</span><span class="sxs-lookup"><span data-stu-id="d6cfd-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="d6cfd-148">`[DesktopName <String>]`: A megadott asztali csoportban található asztal neve</span><span class="sxs-lookup"><span data-stu-id="d6cfd-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="d6cfd-149">`[HostPoolName <String>]`: A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="d6cfd-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="d6cfd-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="d6cfd-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d6cfd-151">`[MsixPackageFullName <String>]`: A megadott állomáspoolon belül az MSIX-csomag teljes neve verzióspecifikus csomag</span><span class="sxs-lookup"><span data-stu-id="d6cfd-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="d6cfd-152">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d6cfd-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d6cfd-153">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="d6cfd-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="d6cfd-154">`[SessionHostName <String>]`: A munkamenet állomásának neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="d6cfd-154">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="d6cfd-155">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d6cfd-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d6cfd-156">`[UserSessionId <String>]`: A megadott munkamenetgazda felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="d6cfd-156">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="d6cfd-157">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="d6cfd-157">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="d6cfd-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6cfd-158">RELATED LINKS</span></span>

